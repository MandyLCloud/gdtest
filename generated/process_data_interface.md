# Process Data Interface for Licensing Self-Certification Portal

This document outlines the Process Data Interface (PDI) for the Licensing Self-Certification Portal (LSCP) of the Buildings Department (BD). It covers the system's data processing approach and its integration with various external systems.

**Version:** 0.1
**Date:** Jan 2025

## 1. Introduction

The Process Data Interface (PDI) document is structured into three main sections:

1.  **Introduction:**  Explains the purpose and contents of the PDI.
2.  **System Data Process Interface:** Defines how data is processed within the LSCP system.
3.  **External Interfaces:** Specifies the integration approach with external systems, including interface specifications.

This PDI aims to guide the physical design and integration of the LSCP with other systems.

## 2. System Data Process Interface

This section describes the physical data design and the components of the physical process within the LSCP. The interface is designed to present the database, implemented using the physical environment, as the Required System Logical Data Model to the processing components. This approach simplifies system implementation and future maintenance.

For each incoming process request, the system:

1.  Accepts and handles the input.
2.  Updates and queries the database.

The following diagram illustrates the position of the PDI relative to the universal function model (In/Out data process flow):

[Diagram of In/Out data process flow - See urs_a1.md for similar diagrams]

## 3. External Interfaces

This section details the integration of the LSCP with external systems, providing interface specifications for each.

### 3.1 List of External Interface Specifications

The following table summarizes the external interfaces:

| System Scope | Interfacing Party/ System                   | Interface Spec. ID | Name                                  | Interface Type             | In / Out | Authentication / Encryption |
| :----------- | :-------------------------------------- | :----------------- | :------------------------------------ | :------------------------- | :------- | :-------------------------- |
| External     | SMIS                                        | INT-SMIS-01        | Data Import from SMIS                 | Stored Procedure           | In       | *To be determined*          |
| External     | OSDP                                        | INT-OSDP-01        | Single Sign-On through OSDP           | HTTP Request Redirection   | In       | TLS 1.2 over HTTPS        |
| External     | MWMS2                                       | INT-MWMS2-01        | Data Import from MWMS2                | SFTP and Excel             | In       | SFTP                      |
| External     | ESH                                         | INT-ESH-01         | Data Import from ESH                  | SFTP                       | In       | SFTP                      |
| External     | ERKS                                        | INT-ERKS-01         | Data Import from ERKS                 | *To be confirmed*          | In       | *To be confirmed*          |
| External     | BRAVO                                       | INT-BRAVO-01        | Data Import from BRAVO                | HTTP Request Redirection   | In       | *To be determined*          |

**Note:** Authentication and encryption methods marked "To be determined" or left blank require further clarification based on the specific requirements and capabilities of each external system.

### 3.2 Interface Specification

#### 3.2.1 INT-SMIS-01 - Data Import from SMIS

*   **Target System:** Statutory Management Information System (SMIS)
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** The LSCP system calls stored procedures in the SMIS database to import necessary data.  Specific data fields will be defined during the detailed design phase.
*   **Data Exchange:** Data is transferred directly between databases via stored procedures.
*   **Authentication:** Authentication method for accessing the SMIS database needs to be determined (e.g., database user credentials, API keys).
*   **Error Handling:** Stored procedures should include error handling for data transfer issues and logging.
*   **Data Mapping:**

    | **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
    | :---------------- | :---------------- | :----------- | :-------------- |
    | *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
    | ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative):**

    ```sql
    EXECUTE SMIS.Import_LSCP_Data;
    ```

#### 3.2.2 INT-OSDP-01 - Single Sign-On through OSDP

*   **Target System:** Open Source Departmental Portal (OSDP)
*   **Interface Type:** URL redirection with departmental portal
*   **In / Out:** In
*   **Frequency:** Per user request

*   **Description:** Users from BD and other B/Ds access the LSCP by logging into their respective OSDPs. A link to redirect to the LSCP is provided in the BD Departmental Portal and other B/Ds Departmental Portal. The connection between the other B/Ds departmental portal and the LSCP is SSL secured.
*   **Access from Buildings Departments (BD) Departmental Portal:**
    *   The link to access the LSCP will be: `https://lscp.bd.gov.hk`
*   **Access from other B/Ds Departmental Portal:**
    *   Users from other B/Ds will access the LSCP through their own departmental portals.
    *   Their departmental portals will redirect the request through the CCGO gateway.
    *   The connection between the other B/Ds departmental portal and the LSCP will be SSL secured.
*   **Authentication and Authorization:**
    *   For the departmental portal users who would like to access the LSCP, they have to apply for Intranet access to ITU.
    *   The LSCP System administrator will register an account in the LSCP with regard to the submitted information.
    *   LSCP authenticates the incoming user by the login name and the department code of the departmental portal account.
    *   If and only if the account with the same login name and department code exists, the departmental portal user could login to the LSCP.
    *   Both BD users and other B/Ds users will be authenticated in this way.
*   **Data Exchange:**
    *   The departmental portal has to forward the ?UID? and ?Dpdeptid? to LSCP in the HTTP response header.
    *   The UID and Dpdeptid should contain information of departmental portal user ID and department code.

