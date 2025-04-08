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

# **1. Introduction** {#1-introduction}

The Process Data Interface (PDI) document outlines the data processing approach within the Licensing Self-Certification Portal (LSCP) system and its integration with external systems. This document is structured into three main sections:

1.  **Introduction:** Provides an overview of the PDI's purpose and scope.
2.  **System Data Process Interface:** Defines the internal data handling mechanisms within the LSCP system.
3.  **External Interfaces:** Specifies the interfaces between the LSCP and external systems, including interface specifications and data exchange details.

This PDI serves as a guide for the physical design and implementation of the LSCP system, ensuring seamless data flow and interoperability with other systems within the Buildings Department (BD) and other government departments.

The following table lists the external systems that LSCP will interface with:

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | ESH (Environmental Safety and Health System)                              | *To be confirmed*                       |
| ERKS         | ERKS (Electronic Records Keeping System)                               | *To be confirmed*                       |
| BRAVO        | BRAVO (Building Records and Viewing Online)                               | *To be confirmed*                       |


# **2. System Data Process Interface** {#2-system-data-process-interface}

The System Data Process Interface (PDI) is designed to bridge the gap between the logical data model and the physical implementation of the LSCP database and processing components. This interface ensures that the physical database effectively supports the system's data processing needs and facilitates system implementation and maintenance.

The PDI follows a consistent pattern for handling incoming process requests. Each function within the system is designed to:

1.  **Accept and Handle Input:** Receive and process incoming data from various sources, including user inputs and external system interfaces.
2.  **Update and Enquire Database:** Interact with the LSCP database to store, retrieve, and update data as required by the process.

The diagram below illustrates the position of the Process Data Interface (PDI) within the universal function model, depicting the data flow direction:

![In/Out data process flow diagram](media/image2.png)


# **3. External Interfaces** {#3-external-interfaces}

## 3.1 List of External Interface Specification {#31-list-of-external-interface-specification}

The LSCP system is designed to interface with several external systems to ensure data consistency, streamline workflows, and enhance system functionality. The following table summarizes the external interfaces and their specifications:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:**
-  Some authentication and encryption methods are marked "To be determined" or left blank, pending further clarification and confirmation based on the specific requirements and capabilities of each external system.

## 3.2 Interface Specification {#32-interface-specification}

### 3.2.1 INT-SMIS-01- Data Import from SMIS  {#321-int-smis-01--data-import-from-smis}

*   **Target System:** SMIS (Statutory Management Information System)
*   **Interface Spec. ID:** INT-SMIS-01
*   **Name:** Data Import from SMIS
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily
*   **Authentication / Encryption:** *To be determined*

*   **Description:**
    The LSCP system will interface with SMIS to import essential data required for case creation and management. This interface will facilitate the retrieval of master data and reference information from BCIS to streamline the application process within LSCP. The specific data fields to be imported will be defined during the detailed design phase.

*   **Data Exchange:**
    Data exchange will be performed through stored procedures residing within the SMIS database. The LSCP system will invoke these stored procedures to retrieve the necessary data.

*   **Authentication:**
    The authentication mechanism for accessing the SMIS database will be determined in consultation with the relevant teams. Options may include database user credentials or API keys.

*   **Error Handling:**
    Robust error handling will be implemented within the stored procedures to manage potential issues during data transfer. Error events will be logged for monitoring and troubleshooting purposes.

*   **Data Mapping:**

    | **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
    | :---------------- | :---------------- | :----------- | :-------------- |
    | *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
    | ...             | ...             | ...          | ...             |
    *(Note: The detailed data mapping will be defined in the detailed design phase based on the specific data requirements.)*

*   **Example Stored Procedure Call (Illustrative):**

```sql
EXECUTE SMIS.Import_LSCP_Data;
```

### 3.2.2 INT-OSDP-01 -Single Sign-On through OSDP {#322-int-osdp-01--single-sign-on-through-osdp}

