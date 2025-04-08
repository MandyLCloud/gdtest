```markdown
![BDlogo](media/image1.jpg)

# Process Data Interface

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

| Distribution |  |
| :---: | :---: |
| Copy No. | Holder |
| 1 | Buildings Department (BD) |
| 2 | Master Concept (Hong Kong) Limited (MC) |

|  Amendment History  |  |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Change Number | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date | Approval Reference |
| 1 |  1st draft | All | 0.1 | 16/01/2025 |  |

**TABLE OF CONTENTS**

[1. Introduction](#1-introduction)
[2. System Data Process Interface](#2-system-data-process-interface)
[3. External Interfaces](#3-external-interfaces)
    [3.1. List of External Interface Specification](#31-list-of-external-interface-specification)
    [3.2. Interface Specification](#32-interface-specification)
        [3.2.1. INT-SMIS-01- Data Import from SMIS](#321-int-smis-01--data-import-from-smis)
        [3.2.2. INT-OSDP-01 -Single Sign-On through OSDP](#322-int-osdp-01--single-sign-on-through-osdp)
        [3.2.3. INT-MWMS2-01- Data Import from MWMS2](#323-int-mwms2-01--data-import-from-mwms2)
        [3.2.4. INT-ESH-01 -Data Import from ESH](#324-int-esh-01--data-import-from-esh)
        [3.2.5. INT-ERKS-01 -Data Import from ERKS](#325-int-erks-01--data-import-from-erks)
        [3.2.6. INT-BRAVO-01 -Data Import from BRAVO](#326-int-bravo-01--data-import-from-bravo)

# 1. Introduction

This Process Data Interface (PDI) document outlines the data processing and system integration aspects of the Licensing Self-Certification Portal (LSCP) for the Buildings Department (BD). The LSCP is a new system designed to streamline the process of receiving, processing, and managing applications for certificates and notices required under the Education Ordinance (Cap.279) and Child Care Services Ordinance (Cap. 243). It also aims to provide building safety comments to the Education Bureau for premises conducting courses under the Non-Local-Higher and Professional Education (Regulation) Ordinance [NLHPE(R)O].

The PDI document is divided into three main sections:

1.  **Introduction:** Provides an overview of the PDI's purpose and scope within the LSCP project.
2.  **System Data Process Interface:** Defines the internal data handling mechanisms within the LSCP system.
3.  **External Interfaces:** Specifies the interfaces for integrating LSCP with other external systems, detailing data exchange, authentication, and error handling.

This document serves as a guide for the physical design and implementation of the LSCP, ensuring seamless data flow and interoperability with existing BD systems and other government systems. The LSCP aims to address current issues such as long processing times, lack of management reports, and the absence of a centralized repository for application records, as highlighted in the Current Environment Description. By implementing efficient data interfaces, the LSCP will enhance the efficiency and effectiveness of the Buildings Department's licensing processes.

The following table lists the external systems that LSCP will interface with:

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | *Unknown*                               | *To be confirmed*                       |
| ERKS         | *Unknown*                               | *To be confirmed*                       |
| BRAVO        | *Unknown*                               | *To be confirmed*                       |

# 2. System Data Process Interface

The System Data Process Interface defines how the LSCP will internally manage and process data. It bridges the gap between the logical data model and the physical database implementation. This interface is designed to simplify system implementation, maintenance, and ensure data integrity.

The core principle of the PDI is that for each incoming process request, the system will:

1.  **Accept and Handle Input:** Receive and validate the incoming data.
2.  **Update and Query Database:** Interact with the physical database to store, retrieve, and modify data as required by the process.

This approach ensures a clear separation of concerns, where processing components interact with the database through a well-defined interface, abstracting away the complexities of the underlying physical data storage.

The diagram below illustrates the position of the Process Data Interface (PDI) within the universal function model, showing the In/Out data process flow:

![PDI Data Flow](media/image2.png)


# 3. External Interfaces

## 3.1. List of External Interface Specification

The LSCP is designed to interface with several external systems to enhance its functionality and data integration. The following table summarizes the external interfaces:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:** Authentication and encryption methods marked "To be determined" or left blank will be clarified and confirmed based on the specific requirements and capabilities of each external system during the detailed design phase.

## 3.2. Interface Specification

### 3.2.1. INT-SMIS-01- Data Import from SMIS

*   **Target System:** Statutory Management Information System (SMIS)
*   **Interface Type:** Stored Procedure
*   **In / Out:** In (LSCP receives data from SMIS)
*   **Frequency:** Daily

*   **Description:**
    The LSCP system will periodically import data from SMIS to maintain data consistency and leverage existing building safety information. This interface will be implemented by calling stored procedures within the SMIS database from LSCP. The specific data fields to be imported will be defined during the detailed design phase to ensure LSCP has access to necessary statutory management information.

*   **Data Exchange:**
    Data will be exchanged directly between the LSCP and SMIS databases using stored procedures. This method ensures efficient and secure data transfer within the government network.

*   **Authentication:**
    Authentication for accessing the SMIS database will be determined based on security protocols and may involve database user credentials or API keys. Secure access is paramount to protect sensitive data.

*   **Error Handling:**
    Stored procedures will incorporate robust error handling mechanisms to manage potential issues during data transfer. Error logging will be implemented to track and resolve any data import failures.

*   **Data Mapping:**

    | **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
    | :---------------- | :---------------- | :----------- | :-------------- |
    | *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
    | ...             | ...             | ...          | ...             |
    *(Detailed data mapping will be defined in the detailed design phase)*

*   **Example Stored Procedure Call (Illustrative):**

    ```sql
    EXECUTE SMIS.Import_LSCP_Data;
    ```

### 3.2.2. INT-OSDP-01 -Single Sign-On through OSDP

*   **Target System:** Open Source Departmental Portal (OSDP)
*   **Interface Type:** URL redirection with departmental portal
*   **In / Out:** In (LSCP receives user authentication from OSDP)
*   **Frequency:** Per user request

*   **Description:**
    To provide seamless access for BD users and users from other government departments, LSCP will implement Single Sign-On (SSO) through the Government Open Source Departmental Portal (OSDP). Users will access LSCP via links within their respective departmental portals. This integration streamlines user login and enhances security by leveraging existing government authentication infrastructure.

*   **Access from Buildings Departments (BD) Departmental Portal:**
    -   The link to access the LSCP will be: `https://lscp.bd.gov.hk`

