# Process Data Interface Document

![BDlogo](media/image1.jpg)

**PROCESS DATA INTERFACE**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**

**LICENSING SELF-CERTIFICATION PORTAL**

**OF**

**BUILDINGS DEPARTMENT**

**Version: 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

## 1. Introduction

This Process Data Interface (PDI) document outlines the approach for handling data processes within the Licensing Self-Certification Portal (LSCP) and its integration with external systems. The LSCP is a new system proposed to modernize and streamline the application process for certificates and notices required by the Buildings Department (BD) for various licensing regimes, including Educational Premises (EP), Child Care Centre (CCC), and Temporary Places of Public Entertainment License (TPPEL).

The PDI document is divided into three main sections:

1.  **Introduction**: Provides an overview of the PDI's purpose and scope.
2.  **System Data Process Interface**: Defines the internal data handling approach within the LSCP system.
3.  **External Interfaces**: Specifies the system's integration with external systems, including interface specifications.

This document serves as a guide for the physical design and implementation of the LSCP, ensuring seamless data flow and interoperability with existing systems.

**Abbreviations:**

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | *Unknown*                               | *To be confirmed*                       |
| ERKS         | Electronic Records Keeping System       | *To be confirmed*                       |
| BRAVO        | Buildings Records and Approval Viewing Online | *To be confirmed*                       |

## 2. System Data Process Interface

The Process Data Interface (PDI) defines how the logical data model of the LSCP is implemented in the physical environment. It focuses on ensuring efficient data handling and processing within the system's components.

The core principle of the PDI is to manage data flow for each incoming process request by:

1.  **Accepting and Handling Input**:  Functions are designed to receive and validate incoming data.
2.  **Database Interaction**: Functions interact with the database to update, query, and retrieve information as needed.

This approach aims to simplify system implementation, enhance maintainability, and ensure data integrity.

**In/Out Data Process Flow Diagram:**

![In/Out data process flow diagram](media/image2.png)

## 3. External Interfaces

The LSCP is designed to interface with several external systems to leverage existing data and functionalities, ensuring a cohesive and efficient workflow.  These interfaces are crucial for data exchange, user authentication, and accessing related information from other BD systems.

### 3.1 List of External Interface Specification

The following table summarizes the external interfaces of the LSCP:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:** Authentication and encryption methods marked "To be determined" will be clarified and confirmed based on the specific requirements and capabilities of each external system during the detailed design phase.

### 3.2 Interface Specification

#### 3.2.1 INT-SMIS-01- Data Import from SMIS

*   **Target System:** Statutory Management Information System (SMIS)
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:**
    The LSCP system will import data from SMIS by calling stored procedures within the SMIS database. This interface aims to retrieve essential master data, such as address lists and file references, from BCIS (Building Control Information System), which is mentioned in `urs_a1.md` as the system to interface with for master data and case creation.  This aligns with the requirement `REQ-IR-01` in `urs_a1.md` to "Receive list of address, file reference or other master data from BCIS to facilitate creation of case on a daily basis".

*   **Data Exchange:**
    Data transfer will occur directly between the LSCP and SMIS databases using stored procedures.

*   **Authentication:**
    The authentication method for accessing the SMIS database will be determined, potentially using database user credentials or API keys.

*   **Error Handling:**
    Stored procedures will incorporate error handling mechanisms to manage data transfer issues and logging.

*   **Data Mapping:**
    *(To be defined in detail design phase)*

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

*   **Description:**
    Single Sign-On (SSO) functionality will be implemented through the OSDP, as per requirement `REQ-GR-07` in `urs_a1.md`. BD users and users from other government departments will access LSCP via their respective departmental portals.  A redirection link will be provided in the BD Departmental Portal and other B/Ds Departmental Portals.

*   **Access URLs:**
    *   **Buildings Departments (BD) Departmental Portal:** `https://lscp.bd.gov.hk`
    *   **Other B/Ds Departmental Portal:** Users will access LSCP through their own portals, which will redirect requests through the CCGO gateway.

*   **Authentication and Authorization:**
    *   Departmental portal users require Intranet access to ITU and a registered LSCP account.
    *   LSCP authenticates users based on login name and department code from the departmental portal account.
    *   User accounts for EDB and SWD will be created for maintaining user accounts and access rights in SCS as mentioned in `REQ-GR-07` of `urs_a1.md`.

*   **Data Exchange:**
    *   The departmental portal forwards "UID" and "Dpdeptid" in the HTTP response header to LSCP.
    *   "UID" and "Dpdeptid" contain departmental portal user ID and department code.

