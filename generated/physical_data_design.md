# Physical Data Design for Licensing Self-Certification Portal (LSCP)

**Version 0.1**

**Jan 2025**

## 1. Introduction

This document provides a comprehensive description of the physical data structure and process design for the Licensing Self-Certification Portal (LSCP) Project. It serves as a blueprint for the implementation of the LSCP database, ensuring a robust and efficient data management system.

The document details the relationships between key business entities within the LSCP, including a visual representation and comprehensive descriptions of each entity, its attributes, and data types. Data relationships are further explained, highlighting primary and foreign keys, and constraints.

This document is a valuable resource for developers, database administrators, and other stakeholders involved in the implementation and maintenance of the LSCP.

## 2. Objectives

The objectives of the Licensing Self-Certification Portal (LSCP) are to:

1.  Provide user-friendly and meaningful messages to users.
2.  Store all electronic and paper submissions from applicants and authorized persons (AP)/registered structural engineers (RSE) for requisite safety certificates for registration of non-purpose built schools and child care centers, and applications related to non-purpose non-local higher and professional education courses.
3.  Provide a BD departmental portal login for internal users (BD), with User ID and password as an alternative.
4.  Support the latest web browsers.
5.  Comply with the standards of the Government System Architecture and government IT security policy.

## 3. Physical Data Structure Specification

This section documents the data model and its associated descriptions of the required system.

### 3.1. Physical Data Structure

An entity-relationship diagram consists of three basic elements such as entity, relationship, and attribute. Along with these are more components based on their main elements like weak entity, multi-valued attribute, and many more. Notations used to make ERD diagram examples include cardinality and ordinality to define relationships in numbers.

![ER Diagram](media/image1.png)

There are 7 categories of entities in the data model design:

-   (GCIS) Frontend - Application Forms submission
-   (GCIS) Frontend - OTP login control
-   Backend - Users
-   Backend - Workflow of Application Forms submission

#### 3.1.1. (GCIS) Frontend - Application Forms Submission

![Application Forms Submission](media/image3.jpg)

#### 3.1.2. (GCIS) Frontend - OTP Login Control

Diagram 3.1-2

Pending

#### 3.1.3. (BD) Backend - TBC

Diagram 3.1-3

Pending

## 4. Data Entity Description

This section states the conversion rules, the assumptions applied for the physical data design, the names of the physical data tables, the corresponding required system entities and key details to be stored into the database.

The database is a physical store of contract related information and textual data inside a database management system (DBMS). For LSCP, **Microsoft SQL Server 2019** is selected for the database management system. **All the spatial and textual entity will be stored into Microsoft SQL Server 2019.**

The following tables document how the Logical Data Model (LDM) can be mapped onto the physical data design.

**Note: Following table needs to review its correctness**

### LSCP Frontend (Node.js Frontend - SQL Database)

| Table ID | LSCP Name                   | LSCP Entity Description                                                     | Key Nature | Key Data Item                |
| :------- | :-------------------------- | :-------------------------------------------------------------------------- | :--------- | :--------------------------- |
| T-S-01   | ApplicationCase             | Table to store all the application number                                   | PK         | Id                           |
|          |                             |                                                                             |            | ApplicationNo                |
| T-S-02   | SchoolApp_Infos             | Table to store the latest update of the submitted application data as 1 row | PK         | Id                           |
|          |                             |                                                                             |            | ApplicationNo                |
| T-S-03   | SchoolApp_Submissions       | Table to store the submission of each application                           | PK         | Id                           |
|          |                             |                                                                             |            | ApplicationNo                |
|          |                             |                                                                             |            | SubmissionId                 |
| T-S-04   | ApplicationFiles            | Table to store all the path of applicant upload files                       | PK         | Id                           |
|          |                             |                                                                             |            | ApplicationNo                |
|          |                             |                                                                             |            | SubmissionId                 |
| T-S-05   | ScsMasterTable              | Table to store meta-data or parameter data for frontend                     | PK         | Id                           |
|          |                             |                                                                             |            | Code                         |
|          |                             |                                                                             |            | Type + Code                  |
| T-S-06   | GenOtp                      | Table to store generated OTP code and the usage status                      | PK         | Id                           |
|          |                             |                                                                             |            | ApplicationNo + userId + Otp |
| T-S-07   | AdrBlk                      | Table to store addresses that import from BCIS                              | PK         | ADR_BLK_ID                   |
| T-S-08   | SYS_META_DATA               | Table to store meta data that import from BCIS                              | PK         | SYS_META_DATA_ID             |
|          |                             |                                                                             |            | REC_TYPE                     |
|          |                             |                                                                             |            | CODE                         |
| T-S-09   | Aprse                       | Table to store AP / RSE information that import from MWMS 2.0               | PK         | Id                           |
|          |                             |                                                                             |            | Name + RegistrationNumber    |

