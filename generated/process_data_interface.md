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

[3.2.1 INT-SMIS-01- Data Import from BCIS](#321-int-smis-01--data-import-from-bcis)

[3.2.2 INT-OSDP-01 - Single Sign-On through OSDP](#322-int-osdp-01---single-sign-on-through-osdp)

[3.2.3 INT-MWMS2-01- Data Import from MWMS2](#323-int-mwms2-01--data-import-from-mwms2)

[3.2.4 INT-ESH-01 - Data Import from ESH](#324-int-esh-01---data-import-from-esh)

[3.2.5 INT-ERKS-01 - Data Import from ERKS](#325-int-erks-01---data-import-from-erks)

[3.2.6 INT-BRAVO-01 - Data Import from BRAVO](#326-int-bravo-01---data-import-from-bravo)

# **1. Introduction** {#1-introduction}

The Process Data Interface (PDI) document outlines the data process and integration aspects of the Licensing Self-Certification Portal (LSCP) for the Buildings Department (BD). This document is divided into three main sections:

1. **Introduction**
    - Provides an overview of the PDI's purpose and scope within the LSCP project.

2. **System Data Process Interface**
    - Describes the internal data handling mechanisms within the LSCP system, focusing on how data is processed and managed within the system's components.

3. **External Interfaces**
    - Details the interfaces for integrating the LSCP system with various external systems. This section includes specifications for each interface, covering data exchange, authentication, and error handling.

This PDI serves as a guide for the physical design and implementation of the LSCP, ensuring seamless data flow and interoperability with other systems within the Buildings Department and related government entities. The LSCP aims to modernize and streamline the application and processing of certificates and notices required under various ordinances, enhancing efficiency and user experience for both applicants and BD users.

The following table lists the external systems that LSCP will interface with:

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| BCIS         | Building Control Information System     | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | E-Submission Hub                        | *To be confirmed*                       |
| ERKS         | Electronic Records Keeping System       | *To be confirmed*                       |
| BRAVO        | Buildings Records and Viewing Online    | *To be confirmed*                       |


# **2. System Data Process Interface** {#2-system-data-process-interface}

The Process Data Interface (PDI) in LSCP is designed to bridge the gap between the logical data model and the physical implementation of the system's database and processing components. This interface ensures that the underlying physical data storage and retrieval mechanisms are transparent to the system's functional modules, simplifying development and maintenance.

The PDI is responsible for:

- **Data Input Handling**: Accepting and validating incoming data from various sources, both internal and external.
- **Database Interaction**:  Providing a consistent and efficient way for system functions to query and update the database.
- **Data Transformation**:  Converting data between different formats as needed for processing and storage.
- **Process Orchestration**: Managing the flow of data through different processing stages within the system.

The diagram below illustrates the position of the Process Data Interface (PDI) within the system's function model, showing the flow of data into and out of the processing components and the database.

![In/Out data process flow diagram](media/image2.png)

# **3. External Interfaces** {#3-external-interfaces}

## 3.1 List of External Interface Specification {#31-list-of-external-interface-specification}

The LSCP system is designed to interface with several external systems to exchange data and leverage existing functionalities. The following table summarizes the external interfaces and their specifications:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | BCIS | INT-SMIS-01 | Data Import from BCIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:**
-  Some authentication and encryption methods are marked "To be determined" or left blank, pending further clarification and confirmation based on the specific requirements and capabilities of each external system.

## 3.2 Interface Specification {#32-interface-specification}

### 3.2.1 INT-SMIS-01- Data Import from BCIS  {#321-int-smis-01--data-import-from-bcis}

**Target System:**		BCIS (Building Control Information System)

**Requirement ID:** REQ-IR-01 Interface with BCIS

**Interface Type:**	Stored Procedure

**In / Out:**		In

**Frequency:**		Daily

*   **Description:**
    The LSCP system will interface with BCIS to facilitate case creation and data synchronization. This interface involves importing master data from BCIS to LSCP and sending application data from LSCP to BCIS.  Specifically, LSCP will call stored procedures within the BCIS database to import necessary data.

*   **Data Exchange:**
    Data will be transferred directly between the databases using stored procedures. This includes:
    1. Receiving lists of addresses, file references, and other master data from BCIS to facilitate case creation in LSCP on a daily basis.
    2. Sending application data from LSCP to BCIS to create cases using stored procedures provided by BCIS in batch mode (To be confirmed).
    3. Updating application dates in BCIS using stored procedures provided by BCIS.
    4. Transferring data from SCS to BCIS for statistics reports.

*   **Authentication:**
    The authentication method for accessing the BCIS database needs to be determined. Options include database user credentials or API keys.

*   **Error Handling:**
    Stored procedures will include error handling mechanisms to manage potential issues during data transfer and logging of errors.

*   **Data Mapping:**
    The exact data fields to be imported and exported will be defined in the detailed design phase. Examples include:

    | **BCIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
    | :---------------- | :---------------- | :----------- | :-------------- |
    | Address List      | Address List      | List          | List of valid addresses |
    | File Reference    | File Reference    | Text          | BD File Reference Number |
    | User Master Data  | User Master Data  | Table         | User details and mappings |
    | ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative):**

    ```sql
    EXECUTE BCIS.Import_LSCP_MasterData;
    EXECUTE BCIS.Export_LSCP_ApplicationData;
    ```

### 3.2.2 INT-OSDP-01 - Single Sign-On through OSDP {#322-int-osdp-01---single-sign-on-through-osdp}

**Target System:**		OSDP (Open Source Departmental Portal)

**Requirement ID:** REQ-GR-07 Single Sign On

**Interface Type:**	URL redirection with departmental portal

**In / Out:**		In

**Frequency:**		Per user request

**Description:**
    Single Sign-On (SSO) will be implemented using the Open Source Departmental Portal (OSDP) to allow BD users, EDB users, and SWD users to access LSCP seamlessly. Users will log in to their respective departmental portals (BD OSDP, EDB OSDP, SWD OSDP) through the Government Backbone Network (GNET) and access LSCP without needing to re-enter credentials.

**Access from Buildings Departments (BD) Departmental Portal**

-   The link to access the LSCP will be provided within the BD Departmental Portal and will redirect to: `https://lscp.bd.gov.hk`

**Access from other B/Ds Departmental Portal (EDB/SWD OSDP)**

-   Users from EDB and SWD will access LSCP through their respective departmental portals.
-   Their departmental portals will redirect the request through the CCGO gateway to LSCP.
-   The connection between the other B/Ds departmental portal and the LSCP will be secured via HTTPS.

**Authentication and Authorization:**

-   Departmental portal users who require access to LSCP must apply for Intranet access through ITU.
-   The LSCP System Administrator will create user accounts in LSCP based on the submitted application details, including user roles and access rights.
-   LSCP authenticates users by verifying the login name and department code against the departmental portal account information forwarded in the HTTP header.
-   Only users with matching login names and department codes in LSCP will be granted access.
-   This authentication process applies to both BD users and users from other departments (EDB/SWD).

**Data Exchange:**

-   The departmental portal must forward the ?UID? (User ID) and ?Dpdeptid? (Department ID) to LSCP in the HTTP response header upon successful user login.
-   These parameters contain the departmental portal user ID and department code, which LSCP uses for authentication and authorization.

**In/Out data process flow diagram**
![OSDP SSO Data Flow](media/image4.png)


### 3.2.3 INT-MWMS2-01- Data Import from MWMS2 {#323-int-mwms2-01--data-import-from-mwms2}

**Target System:**		MWMS2 (Minor Works Management System 2.0)

**Requirement ID:** REQ-IR-03 Interface with Minor Works, REQ-WR-10 AP/RSE Verification

**Interface Type:**	SFTP and Excel

**In / Out:**		In

**Frequency:**		Daily

*   **Description:**
    LSCP will periodically import AP/RSE (Authorized Person/Registered Structural Engineer) data from MWMS 2.0. This data is crucial for verifying the identity and registration status of AP/RSEs who submit applications through LSCP. The data will be transferred securely using SFTP, and the data files will be in Excel format.

*   **Data Exchange:**
    1. **MWMS2 Data Export:** MWMS2 system will generate Excel files containing AP/RSE information and place them in a designated directory on an SFTP server.
    2. **LSCP Data Retrieval:** LSCP system will connect to the SFTP server using secure credentials, authenticate, and download the Excel files on a scheduled basis (e.g., daily).
    3. **Data Parsing and Import:** LSCP will parse the downloaded Excel files, extract the AP/RSE data, and import it into the LSCP database.

*   **Authentication:**
    Authentication for SFTP access will be based on secure SSH keys or username/password credentials to ensure secure data transfer.

*   **Error Handling:**
    LSCP system will implement robust error handling to manage potential issues during file transfer, Excel parsing, and database import. This includes logging errors, implementing retry mechanisms for failed transfers, and alerting system administrators to critical failures.

*   **Excel File Format:**
    The Excel file format for AP/RSE data will be structured as follows:

    | Field Name | Description                                                                   | Data Type | Format/Example |
    | :--------- | :---------------------------------------------------------------------------- | :-------- | :------------- |
    | AP_ID     | Unique identifier for the Authorized Person                                  | Number    | 12345          |
    | AP_NAME   | Name of the Authorized Person                                                | Text      | John Doe       |
    | AP_REG_NO | Registration number of the Authorized Person                               | Text      | AP-98765       |
    | RSE_ID    | Unique identifier for the Registered Structural Engineer                    | Number    | 67890          |
    | RSE_NAME  | Name of the Registered Structural Engineer                                   | Text      | Jane Smith     |
    | RSE_REG_NO| Registration number of the Registered Structural Engineer                   | Text      | RSE-54321      |
    | HKID      | Hong Kong Identity Card number (encrypted)                                    | Text      | ABC123456      |
    | EXPIRY_DATE | Registration Expiry Date                                                     | Date      | YYYY-MM-DD     |
    | ...        | ...                                                                           | ...       | ...            |

    (Note: The exact format and content of the Excel file will be finalized in consultation with the MWMS2 system owners.)

### 3.2.4 INT-ESH-01 - Data Import from ESH {#324-int-esh-01---data-import-from-esh}

**Target System:** ESH (E-Submission Hub)

**Requirement ID:** REQ-IR-04 Interface with ESH

**Interface Type:**	SFTP

**In / Out:**		In

**Frequency:**		Daily

*   **Description:**
    LSCP will interface with ESH to retrieve site project information. This interface is used to validate if a user is involved in a specific site project, enhancing security and access control within LSCP. Data will be transferred daily using SFTP.

*   **Data Exchange:**
    1. **ESH Data Export:** ESH system will generate data files containing site project information and place them in a designated directory on an SFTP server.
    2. **LSCP Data Retrieval:** LSCP system will connect to the SFTP server, authenticate, and download these files on a scheduled basis.
    3. **Data Parsing and Import:** LSCP will parse the files and import the relevant site project data into its database.

*   **Authentication:**
    SFTP access will be authenticated using SSH keys or username/password credentials for secure communication.

*   **Error Handling:**
    LSCP will implement error handling to manage issues during file transfer, parsing, and database import. This includes logging, retry mechanisms, and administrator alerts for failures.

*   **File Format:**
    The file format for data exchange needs to be confirmed with ESH system owners. It could be Excel, CSV, or JSON.

*   **Data Mapping:**

    | ESH Data Item | LSCP Data Item | Data Type | Description |
    | :---- | :---- | :---: | :---- |
    | File Reference | File Reference | string | BD Reference Number of the site project |
    | Site Address | Site Address | string | Address of the site project |
    | AP Registration Number | AP Registration Number | string | Registration number of the AP involved in the site project |
    | RSE Registration Number | RSE Registration Number | string | Registration number of the RSE involved in the site project |
    | RGE Registration Number | RGE Registration Number | string | Registration number of the RGE involved in the site project |
    | RC Registration Number | RC Registration Number | string | Registration number of the RC involved in the site project |
    | ... | ... | ... | ... |

### 3.2.5 INT-ERKS-01 - Data Import from ERKS {#325-int-erks-01---data-import-from-erks}

**Target System:**		ERKS (Electronic Records Keeping System)

**Requirement ID:** REQ-IR-05 Interface with ERKS

**Interface Type:**	*To be confirmed*

**In / Out:**		In

**Frequency:**		*To be confirmed*

*   **Description:**
    LSCP will interface with ERKS to import e-Certificates, e-notices, reply letters, and other generated documents for record-keeping purposes. The detailed data to be exchanged and the interface mechanism will be determined in consultation with ERKS system owners during the SM&S stage.

*   **Data Exchange:**
    The method of data exchange (e.g., API, file transfer, database link) is to be defined based on ERKS capabilities and requirements.

*   **Authentication:**
    Authentication and authorization mechanisms for accessing ERKS data will be established in coordination with ERKS administrators.

*   **Error Handling:**
    Robust error handling will be implemented to address potential issues during data exchange, ensuring data integrity and reliability.

*   **Data Mapping:**
    Data mapping details will be defined based on the chosen data exchange method and the specific data elements required by ERKS. This will include:

    | ERKS Data Item | LSCP Data Item | Data Type | Description |
    | :---- | :---- | :---: | :---- |
    | Document Type | Document Type | string | Type of document (e-Certificate, e-Notice, etc.) |
    | Document Content | Document Content | BLOB/Text | Actual document file or content |
    | Case Reference | Case Reference | string | LSCP Case Application Number |
    | Issue Date | Issue Date | Date | Date of document issuance |
    | ... | ... | ... | ... |

### 3.2.6 INT-BRAVO-01 - Data Import from BRAVO {#326-int-bravo-01---data-import-from-bravo}

**Target System:**		BRAVO (Buildings Records and Viewing Online)

**Requirement ID:** REQ-IR-06 Interface with BRAVO

**Interface Type:**	HTTP Request Redirection

**In / Out:**		In

**Frequency:**		Per User Request

*   **Description:**
    LSCP will integrate with BRAVO to allow users to access building records and related information directly from within LSCP. This integration will primarily use HTTP redirection, allowing LSCP to redirect users to specific BRAVO pages with relevant case or building information pre-filled.

*   **Data Exchange:**
    LSCP system will use HTTP requests (GET or POST) to redirect users to specific BRAVO URLs. Parameters such as Case Number, Year, Block ID, and File Reference No. will be passed in the URL query string to directly access relevant records in BRAVO.

*   **Authentication:**
    Authentication for accessing BRAVO will likely leverage existing BD intranet authentication mechanisms or may require API keys. The specific method needs to be determined in coordination with BRAVO system owners.

*   **Error Handling:**
    LSCP should handle potential errors during redirection or if BRAVO is unavailable, providing user-friendly error messages and fallback options.

*   **URL Syntax (Examples):**

    *   **with Case number and Year**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=<SUBJECT_CODE>&CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>&SPECIAL_CAT=<SPECIAL_CAT>`

    (Note: The exact URL syntax and parameter names need to be confirmed with the BRAVO system owners.)

*   **Data Mapping:**
    Data mapping primarily involves passing relevant LSCP case identifiers to BRAVO URLs. Specific data elements for mapping will be finalized during the detailed design phase.


*** End of document***
```