*   **Access from other B/Ds Departmental Portal:**
    -   Users from other departments will access LSCP through their own departmental portals.
    -   Their departmental portals will redirect the request through the CCGO gateway.
    -   The connection between the other B/Ds departmental portal and the LSCP will be SSL secured (TLS 1.2 over HTTPS).

*   **Authentication and Authorization:**
    -   Departmental portal users intending to access LSCP will need to apply for Intranet access through ITU.
    -   LSCP System administrators will create user accounts in LSCP based on submitted information.
    -   LSCP will authenticate users by verifying the login name and department code against the departmental portal account information.
    -   Only users with matching accounts in LSCP will be granted access. This authentication process applies to both BD users and users from other departments.

*   **Data Exchange:**
    -   The departmental portal must forward the "UID" (User ID) and "Dpdeptid" (Department ID) to LSCP in the HTTP response header.
    -   These parameters will contain the necessary user and department identification for authentication and authorization within LSCP.

*   **In/Out data process flow diagram:**

    ![OSDP Data Flow](media/image4.png)

### 3.2.3. INT-MWMS2-01- Data Import from MWMS2

*   **Target System:** Minor Works Management System 2.0 (MWMS2)
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In (LSCP receives data from MWMS2)
*   **Frequency:** Daily

*   **Description:**
    LSCP requires up-to-date information on Authorized Persons (APs) and Registered Structural Engineers (RSEs) for application verification. This interface will retrieve AP/RSE data from MWMS2, the authoritative source for this information. Data will be transferred daily via SFTP in Excel file format.

*   **Data Exchange:**
    1.  MWMS2 will generate Excel files containing AP/RSE data and place them in a designated SFTP server directory.
    2.  LSCP will connect to the SFTP server using secure SFTP protocol, authenticate, and download the Excel files.
    3.  LSCP will parse the downloaded Excel files and import the AP/RSE data into its database, ensuring data accuracy and consistency.

*   **Authentication:**
    SFTP access will be secured using SSH keys or username/password credentials, ensuring only authorized systems can access the data.

*   **Error Handling:**
    The system will implement error handling for file transfer, parsing, and database import processes. Logging and retry mechanisms will be included to manage potential errors and ensure data integrity.

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
    *(The exact format and content of the Excel file will be confirmed with MWMS2 system owners during detailed design)*

