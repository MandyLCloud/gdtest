```markdown
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

| Distribution |  |
| :---: | :---: |
| Copy No. | Holder |
| 1 | Buildings Department (BD) |
| 2 | Master Concept (Hong Kong) Limited (MC) |

|  Amendment History  |  |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Change Number | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date | Approval Reference |
| 1 |  1st draft | All | 0.1 | 16/01/2025 |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

**TABLE OF CONTENTS**

[1. Introduction](#1-introduction)

[2. System Data Process Interface](#2-system-data-process-interface)

[3. External Interfaces](#3-external-interfaces)

[3.1 List of External Interface Specification](#31-list-of-external-interface-specification)

[3.2 Interface Specification](#32-interface-specification)

[3.2.1 INT-SMIS-01- Data Import from SMIS](#321-int-smis-01--data-import-from-smis)

[3.2.2 INT-OSDP-01 -Single Sign-On through OSDP](#322-int-osdp-01--single-sign-on-through-osdp)

[3.2.3 INT-MWMS2-01- Data Import from MWMS2](#323-int-mwms2-01--data-import-from-mwms2)

[3.2.4 INT-ESH-01 -Data Import from ESH](#324-int-esh-01--data-import-from-esh)

[3.2.5 INT-ERKS-01 -Data Import from ERKS](#325-int-erks-01--data-import-from-erks)

[3.2.6 INT-BRAVO-01 -Data Import from BRAVO](#326-int-bravo-01--data-import-from-bravo)

# 1. Introduction

The Process Data Interface (PDI) document is structured into three main sections:

1. **Introduction**
    - Provides an overview of the PDI's purpose and contents.

2. **System Data Process Interface**
    - Defines the data processing approach within the Licensing Self-Certification Portal (LSCP) system.

3. **External Interfaces**
    - Specifies the system's integration with external systems, including detailed interface specifications.

This document outlines the physical design and integration strategy for the LSCP system of the Buildings Department (BD), focusing on its interactions with external systems.

The following table lists the abbreviations used for external systems referenced in this document:

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | *Unknown*                               | *To be confirmed*                       |
| ERKS         | *Unknown*                               | *To be confirmed*                       |
| BRAVO        | *Unknown*                               | *To be confirmed*                       |


# 2. System Data Process Interface

The Process Data Interface (PDI) defines the physical data design and component interactions within the LSCP system. It ensures that the physical database implementation aligns with the Required System Logical Data Model, simplifying system implementation and future maintenance.

The PDI follows a consistent approach for processing requests:

1. **Input Handling:** Each function begins by accepting and processing input data.
2. **Database Interaction:** Functions then interact with the database to update or query data as required.

The diagram below illustrates the position of the PDI within the universal function model, depicting the In/Out data process flow:

![In/Out data process flow diagram](media/image2.png)

# 3. External Interfaces

## 3.1 List of External Interface Specification

The LSCP system is designed to interface with several external systems to ensure data consistency, streamline workflows, and enhance functionality. The following table summarizes the external interfaces:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:**
-  Authentication and encryption methods marked "To be determined" or left blank will be clarified and confirmed based on the specific requirements and capabilities of each external system during the detailed design phase.

## 3.2 Interface Specification

### 3.2.1 INT-SMIS-01- Data Import from SMIS

*   **Target System:** Statutory Management Information System (SMIS)
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:**
    The LSCP system will utilize stored procedures within the SMIS database to import necessary data. Specific data fields for import will be defined during the detailed design phase. This interface is crucial for maintaining data synchronization and leveraging existing data within BD systems.

*   **Data Exchange:**
    Data transfer will occur directly between the LSCP and SMIS databases via stored procedures, ensuring efficient and secure data retrieval.

*   **Authentication:**
    The authentication method for accessing the SMIS database is to be determined, potentially involving database user credentials or API keys, ensuring secure access and data integrity.

*   **Error Handling:**
    Stored procedures will incorporate error handling mechanisms to manage potential issues during data transfer, including logging for monitoring and debugging.

*   **Data Mapping:**

| **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
| :---------------- | :---------------- | :----------- | :-------------- |
| *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
| ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative):**

```sql
EXECUTE SMIS.Import_LSCP_Data;
```

### 3.2.2 INT-OSDP-01 -Single Sign-On through OSDP

*   **Target System:** Open Source Departmental Portal (OSDP)
*   **Interface Type:** URL redirection with departmental portal
*   **In / Out:** In
*   **Frequency:** Per user request

**Description:**
Single Sign-On (SSO) will be implemented through the OSDP, allowing BD and other Bureaux/Departments (B/Ds) users to access LSCP seamlessly via their departmental portals. This integration simplifies user access and enhances security by leveraging existing government infrastructure.

**Access Points:**

*   **Buildings Department (BD) Departmental Portal:**
    - Access link: `https://lscp.bd.gov.hk`

*   **Other B/Ds Departmental Portals:**
    - Users from other B/Ds will access LSCP through their respective departmental portals.
    - Redirection will occur via the CCGO gateway, ensuring secure communication.
    - Connection between B/Ds departmental portals and LSCP will be SSL secured.

**Authentication and Authorization:**

*   Departmental portal users seeking LSCP access must apply for Intranet access through ITU.
*   The LSCP System Administrator will create user accounts in LSCP based on submitted information.
*   LSCP authenticates users by matching login names and department codes with departmental portal accounts.
*   Only users with matching accounts in LSCP will be granted access.
*   This authentication process applies to both BD users and users from other B/Ds.

