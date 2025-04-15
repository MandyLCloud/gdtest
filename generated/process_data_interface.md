# Process Data Interface

This document consolidates information from multiple source files to provide a comprehensive overview of the Process Data Interface (PDI) for the Licensing Self-Certification Portal (LSCP) of the Buildings Department (BD).

## 1. Introduction

The Process Data Interface (PDI) document describes the approach for performing physical design and integration of the LSCP for the Buildings Department (BD) with other external systems.

The PDI consists of three main sections:

1.  **Introduction:** Explains the contents and purposes of the PDI.
2.  **System Data Process Interface:** Defines the approach for handling data processes within the system.
3.  **External Interfaces:** Defines the handling approach for system integration with external systems, including interface specifications.

## 2. System Data Process Interface

The implemented physical data design defines the components of the physical process. The interface makes the database implemented using the physical environment appear as the Required System Logical Data Model to the processing components. It aims to ease system implementation and future maintenance.

For every incoming process request, the function accepts and handles the input first. Then the function updates and enquires the database.

**In/Out data process flow diagram:**

[Diagram of In/Out data process flow] (./media/image2.png)

## 3. External Interfaces

This section details the system integration with external systems, providing interface specifications.

### 3.1 List of External Interface Specifications

The following table summarizes the external interfaces:

| System Scope | Interfacing Party/ System                   | Interface Spec. ID | Name                          | Interface Type           | In / Out | Authentication / Encryption | N/A | :----------- | :-------------------------------------- | :------------------ | :----------------------------- | :----------------------- | :------- | :-------------------------- | N/A |---|---|---|---|---|---|---| N/A | External     | SMIS         | INT-SMIS-01         | Data Import from SMIS         | Stored Procedure         | In       | *To be determined*        | N/A |---|---|---|---|---|---|---| N/A | External     | OSDP         | INT-OSDP-01         | Single Sign-On through OSDP | HTTP Request Redirection | In       | TLS 1.2 over HTTPS        | N/A |---|---|---|---|---|---|---| N/A | External     | MWMS2        | INT-MWMS2-01        | Data Import from MWMS2       | SFTP and Excel           | In       | SFTP                      | N/A |---|---|---|---|---|---|---| N/A | External     | ESH          | INT-ESH-01          | Data Import from ESH         | SFTP                      | In       | SFTP                      | N/A |---|---|---|---|---|---|---| N/A | External     | ERKS         | INT-ERKS-01          | Data Import from ERKS         | *To be confirmed*        | In       | *To be confirmed*        | N/A |---|---|---|---|---|---|---| N/A | External     | BRAVO        | INT-BRAVO-01        | Data Import from BRAVO       | HTTP Request Redirection | In       | *To be confirmed*        | N/A |---|---|---|---|---|---|---|
**Note:** Some authentication and encryption methods are marked "To be determined" or left blank. These will need to be clarified and confirmed based on the specific requirements and capabilities of each external system.

### 3.2 Interface Specifications

#### 3.2.1 INT-SMIS-01 - Data Import from SMIS

*   **Target System:** SMIS (Statutory Management Information System)
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily
*   **Description:** The LSCP system will call stored procedures in the SMIS database to import the necessary data. The exact data fields to be imported will need to be defined in the detailed design phase.
*   **Data Exchange:** The data will be transferred directly between the databases via the stored procedures.
*   **Authentication:** The authentication method for accessing the SMIS database will need to be determined (e.g., database user credentials, API keys).
*   **Error Handling:** The stored procedures should include error handling to manage potential issues during data transfer and logging.
*   **Data Mapping:**

    | **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | :---------------- | :---------------- | :----------- | :-------------- | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | ...             | ...             | ...          | ...             | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---|
*   **Example Stored Procedure Call (Illustrative):**

    ```sql
    EXECUTE SMIS.Import_LSCP_Data;
    ```

#### 3.2.2 INT-OSDP-01 - Single Sign-On through OSDP

*   **Target System:** OSDP (Open Source Departmental Portal)
*   **Interface Type:** URL redirection with departmental portal
*   **In / Out:** In
*   **Frequency:** Per user request
*   **Description:** Users from BD and other B/Ds will access the LSCP by logging into their respective departmental portals (OSDP). A link to redirect to the LSCP will be provided in the BD Departmental Portal and other B/Ds Departmental Portal. The connection between the other B/Ds departmental portal and the LSCP is SSL secured.
*   **Access from Buildings Departments (BD) Departmental Portal**
    *   The link to access the LSCP will be: `https://lscp.bd.gov.hk`
*   **Access from other B/Ds Departmental Portal**
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

**In/Out data process flow diagram**

