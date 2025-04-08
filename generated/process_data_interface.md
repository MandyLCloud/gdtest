```markdown
# Process Data Interface for Licensing Self-Certification Portal

![BDlogo](media/image1.jpg)

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
    * [1.1. Background](#11-background)
    * [1.2. Purpose of this Document](#12-purpose-of-this-document)
[2. System Data Process Interface](#2-system-data-process-interface)
[3. External Interfaces](#3-external-interfaces)
    * [3.1. List of External Interface Specification](#31-list-of-external-interface-specification)
    * [3.2. Interface Specification](#32-interface-specification)
        * [3.2.1. INT-SMIS-01 - Data Import from SMIS (BCIS)](#321-int-smis-01---data-import-from-smis-bcis)
        * [3.2.2. INT-OSDP-01 - Single Sign-On through OSDP](#322-int-osdp-01---single-sign-on-through-osdp)
        * [3.2.3. INT-MWMS2-01 - Data Import from MWMS2](#323-int-mwms2-01---data-import-from-mwms2)
        * [3.2.4. INT-ESH-01 - Data Import from ESH](#324-int-esh-01---data-import-from-esh)
        * [3.2.5. INT-ERKS-01 - Data Import from ERKS](#325-int-erks-01---data-import-from-erks)
        * [3.2.6. INT-BRAVO-01 - Data Import from BRAVO](#326-int-bravo-01---data-import-from-bravo)

## 1. Introduction

### 1.1. Background

The Buildings Department (BD) of the Hong Kong Special Administrative Region Government is responsible for providing expert advice on building and structural safety matters for various licensing regimes. To enhance efficiency and streamline the application process for certificates and notices, BD is developing the Licensing Self-Certification Portal (LSCP), also referred to as the Self-Certification System (SCS).

The LSCP aims to:

*   Enable online submission of applications and supporting documents by applicants, Authorized Persons (AP), and Registered Structural Engineers (RSE).
*   Facilitate electronic processing of applications by BD users, Education Bureau (EDB) users, and Social Welfare Department (SWD) users.
*   Provide a centralized data repository for all application-related information.
*   Integrate with other relevant government systems to improve data exchange and workflow efficiency.

This Process Data Interface (PDI) document outlines the data processing within the LSCP system and specifies the interfaces for integration with external systems.

### 1.2. Purpose of this Document

This Process Data Interface (PDI) document serves as a guide for the physical design and system integration of the Licensing Self-Certification Portal (LSCP). It is divided into three main sections:

1.  **Introduction:** Provides an overview of the LSCP and the purpose of this document.
2.  **System Data Process Interface:** Defines the general approach for handling data processing within the LSCP system.
3.  **External Interfaces:** Specifies the interfaces for system integration with external systems, including interface specifications.

This document is intended for developers, system administrators, and stakeholders involved in the design, development, and implementation of the LSCP.

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System (BCIS) | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | *Unknown*                               | *To be confirmed*                       |
| ERKS         | *Unknown*                               | *To be confirmed*                       |
| BRAVO        | *Unknown*                               | *To be confirmed*                       |

## 2. System Data Process Interface

The Process Data Interface (PDI) defines how the logical data model of the LSCP is implemented in the physical environment. It focuses on ensuring efficient data handling and facilitating system implementation and maintenance.

The LSCP's data process interface follows a consistent pattern for handling incoming requests:

1.  **Input Acceptance and Handling:**  Functions are designed to receive and process incoming data from various sources, including user inputs and external system interfaces.
2.  **Database Interaction:** Functions interact with the LSCP database to perform data updates, queries, and storage operations based on the processed input.

This approach ensures a structured and modular design for data processing within the LSCP system.

**In/Out data process flow diagram**

![In/Out data process flow diagram](media/image2.png)

## 3. External Interfaces

The LSCP is designed to interface with several external systems to enhance its functionality and data integration. These interfaces are crucial for data exchange, user authentication, and accessing related information from other BD systems.

### 3.1. List of External Interface Specification

The following table summarizes the external interfaces of the LSCP:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS (BCIS) | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:**
-  Some authentication and encryption methods are marked "To be determined" or left blank, pending further clarification and confirmation based on the specific requirements and capabilities of each external system.

### 3.2. Interface Specification

**(RY Note: the following sections are for reference only. Content is incorrect)**

### 3.2.1. INT-SMIS-01 - Data Import from SMIS (BCIS)  {#321-int-smis-01---data-import-from-smis-bcis}

*   **Target System:** Statutory Management Information System (SMIS), also known as BCIS (Building Control Information System)
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** The LSCP system will utilize stored procedures within the BCIS database to import necessary data. The specific data fields for import will be defined during the detailed design phase. This interface is crucial for retrieving address information, file references, and other master data from BCIS to facilitate case creation and data consistency within LSCP. (REQ-IR-01)

*   **Data Exchange:** Data transfer will occur directly between the databases via stored procedures.

*   **Authentication:** The authentication method for accessing the BCIS database is to be determined (e.g., database user credentials, API keys).

*   **Error Handling:** Stored procedures will incorporate error handling mechanisms to manage potential issues during data transfer and logging.

*   **Data Mapping:**

    | **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
    | :---------------- | :---------------- | :----------- | :-------------- |
    | *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
    | ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative):**

    ```sql
    EXECUTE SMIS.Import_LSCP_Data;
    ```

### 3.2.2. INT-OSDP-01 - Single Sign-On through OSDP {#322-int-osdp-01---single-sign-on-through-osdp}

*   **Target System:** Open Source Departmental Portal (OSDP)
*   **Interface Type:** URL redirection with departmental portal
*   **In / Out:** In
*   **Frequency:** Per user request

*   **Description:** This interface enables Single Sign-On (SSO) for BD users, EDB users, and SWD users. Users will access LSCP through their respective departmental portals (OSDP) without needing to re-enter credentials. A redirection link to LSCP will be provided within the BD Departmental Portal and other B/Ds Departmental Portals. The connection between departmental portals and LSCP is secured via SSL. (REQ-GR-07)

*   **Access from Buildings Departments (BD) Departmental Portal:**
    *   The access link to LSCP is: `https://lscp.bd.gov.hk`

