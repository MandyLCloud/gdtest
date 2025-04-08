```markdown
# Process Data Interface for Licensing Self-Certification Portal

![BDlogo](media/image1.jpg)

**Version: 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

## Table of Contents

[1. Introduction](#1-introduction)
[2. Background](#2-background)
[3. System Data Process Interface](#3-system-data-process-interface)
[4. External Interfaces](#4-external-interfaces)
    * [4.1 List of External Interface Specification](#41-list-of-external-interface-specification)
    * [4.2 Interface Specification](#42-interface-specification)
        * [4.2.1 INT-SMIS-01- Data Import from SMIS](#421-int-smis-01--data-import-from-smis)
        * [4.2.2 INT-OSDP-01 -Single Sign-On through OSDP](#422-int-osdp-01--single-sign-on-through-osdp)
        * [4.2.3 INT-MWMS2-01- Data Import from MWMS2](#423-int-mwms2-01--data-import-from-mwms2)
        * [4.2.4 INT-ESH-01 -Data Import from ESH](#424-int-esh-01--data-import-from-esh)
        * [4.2.5 INT-ERKS-01 -Data Import from ERKS](#425-int-erks-01--data-import-from-erks)
        * [4.2.6 INT-BRAVO-01 -Data Import from BRAVO](#426-int-bravo-01--data-import-from-bravo)
[5. Interface Requirements](#5-interface-requirements)
[6. Interface Constraints](#6-interface-constraints)

## 1. Introduction

This Process Data Interface (PDI) document outlines the data process and system integrations for the Licensing Self-Certification Portal (LSCP) being developed for the Buildings Department (BD). This document is structured into three main sections:

1.  **Introduction:** Explains the purpose and scope of this PDI document.
2.  **System Data Process Interface:** Defines the internal data handling and processing within the LSCP system.
3.  **External Interfaces:** Specifies the interfaces for integrating LSCP with external systems, including detailed interface specifications.

This PDI serves as a guide for the physical design and implementation of the LSCP, ensuring seamless data flow and integration with other relevant systems within and outside the Buildings Department.

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | *Unknown*                               | *To be confirmed*                       |
| ERKS         | *Unknown*                               | *To be confirmed*                       |
| BRAVO        | *Unknown*                               | *To be confirmed*                       |

## 2. Background

The Buildings Department (BD) plays a crucial role in various licensing regimes in Hong Kong, providing expert advice on building and structural safety.  Currently, the licensing processes for Educational Premises (EP), Child Care Centres (CCC), and Temporary Places of Public Entertainment License (TPPEL) rely heavily on paper-based submissions and manual processing. Data related to these licenses is primarily stored in the Building Control Information System (BCIS).

The existing system faces several challenges:

*   **Long processing times:** Paper-based processes contribute to delays in license approvals.
*   **Lack of management reports:** Generating comprehensive statistics and reports is difficult.
*   **Disorganized data repository:** Application records and supporting documents are not systematically stored, hindering efficient retrieval.
*   **No system integration:**  The current system operates in isolation, lacking integration with other relevant systems.

To address these issues, the Buildings Department is developing the Licensing Self-Certification Portal (LSCP). This system aims to:

*   **Streamline the application process:** Enable online submission and processing of applications for certificates and notices required under the Education Ordinance and Child Care Services Ordinance.
*   **Enhance efficiency:** Expedite the registration process for non-purpose built Educational Premises (EP) and Child Care Centre (CCC).
*   **Improve collaboration:** Facilitate communication and data exchange between BD users, applicants, and other government departments like the Education Bureau (EDB) and Social Welfare Department (SWD).
*   **Centralize data management:** Create a single repository for all applications and supporting documents, making information easily accessible and searchable.

The Process Data Interface (PDI) is a critical component of the LSCP, designed to ensure seamless data exchange and integration with other essential systems, thereby achieving the objectives of efficiency, data centralization, and improved workflow.

## 3. System Data Process Interface

The LSCP's Process Data Interface (PDI) is designed to facilitate efficient data handling within the system. The physical data design focuses on making the database, implemented in the physical environment, appear as the Required System Logical Data Model to the processing components. This approach simplifies system implementation and future maintenance.

For each incoming process request, the system is designed to:

1.  **Accept and Handle Input:**  Receive and process the incoming data.
2.  **Update and Enquire Database:** Interact with the database to update information or retrieve data as needed.

The following diagram illustrates the position of the Process Data Interface (PDI) within the universal function model, showing the In/Out data process flow:

![In/Out data process flow diagram](media/image2.png)

## 4. External Interfaces

The LSCP is designed to interface with several external systems to enhance its functionality and data integration. These interfaces are crucial for data synchronization, single sign-on capabilities, and accessing relevant information from other government systems.

### 4.1 List of External Interface Specification

The following table summarizes the external interfaces for the LSCP:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:** Some authentication and encryption methods are marked "To be determined" or left blank and will be clarified and confirmed based on the specific requirements and capabilities of each external system.

### 4.2 Interface Specification

#### 4.2.1 INT-SMIS-01- Data Import from SMIS

*   **Target System:** Statutory Management Information System (SMIS)
*   **Interface Type:** Stored Procedure
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** The LSCP system will use stored procedures in the SMIS database to import necessary data. The specific data fields will be defined during the detailed design phase.
*   **Data Exchange:** Data transfer will occur directly between databases via stored procedures.
*   **Authentication:** Authentication method for accessing SMIS database needs to be determined (e.g., database user credentials, API keys).
*   **Error Handling:** Stored procedures will include error handling for data transfer issues and logging.
*   **Data Mapping:**

    | **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
    | :---------------- | :---------------- | :----------- | :-------------- |
    | *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
    | ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative):**
    ```sql
    EXECUTE SMIS.Import_LSCP_Data;
    ```

#### 4.2.2 INT-OSDP-01 -Single Sign-On through OSDP

*   **Target System:** Open Source Departmental Portal (OSDP)
*   **Interface Type:** URL redirection with departmental portal
*   **In / Out:** In
*   **Frequency:** Per user request

*   **Description:** Users from BD and other B/Ds will access LSCP by logging into their OSDP. A redirection link to LSCP will be provided in the BD Departmental Portal and other B/Ds Departmental Portals. Connection is SSL secured.
*   **Access from Buildings Departments (BD) Departmental Portal:**
    *   Link: `https://lscp.bd.gov.hk`
