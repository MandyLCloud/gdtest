```markdown
![BDlogo][image1]

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

[1\. Introduction	](#1.-introduction)

[2\. System Data Process Interface	](#2.-system-data-process-interface)

[3\. External Interfaces](#3.-external-interfaces)

[3.1 List of External Interface Specification](#3.1-list-of-external-interface-specification)

[3.2 Interface Specification](#3.2-interface-specification)

[3.2.1 INT-SMIS-01- Data Import from SMIS](#3.2.1-int-smis-01--data-import-from-smis)

[3.2.2 INT-OSDP-01 \-Single Sign-On through OSDP](#3.2.2-int-osdp-01--single-sign-on-through-osdp)

[3.2.3 INT-MWMS2-01- Data Import from MWMS2](#3.2.3-int-mwms2-01--data-import-from-mwms2)

[3.2.4 INT-ESH-01 -Data Import from ESH](#3.2.4-int-esh-01--data-import-from-esh)

[3.2.5 INT-ERKS-01 -Data Import from ERKS](#3.2.5-int-erks-01--data-import-from-erks)

[3.2.6 INT-BRAVO-01 -Data Import from BRAVO](#3.2.6-int-bravo-01--data-import-from-bravo)

# **1\. Introduction** {#1.-introduction}

The Process Data Interface (PDI) consists of three sections, namely:

1. Introduction

- helps to explain the contents and purposes of the PDI.

2. System Data Process Interface

- defines the approach for handling the data process within the system     .

3. External Interfaces

- defines the handling approach for the system integration with external systems with interface specifications.

This PDI describes the approach for performing physical design and integration of LSCP for the Buildings Department (BD) with other external systems.

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | *Unknown*                               | *To be confirmed*                       |
| ERKS         | *Unknown*                               | *To be confirmed*                       |
| BRAVO        | *Unknown*                               | *To be confirmed*                       |


# **2\. System Data Process Interface** {#2.-system-data-process-interface}

The implemented physical data design the components of the physical process. The interface makes the database implemented using the physical environment appear as the Required System Logical Data Model to the processing components. It aims to ease the system implementation and future maintenance.

For every incoming process request, the function accepts and handles the input first. Then the function updates and enquires the database.

The following is the position of Process Data Interface (PDI) relative to the universal function model:

In/Out data process flow diagram

![][image2]

# 

# **3\. External Interfaces** {#3.-external-interfaces}

## 3.1 List of External Interface Specification {#3.1-list-of-external-interface-specification}

Here below shows the summary of the interface:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:**
-  Some of the authentication and encryption methods are marked "To be determined" or left blank. These will need to be clarified and confirmed based on the specific requirements and capabilities of each external system.

## 

## 3.2 Interface Specification {#3.2-interface-specification}

**(RY Note: the following sections are for reference only. Content is incorrect)**

### 3.2.1 INT-SMIS-01- Data Import from SMIS  {#3.2.1-int-smis-01--data-import-from-smis}

Target System:		SMIS

Interface Type:	Stored Procedure

In / Out:		In

Frequency:		Daily

*   **Description:** The LSCP system will call stored procedures in the SMIS database to import the necessary data. The exact data fields to be imported will need to be defined in the detailed design phase.

*   **Data Exchange:** The data will be transferred directly between the databases via the stored procedures.

*   **Authentication:** The authentication method for accessing the SMIS database will need to be determined (e.g., database user credentials, API keys).

*   **Error Handling:** The stored procedures should include error handling to manage potential issues during data transfer and logging.

*   **Data Mapping:**

| **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
| :---------------- | :---------------- | :----------- | :-------------- |
| *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
| ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative):**

```sql
EXECUTE SMIS.Import_LSCP_Data;
```

### 3.2.2 INT-OSDP-01 \-Single Sign-On through OSDP {#3.2.2-int-osdp-01--single-sign-on-through-osdp}

Target System:		OSDP

Interface Type:	URL redirection with departmental portal

In / Out:		In

Frequency:		Per user request

**Description:** Users from BD and other B/Ds will access the LSCP by logging into their respective departmental portals (OSDP). A link to redirect to the LSCP will be provided in the BD Departmental Portal and other B/Ds Departmental Portal. The connection between the other B/Ds departmental portal and the LSCP is SSL secured.

**Access from Buildings Departments (BD) Departmental Portal**

-   The link to access the LSCP will be: [https://lscp.bd.gov.hk](https://lscp.bd.gov.hk)

**Access from other B/Ds Departmental Portal**

-   Users from other B/Ds will access the LSCP through their own departmental portals.
-   Their departmental portals will redirect the request through the CCGO gateway.
-   The connection between the other B/Ds departmental portal and the LSCP will be SSL secured.

**Authentication and Authorization:**

-   For the departmental portal users who would like to access the LSCP, they have to apply for Intranet access to ITU.
-   The LSCP System administrator will register an account in the LSCP with regard to the submitted information.
-   LSCP authenticates the incoming user by the login name and the department code of the departmental portal account.
-   If and only if the account with the same login name and department code exists, the departmental portal user could login to the LSCP.
-   Both BD users and other B/Ds users will be authenticated in this way.

**Data Exchange:**

-   The departmental portal has to forward the ?UID? and ?Dpdeptid? to LSCP in the HTTP response header.
-   The UID and Dpdeptid should contain information of departmental portal user ID and department code.

**In/Out data process flow diagram**  
![][image4]

### 3.2.3 INT-MWMS2-01- Data Import from MWMS2 {#3.2.3-int-mwms2-01--data-import-from-mwms2}

Target System:		MWMS2

Interface Type:	SFTP and Excel

In / Out:		In

Frequency:		Daily

*   **Description:** The LSCP system will retrieve Excel files containing AP/RSE information from the MWMS2 system via a scheduled task (e.g., daily). The files will be transferred using SFTP.

*   **Data Exchange:**
    1. The MWMS2 system will generate and place Excel files in a designated SFTP server directory.
    2. The LSCP system will connect to the SFTP server, authenticate, and download the Excel files.
    3. The LSCP system will then parse the Excel files and import the data into its database.

*   **Authentication:** Authentication for SFTP access will likely use SSH keys or username/password credentials.

*   **Error Handling:** The system should handle potential errors during file transfer, parsing, and database import, with appropriate logging and retry mechanisms.

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

    (Note: The exact format and content of the Excel file will need to be confirmed with the MWMS2 system owners.)

### 3.2.4 INT-ESH-01 -Data Import from ESH {#3.2.4-int-esh-01--data-import-from-esh}

Target System: ESH

Interface Type:	SFTP

In / Out:		In

Frequency:		Daily

*   **Description:** The LSCP system will retrieve site project information from the ESH system via a scheduled task (e.g., daily). The files will be transferred using SFTP. The imported information is used for validating if a user is involved in the site project.
*   **Data Exchange:**
    1. The ESH system will generate and place files in a designated SFTP server directory.
    2. The LSCP system will connect to the SFTP server, authenticate, and download the files.
    3. The LSCP system will then parse the files and import the data into its database.
*   **Authentication:** Authentication for SFTP access will likely use SSH keys or username/password credentials.
*   **Error Handling:** The system should handle potential errors during file transfer, parsing, and database import, with appropriate logging and retry mechanisms.
*   **File Format:**  The format needs to be confirmed. The file could be excel, csv or json.
*   **Data Mapping:**

| ESH Data Item | LSCP Data Item | Data Type | Description |
| :---- | :---- | :---: | :---- |
| File Reference | File Reference | string | BD Reference Number of the site project |
| Site Address | Site Address | string | address of the site project |
| AP Registration Number | AP Registration Number | string | Registration number of the AP that involve in the related site project |
| RSE Registration Number | RSE Registration Number | string | Registration number of the RSE that involve in the related site project |
| RGE Registration Number | RGE Registration Number | string | Registration number of the RGE that involve in the related site project |
| RC Registration Number | RC Registration Number | string | Registration number of the RC that involve in the related site project |

### 3.2.5 INT-ERKS-01 -Data Import from ERKS {#3.2.5-int-erks-01--data-import-from-erks}

Target System:		ERKS

Interface Type:	TBC

In / Out:		In

Frequency:		TBC

*   **Description:** This interface will likely involve importing data from the ERKS system into LSCP. The specifics of the data and the mechanism will need to be determined in consultation with the ERKS system owners.

*   **Data Exchange:** The method of data exchange (e.g., API, file transfer, database link) needs to be defined.

*   **Authentication:** The authentication and authorization mechanism for accessing ERKS data will need to be established.

*   **Error Handling:** Robust error handling will be required to address any issues during the data exchange process.

*   **Data Mapping:**  
    (This section will need to be filled in with the specific data elements that need to be mapped between ERKS and LSCP)

### 3.2.6 INT-BRAVO-01 -Data Import from BRAVO {#3.2.6-int-bravo-01--data-import-from-bravo}

Target System:		BRAVO

Interface Type:	HTTP Request Redirection

In / Out:		In

Frequency:		Per User Request

*   **Description:** The system can use [https://dp2.bd.hksarg/bravo/intranetSignOn](https://dp2.bd.hksarg/bravo/intranetSignOn) to redirect to BRAVO. Also, the SCS system could be redirected to BRAVO through a URL call with specified parameters.

*   **Data Exchange:** The LSCP system will make HTTP requests (GET or POST) to specific BRAVO URLs, passing any required parameters in the URL query string or request body. The BRAVO system will respond with the relevant data.

*   **Authentication:** The authentication method for accessing BRAVO (e.g., API keys, OAuth) will need to be determined.

*   **Error Handling:** The system should handle any errors returned by the BRAVO API and provide appropriate feedback to the user.

*   **URL Syntax (Examples):**

    *   **with Case number and Year**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    (Note: The exact URL syntax and parameter names need to be confirmed with the BRAVO system owners.)

*   **Data Mapping:**  
    (This section will need to be filled in with the specific data elements that need to be mapped between LSCP and BRAVO.)

### 

\*\*\* End of document\*\*\*

[image1]: <data:image/png;base64,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