```markdown
# Process Data Interface

![BDlogo](media/image1.jpg)

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

## 1. Introduction

This Process Data Interface (PDI) document outlines the data interfaces for the Licensing Self-Certification Portal (LSCP) project for the Buildings Department (BD). It details the system's internal data processing approach and its integration with various external systems. The document is structured into three main sections:

1.  **Introduction**: Provides an overview of the PDI's purpose and scope.
2.  **System Data Process Interface**: Defines the internal data handling mechanisms within the LSCP system.
3.  **External Interfaces**: Specifies the interfaces for integrating LSCP with external systems, including interface specifications.

This document serves as a guide for the physical design and implementation of LSCP, ensuring seamless data flow and interoperability with other BD systems and government portals.

The following table lists the external systems that LSCP will interface with:

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | Environmental Safety and Health System  | *To be confirmed*                       |
| ERKS         | Electronic Records Keeping System       | *To be confirmed*                       |
| BRAVO        | Buildings Records and Vetting Office System | *To be confirmed*                       |

## 2. System Data Process Interface

The System Data Process Interface defines the physical data design and components for processing data within the LSCP system. This interface ensures that the physical database implementation aligns with the Required System Logical Data Model, facilitating system implementation and future maintenance.

The core principle of the PDI is to manage data flow efficiently for each incoming process request. Functions within the system are designed to:

1.  **Accept and Handle Input**: Receive and validate incoming data.
2.  **Update and Enquire Database**: Interact with the database to process requests, update information, and retrieve data as needed.

The diagram below illustrates the position of the Process Data Interface (PDI) within the universal function model, depicting the In/Out data process flow:

![In/Out data process flow diagram](media/image2.png)

## 3. External Interfaces

This section details the external interfaces of the LSCP system, providing specifications for each integration point.

### 3.1. List of External Interface Specification

The table below summarizes the external interfaces for the LSCP system, including interface specifications, types, and security measures:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:** Some authentication and encryption methods are marked "To be determined" or left blank, pending further clarification and confirmation based on the specific requirements and capabilities of each external system.

### 3.2. Interface Specification

This section provides detailed specifications for each external interface.

#### 3.2.1. INT-SMIS-01- Data Import from SMIS

*   **Target System:** Statutory Management Information System (SMIS)
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** The LSCP system will utilize stored procedures within the SMIS database to import necessary data. The specific data fields for import will be defined during the detailed design phase. This interface aims to facilitate data consistency and reduce manual data entry.

*   **Data Exchange:** Data transfer will occur directly between the databases using stored procedures.

*   **Authentication:** The authentication method for accessing the SMIS database is to be determined (e.g., database user credentials, API keys).

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

#### 3.2.2. INT-OSDP-01 -Single Sign-On through OSDP

*   **Target System:** Open Source Departmental Portal (OSDP)
*   **Interface Type:** URL redirection with departmental portal
*   **In / Out:** In
*   **Frequency:** Per user request

*   **Description:** Single Sign-On (SSO) will be implemented through the OSDP, allowing users from BD and other government departments (B/Ds) to access LSCP using their existing departmental portal credentials. A redirection link to LSCP will be provided within the BD Departmental Portal and other B/Ds Departmental Portals. The connection between departmental portals and LSCP will be secured with SSL.

*   **Access Points:**
    *   **Buildings Departments (BD) Departmental Portal:** `https://lscp.bd.gov.hk`
    *   **Other B/Ds Departmental Portal:** Users from other B/Ds will access LSCP through their respective departmental portals, which will redirect requests via the CCGO gateway.

*   **Authentication and Authorization:**
    *   Departmental portal users seeking LSCP access must apply for Intranet access through ITU.
    *   LSCP System administrators will create accounts in LSCP based on submitted information.
    *   LSCP authenticates users by matching the login name and department code from the departmental portal account.
    *   Only users with matching accounts in LSCP will be granted access.

*   **Data Exchange:**
    *   Departmental portals must forward the "UID" (User ID) and "Dpdeptid" (Department ID) to LSCP in the HTTP response header.
    *   These parameters should contain the departmental portal user's ID and department code.

*   **In/Out data process flow diagram:**

    ![In/Out data process flow diagram](media/image4.png)