*   **In/Out data process flow diagram:**

    [Diagram of In/Out data process flow - See urs_a1.md for similar diagrams]

#### 3.2.3 INT-MWMS2-01 - Data Import from MWMS2

*   **Target System:** Minor Works Management System 2.0 (MWMS2)
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** The LSCP system retrieves Excel files containing AP/RSE information from MWMS2 via a scheduled task (e.g., daily). Files are transferred using SFTP.
*   **Data Exchange:**
    1.  MWMS2 generates and places Excel files in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the Excel files.
    3.  LSCP parses the Excel files and imports the data into its database.
*   **Authentication:** SFTP access uses SSH keys or username/password credentials.
*   **Error Handling:** The system handles potential errors during file transfer, parsing, and database import, with logging and retry mechanisms.
*   **Excel File Format:**

    | Field Name | Description                                                                   | Data Type | Format/Example |
    | :--------- | :---------------------------------------------------------------------------- | :-------- | :------------- |
    | AP\_ID     | Unique identifier for the Authorized Person                                  | Number    | 12345          |
    | AP\_NAME   | Name of the Authorized Person                                                | Text      | John Doe       |
    | AP\_REG\_NO | Registration number of the Authorized Person                               | Text      | AP-98765       |
    | RSE\_ID    | Unique identifier for the Registered Structural Engineer                    | Number    | 67890          |
    | RSE\_NAME  | Name of the Registered Structural Engineer                                   | Text      | Jane Smith     |
    | RSE\_REG\_NO| Registration number of the Registered Structural Engineer                   | Text      | RSE-54321      |
    | ...        | ...                                                                           | ...       | ...            |

    (Note: The exact format and content of the Excel file will need to be confirmed with the MWMS2 system owners.)

#### 3.2.4 INT-ESH-01 - Data Import from ESH

*   **Target System:** ESH (Name needs to be confirmed)
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** The LSCP system retrieves site project information from the ESH system via a scheduled task (e.g., daily). Files are transferred using SFTP. The imported information is used for validating if a user is involved in the site project.
*   **Data Exchange:**
    1.  ESH generates and places files in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the files.
    3.  LSCP parses the files and imports the data into its database.
*   **Authentication:** SFTP access uses SSH keys or username/password credentials.
*   **Error Handling:** The system handles potential errors during file transfer, parsing, and database import, with appropriate logging and retry mechanisms.
*   **File Format:**  The format needs to be confirmed. The file could be excel, csv or json.
*   **Data Mapping:**

    | ESH Data Item | LSCP Data Item | Data Type | Description |
    | :---- | :---- | :---: | :---- |
    | File Reference | File Reference | string | BD Reference Number of the site project |
    | Site Address | Site Address | string | address of the site project |
    | AP Registration Number | AP Registration Number | string | Registration number of the AP that involve in the related site project |
    | RSE Registration Number | RSE Registration Number | string | Registration number of the RSE that involve in the related site project |
    | RGE Registration Number | RGE Registration Number | string | Registration number of the RGE that involve in the related site project |
    | RC Registration Number | RC Registration Number | string | Registration number of the RC that involve in the related site project |

#### 3.2.5 INT-ERKS-01 - Data Import from ERKS

*   **Target System:** ERKS (Name needs to be confirmed)
*   **Interface Type:** TBC (To Be Confirmed)
*   **In / Out:** In
*   **Frequency:** TBC (To Be Confirmed)

*   **Description:** This interface will likely involve importing data from the ERKS system into LSCP. The specifics of the data and the mechanism will need to be determined in consultation with the ERKS system owners.
*   **Data Exchange:** The method of data exchange (e.g., API, file transfer, database link) needs to be defined.
*   **Authentication:** The authentication and authorization mechanism for accessing ERKS data will need to be established.
*   **Error Handling:** Robust error handling will be required to address any issues during the data exchange process.
*   **Data Mapping:**
    (This section will need to be filled in with the specific data elements that need to be mapped between ERKS and LSCP)

#### 3.2.6 INT-BRAVO-01 - Data Import from BRAVO

*   **Target System:** BRAVO (Name needs to be confirmed)
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In
*   **Frequency:** Per User Request

*   **Description:** The system can use `https://dp2.bd.hksarg/bravo/intranetSignOn` to redirect to BRAVO. Also, the SCS system could be redirected to BRAVO through a URL call with specified parameters.
*   **Data Exchange:** The LSCP system will make HTTP requests (GET or POST) to specific BRAVO URLs, passing any required parameters in the URL query string or request body. The BRAVO system will respond with the relevant data.
*   **Authentication:** The authentication method for accessing BRAVO (e.g., API keys, OAuth) will need to be determined.
*   **Error Handling:** The system should handle any errors returned by the BRAVO API and provide appropriate feedback to the user.
*   **URL Syntax (Examples):**

    *   **with Case number and Year**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    (Note: The exact URL syntax and parameter names need to be confirmed with the BRAVO system owners.)

*   **Data Mapping:**
    (This section will need to be filled in with the specific data elements that need to be mapped between LSCP and BRAVO.)