### LSCP Backend (MongoDB Database)

| Table ID | LSCP Name     | LSCP Entity Description                                                     | Key Nature | Key Data Item    |
| :------- | :-------------- | :-------------------------------------------------------------------------- | :--------- | :----------------- |
| T-S-01   | Application   | Table to store application data                                             | PK         | _id               |
|          |               |                                                                             |            | ApplicationNo    |
| T-S-02   | Submission    | Table to store submission data                                              | PK         | _id               |
|          |               |                                                                             |            | application       |
| T-S-03   | Attachment    | Table to store attachments                                                  | PK         | _id               |
|          |               |                                                                             |            | application       |
| T-S-04   | BsBlock       | Table to store Building Safety Blocks                                       | PK         | _id               |
|          |               |                                                                             |            | blockId          |
| T-S-05   | Task          | Table to store tasks                                                        | PK         | _id               |
|          |               |                                                                             |            | application       |
| T-S-06   | Case          | Table to store cases                                                        | PK         | _id               |
|          |               |                                                                             |            | application       |
| T-S-07   | Eminute       | Table to store electronic minutes                                           | PK         | _id               |
|          |               |                                                                             |            | submissionCase    |
| T-S-08   | OAuthToken    | Table to store OAuth tokens                                                 | PK         | _id               |
|          |               |                                                                             |            | accessToken       |
| T-S-09   | User          | Table to store user data                                                    | PK         | _id               |
|          |               |                                                                             |            | osdpLoginId       |
| T-S-10   | Notification  | Table to store notifications                                                | PK         | _id               |
|          |               |                                                                             |            | user              |
| T-S-11   | SysFileRef    | Table to store system file references                                       | PK         | _id               |
|          |               |                                                                             |            | sysFileRefId      |
| T-S-12   | AdrBlkFileRef | Table to store address block file references                                | PK         | _id               |
|          |               |                                                                             |            | adrBlkFileRefId |

## 5. Collection Details (MongoDB)

This section provides detailed information about each collection in the MongoDB database, including statistics and field analysis.

### 5.1. Collection: tasks

-   Document Count: 5523
-   Size: 0.99 MB
-   Average Document Size: 0.18 KB

**Field Analysis:**

| Field          | Types                | Occurrences |
| :------------- | :------------------- | :---------- |
| \_\_v          | objectId, int        | 1000        |
| \_id           | objectId             | 1000        |
| application    | objectId             | 998         |
| createdAt      | date                 | 1000        |
| status         | string               | 1000        |
| submissionCase | objectId             | 998         |
| taskType       | string               | 998         |
| team           | string               | 835         |
| user           | string, objectId     | 713         |

### 5.2. Collection: eminutes

-   Document Count: 133
-   Size: 0.03 MB
-   Average Document Size: 0.24 KB

**Field Analysis:**

| Field          | Types           | Occurrences |
| :------------- | :-------------- | :---------- |
| \_\_v          | int             | 133         |
| \_id           | objectId        | 133         |
| comment        | string          | 64          |
| content        | string          | 133         |
| createdAt      | date            | 133         |
| efolio         | string          | 100         |
| eminuteId      | string          | 133         |
| from           | objectId, string| 133         |
| status         | string          | 133         |
| subject        | string          | 133         |
| submissionCase | objectId        | 133         |
| sysFileRefId   | string          | 65          |
| to             | objectId, string| 129         |

### 5.3. Collection: submissions

-   Document Count: 0
-   Size: 0.00 MB
-   Average Document Size: 0.00 KB

**Field Analysis:** (No data available)

### 5.4. Collection: applications

-   Document Count: 381
-   Size: 0.36 MB
-   Average Document Size: 0.96 KB

**Field Analysis:**