#### 3.2.3. INT-MWMS2-01- Data Import from MWMS2

*   **Target System:** Minor Works Management System 2.0 (MWMS2)
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** LSCP will retrieve Authorized Person (AP) / Registered Structural Engineer (RSE) information from MWMS2 via scheduled daily tasks. Data will be transferred as Excel files using SFTP. This interface ensures that AP/RSE data within LSCP is up-to-date and consistent with MWMS2.

*   **Data Exchange:**
    1.  MWMS2 generates Excel files and places them in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the Excel files.
    3.  LSCP parses the Excel files and imports the data into its database.

*   **Authentication:** SFTP access will be authenticated using SSH keys or username/password credentials.

*   **Error Handling:** The system will handle errors during file transfer, parsing, and database import, with logging and retry mechanisms.

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

#### 3.2.4. INT-ESH-01 -Data Import from ESH

*   **Target System:** Environmental Safety and Health System (ESH)
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** LSCP will retrieve site project information from ESH daily via scheduled tasks. Data will be transferred using SFTP. This interface is used to validate user involvement in site projects.

*   **Data Exchange:**
    1.  ESH generates files and places them in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the files.
    3.  LSCP parses the files and imports the data into its database.

*   **Authentication:** SFTP access will be authenticated using SSH keys or username/password credentials.

*   **Error Handling:** The system will handle errors during file transfer, parsing, and database import, with logging and retry mechanisms.

*   **File Format:**  The format needs to be confirmed (Excel, CSV, or JSON).

*   **Data Mapping:**

    | ESH Data Item | LSCP Data Item | Data Type | Description |
    | :---- | :---- | :---: | :---- |
    | File Reference | File Reference | string | BD Reference Number of the site project |
    | Site Address | Site Address | string | Address of the site project |
    | AP Registration Number | AP Registration Number | string | Registration number of the AP involved in the site project |
    | RSE Registration Number | RSE Registration Number | string | Registration number of the RSE involved in the site project |
    | RGE Registration Number | RGE Registration Number | string | Registration number of the RGE involved in the site project |
    | RC Registration Number | RC Registration Number | string | Registration number of the RC involved in the site project |

#### 3.2.5. INT-ERKS-01 -Data Import from ERKS

*   **Target System:** Electronic Records Keeping System (ERKS)
*   **Interface Type:** To Be Confirmed (TBC)
*   **In / Out:** In
*   **Frequency:** TBC

*   **Description:** This interface will facilitate data import from ERKS into LSCP. The specific data and mechanism will be defined in consultation with ERKS system owners. This integration will ensure that LSCP can leverage existing records within ERKS for improved data management and accessibility.

*   **Data Exchange:** The method of data exchange (API, file transfer, database link) needs to be defined.

*   **Authentication:** Authentication and authorization mechanisms for accessing ERKS data are to be established.

*   **Error Handling:** Robust error handling will be implemented to address issues during data exchange.

*   **Data Mapping:** (Specific data elements for mapping between ERKS and LSCP will be defined later)

#### 3.2.6. INT-BRAVO-01 -Data Import from BRAVO

*   **Target System:** Buildings Records and Vetting Office System (BRAVO)
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In
*   **Frequency:** Per User Request

*   **Description:** LSCP will integrate with BRAVO through HTTP redirection, allowing users to access BRAVO functionalities directly from LSCP. This interface will enable seamless access to building records and related information stored in BRAVO.

*   **Data Exchange:** LSCP will send HTTP requests (GET or POST) to BRAVO URLs, passing parameters in the URL query string or request body. BRAVO will respond with the requested data.

*   **Authentication:** The authentication method for accessing BRAVO (API keys, OAuth) is to be determined.

*   **Error Handling:** The system will handle errors returned by the BRAVO API and provide user feedback.

*   **URL Syntax (Examples):**
    *   **with Case number and Year:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`
    *   **with Block ID:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`
    *   **with full File Reference No:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    (Note: The exact URL syntax and parameter names need to be confirmed with BRAVO system owners.)

*   **Data Mapping:** (Specific data elements for mapping between LSCP and BRAVO will be defined later.)

*** End of document***
```