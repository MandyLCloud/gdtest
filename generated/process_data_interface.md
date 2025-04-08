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

## 1. Introduction

This Process Data Interface (PDI) document outlines the data processes and external system integrations for the Licensing Self-Certification Portal (LSCP) project for the Buildings Department (BD).

This document is divided into three main sections:

1.  **Introduction**: Provides an overview of the PDI document's purpose and scope.
2.  **System Data Process Interface**: Defines the internal data handling approach within the LSCP system.
3.  **External Interfaces**: Specifies the system's integration with external systems, including interface specifications.

This PDI is crucial for the physical design and implementation of the LSCP, ensuring seamless data flow and interoperability with other systems.

The following table lists the abbreviations used for external systems referenced in this document:

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | *Unknown*                               | *To be confirmed*                       |
| ERKS         | *Unknown*                               | *To be confirmed*                       |
| BRAVO        | *Unknown*                               | *To be confirmed*                       |

## 2. System Data Process Interface

The System Data Process Interface defines how the LSCP system's components interact with the physical data storage. It ensures that the database, implemented in the physical environment, effectively serves the processing components as defined in the system's logical data model. This approach simplifies system implementation and future maintenance.

For each incoming process request, the system is designed to:

1.  Accept and handle the input data.
2.  Update and query the database as required.

The diagram below illustrates the position of the Process Data Interface (PDI) within the universal function model, showing the in/out data process flow:

![In/Out data process flow diagram](media/image2.png)

## 3. External Interfaces

### 3.1 List of External Interface Specification

The following table summarizes the external interfaces of the LSCP system:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:** Some authentication and encryption methods are marked "To be determined" or left blank, pending clarification based on the specific requirements and capabilities of each external system.

### 3.2 Interface Specification

#### 3.2.1 INT-SMIS-01- Data Import from SMIS  {#3.2.1-int-smis-01--data-import-from-smis}

*   **Target System:** SMIS
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** The LSCP system will import data from the Statutory Management Information System (SMIS) by calling stored procedures in the SMIS database. This interface is crucial for retrieving necessary master data to facilitate case creation and other functionalities within LSCP. (Related User Requirement: REQ-IR-01 Interface with BCIS)

*   **Data Exchange:** Data transfer will occur directly between the LSCP and SMIS databases via stored procedures.

*   **Authentication:** The authentication method for accessing the SMIS database (e.g., database user credentials, API keys) is to be determined.

*   **Error Handling:** Stored procedures will incorporate error handling mechanisms to manage data transfer issues and logging.

*   **Data Mapping:** (Illustrative - To be defined in detail design phase)

    | **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
    | :---------------- | :---------------- | :----------- | :-------------- |
    | *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
    | ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative):**

    ```sql
    EXECUTE SMIS.Import_LSCP_Data;
    ```

#### 3.2.2 INT-OSDP-01 \-Single Sign-On through OSDP {#3.2.2-int-osdp-01--single-sign-on-through-osdp}

*   **Target System:** OSDP
*   **Interface Type:** URL redirection with departmental portal
*   **In / Out:** In
*   **Frequency:** Per user request

*   **Description:** This interface enables Single Sign-On (SSO) for BD users and users from other Bureaus/Departments (B/Ds) through their respective Open Source Departmental Portals (OSDP). Users access LSCP via a link in their departmental portal, ensuring seamless and secure access within the government network. (Related User Requirement: REQ-GR-07 Single Sign On)

*   **Access Points:**
    *   **Buildings Departments (BD) Departmental Portal:** Access link: `https://lscp.bd.gov.hk`
    *   **Other B/Ds Departmental Portal:** Users from other B/Ds will be redirected through the CCGO gateway. All connections are SSL secured.

*   **Authentication and Authorization:**
    *   Departmental portal users require Intranet access to LSCP, managed by ITU.
    *   LSCP System Administrator registers user accounts based on submitted information.
    *   LSCP authenticates users based on login name and department code from the departmental portal account.
    *   Only users with matching accounts in LSCP are granted access.

*   **Data Exchange:**
    *   The departmental portal forwards "UID" (User ID) and "Dpdeptid" (Department Code) to LSCP in the HTTP response header.

*   **In/Out data process flow diagram:**

    ![OSDP Interface Data Flow](media/image4.png)

#### 3.2.3 INT-MWMS2-01- Data Import from MWMS2 {#3.2.3-int-mwms2-01--data-import-from-mwms2}

*   **Target System:** MWMS2
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** LSCP imports Authorized Person (AP) and Registered Structural Engineer (RSE) data from Minor Works Management System 2.0 (MWMS2) daily. This data is crucial for verifying AP/RSE identities and qualifications during application submissions. (Related User Requirement: REQ-IR-03 Interface with Minor Works, REQ-WR-10 AP/RSE Verification)

*   **Data Exchange:**
    1.  MWMS2 generates Excel files containing AP/RSE information and places them in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the Excel files.
    3.  LSCP parses the Excel files and imports the data into its database.

*   **Authentication:** SFTP access authentication will likely use SSH keys or username/password credentials.

