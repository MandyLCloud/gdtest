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
    [3.1. List of External Interface Specification](#31-list-of-external-interface-specification)
    [3.2. Interface Specification](#32-interface-specification)
        [3.2.1. INT-SMIS-01- Data Import from SMIS](#321-int-smis-01--data-import-from-smis)
        [3.2.2. INT-OSDP-01 -Single Sign-On through OSDP](#322-int-osdp-01--single-sign-on-through-osdp)
        [3.2.3. INT-MWMS2-01- Data Import from MWMS2](#323-int-mwms2-01--data-import-from-mwms2)
        [3.2.4. INT-ESH-01 -Data Import from ESH](#324-int-esh-01--data-import-from-esh)
        [3.2.5. INT-ERKS-01 -Data Import from ERKS](#325-int-erks-01--data-import-from-erks)
        [3.2.6. INT-BRAVO-01 -Data Import from BRAVO](#326-int-bravo-01--data-import-from-bravo)

# 1. Introduction

The Process Data Interface (PDI) document is structured into three main sections:

1. **Introduction**
    - Provides an overview of the PDI's purpose and contents.
2. **System Data Process Interface**
    - Defines the methodology for managing data processes within the Licensing Self-Certification Portal (LSCP) system.
3. **External Interfaces**
    - Details the approach for system integration with external systems, including specific interface specifications.

This PDI outlines the strategy for the physical design and integration of the LSCP for the Buildings Department (BD) with various external systems. The LSCP aims to modernize and streamline the process for handling applications related to Educational Premises (EP), Child Care Centres (CCC), and Temporary Places of Public Entertainment License (TPPEL).

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

The physical data design of the LSCP incorporates components that manage the physical processes of data handling. This interface is designed to make the database, implemented within the physical environment, appear as the Required System Logical Data Model to the processing components. This approach is intended to simplify system implementation and facilitate future maintenance.

For each incoming process request, the system is designed to:
1. Accept and process the input data.
2. Update and query the database as required.

The Process Data Interface (PDI) is positioned within the universal function model as depicted below:

**In/Out data process flow diagram**

![In/Out Data Process Flow Diagram](media/image2.png)


# 3. External Interfaces

## 3.1. List of External Interface Specification

The following table summarizes the external interfaces for the LSCP system:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:**
-  Authentication and encryption methods marked "To be determined" or left blank will be clarified and confirmed based on the specific requirements and capabilities of each external system.

## 3.2. Interface Specification

### 3.2.1. INT-SMIS-01- Data Import from SMIS

*   **Target System:** SMIS
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** The LSCP system will use stored procedures in the SMIS database to import necessary data. Specific data fields will be defined during the detailed design phase.
*   **Data Exchange:** Data transfer will occur directly between databases via stored procedures.
*   **Authentication:** Authentication method for SMIS database access to be determined (e.g., database user credentials, API keys).
*   **Error Handling:** Stored procedures will include error handling and logging for data transfer issues.
*   **Data Mapping:**

    | **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
    | :---------------- | :---------------- | :----------- | :-------------- |
    | *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
    | ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative):**
    ```sql
    EXECUTE SMIS.Import_LSCP_Data;
    ```

### 3.2.2. INT-OSDP-01 -Single Sign-On through OSDP

*   **Target System:** OSDP
*   **Interface Type:** URL redirection with departmental portal
*   **In / Out:** In
*   **Frequency:** Per user request

*   **Description:** BD and other Buildings Department (B/Ds) users will access LSCP through their departmental portals (OSDP). A redirection link to LSCP will be available on the BD Departmental Portal and other B/Ds Departmental Portals. Connections are SSL secured.

*   **Access from Buildings Departments (BD) Departmental Portal**
    -   Access link: [https://lscp.bd.gov.hk](https://lscp.bd.gov.hk)

*   **Access from other B/Ds Departmental Portal**
    -   Users from other B/Ds access LSCP via their departmental portals.
    -   Portals redirect requests through the CCGO gateway.
    -   Connections are SSL secured.

*   **Authentication and Authorization:**
    -   Departmental portal users require Intranet access application to ITU.
    -   LSCP System administrator creates accounts in LSCP based on submitted information.
    -   LSCP authenticates users using login name and department code from the departmental portal account.
    -   Login is granted only if matching account exists.
    -   Authentication applies to both BD and other B/Ds users.

*   **Data Exchange:**
    -   Departmental portal forwards "UID" and "Dpdeptid" to LSCP in the HTTP response header.
    -   UID and Dpdeptid contain departmental portal user ID and department code.

**In/Out data process flow diagram**
![OSDP Data Flow Diagram](media/image4.png)


### 3.2.3. INT-MWMS2-01- Data Import from MWMS2

*   **Target System:** MWMS2
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** LSCP retrieves AP/RSE information from MWMS2 via scheduled daily tasks. Files are transferred using SFTP.
*   **Data Exchange:**
    1. MWMS2 generates Excel files and places them in a designated SFTP server directory.
    2. LSCP connects to the SFTP server, authenticates, and downloads Excel files.
    3. LSCP parses Excel files and imports data into its database.
*   **Authentication:** SFTP access uses SSH keys or username/password credentials.
*   **Error Handling:** System handles errors during file transfer, parsing, and database import, with logging and retry mechanisms.
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

    (Note: Exact format and content to be confirmed with MWMS2 system owners.)

### 3.2.4. INT-ESH-01 -Data Import from ESH

*   **Target System:** ESH
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** LSCP retrieves site project information from ESH daily via SFTP. Imported data validates user involvement in site projects.
*   **Data Exchange:**
    1. ESH generates files and places them in a designated SFTP server directory.
    2. LSCP connects to the SFTP server, authenticates, and downloads files.
    3. LSCP parses files and imports data into its database.
*   **Authentication:** SFTP access uses SSH keys or username/password credentials.
*   **Error Handling:** System handles errors during file transfer, parsing, and database import, with logging and retry mechanisms.
*   **File Format:** Format needs confirmation (Excel, CSV, or JSON).
*   **Data Mapping:**

    | ESH Data Item | LSCP Data Item | Data Type | Description |
    | :---- | :---- | :---: | :---- |
    | File Reference | File Reference | string | BD Reference Number of the site project |
    | Site Address | Site Address | string | address of the site project |
    | AP Registration Number | AP Registration Number | string | Registration number of the AP that involve in the related site project |
    | RSE Registration Number | RSE Registration Number | string | Registration number of the RSE that involve in the related site project |
    | RGE Registration Number | RGE Registration Number | string | Registration number of the RGE that involve in the related site project |
    | RC Registration Number | RC Registration Number | string | Registration number of the RC that involve in the related site project |

### 3.2.5. INT-ERKS-01 -Data Import from ERKS

*   **Target System:** ERKS
*   **Interface Type:** TBC
*   **In / Out:** In
*   **Frequency:** TBC

*   **Description:** Interface involves importing data from ERKS to LSCP. Specifics to be determined with ERKS system owners.
*   **Data Exchange:** Data exchange method (API, file transfer, database link) to be defined.
*   **Authentication:** Authentication and authorization for ERKS data access to be established.
*   **Error Handling:** Robust error handling for data exchange issues required.
*   **Data Mapping:** (Specific data elements for mapping between ERKS and LSCP to be defined).

### 3.2.6. INT-BRAVO-01 -Data Import from BRAVO

*   **Target System:** BRAVO
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In
*   **Frequency:** Per User Request

*   **Description:** System redirects to BRAVO using [https://dp2.bd.hksarg/bravo/intranetSignOn](https://dp2.bd.hksarg/bravo/intranetSignOn) or via URL calls with parameters.
*   **Data Exchange:** LSCP makes HTTP requests (GET/POST) to BRAVO URLs, passing parameters in URL query string or request body. BRAVO responds with data.
*   **Authentication:** Authentication for BRAVO access (API keys, OAuth) to be determined.
*   **Error Handling:** System handles BRAVO API errors and provides user feedback.
*   **URL Syntax (Examples):**
    *   **with Case number and Year**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`
    *   **with Block ID**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`
    *   **with full File Reference No**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    (Note: Exact URL syntax and parameter names need confirmation from BRAVO system owners.)

*   **Data Mapping:** (Specific data elements for mapping between LSCP and BRAVO to be defined.)

*** End of document***
```