*   **In/Out Data Process Flow Diagram:**
    ![In/Out data process flow diagram for OSDP](media/image4.png)

#### 3.2.3 INT-MWMS2-01- Data Import from MWMS2

*   **Target System:** Minor Works Management System 2.0 (MWMS2)
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:**
    LSCP will retrieve AP/RSE (Authorized Person/Registered Structural Engineer) data from MWMS 2.0 daily, as required by `REQ-WR-10` in `urs_a1.md` for AP/RSE verification. This data is crucial for verifying the identity and registration status of AP/RSEs involved in applications.

*   **Data Exchange:**
    1.  MWMS2 generates Excel files containing AP/RSE data and places them in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the Excel files.
    3.  LSCP parses the Excel files and imports the data into its database.

*   **Authentication:**
    SFTP access will be authenticated using SSH keys or username/password credentials.

*   **Error Handling:**
    The system will handle errors during file transfer, parsing, and database import, with logging and retry mechanisms.

*   **Excel File Format:**
    *(Note: The exact format and content of the Excel file will need to be confirmed with MWMS2 system owners.)*

    | Field Name | Description                                                                   | Data Type | Format/Example |
    | :--------- | :---------------------------------------------------------------------------- | :-------- | :------------- |
    | AP\_ID     | Unique identifier for the Authorized Person                                  | Number    | 12345          |
    | AP\_NAME   | Name of the Authorized Person                                                | Text      | John Doe       |
    | AP\_REG\_NO | Registration number of the Authorized Person                               | Text      | AP-98765       |
    | RSE\_ID    | Unique identifier for the Registered Structural Engineer                    | Number    | 67890          |
    | RSE\_NAME  | Name of the Registered Structural Engineer                                   | Text      | Jane Smith     |
    | RSE\_REG\_NO| Registration number of the Registered Structural Engineer                   | Text      | RSE-54321      |
    | ...        | ...                                                                           | ...       | ...            |

#### 3.2.4 INT-ESH-01 - Data Import from ESH

*   **Target System:** ESH (System Name Unknown)
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:**
    LSCP will import site project information from the ESH system daily via SFTP. This interface is intended to validate user involvement in site projects, although the specific purpose and data details require further clarification.

*   **Data Exchange:**
    1.  ESH generates files and places them in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the files.
    3.  LSCP parses the files and imports the data into its database.

*   **Authentication:**
    SFTP access will be authenticated using SSH keys or username/password credentials.

*   **Error Handling:**
    The system will handle errors during file transfer, parsing, and database import, with logging and retry mechanisms.

*   **File Format:**  *(To be confirmed - could be Excel, CSV, or JSON)*

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

*   **Target System:** Electronic Records Keeping System (ERKS)
*   **Interface Type:** *To be confirmed*
*   **In / Out:** In
*   **Frequency:** *To be confirmed*

*   **Description:**
    This interface is for importing data from ERKS into LSCP, primarily for record keeping purposes as mentioned in `REQ-IR-05` of `urs_a1.md`.  The specific data and interface mechanism are to be determined in consultation with ERKS system owners.

*   **Data Exchange:**
    The data exchange method (API, file transfer, database link) needs to be defined.

*   **Authentication:**
    Authentication and authorization mechanisms for accessing ERKS data need to be established.

*   **Error Handling:**
    Robust error handling is required for data exchange issues.

*   **Data Mapping:**
    *(This section will be filled in with specific data elements to be mapped between ERKS and LSCP)*

#### 3.2.6 INT-BRAVO-01 - Data Import from BRAVO

*   **Target System:** Buildings Records and Approval Viewing Online (BRAVO)
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In
*   **Frequency:** Per User Request

*   **Description:**
    LSCP will interface with BRAVO using HTTP redirection to access building records and approved plans, as per `REQ-IR-06` in `urs_a1.md`. This allows BD users to retrieve approved plans for site inspections and case processing.

*   **Data Exchange:**
    LSCP will make HTTP requests (GET or POST) to BRAVO URLs, passing parameters in the URL query string or request body. BRAVO will respond with the requested data.

*   **Authentication:**
    The authentication method for accessing BRAVO (API keys, OAuth) needs to be determined.

*   **Error Handling:**
    The system should handle errors returned by the BRAVO API and provide user feedback.

*   **URL Syntax (Examples):**
    *   **with Case number and Year:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    *(Note: The exact URL syntax and parameter names need to be confirmed with BRAVO system owners.)*

*   **Data Mapping:**
    *(This section will be filled in with specific data elements to be mapped between LSCP and BRAVO.)*

*** End of document***