```markdown
<img src="media/image1.jpg" style="width:2.03125in;height:1.52083in"
alt="BDlogo" />

**<span class="smallcaps">DATA CATALOGUE</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">COMBINED SYSTEM DEVELOPMENT SERVICES</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**<span class="smallcaps">OF</span>**

**<span class="smallcaps">BUILDINGS DEPARTMENT</span>**

**Version: 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR.

| **Distribution** |                                         |
|------------------|-----------------------------------------|
| Copy No.         | Holder                                  |
| 1                | Buildings Department (BD)               |
| 2                | Master Concept (Hong Kong) Limited (MC) |

| **Amendment History** |                      |                                      |                           |            |                    |
|------------|------------|------------|------------|------------|------------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date       | Approval Reference |
| 1                     | 1st draft            | All                                  | 0.1                       | 16/01/2025 |                    |
|                       |                      |                                      |                           |            |                    |
|                       |                      |                                      |                           |            |                    |
|                       |                      |                                      |                           |            |                    |
|                       |                      |                                      |                           |            |                    |
|                       |                      |                                      |                           |            |                    |
|                       |                      |                                      |                           |            |                    |
|                       |                      |                                      |                           |            |                    |
|                       |                      |                                      |                           |            |                    |

**TABLE OF CONTENTS**

[**1. Introduction 5**](#introduction)

[**2. Definitions 6**](#definitions)

[**3. Database Overview 7**](#database-overview)

[**4. Data Entity Description 8**](#data-entity-description)

[**5. Equipment Configuration 9**](#equipment-configuration)

> [5.1 Objective 10](#objective)
>
> [5.1.1. tasks 10](#tasks)
>
> [5.1.2. eminutes 11](#eminutes)
>
> [5.1.3. submissions 12](#submissions)
>
> [5.1.4. applications 12](#applications)
>
> [5.1.5. notifications 14](#notifications)
>
> [5.1.6. bsblocks 15](#bsblocks)
>
> [5.1.7. cases 15](#cases)
>
> [5.1.8. oauthtokens 17](#oauthtokens)
>
> [5.1.9. sysfilerefs 18](#sysfilerefs)
>
> [5.1.10. attachments 19](#attachments)
>
> [5.1.11. users 20](#users)
>
> [5.1.12. adrblkfilerefs 21](#adrblkfilerefs)


# 1. Introduction

This document provides a description of data catalogue of the Combined
System Development Services of the LSCP of the Buildings Department. This catalogue is based on the analysis of the database named `bd` as of 2025/3/4 ??10:10:39.

# 2. Definitions

| Terms | Definitions          |
|-------|----------------------|
| BD    | Buildings Department |
| LSCP  | Licensing Self-Certification Portal |
| MC    | Master Concept (Hong Kong) Limited |
|       |                      |
|       |                      |
|       |                      |
|       |                      |
|       |                      |

# 3. Database Overview

This section provides a statistical overview of the LSCP Database (`bd`).

## Database Statistics
- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1278983
- Total Data Size: 371.24 MB

## Collections Overview
- tasks: 5523 documents, 0.99 MB
- eminutes: 133 documents, 0.03 MB
- submissions: 0 documents, 0.00 MB
- applications: 381 documents, 0.36 MB
- notifications: 1837 documents, 0.24 MB
- bsblocks: 98397 documents, 6.40 MB
- cases: 451 documents, 1.17 MB
- oauthtokens: 3019 documents, 2.29 MB
- sysfilerefs: 601808 documents, 204.70 MB
- attachments: 370 documents, 0.13 MB
- users: 116 documents, 0.04 MB
- adrblkfilerefs: 566948 documents, 154.89 MB


# 4. Data Entity Description

This section states all the entities (Collections) in the LSCP Database.

The following section describes how the LSCP entities are physically designed in the database.

-   Entities list for LSCP Data

| **Item** | **Entity Name** | **Entity Description** |
|----------|-----------------|------------------------|
| 1        | tasks           | Tasks Collection       |
| 2        | eminutes        | Eminutes Collection      |
| 3        | submissions     | Submissions Collection   |
| 4        | applications    | Applications Collection  |
| 5        | notifications   | Notifications Collection |
| 6        | bsblocks        | Bsblocks Collection      |
| 7        | cases           | Cases Collection         |
| 8        | oauthtokens     | Oauthtokens Collection   |
| 9        | sysfilerefs     | Sysfilerefs Collection   |
| 10       | attachments     | Attachments Collection   |
| 11       | users           | Users Collection         |
| 12       | adrblkfilerefs  | Adrblkfilerefs Collection|
|          |                 |                        |
|          |                 |                        |
|          |                 |                        |

# 5. Equipment Configuration

This section details the data items for each database collection in the physical design. The explanation for columns is as follows.

Database-level validation is not utilized. Instead, all validations are implemented on the server side.

> **Entity Name** - Name of database collection
>
> **Description** - Description of entity
>
> **Field Name** - Name of object attributes
>
> **Field Format** - Type of the data item:
>
> - objectId: MongoDB ObjectId
> - string: String
> - int: Integer
> - date: Date (Datetime)
> - bool: Boolean
> - object: Object (Embedded Document)
> - array: Array
> - null: Null Value
>
> **Field Length** - Specify the max number of characters of string field (Variable where applicable)
>
> **Mandatory** - Specify if the data item is mandatory. ?Y? if true. (Inferred from Occurrences, assuming 1000 occurrences in sample implies mandatory in sample, but not necessarily truly mandatory in schema)
>
> **Primary Key** - Indicates if data item is part of the Primary Key (`_id` is assumed to be primary key)
>
> **Foreign Key** - Indicates if data item is likely a Foreign Key (Inferred from field names like `application`, `submissionCase`, `user` etc. pointing to other collections)

## 

## 5.1 Objective

> Name Space: LSCP
>
> Description: LSCP Data Storage
>
> Storage Location: TBC
>
> File Name: TBC

### 5.1.1. tasks

> Entity Name: tasks
>
> Description: Collection for storing tasks related information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v             |  Version field      | int, objectId         | Variable         | Y           | N         | N         |
| _id             |  Document ID      | objectId         | Variable         | Y           | Y         | N         |
| application     |  Reference to application      | objectId         | Variable         | Y           | N         | Y         |
| createdAt       |  Creation Timestamp      | date         | Variable         | Y           | N         | N         |
| status          |  Task Status      | string         | Variable         | Y           | N         | N         |
| submissionCase  |  Reference to submission case      | objectId         | Variable         | Y           | N         | Y         |
| taskType        |  Type of Task      | string         | Variable         | Y           | N         | N         |
| team            |  Team assigned to task      | string         | Variable         | N           | N         | N         |
| user            |  User related to task      | string, objectId         | Variable         | N           | N         | Y         |

### 5.1.2. eminutes

> Entity Name: eminutes
>
> Description: Collection for storing electronic minutes information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v             |  Version field      | int         | Variable         | Y           | N         | N         |
| _id             |  Document ID      | objectId         | Variable         | Y           | Y         | N         |
| comment         |  Comment in eminute      | string         | Variable         | N           | N         | N         |
| content         |  Content of eminute      | string         | Variable         | Y           | N         | N         |
| createdAt       |  Creation Timestamp      | date         | Variable         | Y           | N         | N         |
| efolio          |  eFolio reference      | string         | Variable         | N           | N         | N         |
| eminuteId       |  E-minute ID      | string         | Variable         | Y           | N         | N         |
| from            |  Sender of eminute      | objectId, string         | Variable         | Y           | N         | Y         |
| status          |  Status of eminute      | string         | Variable         | Y           | N         | N         |
| subject         |  Subject of eminute      | string         | Variable         | Y           | N         | N         |
| submissionCase  |  Reference to submission case      | objectId         | Variable         | Y           | N         | Y         |
| sysFileRefId    |  Reference to system file      | string         | Variable         | N           | N         | Y         |
| to              |  Recipient of eminute      | objectId, string         | Variable         | N           | N         | Y         |

### 5.1.3. submissions

> Entity Name: submissions
>
> Description: Collection for storing submission related information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* |

### 5.1.4. applications

> Entity Name: applications
>
> Description: Collection for storing application related information.

| **Field Name**          | **Description**               | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-------------------------------|------------------|------------------|-------------|---------------|---------------|
| APP13                   |  APP13 data                   | object, array    | Variable         | N           | N             | N             |
| AddressOfPremiseCN      |  Address of Premise (CN)       | string           | Variable         | N           | N             | N             |
| AddressOfPremiseCNFloor |  Address of Premise Floor (CN)  | string           | Variable         | N           | N             | N             |
| AddressOfPremiseCNUnit  |  Address of Premise Unit (CN)   | string           | Variable         | N           | N             | N             |
| AddressOfPremiseEN      |  Address of Premise (EN)       | string           | Variable         | N           | N             | N             |
| AddressOfPremiseENFloor |  Address of Premise Floor (EN)  | string           | Variable         | N           | N             | N             |
| AddressOfPremiseENUnit  |  Address of Premise Unit (EN)   | string           | Variable         | N           | N             | N             |
| AgeOfStudent            |  Age of Student                | null, string     | Variable         | N           | N             | N             |
| ApplicantAddress        |  Applicant Address             | string           | Variable         | N           | N             | N             |
| ApplicantEmail          |  Applicant Email               | string           | Variable         | N           | N             | N             |
| ApplicantFax            |  Applicant Fax                 | string           | Variable         | N           | N             | N             |
| ApplicantMobile         |  Applicant Mobile              | string           | Variable         | N           | N             | N             |
| ApplicantName           |  Applicant Name                | string           | Variable         | N           | N             | N             |
| ApplicantNameCN         |  Applicant Name (CN)           | string           | Variable         | N           | N             | N             |
| ApplicantNameEN         |  Applicant Name (EN)           | null, string     | Variable         | N           | N             | N             |
| ApplicantTel            |  Applicant Telephone           | null, string     | Variable         | N           | N             | N             |
| ApplicationNo           |  Application Number            | null, string     | Variable         | Y           | N             | N             |
| ApplicationType         |  Application Type              | string           | Variable         | Y           | N             | N             |
| Area                    |  Area                          | string           | Variable         | N           | N             | N             |
| BlockID                 |  Block ID                      | string           | Variable         | N           | N             | N             |
| ContactPerson           |  Contact Person                | string           | Variable         | N           | N             | N             |
| ContactPersonCN         |  Contact Person (CN)           | string           | Variable         | N           | N             | N             |
| ContactPersonEN         |  Contact Person (EN)           | string           | Variable         | N           | N             | N             |
| ContactPersonEmail      |  Contact Person Email          | string           | Variable         | N           | N             | N             |
| ContactPersonTel        |  Contact Person Telephone        | string           | Variable         | N           | N             | N             |
| DescriptionOfSchool     |  Description of School         | string, null     | Variable         | N           | N             | N             |
| District                |  District                      | string           | Variable         | N           | N             | N             |
| EstimatedNoOfStudent    |  Estimated Number of Students  | int, null        | Variable         | N           | N             | N             |
| FileReference           |  File Reference                | string           | Variable         | N           | N             | N             |
| NameOfSchoolCN          |  Name of School (CN)           | string           | Variable         | N           | N             | N             |
| NameOfSchoolEN          |  Name of School (EN)           | string           | Variable         | N           | N             | N             |
| Region                  |  Region                        | string           | Variable         | N           | N             | N             |
| RelatedPremise          |  Related Premise               | string           | Variable         | N           | N             | N             |
| RelatedPremises         |  Related Premises              | array            | Variable         | Y           | N             | N             |
| SelfCertification      |  Self Certification Data        | object, null     | Variable         | N           | N             | N             |
| StructuralCalculation   |  Structural Calculation Data    | object           | Variable         | N           | N             | N             |
| SubmissionType          |  Submission Type               | string           | Variable         | N           | N             | N             |
| __v                     |  Version field                 | int              | Variable         | Y           | N             | N             |
| _id                     |  Document ID                   | objectId         | Variable         | Y           | Y             | N             |
| address                 |  Address Object                | object           | Variable         | N           | N             | N             |
| assignedBS              |  Assigned Building Surveyor    | objectId, string, null | Variable     | N           | N             | Y             |
| assignedGR              |  Assigned Geotechnical Engineer| objectId, null   | Variable         | N           | N             | Y             |
| assignedSBS             |  Assigned Structural Engineer  | string, null     | Variable         | N           | N             | Y             |
| createdAt               |  Creation Timestamp            | date             | Variable         | Y           | N             | N             |
| updatedAt               |  Update Timestamp              | date             | Variable         | N           | N             | N             |

### 5.1.5. notifications

> Entity Name: notifications
>
> Description: Collection for storing notification related information.

| **Field Name**      | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------|-----------------------------|------------------|------------------|-------------|---------------|---------------|
| __v               | Version field               | int              | Variable         | Y           | N             | N             |
| _id               | Document ID                 | objectId         | Variable         | Y           | Y             | N             |
| createdAt         | Creation Timestamp          | date             | Variable         | Y           | N             | N             |
| eminute           | Reference to eminute        | objectId         | Variable         | N           | N             | Y             |
| notificationType  | Type of Notification        | string           | Variable         | Y           | N             | N             |
| requireSendEmail  | Flag to require sending email| bool             | Variable         | Y           | N             | N             |
| task              | Reference to task           | objectId         | Variable         | N           | N             | Y             |
| user              | User related to notification| string           | Variable         | Y           | N             | Y             |

### 5.1.6. bsblocks

> Entity Name: bsblocks
>
> Description: Collection for storing building blocks information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v             | Version field      | int         | Variable         | Y           | N         | N         |
| _id             | Document ID      | objectId         | Variable         | Y           | Y         | N         |
| bdgis           | BDGIS Block ID      | string         | Variable         | Y           | N         | N         |
| blockId         | Block ID          | string         | Variable         | Y           | N         | N         |

### 5.1.7. cases

> Entity Name: cases
>
> Description: Collection for storing case related information.

| **Field Name**              | **Description**                     | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------------|-------------------------------------|------------------|------------------|-------------|---------------|---------------|
| ActualReplyDate           | Actual Reply Date                   | null, date       | Variable         | N           | N             | N             |
| Area                      | Area                                | string           | Variable         | N           | N             | N             |
| AuditResult               | Audit Result                        | string           | Variable         | N           | N             | N             |
| CaseOfficer               | Case Officer                        | string           | Variable         | N           | N             | N             |
| Category                  | Case Category                       | string           | Variable         | Y           | N             | N             |
| District                  | District                            | string           | Variable         | N           | N             | N             |
| FileReference             | File Reference                      | string           | Variable         | N           | N             | N             |
| LAFileReference           | LA File Reference                   | object           | Variable         | N           | N             | N             |
| Nature                    | Case Nature                         | null, string     | Variable         | N           | N             | N             |
| ObjectiontoLR             | Objection to LR                     | string           | Variable         | N           | N             | N             |
| ReceivedDate              | Received Date                       | date, null       | Variable         | N           | N             | N             |
| Referrer                  | Referrer Information                | object           | Variable         | N           | N             | N             |
| Region                    | Region                              | string           | Variable         | N           | N             | N             |
| Remarks                   | Remarks                             | string           | Variable         | N           | N             | N             |
| Reminders                 | Reminders Array                     | array            | Variable         | Y           | N             | N             |
| SubmissionType            | Submission Type                     | string           | Variable         | N           | N             | N             |
| SubstantialReplyDate      | Substantial Reply Date              | null, date       | Variable         | N           | N             | N             |
| TargetReplyDate           | Target Reply Date                   | date, null       | Variable         | N           | N             | N             |
| ThreeTierReqt             | Three Tier Requirement              | string           | Variable         | N           | N             | N             |
| ViaSCS                    | Via SCS Flag                        | bool             | Variable         | N           | N             | N             |
| __v                       | Version field                       | int              | Variable         | Y           | N             | N             |
| _id                       | Document ID                         | objectId         | Variable         | Y           | Y             | N             |
| application               | Reference to application            | objectId         | Variable         | Y           | N             | Y             |
| assignedBS                | Assigned Building Surveyor          | objectId         | Variable         | N           | N             | Y             |
| assignedGR                | Assigned Geotechnical Engineer        | objectId         | Variable         | N           | N             | Y             |
| building_information      | Building Information Object         | object           | Variable         | N           | N             | N             |
| caseDescription           | Case Description Object             | object           | Variable         | N           | N             | N             |
| caseOfficerReceive        | Case Officer Receive User           | string           | Variable         | N           | N             | Y             |
| caseOfficerReply          | Case Officer Reply User             | string           | Variable         | N           | N             | Y             |
| createdAt                 | Creation Timestamp                  | date             | Variable         | Y           | N             | N             |
| deck_study                | Deck Study Object                   | object           | Variable         | Y           | N             | N             |
| documentChecklist         | Document Checklist Object           | object           | Variable         | N           | N             | N             |
| dv                        | DV Object                           | object           | Variable         | Y           | N             | N             |
| frc                       | FRC Object                          | object           | Variable         | Y           | N             | N             |
| misc                      | Miscellaneous Object                | object           | Variable         | Y           | N             | N             |
| moe                       | MOE Object                          | object           | Variable         | Y           | N             | N             |
| seniorCaseOfficerReceive  | Senior Case Officer Receive User    | string           | Variable         | N           | N             | Y             |
| seniorCaseOfficerReply    | Senior Case Officer Reply User      | string           | Variable         | N           | N             | Y             |
| site_inspection           | Site Inspection Object              | object           | Variable         | N           | N             | N             |
| structural_ccc_bs         | Structural CCC BS Object            | object           | Variable         | Y           | N             | N             |
| structural_schnlh         | Structural SCHNLH Object            | object           | Variable         | Y           | N             | N             |
| structural_schnlhkinds    | Structural SCHNLH Kinds Object      | object           | Variable         | Y           | N             | N             |
| team                      | Team assigned to case               | string           | Variable         | Y           | N             | N             |
| ubw                       | UBW Object                          | object           | Variable         | Y           | N             | N             |
| updatedAt                 | Update Timestamp                    | date             | Variable         | N           | N             | N             |

### 5.1.8. oauthtokens

> Entity Name: oauthtokens
>
> Description: Collection for storing OAuth tokens information.

| **Field Name**          | **Description**               | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-------------------------------|------------------|------------------|-------------|---------------|---------------|
| __v                   | Version field                 | int              | Variable         | Y           | N             | N             |
| _id                   | Document ID                   | objectId         | Variable         | Y           | Y             | N             |
| accessToken           | Access Token                  | string           | Variable         | Y           | N             | N             |
| accessTokenExpiresAt  | Access Token Expiration Date  | date             | Variable         | Y           | N             | N             |
| client                | Client Information            | object           | Variable         | Y           | N             | N             |
| refreshToken          | Refresh Token                 | string           | Variable         | Y           | N             | N             |
| refreshTokenExpiresAt | Refresh Token Expiration Date | date             | Variable         | Y           | N             | N             |
| user                  | Reference to User             | objectId         | Variable         | Y           | N             | Y             |

### 5.1.9. sysfilerefs

> Entity Name: sysfilerefs
>
> Description: Collection for storing system file references information.

| **Field Name**        | **Description**                 | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------|---------------------------------|------------------|------------------|-------------|---------------|---------------|
| __v                 | Version field                   | int              | Variable         | Y           | N             | N             |
| _id                 | Document ID                   | objectId         | Variable         | Y           | Y             | N             |
| createdDt           | Creation Date                   | date             | Variable         | Y           | N             | N             |
| createdName         | Creator Name                    | null, string     | Variable         | Y           | N             | N             |
| createdPost         | Creator Post                    | null, string     | Variable         | Y           | N             | N             |
| createdSection      | Creator Section                 | null, string     | Variable         | Y           | N             | N             |
| display             | Display Name                    | string           | Variable         | Y           | N             | N             |
| dvExceed            | DV Exceed Flag                  | null, string     | Variable         | Y           | N             | N             |
| dvStatusDt          | DV Status Date                  | null, date       | Variable         | Y           | N             | N             |
| frefPref            | File Reference Prefix           | string, null     | Variable         | Y           | N             | N             |
| frefSeq             | File Reference Sequence         | null, string     | Variable         | Y           | N             | N             |
| frefSuf             | File Reference Suffix           | null, string     | Variable         | Y           | N             | N             |
| frefYr              | File Reference Year             | null, string     | Variable         | Y           | N             | N             |
| lastModifiedDt      | Last Modified Date              | date             | Variable         | Y           | N             | N             |
| lastModifiedName    | Last Modifier Name              | null, string     | Variable         | Y           | N             | N             |
| lastModifiedPost    | Last Modifier Post              | null, string     | Variable         | Y           | N             | N             |
| lastModifiedSection | Last Modified Section           | null             | Variable         | Y           | N             | N             |
| sysFileRefId        | System File Reference ID        | string           | Variable         | Y           | N             | N             |

### 5.1.10. attachments

> Entity Name: attachments
>
> Description: Collection for storing attachment related information.

| **Field Name**      | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------|-----------------------------|------------------|------------------|-------------|---------------|---------------|
| __v               | Version field               | int              | Variable         | Y           | N             | N             |
| _id               | Document ID                 | objectId         | Variable         | Y           | Y             | N             |
| application       | Reference to application    | objectId         | Variable         | Y           | N             | Y             |
| createdAt         | Creation Timestamp          | date             | Variable         | Y           | N             | N             |
| efolio            | eFolio reference            | null, string     | Variable         | N           | N             | N             |
| file              | File Object/Reference       | object, string   | Variable         | N           | N             | N             |
| filePartNo        | File Part Number            | string           | Variable         | N           | N             | N             |
| receivedDate      | Received Date               | date             | Variable         | Y           | N             | N             |
| remarks           | Remarks                     | string           | Variable         | N           | N             | N             |
| subType           | Attachment Sub-Type         | string           | Variable         | N           | N             | N             |
| submissionCase    | Reference to submission case| objectId         | Variable         | Y           | N             | Y             |
| sysFileRefId      | System File Reference ID    | string           | Variable         | N           | N             | Y             |
| type              | Attachment Type             | string           | Variable         | Y           | N             | N             |
| updatedAt         | Update Timestamp            | date             | Variable         | N           | N             | N             |

### 5.1.11. users

> Entity Name: users
>
> Description: Collection for storing user information.

| **Field Name**         | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|----------------------|-----------------------------|------------------|------------------|-------------|---------------|---------------|
| __v                  | Version field               | int              | Variable         | Y           | N             | N             |
| _id                  | Document ID                 | objectId         | Variable         | Y           | Y             | N             |
| bdgis                | BDGIS User ID               | string           | Variable         | N           | N             | N             |
| begis                | BEGIS User ID               | string           | Variable         | N           | N             | N             |
| delegateTo           | Delegate To User            | string           | Variable         | N           | N             | Y             |
| department           | Department                  | string           | Variable         | Y           | N             | N             |
| email                | Email Address               | string           | Variable         | Y           | N             | N             |
| group                | User Group                  | string           | Variable         | N           | N             | N             |
| lastLoginAt          | Last Login Timestamp        | date             | Variable         | N           | N             | N             |
| letterLongPosition   | Letter Long Position (EN)   | string           | Variable         | N           | N             | N             |
| letterLongPositionCn | Letter Long Position (CN)   | string           | Variable         | N           | N             | N             |
| letterName           | Letter Name (EN)            | string           | Variable         | N           | N             | N             |
| letterNameCn         | Letter Name (CN)            | string           | Variable         | N           | N             | N             |
| letterPosition       | Letter Position (EN)        | string           | Variable         | N           | N             | N             |
| letterPositionCn     | Letter Position (CN)        | string           | Variable         | N           | N             | N             |
| lock                 | Account Lock Status         | bool             | Variable         | Y           | N             | N             |
| luPostName           | LU Post Name                | string           | Variable         | N           | N             | N             |
| name                 | User Name (EN)              | string           | Variable         | N           | N             | N             |
| notificationEmail    | Notification Email Address  | string           | Variable         | N           | N             | N             |
| osdpEmail            | OSDP Email Address          | string           | Variable         | N           | N             | N             |
| osdpLoginId          | OSDP Login ID               | string           | Variable         | Y           | N             | N             |
| password             | Password (Hashed)           | string           | Variable         | Y           | N             | N             |
| phoneNumber          | Phone Number                | string           | Variable         | N           | N             | N             |
| position             | Position (EN)               | string           | Variable         | N           | N             | N             |
| role                 | User Role                   | string           | Variable         | Y           | N             | N             |
| team                 | Team assigned to user       | string           | Variable         | N           | N             | N             |
| userType             | User Type                   | string           | Variable         | Y           | N             | N             |

### 5.1.12. adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: Collection for storing address block file references information.

| **Field Name**        | **Description**                 | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------|---------------------------------|------------------|------------------|-------------|---------------|---------------|
| __v                 | Version field                   | int              | Variable         | Y           | N             | N             |
| _id                 | Document ID                   | objectId         | Variable         | Y           | Y             | N             |
| adrBlkFileRefId     | Address Block File Reference ID | string           | Variable         | Y           | N             | N             |
| adrBlkId            | Address Block ID              | string           | Variable         | Y           | N             | N             |
| createdDt           | Creation Date                   | date             | Variable         | Y           | N             | N             |
| createdName         | Creator Name                    | null, string     | Variable         | Y           | N             | N             |
| createdPost         | Creator Post                    | string           | Variable         | Y           | N             | N             |
| createdSection      | Creator Section                 | null, string     | Variable         | Y           | N             | N             |
| lastModifiedDt      | Last Modified Date              | date             | Variable         | Y           | N             | N             |
| lastModifiedName    | Last Modifier Name              | null, string     | Variable         | Y           | N             | N             |
| lastModifiedPost    | Last Modifier Post              | string           | Variable         | Y           | N             | N             |
| lastModifiedSection | Last Modified Section           | string, null     | Variable         | Y           | N             | N             |
| sysFileRefId        | System File Reference ID        | string           | Variable         | Y           | N             | Y             |
```