*   **Target System:** OSDP (Open Source Departmental Portal)
*   **Interface Spec. ID:** INT-OSDP-01
*   **Name:** Single Sign-On through OSDP
*   **Interface Type:** HTTP Request Redirection with departmental portal
*   **In / Out:** In
*   **Frequency:** Per user request
*   **Authentication / Encryption:** TLS 1.2 over HTTPS

*   **Description:**
    Single Sign-On (SSO) will be implemented using the Open Source Departmental Portal (OSDP) to allow seamless access for BD users, EDB users, and SWD users. Users logged into their respective departmental portals (BD OSDP, EDB OSDP, SWD OSDP) will be able to access the LSCP system without requiring separate login credentials.

*   **Access Points:**
    -   **Buildings Department (BD) Departmental Portal:** Access via a direct link: `https://lscp.bd.gov.hk`
    -   **Other B/Ds Departmental Portal:** Users from other Bureaus/Departments (B/Ds) will access LSCP through their departmental portals. The departmental portals will redirect requests through the CCGO gateway to LSCP.

*   **Authentication and Authorization:**
    -   Departmental portal users seeking access to LSCP must apply for Intranet access through ITU.
    -   The LSCP System Administrator will create user accounts in LSCP based on submitted information, linking them to departmental portal accounts.
    -   LSCP authenticates users by verifying the login name and department code against registered accounts.
    -   Only users with matching login names and department codes in LSCP will be granted access.

*   **Data Exchange:**
    -   The departmental portal must forward the "UID" (User ID) and "Dpdeptid" (Department ID) to LSCP within the HTTP response header.
    -   These parameters will contain the departmental portal user's ID and department code, enabling LSCP to identify and authenticate the user.

*   **In/Out data process flow diagram**
    ![In/Out data process flow diagram](media/image4.png)

### 3.2.3 INT-MWMS2-01- Data Import from MWMS2 {#323-int-mwms2-01--data-import-from-mwms2}

*   **Target System:** MWMS2 (Minor Works Management System 2.0)
*   **Interface Spec. ID:** INT-MWMS2-01
*   **Name:** Data Import from MWMS2
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily
*   **Authentication / Encryption:** SFTP

*   **Description:**
    The LSCP system will interface with MWMS 2.0 to retrieve Authorized Person (AP) and Registered Structural Engineer (RSE) data. This data will be used for AP/RSE verification and to ensure that only registered professionals are involved in self-certification submissions. Data will be transferred daily via SFTP in Excel file format.

*   **Data Exchange:**
    1.  MWMS2 system generates Excel files containing AP/RSE information and places them in a designated SFTP server directory.
    2.  LSCP system connects to the SFTP server, authenticates using SSH keys or username/password, and downloads the Excel files.
    3.  LSCP system parses the Excel files and imports the data into the LSCP database.

*   **Authentication:**
    SFTP access authentication will be secured using SSH keys or username/password credentials, as determined by security protocols.

*   **Error Handling:**
    The system will implement error handling mechanisms for file transfer, parsing, and database import failures. Error events will be logged, and retry mechanisms will be incorporated to ensure data integrity.

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
    *(Note: The exact format and content of the Excel file will be confirmed with the MWMS2 system owners.)*

### 3.2.4 INT-ESH-01 -Data Import from ESH {#324-int-esh-01--data-import-from-esh}

*   **Target System:** ESH (Environmental Safety and Health System)
*   **Interface Spec. ID:** INT-ESH-01
*   **Name:** Data Import from ESH
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily
*   **Authentication / Encryption:** SFTP

*   **Description:**
    The LSCP system will interface with the ESH system to retrieve site project information. This information will be used to validate user involvement in site projects, ensuring that users accessing project-related data are authorized personnel. Data will be transferred daily via SFTP.