### 3.2.4. INT-ESH-01 -Data Import from ESH

*   **Target System:** ESH (System Name to be Confirmed)
*   **Interface Type:** SFTP
*   **In / Out:** In (LSCP receives data from ESH)
*   **Frequency:** Daily

*   **Description:**
    To enhance user validation and project context, LSCP will import site project information from ESH. This interface will facilitate the validation of user involvement in specific site projects, potentially for authorization purposes. Data will be transferred daily via SFTP.

*   **Data Exchange:**
    1.  ESH will generate files containing site project information and place them in a designated SFTP server directory.
    2.  LSCP will connect to the SFTP server using secure SFTP protocol, authenticate, and download the files.
    3.  LSCP will parse the downloaded files and import the relevant site project data into its database.

*   **Authentication:**
    SFTP access will be secured using SSH keys or username/password credentials.

*   **Error Handling:**
    Error handling mechanisms will be implemented to manage file transfer, parsing, and database import errors, including logging and retry attempts.

*   **File Format:** The file format (Excel, CSV, JSON, etc.) needs to be confirmed with the ESH system owners.

*   **Data Mapping:**

    | ESH Data Item | LSCP Data Item | Data Type | Description |
    | :---- | :---- | :---: | :---- |
    | File Reference | File Reference | string | BD Reference Number of the site project |
    | Site Address | Site Address | string | Address of the site project |
    | AP Registration Number | AP Registration Number | string | Registration number of the AP involved in the site project |
    | RSE Registration Number | RSE Registration Number | string | Registration number of the RSE involved in the site project |
    | RGE Registration Number | RGE Registration Number | string | Registration number of the RGE involved in the site project |
    | RC Registration Number | RC Registration Number | string | Registration number of the RC involved in the site project |
    *(Detailed data mapping and file format will be confirmed with ESH system owners during detailed design)*

### 3.2.5. INT-ERKS-01 -Data Import from ERKS

*   **Target System:** ERKS (System Name to be Confirmed)
*   **Interface Type:** To Be Confirmed (TBC)
*   **In / Out:** In (LSCP receives data from ERKS)
*   **Frequency:** To Be Confirmed (TBC)

*   **Description:**
    LSCP will interface with ERKS to import relevant data, likely for record-keeping and data synchronization purposes. The specific data to be exchanged and the interface mechanism are yet to be determined and will be finalized in consultation with ERKS system owners.

*   **Data Exchange:** The method of data exchange (API, file transfer, database link, etc.) needs to be defined based on ERKS capabilities and security requirements.

*   **Authentication:** Authentication and authorization mechanisms for accessing ERKS data will be established in coordination with ERKS system administrators to ensure secure data access.

*   **Error Handling:** Robust error handling will be implemented to address potential issues during data exchange, ensuring data integrity and system stability.

*   **Data Mapping:**
    *(Specific data elements for mapping between ERKS and LSCP will be defined during the detailed design phase in collaboration with ERKS system owners)*

### 3.2.6. INT-BRAVO-01 -Data Import from BRAVO

*   **Target System:** BRAVO (Buildings Department Records and Archives Viewing Online)
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In (LSCP redirects user to BRAVO and receives data via redirection)
*   **Frequency:** Per User Request

*   **Description:**
    LSCP will integrate with BRAVO to allow users to access building records and related case information directly from within LSCP. This interface will be implemented through HTTP request redirection, allowing users to seamlessly navigate to BRAVO with relevant case parameters.

*   **Data Exchange:**
    LSCP will use HTTP requests (GET or POST) to redirect users to specific BRAVO URLs. Parameters such as Case Number, Year, Block ID, and File Reference No. will be passed in the URL to directly access relevant records in BRAVO. BRAVO will respond by displaying the requested information within the user's browser.

*   **Authentication:** The authentication method for accessing BRAVO will be determined, potentially using API keys or OAuth, to ensure secure access to building records.

*   **Error Handling:** LSCP will handle any errors returned by BRAVO and provide appropriate feedback to the user, ensuring a user-friendly experience even in case of integration issues.

*   **URL Syntax (Examples):**

    *   **with Case number and Year:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    *(The exact URL syntax and parameter names will be confirmed with BRAVO system owners during detailed design)*

*   **Data Mapping:**
    *(Specific data elements for mapping between LSCP and BRAVO will be defined during the detailed design phase in collaboration with BRAVO system owners)*

*** End of document***
```