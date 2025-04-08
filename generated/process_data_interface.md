```markdown
# Process Data Interface for Licensing Self-Certification Portal

**Version: 0.1**
**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

## 1. Introduction

This Process Data Interface (PDI) document outlines the data process interfaces for the Licensing Self-Certification Portal (LSCP) for the Buildings Department (BD). It describes both the internal system data process interface and the external interfaces with other systems.

This document is structured as follows:

1.  **Introduction**: Provides an overview of the PDI document and its purpose.
2.  **System Data Process Interface**: Defines the approach for handling data processing within the LSCP system.
3.  **External Interfaces**: Details the system integration with external systems, including interface specifications.

This PDI serves as a guide for the physical design and integration of the LSCP with external systems, ensuring seamless data flow and system interoperability.

## 2. System Overview of Self-Certification System (SCS)

The proposed Self-Certification System (SCS), also referred to as Licensing Self-Certification Portal (LSCP), is designed to modernize and streamline the application, processing, and management of certificates and notices required by the Buildings Department (BD) for:

*   **Educational Premises (EP)** under the Education Ordinance (Cap. 279)
*   **Child Care Centre (CCC)** under the Child Care Services Ordinance (Cap. 243)
*   **Non-Local-Higher and Professional Education (Regulation) Ordinance [NLHP(R)O]** applications
*   **Temporary Places of Public Entertainment License (TPPEL)** - Application for inclusion of Temporary Structures in the Pre-accepted Temporary Structure (PTS) Register

The SCS aims to provide a single, centralized repository for all applications and supporting documents, facilitating efficient processing and easy retrieval of records for BD users, as well as providing online e-submission capabilities for applicants, Authorized Persons (AP), Registered Structure Engineers (RSE), and users from Education Bureau (EDB) and Social Welfare Department (SWD).

Currently, the Buildings Department relies on the Building Control Information System (BCIS) and primarily paper-based processes for managing these applications. The SCS is intended to address the limitations of the current system by introducing e-submission, e-processing, and e-tracking functionalities, along with interfaces to other relevant government systems.

## 3. System Data Process Interface

The System Data Process Interface defines how data is handled internally within the LSCP system. It focuses on the physical data design and the components of the physical process, ensuring that the database implementation aligns with the Required System Logical Data Model. This approach aims to simplify system implementation and future maintenance.

For each incoming process request, the system will:

1.  **Accept and Handle Input**: Receive and validate the input data.
2.  **Update and Enquire Database**: Process the data by updating or querying the database as required.

The following diagram illustrates the position of the Process Data Interface (PDI) within the universal function model:

![In/Out data process flow diagram](media/image2.png)
*In/Out data process flow diagram from pdi_t1.md*

## 4. External Interfaces

The LSCP system is designed to interface with several external systems to enhance its functionality and data integration. These interfaces are crucial for data exchange, user authentication, and system interoperability.

### 4.1 List of External Interface Specifications

The following table summarizes the external interfaces of the LSCP system:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name                               | Interface Type             | In / Out | Authentication / Encryption |
| :----------- | :------------------------ | :----------------- | :---------------------------------- | :------------------------- | :------- | :-------------------------- |
| External     | SMIS                      | INT-SMIS-01        | Data Import from SMIS               | Stored Procedure           | In       | *To be determined*          |
| External     | OSDP                      | INT-OSDP-01        | Single Sign-On through OSDP         | HTTP Request Redirection   | In       | TLS 1.2 over HTTPS          |
| External     | MWMS2                     | INT-MWMS2-01       | Data Import from MWMS2              | SFTP and Excel             | In       | SFTP                        |
| External     | ESH                       | INT-ESH-01         | Data Import from ESH                | SFTP                       | In       | SFTP                        |
| External     | ERKS                      | INT-ERKS-01        | Data Import from ERKS               | *To be confirmed*          | In       | *To be confirmed*          |
| External     | BRAVO                     | INT-BRAVO-01       | Data Import from BRAVO              | HTTP Request Redirection   | In       | *To be confirmed*          |

**Note:** Authentication and encryption methods marked "To be determined" will be clarified and confirmed during the detailed design phase based on the specific requirements and capabilities of each external system.

### 4.2 Interface Specifications

#### 4.2.1 INT-SMIS-01 - Data Import from SMIS

*   **Target System:** Statutory Management Information System (SMIS)
*   **Interface Type:** Stored Procedure
*   **In/Out:** In
*   **Frequency:** Daily

**Description:** The LSCP system will import necessary data from SMIS by calling stored procedures in the SMIS database. The specific data fields to be imported will be defined during the detailed design phase.

**Data Exchange:** Data will be transferred directly between databases via stored procedures.

**Authentication:** Authentication method for accessing the SMIS database will be determined (e.g., database user credentials, API keys).

**Error Handling:** Stored procedures will include error handling and logging mechanisms.

**Data Mapping:** Data mapping details will be defined in the detailed design phase.

**Example Stored Procedure Call (Illustrative):**
```sql
EXECUTE SMIS.Import_LSCP_Data;
```

#### 4.2.2 INT-OSDP-01 - Single Sign-On through OSDP

*   **Target System:** Open Source Departmental Portal (OSDP)
*   **Interface Type:** URL redirection with departmental portal
*   **In/Out:** In
*   **Frequency:** Per user request

**Description:** Single Sign-On (SSO) will be implemented through departmental portals (OSDP) for BD users, EDB users, and SWD users. Users will access LSCP via a link in their respective departmental portals.

**Access Points:**
*   **Buildings Department (BD) Departmental Portal:** `https://lscp.bd.gov.hk`
*   **Other B/Ds Departmental Portals:** Requests will be redirected through the CCGO gateway, with SSL secured connections.