*   **Access from other B/Ds Departmental Portal:**
    *   Users from other B/Ds will access LSCP through their own departmental portals, which will redirect requests through the CCGO gateway. Connection is SSL secured.
*   **Authentication and Authorization:**
    *   Departmental portal users need to apply for Intranet access to ITU.
    *   LSCP System administrator will create accounts in LSCP based on submitted information.
    *   LSCP authenticates users by login name and department code from the departmental portal account.
    *   Login is granted only if an account with matching login name and department code exists.
*   **Data Exchange:**
    *   Departmental portal forwards "UID" and "Dpdeptid" to LSCP in the HTTP response header, containing departmental portal user ID and department code.

*   **In/Out data process flow diagram**
    ![In/Out data process flow diagram for OSDP](media/image4.png)

#### 4.2.3 INT-MWMS2-01- Data Import from MWMS2

*   **Target System:** Minor Works Management System 2.0 (MWMS2)
*   **Interface Type:** SFTP and Excel
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** LSCP retrieves Excel files containing AP/RSE information from MWMS2 via a scheduled daily task using SFTP.
*   **Data Exchange:**
    1.  MWMS2 generates and places Excel files in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads Excel files.
    3.  LSCP parses Excel files and imports data into its database.
*   **Authentication:** SFTP access uses SSH keys or username/password credentials.
*   **Error Handling:** System handles errors during file transfer, parsing, and database import with logging and retry mechanisms.
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

    (Note: Exact format and content of the Excel file will be confirmed with MWMS2 system owners.)

#### 4.2.4 INT-ESH-01 -Data Import from ESH

*   **Target System:** ESH
*   **Interface Type:** SFTP
*   **In / Out:** In
*   **Frequency:** Daily

*   **Description:** LSCP retrieves site project information from ESH via a scheduled daily task using SFTP to validate user involvement in site projects.
*   **Data Exchange:**
    1.  ESH generates and places files in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads files.
    3.  LSCP parses files and imports data into its database.
*   **Authentication:** SFTP access uses SSH keys or username/password credentials.
*   **Error Handling:** System handles errors during file transfer, parsing, and database import with logging and retry mechanisms.
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