*   **Data Exchange:**
    1.  ESH system generates files containing site project information and places them in a designated SFTP server directory.
    2.  LSCP system connects to the SFTP server, authenticates, and downloads the files.
    3.  LSCP system parses the files and imports the data into its database.

*   **Authentication:**
    SFTP access authentication will be secured using SSH keys or username/password credentials.

*   **Error Handling:**
    Error handling mechanisms will be implemented to manage file transfer, parsing, and database import errors. Logging and retry mechanisms will be included.

*   **File Format:**
    The file format for data exchange with ESH is to be confirmed. It may be Excel, CSV, or JSON format.

*   **Data Mapping:**

    | ESH Data Item | LSCP Data Item | Data Type | Description |
    | :---- | :---- | :---: | :---- |
    | File Reference | File Reference | string | BD Reference Number of the site project |
    | Site Address | Site Address | string | Address of the site project |
    | AP Registration Number | AP Registration Number | string | Registration number of the AP involved in the site project |
    | RSE Registration Number | RSE Registration Number | string | Registration number of the RSE involved in the site project |
    | RGE Registration Number | RGE Registration Number | string | Registration number of the RGE involved in the site project |
    | RC Registration Number | RC Registration Number | string | Registration number of the RC involved in the site project |

### 3.2.5 INT-ERKS-01 -Data Import from ERKS {#325-int-erks-01--data-import-from-erks}

*   **Target System:** ERKS (Electronic Records Keeping System)
*   **Interface Spec. ID:** INT-ERKS-01
*   **Name:** Data Import from ERKS
*   **Interface Type:** *To be confirmed*
*   **In / Out:** In
*   **Frequency:** *To be confirmed*
*   **Authentication / Encryption:** *To be confirmed*

*   **Description:**
    The LSCP system will interface with ERKS for record-keeping purposes. Certificates, notices, reply letters, and other generated documents from LSCP will be imported into ERKS for archival and compliance. The specific data and interface mechanism will be determined in consultation with ERKS system owners during the SM&S stage.

*   **Data Exchange:**
    The method of data exchange (API, file transfer, database link, etc.) will be defined based on ERKS capabilities and requirements.

*   **Authentication:**
    Authentication and authorization mechanisms for accessing ERKS data will be established in accordance with security protocols.

*   **Error Handling:**
    Robust error handling will be implemented to address any issues during data exchange, ensuring data integrity and completeness.

*   **Data Mapping:**
    *(This section will be filled in with specific data elements and mapping details between ERKS and LSCP once the interface type and data requirements are finalized.)*

### 3.2.6 INT-BRAVO-01 -Data Import from BRAVO {#326-int-bravo-01--data-import-from-bravo}

*   **Target System:** BRAVO (Building Records and Viewing Online)
*   **Interface Spec. ID:** INT-BRAVO-01
*   **Name:** Data Import from BRAVO
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In
*   **Frequency:** Per User Request
*   **Authentication / Encryption:** *To be confirmed*

*   **Description:**
    The LSCP system will provide users with seamless access to BRAVO for retrieving building records and related information. This interface will be implemented through HTTP request redirection, allowing users to navigate to BRAVO directly from within LSCP.

*   **Data Exchange:**
    LSCP will use HTTP requests (GET or POST) to redirect users to specific BRAVO URLs. Parameters, such as case numbers or block IDs, will be passed in the URL query string to directly access relevant building information in BRAVO.

*   **Authentication:**
    The authentication method for accessing BRAVO will be determined based on BRAVO's security requirements and capabilities.

*   **Error Handling:**
    The system will handle potential errors during redirection and provide appropriate feedback to the user if BRAVO access is unsuccessful.

*   **URL Syntax (Examples):**

    *   **with Case number and Year**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    *(Note: The exact URL syntax and parameter names will be confirmed with the BRAVO system owners.)*

*   **Data Mapping:**
    *(This section will be filled in with the specific data elements and mapping details between LSCP and BRAVO, if any, once the interface requirements are finalized.)*

*** End of document***
```