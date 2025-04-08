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
    [3.1 List of External Interface Specification](#31-list-of-external-interface-specification)
    [3.2 Interface Specification](#32-interface-specification)
        [3.2.1 INT-SMIS-01- Data Import from SMIS](#321-int-smis-01--data-import-from-smis)
        [3.2.2 INT-OSDP-01 -Single Sign-On through OSDP](#322-int-osdp-01--single-sign-on-through-osdp)
        [3.2.3 INT-MWMS2-01- Data Import from MWMS2](#323-int-mwms2-01--data-import-from-mwms2)
        [3.2.4 INT-ESH-01 -Data Import from ESH](#324-int-esh-01--data-import-from-esh)
        [3.2.5 INT-ERKS-01 -Data Import from ERKS](#325-int-erks-01--data-import-from-erks)
        [3.2.6 INT-BRAVO-01 -Data Import from BRAVO](#326-int-bravo-01--data-import-from-bravo)

## 1. Introduction

This Process Data Interface (PDI) document outlines the data processing and system integration aspects for the Licensing Self-Certification Portal (LSCP) project for the Buildings Department (BD).

The PDI document is divided into three main sections:

1.  **Introduction**: Provides an overview of the PDI's purpose and scope.
2.  **System Data Process Interface**: Defines the internal data handling mechanisms within the LSCP system.
3.  **External Interfaces**: Specifies how the LSCP system interacts and exchanges data with external systems.

This document serves as a guide for the physical design and implementation of the LSCP system, ensuring seamless integration with existing and necessary external systems.

The following table lists the external systems that LSCP will interface with:

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | *Unknown*                               | *To be confirmed*                       |
| ERKS         | *Unknown*                               | *To be confirmed*                       |
| BRAVO        | *Unknown*                               | *To be confirmed*                       |

## 2. System Data Process Interface

The Process Data Interface (PDI) is designed to bridge the gap between the logical data model and the physical database implementation. It ensures that the database, in its physical environment, effectively serves the processing components as defined in the system's logical data model. This approach simplifies system implementation and facilitates future maintenance.

The PDI operates on a principle of request-response. For each incoming process request, the system function will:

1.  **Accept and Handle Input**: Receive and validate the incoming data.
2.  **Database Interaction**: Update and query the database based on the request.

The diagram below illustrates the position of the Process Data Interface (PDI) within the universal function model, showing the data flow:

![In/Out data process flow diagram](media/image2.png)

## 3. External Interfaces

### 3.1 List of External Interface Specification

The LSCP system is designed to interface with several external systems to ensure data consistency, streamline workflows, and enhance functionality. The following table summarizes the external interfaces:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:** Authentication and encryption methods marked "To be determined" or blank will be clarified and confirmed based on the specific requirements and capabilities of each external system during the detailed design phase.

### 3.2 Interface Specification

#### 3.2.1 INT-SMIS-01- Data Import from SMIS

*   **Target System**: SMIS
*   **Interface Type**: Stored Procedure
*   **In / Out**: In
*   **Frequency**: Daily

*   **Description**: The LSCP system will import data from the Statutory Management Information System (SMIS) by calling stored procedures within the SMIS database. The specific data fields for import will be defined during the detailed design phase.
*   **Data Exchange**: Data will be directly transferred between databases using stored procedures.
*   **Authentication**: The authentication method for accessing the SMIS database is to be determined (e.g., database user credentials, API keys).
*   **Error Handling**: Stored procedures will include error handling mechanisms for data transfer issues and logging.
*   **Data Mapping**:

    | **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
    | :---------------- | :---------------- | :----------- | :-------------- |
    | *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
    | ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative)**:
    ```sql
    EXECUTE SMIS.Import_LSCP_Data;
    ```

#### 3.2.2 INT-OSDP-01 -Single Sign-On through OSDP

*   **Target System**: OSDP
*   **Interface Type**: URL redirection with departmental portal
*   **In / Out**: In
*   **Frequency**: Per user request

*   **Description**: Single Sign-On (SSO) will be implemented through the Open Source Departmental Portal (OSDP). Users from BD and other Bureaus/Departments (B/Ds) will access LSCP via their respective departmental portals. A redirection link to LSCP will be available in the BD Departmental Portal and other B/Ds Departmental Portals. Connections are SSL secured.

    *   **Access from Buildings Departments (BD) Departmental Portal**:
        -   Link: `https://lscp.bd.gov.hk`
    *   **Access from other B/Ds Departmental Portal**:
        -   Users will access LSCP through their own departmental portals, which redirect requests via the CCGO gateway. Connections are SSL secured.

*   **Authentication and Authorization**:
    -   Departmental portal users require Intranet access to ITU to access LSCP.
    -   LSCP System Administrator will create user accounts in LSCP based on submitted information.
    -   LSCP authenticates users based on login name and department code from the departmental portal account.
    -   Login is granted only if a matching account exists in LSCP. This authentication applies to both BD and other B/Ds users.

*   **Data Exchange**:
    -   The departmental portal must forward "UID" and "Dpdeptid" in the HTTP response header, containing departmental portal user ID and department code.

*   **In/Out data process flow diagram**:
    ![In/Out data process flow diagram for OSDP](media/image4.png)

#### 3.2.3 INT-MWMS2-01- Data Import from MWMS2

*   **Target System**: MWMS2
*   **Interface Type**: SFTP and Excel
*   **In / Out**: In
*   **Frequency**: Daily

*   **Description**: The LSCP system will retrieve AP/RSE (Authorized Person/Registered Structural Engineer) information from Minor Works Management System 2.0 (MWMS2) daily via scheduled SFTP transfer of Excel files.
*   **Data Exchange**:
    1.  MWMS2 generates Excel files and places them in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the Excel files.
    3.  LSCP parses the Excel files and imports the data into its database.
*   **Authentication**: SFTP access will use SSH keys or username/password credentials.
*   **Error Handling**: The system will handle file transfer, parsing, and database import errors with logging and retry mechanisms.
*   **Excel File Format**:

    | Field Name | Description                                                                   | Data Type | Format/Example |
    | :--------- | :---------------------------------------------------------------------------- | :-------- | :------------- |
    | AP\_ID     | Unique identifier for the Authorized Person                                  | Number    | 12345          |
    | AP\_NAME   | Name of the Authorized Person                                                | Text      | John Doe       |
    | AP\_REG\_NO | Registration number of the Authorized Person                               | Text      | AP-98765       |
    | RSE\_ID    | Unique identifier for the Registered Structural Engineer                    | Number    | 67890          |
    | RSE\_NAME  | Name of the Registered Structural Engineer                                   | Text      | Jane Smith     |
    | RSE\_REG\_NO| Registration number of the Registered Structural Engineer                   | Text      | RSE-54321      |
    | ...        | ...                                                                           | ...       | ...            |

    *(Note: The exact format and content of the Excel file will be confirmed with MWMS2 system owners.)*

#### 3.2.4 INT-ESH-01 -Data Import from ESH

*   **Target System**: ESH
*   **Interface Type**: SFTP
*   **In / Out**: In
*   **Frequency**: Daily

*   **Description**: LSCP will import site project information from the ESH system daily via scheduled SFTP file transfer. This information validates user involvement in site projects.
*   **Data Exchange**:
    1.  ESH generates files and places them in a designated SFTP server directory.
    2.  LSCP connects to the SFTP server, authenticates, and downloads the files.
    3.  LSCP parses the files and imports the data into its database.
*   **Authentication**: SFTP access will use SSH keys or username/password credentials.
*   **Error Handling**: The system will handle file transfer, parsing, and database import errors with logging and retry mechanisms.
*   **File Format**: To be confirmed (Excel, CSV, or JSON).
*   **Data Mapping**:

    | ESH Data Item | LSCP Data Item | Data Type | Description |
    | :---- | :---- | :---: | :---- |
    | File Reference | File Reference | string | BD Reference Number of the site project |
    | Site Address | Site Address | string | address of the site project |
    | AP Registration Number | AP Registration Number | string | Registration number of the AP that involve in the related site project |
    | RSE Registration Number | RSE Registration Number | string | Registration number of the RSE that involve in the related site project |
    | RGE Registration Number | RGE Registration Number | string | Registration number of the RGE that involve in the related site project |
    | RC Registration Number | RC Registration Number | string | Registration number of the RC that involve in the related site project |

#### 3.2.5 INT-ERKS-01 -Data Import from ERKS

*   **Target System**: ERKS
*   **Interface Type**: TBC (To Be Confirmed)
*   **In / Out**: In
*   **Frequency**: TBC (To Be Confirmed)

*   **Description**: This interface will import data from the ERKS system into LSCP. Specifics will be determined in consultation with ERKS system owners.
*   **Data Exchange**: Data exchange method (API, file transfer, database link) to be defined.
*   **Authentication**: Authentication and authorization mechanisms for ERKS data access to be established.
*   **Error Handling**: Robust error handling for data exchange issues.
*   **Data Mapping**: To be defined based on specific data elements for mapping between ERKS and LSCP.

#### 3.2.6 INT-BRAVO-01 -Data Import from BRAVO

*   **Target System**: BRAVO
*   **Interface Type**: HTTP Request Redirection
*   **In / Out**: In
*   **Frequency**: Per User Request

*   **Description**: LSCP will redirect to BRAVO using `https://dp2.bd.hksarg/bravo/intranetSignOn`.  LSCP can also redirect to BRAVO via URL calls with parameters.
*   **Data Exchange**: LSCP sends HTTP requests (GET or POST) to BRAVO URLs, passing parameters in the URL query string or request body. BRAVO responds with relevant data.
*   **Authentication**: Authentication method for BRAVO access (API keys, OAuth) to be determined.
*   **Error Handling**: System should handle errors from BRAVO API and provide user feedback.
*   **URL Syntax (Examples)**:
    *   **with Case number and Year**:
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`
    *   **with Block ID**:
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`
    *   **with full File Reference No**:
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    *(Note: Exact URL syntax and parameters need confirmation from BRAVO system owners.)*

*   **Data Mapping**: To be defined based on specific data elements for mapping between LSCP and BRAVO.

*** End of document***
```