**Authentication and Authorization:**
*   Departmental portal users require Intranet access to ITU.
*   LSCP System Administrator will create user accounts in LSCP based on submitted information.
*   LSCP authenticates users based on login name and department code from the departmental portal account.

**Data Exchange:**
*   Departmental portal forwards "UID" and "Dpdeptid" in the HTTP response header to LSCP.
*   "UID" and "Dpdeptid" contain departmental portal user ID and department code.

**In/Out Data Process Flow Diagram:**

![In/Out data process flow diagram for OSDP](media/image4.png)
*In/Out data process flow diagram from pdi_t1.md*


#### 4.2.3 INT-MWMS2-01 - Data Import from MWMS2

*   **Target System:** Minor Works Management System 2.0 (MWMS2)
*   **Interface Type:** SFTP and Excel
*   **In/Out:** In
*   **Frequency:** Daily

**Description:** LSCP will retrieve AP/RSE information from MWMS2 daily via SFTP in Excel files.

**Data Exchange:**
1.  MWMS2 generates and places Excel files in a designated SFTP server directory.
2.  LSCP connects to the SFTP server, authenticates, and downloads Excel files.
3.  LSCP parses Excel files and imports data into its database.

**Authentication:** SFTP access uses SSH keys or username/password.

**Error Handling:** System handles file transfer, parsing, and database import errors with logging and retry mechanisms.

**Excel File Format:** (Example - Actual format to be confirmed)

| Field Name     | Description                                 | Data Type | Format/Example |
| :------------- | :------------------------------------------ | :-------- | :------------- |
| AP\_ID         | Unique identifier for Authorized Person       | Number    | 12345          |
| AP\_NAME       | Name of Authorized Person                     | Text      | John Doe       |
| AP\_REG\_NO    | Registration number of Authorized Person      | Text      | AP-98765       |
| RSE\_ID        | Unique identifier for Registered Structure Engineer | Number    | 67890          |
| RSE\_NAME      | Name of Registered Structure Engineer         | Text      | Jane Smith     |
| RSE\_REG\_NO   | Registration number of Registered Structure Engineer | Text      | RSE-54321      |
| ...            | ...                                         | ...       | ...            |

#### 4.2.4 INT-ESH-01 - Data Import from ESH

*   **Target System:** ESH (System Name to be confirmed)
*   **Interface Type:** SFTP
*   **In/Out:** In
*   **Frequency:** Daily

**Description:** LSCP retrieves site project information from ESH daily via SFTP to validate user involvement in site projects.

**Data Exchange:**
1.  ESH generates and places files in a designated SFTP server directory.
2.  LSCP connects to the SFTP server, authenticates, and downloads files.
3.  LSCP parses files and imports data into its database.

**Authentication:** SFTP access uses SSH keys or username/password.

**Error Handling:** System handles file transfer, parsing, and database import errors with logging and retry mechanisms.

**File Format:** (To be confirmed - could be Excel, CSV, or JSON)

**Data Mapping:**

| ESH Data Item           | LSCP Data Item          | Data Type | Description                                                                  |
| :---------------------- | :---------------------- | :-------- | :--------------------------------------------------------------------------- |
| File Reference          | File Reference          | string    | BD Reference Number of the site project                                      |
| Site Address            | Site Address            | string    | Address of the site project                                                  |
| AP Registration Number  | AP Registration Number  | string    | Registration number of the AP involved in the related site project            |
| RSE Registration Number | RSE Registration Number | string    | Registration number of the RSE involved in the related site project           |
| RGE Registration Number | RGE Registration Number | string    | Registration number of the RGE involved in the related site project           |
| RC Registration Number  | RC Registration Number  | string    | Registration number of the RC involved in the related site project            |

#### 4.2.5 INT-ERKS-01 - Data Import from ERKS

*   **Target System:** ERKS (System Name to be confirmed)
*   **Interface Type:** To Be Confirmed (TBC)
*   **In/Out:** In
*   **Frequency:** TBC

**Description:** Interface for importing data from ERKS into LSCP. Specifics to be determined in consultation with ERKS system owners.

**Data Exchange:** Method of data exchange (API, file transfer, database link) to be defined.

**Authentication:** Authentication and authorization mechanism for accessing ERKS data to be established.

**Error Handling:** Robust error handling required for data exchange process.

**Data Mapping:** Data mapping details to be defined based on specific data elements to be exchanged.

#### 4.2.6 INT-BRAVO-01 - Data Import from BRAVO

*   **Target System:** BRAVO
*   **Interface Type:** HTTP Request Redirection
*   **In/Out:** In
*   **Frequency:** Per User Request

**Description:** LSCP redirects to BRAVO using URL calls with specified parameters for accessing building information.

**Data Exchange:** LSCP makes HTTP requests (GET or POST) to BRAVO URLs, passing parameters in the URL query string or request body. BRAVO responds with relevant data.

**Authentication:** Authentication method for accessing BRAVO (API keys, OAuth) to be determined.

**Error Handling:** System handles errors returned by BRAVO API and provides feedback to the user.

**URL Syntax (Examples):**
*   **with Case number and Year:** `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`
*   **with Block ID:** `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`
*   **with full File Reference No:** `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

**Data Mapping:** Data mapping details to be defined based on specific data elements to be exchanged.

## 5. Conclusion

The Process Data Interface is a critical component of the Licensing Self-Certification Portal, enabling seamless integration with external systems and efficient internal data processing. These interfaces are essential for achieving the goals of the SCS, including streamlined application processing, improved data management, and enhanced user experience for both BD staff and external users. Further refinement and detailing of these interfaces will be carried out in subsequent phases of system development.

*** End of document***
```