[Diagram of OSDP Data Flow] (./media/image4.png)

#### 3.2.3 INT-MWMS2-01 - Data Import from MWMS2

*   **Target System:** MWMS2 (Minor Works Management System 2.0)
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily
*   **Description:** The LSCP system will retrieve Excel files containing AP/RSE information from the MWMS2 system via a scheduled task (e.g., daily). The files will be transferred using SFTP.
*   **Data Exchange:**
    1.  The MWMS2 system will generate and place Excel files in a designated SFTP server directory.
    2.  The LSCP system will connect to the SFTP server, authenticate, and download the Excel files.
    3.  The LSCP system will then parse the Excel files and import the data into its database.
*   **Authentication:** Authentication for SFTP access will likely use SSH keys or username/password credentials.
*   **Error Handling:** The system should handle potential errors during file transfer, parsing, and database import, with appropriate logging and retry mechanisms.
*   **Excel File Format:**

    | Field Name | Description                                                                   | Data Type | Format/Example | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | :--------- | :---------------------------------------------------------------------------- | :-------- | :------------- | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | AP_ID     | Unique identifier for the Authorized Person                                  | Number    | 12345          | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | AP_NAME   | Name of the Authorized Person                                                | Text      | John Doe       | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | AP_REG_NO | Registration number of the Authorized Person                               | Text      | AP-98765       | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | RSE_ID    | Unique identifier for the Registered Structural Engineer                    | Number    | 67890          | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | RSE_NAME  | Name of the Registered Structural Engineer                                   | Text      | Jane Smith     | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | RSE_REG_NO| Registration number of the Registered Structural Engineer                   | Text      | RSE-54321      | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | ...        | ...                                                                           | ...       | ...            | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---|
    (Note: The exact format and content of the Excel file will need to be confirmed with the MWMS2 system owners.)

#### 3.2.4 INT-ESH-01 - Data Import from ESH

*   **Target System:** ESH
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily
*   **Description:** The LSCP system will retrieve site project information from the ESH system via a scheduled task (e.g., daily). The files will be transferred using SFTP. The imported information is used for validating if a user is involved in the site project.
*   **Data Exchange:**
    1.  The ESH system will generate and place files in a designated SFTP server directory.
    2.  The LSCP system will connect to the SFTP server, authenticate, and download the files.
    3.  The LSCP system will then parse the files and import the data into its database.
*   **Authentication:** Authentication for SFTP access will likely use SSH keys or username/password credentials.
*   **Error Handling:** The system should handle potential errors during file transfer, parsing, and database import, with appropriate logging and retry mechanisms.
*   **File Format:** The format needs to be confirmed. The file could be excel, csv or json.
*   **Data Mapping:**

    | ESH Data Item | LSCP Data Item | Data Type | Description | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | :---- | :---- | :---: | :---- | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | File Reference | File Reference | string | BD Reference Number of the site project | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | Site Address | Site Address | string | address of the site project | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | AP Registration Number | AP Registration Number | string | Registration number of the AP that involve in the related site project | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | RSE Registration Number | RSE Registration Number | string | Registration number of the RSE that involve in the related site project | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | RGE Registration Number | RGE Registration Number | string | Registration number of the RGE that involve in the related site project | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---| N/A | RC Registration Number | RC Registration Number | string | Registration number of the RC that involve in the related site project | N/A |---|---|---|---| N/A | N/A |---|---|---|---|---|
#### 3.2.5 INT-ERKS-01 - Data Import from ERKS

*   **Target System:** ERKS
*   **Interface Type:** TBC (To Be Confirmed)
*   **In / Out:** In
*   **Frequency:** TBC (To Be Confirmed)
*   **Description:** This interface will likely involve importing data from the ERKS system into LSCP. The specifics of the data and the mechanism will need to be determined in consultation with the ERKS system owners.
*   **Data Exchange:** The method of data exchange (e.g., API, file transfer, database link) needs to be defined.
*   **Authentication:** The authentication and authorization mechanism for accessing ERKS data will need to be established.
*   **Error Handling:** Robust error handling will be required to address any issues during the data exchange process.
*   **Data Mapping:** (This section will need to be filled in with the specific data elements that need to be mapped between ERKS and LSCP)

#### 3.2.6 INT-BRAVO-01 - Data Import from BRAVO

*   **Target System:** BRAVO
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
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=<SUBJECT_CODE>&CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>&SPECIAL_CAT=<SPECIAL_CAT>`

    (Note: The exact URL syntax and parameter names need to be confirmed with the BRAVO system owners.)
*   **Data Mapping:** (This section will need to be filled in with the specific data elements that need to be mapped between LSCP and BRAVO.)

***End of document***