| Field                    | Types             | Occurrences |
| :----------------------- | :---------------- | :---------- |
| APP13                    | object, array     | 172         |
| AddressOfPremiseCN       | string            | 267         |
| AddressOfPremiseCNFloor  | string            | 147         |
| AddressOfPremiseCNUnit   | string            | 147         |
| AddressOfPremiseEN       | string            | 271         |
| AddressOfPremiseENFloor  | string            | 155         |
| AddressOfPremiseENUnit   | string            | 154         |
| AgeOfStudent             | null, string      | 328         |
| ApplicantAddress         | string            | 335         |
| ApplicantEmail           | string            | 289         |
| ApplicantFax             | string            | 21          |
| ApplicantMobile          | string            | 288         |
| ApplicantName            | string            | 189         |
| ApplicantNameCN          | string            | 28          |
| ApplicantNameEN          | null, string      | 148         |
| ApplicantTel             | null, string      | 307         |
| ApplicationNo            | null, string      | 381         |
| ApplicationType          | string            | 356         |
| Area                     | string            | 28          |
| BlockID                  | string            | 178         |
| ContactPerson            | string            | 95          |
| ContactPersonCN          | string            | 6           |
| ContactPersonEN          | string            | 6           |
| ContactPersonEmail       | string            | 6           |
| ContactPersonTel         | string            | 6           |
| DescriptionOfSchool      | string, null      | 329         |
| District                 | string            | 33          |
| EstimatedNoOfStudent     | int, null         | 328         |
| FileReference            | string            | 35          |
| NameOfSchoolCN           | string            | 323         |
| NameOfSchoolEN           | string            | 350         |
| Region                   | string            | 29          |
| RelatedPremise           | string            | 62          |
| RelatedPremises          | array             | 381         |
| SelfCertification        | object, null      | 65          |
| StructuralCalculation    | object            | 18          |
| SubmissionType           | string            | 187         |
| \_\_v                    | int               | 381         |
| \_id                     | objectId          | 381         |
| address                  | object            | 69          |
| assignedBS               | objectId, string, null | 364         |
| assignedGR               | objectId, null      | 64          |
| assignedSBS              | string, null      | 53          |
| createdAt                | date              | 381         |
| updatedAt                | date              | 194         |

### 5.5. Collection: notifications

-   Document Count: 1837
-   Size: 0.24 MB
-   Average Document Size: 0.13 KB

**Field Analysis:**

| Field            | Types      | Occurrences |
| :--------------- | :--------- | :---------- |
| \_\_v            | int        | 1000        |
| \_id             | objectId   | 1000        |
| createdAt        | date       | 1000        |
| eminute          | objectId   | 58          |
| notificationType | string     | 1000        |
| requireSendEmail | bool       | 1000        |
| task             | objectId   | 942         |
| user             | string     | 991         |

### 5.6. Collection: bsblocks

-   Document Count: 98397
-   Size: 6.40 MB
-   Average Document Size: 0.07 KB

**Field Analysis:**

| Field     | Types  | Occurrences |
| :-------- | :----- | :---------- |
| \_\_v     | int    | 1000        |
| \_id      | objectId | 1000        |
| bdgis     | string | 1000        |
| blockId   | string | 1000        |

### 5.7. Collection: cases

-   Document Count: 451
-   Size: 1.17 MB
-   Average Document Size: 2.65 KB

**Field Analysis:**

| Field                    | Types           | Occurrences |
| :----------------------- | :-------------- | :---------- |
| ActualReplyDate          | null, date      | 39          |
| Area                     | string          | 26          |
| AuditResult              | string          | 11          |
| CaseOfficer              | string          | 108         |
| Category                 | string          | 384         |
| District                 | string          | 37          |
| FileReference            | string          | 60          |
| LAFileReference          | object          | 17          |
| Nature                   | null, string      | 382         |
| ObjectiontoLR            | string          | 12          |
| ReceivedDate             | date, null      | 375         |
| Referrer                 | object          | 43          |
| Region                   | string          | 32          |
| Remarks                  | string          | 7           |
| Reminders                | array           | 55          |
| SubmissionType           | string          | 8           |
| SubstantialReplyDate     | null, date      | 42          |
| TargetReplyDate          | date, null      | 111         |
| ThreeTierReqt            | string          | 12          |
| ViaSCS                   | bool            | 17          |
| \_\_v                    | int             | 451         |
| \_id                     | objectId          | 451         |
| application              | objectId          | 450         |
| assignedBS               | objectId          | 274         |
| assignedGR               | objectId          | 137         |
| building_information     | object          | 14          |
| caseDescription          | object          | 9           |
| caseOfficerReceive       | string          | 172         |
| caseOfficerReply         | string          | 72          |
| createdAt                | date            | 451         |
| deck_study               | object          | 451         |
| documentChecklist        | object          | 2           |
| dv                       | object          | 197         |
| frc                      | object          | 451         |
| misc                     | object          | 451         |
| moe                      | object          | 451         |
| seniorCaseOfficerReceive | string          | 54          |
| seniorCaseOfficerReply   | string          | 41          |
| site_inspection          | object          | 7           |
| structural_ccc_bs        | object          | 451         |
| structural_schnlh        | object          | 152         |
| structural_schnlhkinds   | object          | 301         |
| team                     | string          | 374         |
| ubw                      | object          | 451         |
| updatedAt                | date            | 16          |