**Data Exchange:**

*   The departmental portal must forward the "UID" and "Dpdeptid" to LSCP in the HTTP response header.
*   "UID" and "Dpdeptid" will contain departmental portal user ID and department code information for authentication and authorization within LSCP.

**In/Out data process flow diagram**
![OSDP Data Flow](media/image4.png)

### 3.2.3 INT-MWMS2-01- Data Import from MWMS2

*   **Target System:** Minor Works Management System 2.0 (MWMS2)
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:**
    The LSCP system will automatically retrieve Authorized Person (AP) and Registered Structural Engineer (RSE) information from MWMS2 daily. This data is essential for verifying the credentials and registration status of APs and RSEs involved in self-certification processes.

*   **Data Exchange:**
    1. MWMS2 generates Excel files containing AP/RSE data and places them in a designated SFTP server directory.
    2. LSCP connects to the SFTP server, authenticates, and downloads these Excel files.
    3. LSCP parses the Excel files and imports the data into its database for use in the system.

*   **Authentication:**
    SFTP access authentication will likely utilize SSH keys or username/password credentials, ensuring secure file transfer.

*   **Error Handling:**
    Robust error handling will be implemented to manage potential issues during file transfer, parsing, and database import. This includes logging errors and implementing retry mechanisms to ensure data integrity.

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

    (Note: The exact format and content of the Excel file will be confirmed with the MWMS2 system owners.)

### 3.2.4 INT-ESH-01 -Data Import from ESH

*   **Target System:** ESH (System Name to be Confirmed)
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:**
    LSCP will retrieve site project information from the ESH system daily via SFTP. This interface is crucial for validating user involvement in site projects, ensuring that only authorized personnel can access and manage project-related data within LSCP.

*   **Data Exchange:**
    1. ESH generates files containing site project information and places them in a designated SFTP server directory.
    2. LSCP connects to the SFTP server, authenticates, and downloads these files.
    3. LSCP parses the files and imports the data into its database.

*   **Authentication:**
    SFTP access authentication will likely use SSH keys or username/password credentials.

*   **Error Handling:**
    Error handling will be implemented to manage potential issues during file transfer, parsing, and database import, including logging and retry mechanisms.

*   **File Format:**  The file format (Excel, CSV, JSON, etc.) needs to be confirmed with the ESH system owners.

*   **Data Mapping:**

| ESH Data Item | LSCP Data Item | Data Type | Description |
| :---- | :---- | :---: | :---- |
| File Reference | File Reference | string | BD Reference Number of the site project |
| Site Address | Site Address | string | Address of the site project |
| AP Registration Number | AP Registration Number | string | Registration number of the AP involved in the site project |
| RSE Registration Number | RSE Registration Number | string | Registration number of the RSE involved in the site project |
| RGE Registration Number | RGE Registration Number | string | Registration number of the RGE involved in the site project |
| RC Registration Number | RC Registration Number | string | Registration number of the RC involved in the site project |

### 3.2.5 INT-ERKS-01 -Data Import from ERKS

*   **Target System:** ERKS (System Name to be Confirmed)
*   **Interface Type:** To Be Confirmed (TBC)
*   **In / Out:** In
*   **Frequency:** TBC

*   **Description:**
    This interface will facilitate data import from the ERKS system into LSCP. The specific data to be exchanged and the interface mechanism will be determined in consultation with ERKS system owners during the detailed design phase.

*   **Data Exchange:**
    The data exchange method (API, file transfer, database link, etc.) is yet to be defined and will depend on ERKS capabilities and security requirements.

*   **Authentication:**
    The authentication and authorization mechanism for accessing ERKS data will be established in coordination with ERKS system administrators to ensure secure data access.

*   **Error Handling:**
    Robust error handling will be implemented to address any potential issues during the data exchange process, ensuring data integrity and system stability.

*   **Data Mapping:**
    (This section will be populated with specific data elements to be mapped between ERKS and LSCP once the data exchange requirements are finalized.)

### 3.2.6 INT-BRAVO-01 -Data Import from BRAVO

*   **Target System:** BRAVO
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In
*   **Frequency:** Per User Request

*   **Description:**
    LSCP will integrate with BRAVO via HTTP request redirection, allowing users to seamlessly access building plan information and case details directly from BRAVO. This integration enhances user experience by providing quick access to relevant building information.

*   **Data Exchange:**
    LSCP will send HTTP requests (GET or POST) to BRAVO URLs, passing necessary parameters in the URL query string or request body. BRAVO will respond with the requested data, typically redirecting the user to the relevant information within BRAVO.

*   **Authentication:**
    The authentication method for accessing BRAVO (API keys, OAuth, etc.) is to be determined in coordination with BRAVO system administrators.

*   **Error Handling:**
    LSCP will handle any errors returned by the BRAVO API and provide appropriate feedback to the user, ensuring a smooth and informative user experience.

*   **URL Syntax (Examples):**

    *   **with Case number and Year**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    (Note: The exact URL syntax and parameter names need to be confirmed with the BRAVO system owners.)

*   **Data Mapping:**
    (This section will be populated with specific data elements to be mapped between LSCP and BRAVO once the data exchange requirements are finalized.)

*** End of document***
```