#### 4.2.5 INT-ERKS-01 -Data Import from ERKS

*   **Target System:** ERKS
*   **Interface Type:** TBC (*To be confirmed*)
*   **In / Out:** In
*   **Frequency:** TBC (*To be confirmed*)

*   **Description:** Interface involves importing data from ERKS into LSCP. Specifics of data and mechanism to be determined with ERKS system owners.
*   **Data Exchange:** Method (API, file transfer, database link) needs definition.
*   **Authentication:** Authentication and authorization mechanism for accessing ERKS data needs to be established.
*   **Error Handling:** Robust error handling required for data exchange issues.
*   **Data Mapping:** (Specific data elements mapping between ERKS and LSCP to be defined).

#### 4.2.6 INT-BRAVO-01 -Data Import from BRAVO

*   **Target System:** BRAVO
*   **Interface Type:** HTTP Request Redirection
*   **In / Out:** In
*   **Frequency:** Per User Request

*   **Description:** System uses `https://dp2.bd.hksarg/bravo/intranetSignOn` to redirect to BRAVO. LSCP can also be redirected to BRAVO via URL calls with parameters.
*   **Data Exchange:** LSCP makes HTTP requests (GET or POST) to BRAVO URLs, passing parameters in URL query string or request body. BRAVO responds with data.
*   **Authentication:** Authentication method for accessing BRAVO (e.g., API keys, OAuth) needs to be determined.
*   **Error Handling:** System handles errors from BRAVO API and provides user feedback.
*   **URL Syntax (Examples):**
    *   **with Case number and Year:** `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`
    *   **with Block ID:** `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`
    *   **with full File Reference No:** `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    (Note: Exact URL syntax and parameter names need confirmation with BRAVO system owners.)

*   **Data Mapping:** (Specific data elements mapping between LSCP and BRAVO to be defined.)

## 5. Interface Requirements

The User Requirements Specifications document outlines several interface requirements for the LSCP, categorized as Interface Requirements (REQ-IR). These requirements are crucial for the LSCP to interact effectively with other systems.

*   **REQ-IR-01 Interface with BCIS:**
    *   Receive address lists and master data from BCIS daily.
    *   Send application data to BCIS for case creation using stored procedures in batch.
    *   Update application dates in BCIS using stored procedures.
    *   Establish reference links between SCS and BCIS.
    *   Transfer data from SCS to BCIS for statistical reporting.
    *   Enable block selection for new addresses in BCIS via to-do lists and email.
    *   Handle input and editing of 12 & 13 file Licensing cases in SCS instead of BCIS.
    *   Map BCIS users (User name, Post, File reference, DP login id, case officer).
    *   Include Licensing nature enquiry.
    *   Link to DV tables of BCIS.
    *   Conduct a detailed study for easy record retrieval from SCS by comparing data storage against a reference link from SCS and BCIS.

*   **REQ-IR-02 Interface with BD Website:**
    *   Display Pre-accepted Proprietary Temporary structure data on the BD website.

*   **REQ-IR-03 Interface with Minor Works:**
    *   Collect AP/RSE data (User Name, Registration Number, HKID, Expiry Date, etc.) daily from MWMS 2.0 via sFTP.
    *   Redirect to CRM of MWMS via Departmental Portal link to view detailed AP/RSE information.

*   **REQ-IR-04 Interface with ESH:**
    *   Provide case information and hyperlinks of SCS to ESH for viewing related case information and redirection to SCS.

*   **REQ-IR-05 Interface with ERKS:**
    *   Import e-Certificates, e-notices, reply letters, and other documents into ERKS for record keeping. Detailed interface specifications will be developed in the SM&S stage.

*   **REQ-IR-06 Interface with BRAVO:**
    *   Enable redirection to BRAVO using `https://dp2.bd.hksarg/bravo/intranetSignOn`.
    *   Allow redirection to BRAVO via URL calls with parameters (Case number, Year, Block ID, File Reference No).

## 6. Interface Constraints

The Constraints List in the User Requirements Specifications document identifies potential constraints that may impact the system design and implementation of the PDI.

*   **Complexity of Address Identification:** Due to the complexity of address identification, case creation might be delegated to BCIS. Once created in BCIS, data will be sent back to SCS for workflow processing. This constraint highlights the dependency on the BCIS interface for address-related functionalities.

*** End of document***
```