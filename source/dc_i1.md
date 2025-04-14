**DATA CATALOGUE**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**  
**LICENSING SELF-CERTIFICATION PORTAL**  
**OF**  
**BUILDINGS DEPARTMENT**

**Version: 1.1**

**January 21, 2025**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

| Distribution |  |
| :---: | :---: |
| Copy No. | Holder |
| 1 | Buildings Department (BD) |
| 2 | Master Concept (Hong Kong) Limited (MC) |

| Amendment History |  |  |  |  |  |
| ----- | ----- | ----- | ----- | ----- | ----- |
| Change Number | Revision Description | Pages Affected | Revision/Version Number | Date | Approval Reference |
| 1 | First Draft | All | 1.0 | 21/01/2025 |  |
| 2 | Added missing models and descriptions | 1,3,4-6| 1.1 | 21/01/2025 | |

**TABLE OF CONTENTS**

[**1. Introduction**](#1-introduction)

[**2. Definitions**](#2-definitions)

[**3. Data Architecture Overview**](#3-data-architecture-overview)

[**4. Database Specifications**](#4-database-specifications)

[4.1 MongoDB Collections](#41-mongodb-collections)
[4.1.1 tasks](#411-tasks)
[4.1.2 eminutes](#412-eminutes)
[4.1.3 submissions](#413-submissions)
[4.1.4 applications](#414-applications)
[4.1.5 notifications](#415-notifications)
[4.1.6 bsblocks](#416-bsblocks)
[4.1.7 cases](#417-cases)
[4.1.8 oauthtokens](#418-oauthtokens)
[4.1.9 sysfilerefs](#419-sysfilerefs)
[4.1.10 attachments](#4110-attachments)
[4.1.11 users](#4111-users)
[4.1.12 adrblkfilerefs](#4112-adrblkfilerefs)

[4.2 MSSQL Tables](#42-mssql-tables)
[4.2.1 __EFMigrationsHistory](#421-efmigrationshistory)
[4.2.2 AdrBlk](#422-adrblk)
[4.2.3 AdrBlk_T](#423-adrblk_t)
[4.2.4 ApplicationCases](#424-applicationcases)
[4.2.5 ApplicationFiles](#425-applicationfiles)
[4.2.6 ApRse](#426-aprse)
[4.2.7 Attachment](#427-attachment)
[4.2.8 BackendUpdate](#428-backendupdate)
[4.2.9 ChildCareCentreApplications](#429-childcarecentreapplications)
[4.2.10 GenOtp](#4210-genotp)
[4.2.11 IamSmart](#4211-iamsmart)
[4.2.12 LogEvents](#4212-logevents)
[4.2.13 SchoolApp_Infos](#4213-schoolapp_infos)
[4.2.14 SchoolApp_Submission](#4214-schoolapp_submission)
[4.2.15 SchoolApp_Submissions](#4215-schoolapp_submissions)
[4.2.16 ScsMasterTable](#4216-scsmastertable)
[4.2.17 SequelizeMeta](#4217-sequelizeMeta)
[4.2.18 Sys_Meta_Data](#4218-sys_meta_data)
[4.2.19 Sys_Meta_Data_T](#4219-sys_meta_data_t)

# **1. Introduction**

This document provides a description of the data catalog for the Combined System Development Services of the LSCP of the Buildings Department. The system uses a dual-database architecture with MongoDB for operational data and MSSQL for transactional data.

# **2. Definitions**

| Terms | Definitions |
| :---- | :---- |
| BD | Buildings Department |
| LSCP | Licensing Self-Certification Portal |
| AP | Authorized Person |
| RSE | Registered Structural Engineer |
| IAM Smart | A single digital identity authentication platform for the Hong Kong Government |
| OTP | One-Time Password |
| BD Letter | A formal letter issued by Buildings Department |
| LSO | Licensing Subject Officer |
| MSSQL | Microsoft SQL Server database |
| MongoDB | NoSQL document-oriented database |

# **3. Data Architecture Overview**

The LSCP system employs a dual-database architecture:

## MongoDB Database
MongoDB serves as the primary operational database, handling dynamic application data, user sessions, and day-to-day operations. It provides flexibility for evolving data structures and supports high-volume read operations.

**Key Statistics:**
- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1,278,983
- Total Data Size: 371.24 MB

## MSSQL Database
Microsoft SQL Server serves as the transactional database, storing structured data related to applications, submissions, and system reference data. It provides robust data integrity and transaction support.

**Key Database:** bd_scs
**Schema:** dbo

## Data Flow Between Systems
- MongoDB handles frontend operational data and user sessions
- MSSQL stores backend transactional data and historical records
- Data synchronization occurs through application services
- Critical data is maintained in both systems with appropriate reconciliation mechanisms

## Data Entity Relationships

The following diagram represents the high-level relationships between key entities across both databases:

```
                                 +----------------+
                                 |    Users       |
                                 +----------------+
                                        |
                                        v
+----------------+            +----------------+            +----------------+
|  Applications  |<---------->|     Cases      |<---------->|  Submissions   |
+----------------+            +----------------+            +----------------+
        |                            |                             |
        v                            v                             v
+----------------+            +----------------+            +----------------+
|  Attachments   |            |    Tasks       |            |    Eminutes    |
+----------------+            +----------------+            +----------------+
```

# **4. Database Specifications**

This section details the structure of both databases used in the LSCP system.

## 4.1 MongoDB Collections

MongoDB is used for operational data with the following collections:

### 4.1.1 tasks
**Collection Statistics**
- Document Count: 5,523
- Size: 0.99 MB
- Average Document Size: 0.18 KB

**Field Structure**
| Field Name | Data Type | Description |
| :--------- | :-------- | :---------- |
| _id | objectId | Unique identifier |
| application | objectId | Reference to application |
| createdAt | date | Creation timestamp |
| status | string | Task status |
| submissionCase | objectId | Reference to submission case |
| taskType | string | Type of task |
| team | string | Team assigned to the task |
| user | string/objectId | User assigned to the task |
| __v | int | Version number |

### 4.1.2 eminutes
**Collection Statistics**
- Document Count: 133
- Size: 0.03 MB
- Average Document Size: 0.24 KB

**Field Structure**
| Field Name | Data Type | Description |
| :--------- | :-------- | :---------- |
| _id | objectId | Unique identifier |
| comment | string | Comment text |
| content | string | Main content |
| createdAt | date | Creation timestamp |
| efolio | string | Electronic folio reference |
| eminuteId | string | Minute identifier |
| from | objectId/string | Sender reference |
| status | string | Status of the minute |
| subject | string | Subject of the minute |
| submissionCase | objectId | Reference to submission case |
| sysFileRefId | string | System file reference ID |
| to | objectId/string | Recipient reference |
| __v | int | Version number |

### 4.1.3 submissions
**Collection Statistics**
- Document Count: 0
- Size: 0.00 MB
- Average Document Size: 0.00 KB

**Note:** This collection exists but currently contains no documents.

### 4.1.4 applications
**Collection Statistics**
- Document Count: 381
- Size: 0.36 MB
- Average Document Size: 0.96 KB

**Field Structure**
| Field Name | Data Type | Description |
| :--------- | :-------- | :---------- |
| _id | objectId | Unique identifier |
| APP13 | object/array | APP13 form information |
| AddressOfPremiseCN | string | Premises address (Chinese) |
| AddressOfPremiseEN | string | Premises address (English) |
| ApplicationNo | string | Application number |
| ApplicationType | string | Type of application |
| NameOfSchoolCN | string | School name (Chinese) |
| NameOfSchoolEN | string | School name (English) |
| assignedBS | objectId/string | Assigned Building Surveyor |
| assignedGR | objectId | Assigned General Registry |
| assignedSBS | string | Assigned Senior Building Surveyor |
| createdAt | date | Creation timestamp |
| updatedAt | date | Last update timestamp |
| __v | int | Version number |
| ... | ... | (Additional fields omitted for brevity) |

## 4.2 MSSQL Tables

MSSQL database (bd_scs) contains the following tables in the dbo schema:

### 4.2.1 __EFMigrationsHistory
**Description**: Stores Entity Framework migrations history

**Table Structure**
| Column Name | Data Type | Length | Nullable | PK | Description |
| :---------- | :-------- | :----- | :------- | :- | :---------- |
| MigrationId | nvarchar | 300 | No | Yes | Migration identifier |
| ProductVersion | nvarchar | 64 | No | No | EF Core product version |

### 4.2.2 AdrBlk
**Description**: Stores building address information

**Table Structure**
| Column Name | Data Type | Length | Nullable | PK | Description |
| :---------- | :-------- | :----- | :------- | :- | :---------- |
| ADR_BLK_ID | bigint | 8 | No | Yes | Address block ID |
| BLK_TYPE_ID | bigint | 8 | Yes | No | Block type ID |
| BLDG_CAT_ID | bigint | 8 | Yes | No | Building category ID |
| BLDG_USAGE_ID | bigint | 8 | Yes | No | Building usage ID |
| SYS_REGION_ID | bigint | 8 | Yes | No | System region ID |
| SYS_DISTRICT_ID | bigint | 8 | Yes | No | System district ID |
| AREA_ID | bigint | 8 | Yes | No | Area ID |
| BLK_DESC_E_ID | bigint | 8 | Yes | No | Block description English ID |
| BLK_NO_NUM | int | 4 | Yes | No | Block number (numeric) |
| BLK_NO_ALPHA | nvarchar | 20 | Yes | No | Block number (alphanumeric) |
| BLDG_NAME_E1 | nvarchar | 90 | Yes | No | Building name English 1 |
| BLDG_NAME_E2 | nvarchar | 90 | Yes | No | Building name English 2 |
| BLDG_NAME_E3 | nvarchar | 90 | Yes | No | Building name English 3 |
| BLDG_NAME_C1 | nvarchar | 160 | Yes | No | Building name Chinese 1 |
| BLDG_NAME_C2 | nvarchar | 160 | Yes | No | Building name Chinese 2 |
| BLDG_NAME_C3 | nvarchar | 160 | Yes | No | Building name Chinese 3 |
| OSADR_E1 | nvarchar | 90 | Yes | No | Original source address English 1 |
| ... | ... | ... | ... | ... | ... |
| OBSOLETE | nvarchar | 160 | Yes | No | Obsolete flag |
| CreatedAt | datetime2 | 8 | Yes | No | Creation timestamp |
| UpdatedAt | datetime2 | 8 | Yes | No | Last update timestamp |

### 4.2.3 AdrBlk_T
**Description**: Temporary table for building address information

**Table Structure**
| Column Name | Data Type | Length | Nullable | PK | Description |
| :---------- | :-------- | :----- | :------- | :- | :---------- |
| ADR_BLK_ID | bigint | 8 | No | Yes | Address block ID (identity) |
| BLK_TYPE_ID | bigint | 8 | Yes | No | Block type ID |
| BLDG_CAT_ID | bigint | 8 | Yes | No | Building category ID |
| ... | ... | ... | ... | ... | ... |
| createdAt | datetimeoffset | 10 | No | No | Creation timestamp |
| updatedAt | datetimeoffset | 10 | No | No | Last update timestamp |

### 4.2.4 ApplicationCases
**Description**: Stores application case information

**Table Structure**
| Column Name | Data Type | Length | Nullable | PK | Description |
| :---------- | :-------- | :----- | :------- | :- | :---------- |
| Id | bigint | 8 | No | Yes | Case ID (identity) |
| ApplicationNo | nvarchar | 30 | Yes | No | Application number |
| CreatedAt | datetime2 | 8 | Yes | No | Creation timestamp |
| CreatedBy | nvarchar | 200 | Yes | No | Creator |
| UpdatedAt | datetime2 | 8 | Yes | No | Last update timestamp |
| UpdatedBy | nvarchar | 200 | Yes | No | Last updater |
| FromId | bigint | 8 | Yes | No | Source ID |
| FileDate | datetime2 | 8 | Yes | No | File date |

### 4.2.5 ApplicationFiles
**Description**: Stores application file information

**Table Structure**
| Column Name | Data Type | Length | Nullable | PK | Description |
| :---------- | :-------- | :----- | :------- | :- | :---------- |
| Id | bigint | 8 | No | Yes | File ID (identity) |
| FileName | nvarchar | 200 | Yes | No | File name |
| DocumentType | nvarchar | 40 | Yes | No | Document type |
| SignType | nvarchar | 60 | Yes | No | Sign type |
| FilePath | nvarchar | 510 | Yes | No | File path |
| CreatedAt | datetime2 | 8 | Yes | No | Creation timestamp |
| ... | ... | ... | ... | ... | ... |
| RemoveStatus | nvarchar | 100 | Yes | No | Remove status |