*   **Access from other B/Ds Departmental Portal:**
    *   Users from other B/Ds will access LSCP through their departmental portals.
    *   Departmental portals will redirect requests through the CCGO gateway.
    *   The connection between departmental portals and LSCP will be SSL secured.

*   **Authentication and Authorization:**
    *   Departmental portal users need to apply for Intranet access to ITU to access LSCP.
    *   The LSCP System Administrator will create user accounts in LSCP based on submitted information.
    *   LSCP authenticates users based on the login name and department code forwarded from the departmental portal.
    *   Only users with matching login names and department codes in LSCP will be granted access.
    *   This authentication process applies to both BD users and other B/Ds users.

*   **Data Exchange:**
    *   The departmental portal must forward the "UID" (User ID) and "Dpdeptid" (Department ID) to LSCP in the HTTP response header.
    *   UID and Dpdeptid should contain the departmental portal user ID and department code.

**In/Out data process flow diagram**
![In/Out data process flow diagram for OSDP](media/image4.png)


### 3.2.3. INT-MWMS2-01 - Data Import from MWMS2 {#323-int-mwms2-01---data-import-from-mwms2}

*   **Target System:** Minor Works Management System 2.0 (MWMS2)
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** The LSCP system will retrieve AP/RSE (Authorized Person/Registered Structural Engineer) information from MWMS2. This data is crucial for verifying the identity and registration status of AP/RSEs who submit applications through LSCP. (REQ-WR-10, REQ-IR-03)

*   **Data Exchange:**
    1.  MWMS2 will generate Excel files containing AP/RSE data and place them in a designated SFTP server directory.
    2.  LSCP will connect to the SFTP server, authenticate, and download the Excel files via a scheduled task (e.g., daily).
    3.  LSCP will parse the Excel files and import the data into its database.

*   **Authentication:** SFTP access authentication will likely use SSH keys or username/password credentials.

*   **Error Handling:** The system should handle errors during file transfer, parsing, and database import, with logging and retry mechanisms.

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

    (Note: The exact format and content of the Excel file will be confirmed with MWMS2 system owners.)

### 3.2.4. INT-ESH-01 - Data Import from ESH {#324-int-esh-01---data-import-from-esh}

*   **Target System:** ESH (System Name to be confirmed)
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** LSCP will retrieve site project information from the ESH system via a scheduled daily task using SFTP. This interface is intended to validate if a user is involved in a specific site project, potentially for access control or application context. (REQ-IR-04)

*   **Data Exchange:**
    1.  ESH will generate and place files containing site project information in a designated SFTP server directory.
    2.  LSCP will connect to the SFTP server, authenticate, and download the files.
    3.  LSCP will parse the files and import the data into its database.

*   **Authentication:** SFTP access authentication will likely use SSH keys or username/password credentials.

*   **Error Handling:** The system should handle errors during file transfer, parsing, and database import, with appropriate logging and retry mechanisms.

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

### 3.2.5. INT-ERKS-01 - Data Import from ERKS {#325-int-erks-01---data-import-from-erks}

*   **Target System:** ERKS (System Name to be confirmed - likely Electronic Records Keeping System)
*   **Interface Type:** To Be Confirmed (TBC)
*   **In / Out:** In
*   **Frequency:** TBC

*   **Description:** This interface is for importing data from the ERKS system into LSCP for record-keeping purposes. The specific data to be imported and the interface mechanism are to be determined in consultation with ERKS system owners. (REQ-IR-05)

*   **Data Exchange:** The data exchange method (API, file transfer, database link, etc.) needs to be defined.

*   **Authentication:** The authentication and authorization mechanism for accessing ERKS data will need to be established.

*   **Error Handling:** Robust error handling is required to address issues during data exchange.

*   **Data Mapping:**  
    (This section will be populated with specific data elements mapped between ERKS and LSCP once details are confirmed.)

### 3.2.6. INT-BRAVO-01 - Data Import from BRAVO {#326-int-bravo-01---data-import-from-bravo}

*   **Target System:** BRAVO (System Name to be confirmed - likely BD Records and Archives Viewing Online)
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In
*   **Frequency:** Per User Request

*   **Description:** This interface enables LSCP to redirect users to BRAVO to view relevant building records and plans. LSCP can use URL redirection to BRAVO, passing parameters to search for specific cases or building information within BRAVO. (REQ-IR-06)

*   **Data Exchange:** LSCP will make HTTP requests (GET or POST) to BRAVO URLs, passing parameters in the URL query string or request body. BRAVO will respond with the requested data or redirect the user to the relevant information within the BRAVO system.

*   **Authentication:** The authentication method for accessing BRAVO (e.g., API keys, OAuth, or Intranet Sign-On) needs to be determined.

*   **Error Handling:** The system should handle errors returned by the BRAVO API and provide appropriate feedback to the user.

*   **URL Syntax (Examples):**

    *   **with Case number and Year:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    (Note: The exact URL syntax and parameter names need to be confirmed with the BRAVO system owners.)

*   **Data Mapping:**  
    (This section will be populated with specific data elements mapped between LSCP and BRAVO once details are confirmed.)

*** End of document***
```