*   **Error Handling:** The system will handle errors during file transfer, parsing, and database import, with logging and retry mechanisms.

*   **Excel File Format:** (Illustrative - To be confirmed with MWMS2 system owners)

    | Field Name | Description                                                                   | Data Type | Format/Example |
    | :--------- | :---------------------------------------------------------------------------- | :-------- | :------------- |
    | AP\_ID     | Unique identifier for the Authorized Person                                  | Number    | 12345          |
    | AP\_NAME   | Name of the Authorized Person                                                | Text      | John Doe       |
    | AP\_REG\_NO | Registration number of the Authorized Person                               | Text      | AP-98765       |
    | RSE\_ID    | Unique identifier for the Registered Structural Engineer                    | Number    | 67890          |
    | RSE\_NAME  | Name of the Registered Structural Engineer                                   | Text      | Jane Smith     |
    | RSE\_REG\_NO| Registration number of the Registered Structural Engineer                   | Text      | RSE-54321      |
    | ...        | ...                                                                           | ...       | ...            |

#### 3.2.4 INT-ESH-01 -Data Import from ESH {#3.2.4-int-esh-01--data-import-from-esh}

*   **Target System:** ESH
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** LSCP retrieves site project information from the ESH system daily via SFTP. This interface is used to validate user involvement in site projects. (Related User Requirement: REQ-IR-04 Interface with ESH)

*   **Data Exchange:**
    1.  ESH generates files and places them in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the files.
    3.  LSCP parses the files and imports the data into its database.

*   **Authentication:** SFTP access authentication will likely use SSH keys or username/password credentials.

*   **Error Handling:** The system will handle errors during file transfer, parsing, and database import, with logging and retry mechanisms.

*   **File Format:** (To be confirmed - could be Excel, CSV, or JSON)

*   **Data Mapping:** (Illustrative - To be confirmed)

    | ESH Data Item | LSCP Data Item | Data Type | Description |
    | :---- | :---- | :---: | :---- |
    | File Reference | File Reference | string | BD Reference Number of the site project |
    | Site Address | Site Address | string | address of the site project |
    | AP Registration Number | AP Registration Number | string | Registration number of the AP that involve in the related site project |
    | RSE Registration Number | RSE Registration Number | string | Registration number of the RSE that involve in the related site project |
    | RGE Registration Number | RGE Registration Number | string | Registration number of the RGE that involve in the related site project |
    | RC Registration Number | RC Registration Number | string | Registration number of the RC that involve in the related site project |

#### 3.2.5 INT-ERKS-01 -Data Import from ERKS {#3.2.5-int-erks-01--data-import-from-erks}

*   **Target System:** ERKS
*   **Interface Type:** TBC (*To be confirmed*)
*   **In / Out:** In
*   **Frequency:** TBC (*To be confirmed*)

*   **Description:** This interface is designed to import data from the ERKS system into LSCP for record-keeping purposes. The specific data and interface mechanism are to be determined in consultation with ERKS system owners. (Related User Requirement: REQ-IR-05 Interface with ERKS)

*   **Data Exchange:** The method of data exchange (e.g., API, file transfer, database link) needs to be defined.

*   **Authentication:** Authentication and authorization mechanisms for accessing ERKS data are to be established.

*   **Error Handling:** Robust error handling will be implemented to manage data exchange issues.

*   **Data Mapping:** (To be defined based on specific data elements to be mapped between ERKS and LSCP)

#### 3.2.6 INT-BRAVO-01 -Data Import from BRAVO {#3.2.6-int-bravo-01--data-import-from-bravo}

*   **Target System:** BRAVO
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In
*   **Frequency:** Per User Request

*   **Description:** LSCP integrates with BRAVO through HTTP redirection, allowing users to access BRAVO functionalities directly from LSCP, particularly for retrieving building information and approved plans. (Related User Requirement: REQ-IR-06 Interface with BRAVO, REQ-WR-04 Perform Site Inspection)

*   **Data Exchange:** LSCP makes HTTP requests (GET or POST) to BRAVO URLs, passing parameters in the URL query string or request body. BRAVO responds with the requested data.

*   **Authentication:** The authentication method for accessing BRAVO (e.g., API keys, OAuth) is to be determined.

*   **Error Handling:** The system will handle errors returned by the BRAVO API and provide feedback to the user.

*   **URL Syntax (Examples):**
    *   **with Case number and Year:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No:**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

*   **Data Mapping:** (To be defined based on specific data elements to be mapped between LSCP and BRAVO)

## 4. Constraints

Based on the User Requirements Specification, there are no explicit constraints listed that directly impact the Process Data Interface. However, the document mentions "Complexity of Address Identification" which might indirectly influence data exchange with BCIS/SMIS if address data handling becomes a bottleneck.

## 5. Conclusion

The Process Data Interface is a critical component of the Licensing Self-Certification Portal, ensuring efficient data processing within the system and seamless integration with key external systems. These interfaces are essential for data exchange, user authentication, and accessing external functionalities, contributing to the overall effectiveness and efficiency of the LSCP system for the Buildings Department and its users.

*** End of document***
```