### 5.8. Collection: oauthtokens

-   Document Count: 3019
-   Size: 2.29 MB
-   Average Document Size: 0.78 KB

**Field Analysis:**

| Field               | Types  | Occurrences |
| :------------------ | :----- | :---------- |
| \_\_v               | int    | 1000        |
| \_id                | objectId | 1000        |
| accessToken         | string | 1000        |
| accessTokenExpiresAt| date   | 1000        |
| client              | object | 1000        |
| refreshToken        | string | 1000        |
| refreshTokenExpiresAt | date   | 1000        |
| user                | objectId | 1000        |

### 5.9. Collection: sysfilerefs

-   Document Count: 601808
-   Size: 204.70 MB
-   Average Document Size: 0.35 KB

**Field Analysis:**

| Field               | Types           | Occurrences |
| :------------------ | :-------------- | :---------- |
| \_\_v               | int             | 1000        |
| \_id                | objectId        | 1000        |
| createdDt           | date            | 1000        |
| createdName         | null, string      | 1000        |
| createdPost         | null, string      | 1000        |
| createdSection      | null, string      | 1000        |
| display             | string          | 1000        |
| dvExceed            | null, string      | 1000        |
| dvStatusDt          | null, date        | 1000        |
| frefPref            | string, null      | 1000        |
| frefSeq             | null, string      | 1000        |
| frefSuf             | null, string      | 1000        |
| frefYr              | null, string      | 1000        |
| lastModifiedDt      | date            | 1000        |
| lastModifiedName    | null, string      | 1000        |
| lastModifiedPost    | null, string      | 1000        |
| lastModifiedSection | null            | 1000        |
| sysFileRefId        | string          | 1000        |

### 5.10. Collection: attachments

-   Document Count: 370
-   Size: 0.13 MB
-   Average Document Size: 0.37 KB

**Field Analysis:**

| Field          | Types           | Occurrences |
| :------------- | :-------------- | :---------- |
| \_\_v          | int             | 370         |
| \_id           | objectId        | 370         |
| application    | objectId        | 364         |
| createdAt      | date            | 370         |
| efolio         | null, string      | 351         |
| file           | object, string    | 247         |
| filePartNo     | string          | 216         |
| receivedDate   | date            | 352         |
| remarks        | string          | 216         |
| subType        | string          | 203         |
| submissionCase | objectId        | 350         |
| sysFileRefId   | string          | 67          |
| type           | string          | 348         |
| updatedAt      | date            | 3           |

### 5.11. Collection: users

-   Document Count: 116
-   Size: 0.04 MB
-   Average Document Size: 0.39 KB

**Field Analysis:**

| Field               | Types  | Occurrences |
| :------------------ | :----- | :---------- |
| \_\_v               | int    | 116         |
| \_id                | objectId | 116         |
| bdgis               | string | 29          |
| begis               | string | 1           |
| delegateTo          | string | 8           |
| department          | string | 116         |
| email               | string | 109         |
| group               | string | 17          |
| lastLoginAt         | date   | 41          |
| letterLongPosition  | string | 11          |
| letterLongPositionCn| string | 12          |
| letterName          | string | 76          |
| letterNameCn        | string | 75          |
| letterPosition      | string | 79          |
| letterPositionCn    | string | 1           |
| lock                | bool   | 116         |
| luPostName          | string | 78          |
| name                | string | 80          |
| notificationEmail   | string | 23          |
| osdpEmail           | string | 62          |
| osdpLoginId         | string | 102         |
| password            | string | 108         |
| phoneNumber         | string | 65          |
| position            | string | 85          |
| role                | string | 112         |
| team                | string | 52          |
| userType            | string | 116         |

### 5.12. Collection: adrblkfilerefs

-   Document Count: 566948
-   Size: 154.89 MB
-   Average Document Size: 0.28 KB

**Field Analysis:**

| Field               | Types           | Occurrences |
| :------------------ | :-------------- | :---------- |
| \_\_v               | int             | 1000        |
| \_id                | objectId        | 1000        |
| adrBlkFileRefId     | string          | 1000        |
| adrBlkId            | string          | 1000        |
| createdDt           | date            | 1000        |
| createdName         | null, string      | 1000        |
| createdPost         | string          | 1000        |
| createdSection      | null, string      | 1000        |
| lastModifiedDt      | date            | 1000        |
| lastModifiedName    | null, string      | 1000        |
| lastModifiedPost    | string          | 1000        |
| lastModifiedSection | string, null      | 1000        |
| sysFileRefId        | string          | 1000        |

---

**End of Document**