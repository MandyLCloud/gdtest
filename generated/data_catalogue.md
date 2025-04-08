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

[**2. Database Overview 6**](#database-overview)

[**3. Definitions 7**](#definitions)

[**4. Data Entity Description 8**](#data-entity-description)

[**5. Equipment Configuration 9**](#equipment-configuration)

> [5.1 Objective 10](#objective)
>
> [5.1.1. tasks 10](#tasks)
>
> [5.1.2. eminutes 12](#eminutes)
>
> [5.1.3. submissions 14](#submissions)
>
> [5.1.4. applications 14](#applications)
>
> [5.1.5. notifications 17](#notifications)
>
> [5.1.6. bsblocks 18](#bsblocks)
>
> [5.1.7. cases 19](#cases)
>
> [5.1.8. oauthtokens 22](#oauthtokens)
>
> [5.1.9. sysfilerefs 23](#sysfilerefs)
>
> [5.1.10. attachments 25](#attachments)
>
> [5.1.11. users 27](#users)
>
> [5.1.12. adrblkfilerefs 29](#adrblkfilerefs)

# 1. Introduction

This document provides a description of data catalogue of the Combined
System Development Services of the LSCP of the Buildings Department. It outlines the database structure, entities, and data items within the system.

# 2. Database Overview

This section provides a high-level overview of the LSCP database, named `bd`, including statistics on its size, collections, and data volume.

**Database Statistics:**
- Database Name: `bd`
- Last Updated: 2025/3/4 ??10:10:39
- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1278983
- Total Data Size: 371.24 MB

**Collections Overview:**
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

# 3. Definitions

| Terms | Definitions          |
|-------|----------------------|
| BD    | Buildings Department |
| LSCP  | Licensing Self-Certification Portal |
| MB    | Megabytes            |
| KB    | Kilobytes            |
| TBC   | To Be Confirmed      |
|       |                      |
|       |                      |
|       |                      |
|       |                      |
|       |                      |
|       |                      |
|       |                      |

# 4. Data Entity Description

This section states all the entities (Collections) in the LSCP Database (`bd`).

-   Entities list for LSCP Data

| **Item** | **Entity Name** | **Entity Description** |
|----------|-----------------|------------------------|
| 1        | tasks           | Collection of tasks related data. |
| 2        | eminutes        | Collection of e-minutes (electronic minutes) data. |
| 3        | submissions     | Collection of submissions data. |
| 4        | applications    | Collection of applications data. |
| 5        | notifications   | Collection of notifications data. |
| 6        | bsblocks        | Collection of building services blocks data. |
| 7        | cases           | Collection of cases data. |
| 8        | oauthtokens     | Collection of OAuth tokens data for authentication. |
| 9        | sysfilerefs     | Collection of system file references data. |
| 10       | attachments     | Collection of attachments data. |
| 11       | users           | Collection of user data. |
| 12       | adrblkfilerefs  | Collection of address block file references data. |
|          |                 |                        |
|          |                 |                        |
|          |                 |                        |

# 5. Equipment Configuration

This section details the data items for each database collection in the physical design.

The explanation for columns is as follows:

> **Entity Name** - Name of database collection
>
> **Description** - Description of collection
>
> **Field Name** - Name of attribute within the collection
>
> **Field Format** - Type of the data item:
>
> BIGINT: The BIGINT data type is used to store larger integer values (e.g., from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807).
>
> NVARCHAR: The NVARCHAR data type stores character data in a variable-length field.
>
> DATETIME2: "DATETIME2" data type is used to store date and time values.
>
> UNIQUEIDENTIFIER: A column or local variable of unique identifier data type. Represents ObjectId.
>
> BIT: BIT data type is used to represent a Boolean value.
>
> OBJECT/ARRAY: Represents complex data structures, stored as NVARCHAR for simplicity in this catalogue.
>
> **Field Length** - Specify the max number of characters of string field (Not Specified in Source).
>
> **Mandatory** - Specify if the data item is mandatory. ?Y? if true (Not Specified in Source).
>
> **Primary Key** - Indicates if data item is part of the Primary Key (Inferred `_id` as Primary Key).
>
> **Foreign Key** - Indicates if data item is part of the Foreign Key (Not Specified in Source).

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
> Description: Collection storing information about tasks.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version field   | BIGINT/UNIQUEIDENTIFIER         |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| application   | Application ID  | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| createdAt     | Creation Timestamp | DATETIME2       |                  |               |                 |                 |
| status        | Task Status     | NVARCHAR        |                  |               |                 |                 |
| submissionCase| Submission Case ID | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| taskType      | Task Type       | NVARCHAR        |                  |               |                 |                 |
| team          | Team identifier | NVARCHAR        |                  |               |                 |                 |
| user          | User identifier | NVARCHAR/UNIQUEIDENTIFIER         |                  |               |                 | Y               |

### 5.1.2. eminutes

> Entity Name: eminutes
>
> Description: Collection storing information about electronic minutes.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| comment       | Comment         | NVARCHAR        |                  |               |                 |                 |
| content       | Content         | NVARCHAR        |                  |               |                 |                 |
| createdAt     | Creation Timestamp | DATETIME2       |                  |               |                 |                 |
| efolio        | Efolio identifier | NVARCHAR        |                  |               |                 |                 |
| eminuteId     | E-minute ID     | NVARCHAR        |                  |               |                 |                 |
| from          | Sender identifier | UNIQUEIDENTIFIER/NVARCHAR         |                  |               |                 | Y               |
| status        | Status          | NVARCHAR        |                  |               |                 |                 |
| subject       | Subject         | NVARCHAR        |                  |               |                 |                 |
| submissionCase| Submission Case ID | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| sysFileRefId  | System File Reference ID | NVARCHAR        |                  |               |                 |                 |
| to            | Recipient identifier | UNIQUEIDENTIFIER/NVARCHAR         |                  |               |                 | Y               |

### 5.1.3. submissions

> Entity Name: submissions
>
> Description: Collection storing information about submissions. Currently empty.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* | *(No Fields Defined)* |

### 5.1.4. applications

> Entity Name: applications
>
> Description: Collection storing information about applications.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| APP13         | APP13 data      | OBJECT/ARRAY        |                  |               |                 |                 |
| AddressOfPremiseCN | Address of Premise (CN) | NVARCHAR        |                  |               |                 |                 |
| AddressOfPremiseCNFloor | Address of Premise Floor (CN) | NVARCHAR        |                  |               |                 |
| AddressOfPremiseCNUnit | Address of Premise Unit (CN) | NVARCHAR        |                  |               |                 |
| AddressOfPremiseEN | Address of Premise (EN) | NVARCHAR        |                  |               |                 |                 |
| AddressOfPremiseENFloor | Address of Premise Floor (EN) | NVARCHAR        |                  |               |                 |
| AddressOfPremiseENUnit | Address of Premise Unit (EN) | NVARCHAR        |                  |               |                 |
| AgeOfStudent  | Age of Student  | NVARCHAR        |                  |               |                 |                 |
| ApplicantAddress | Applicant Address | NVARCHAR        |                  |               |                 |                 |
| ApplicantEmail | Applicant Email | NVARCHAR        |                  |               |                 |                 |
| ApplicantFax  | Applicant Fax   | NVARCHAR        |                  |               |                 |                 |
| ApplicantMobile | Applicant Mobile | NVARCHAR        |                  |               |                 |                 |
| ApplicantName | Applicant Name  | NVARCHAR        |                  |               |                 |                 |
| ApplicantNameCN | Applicant Name (CN) | NVARCHAR        |                  |               |                 |                 |
| ApplicantNameEN | Applicant Name (EN) | NVARCHAR        |                  |               |                 |                 |
| ApplicantTel  | Applicant Tel   | NVARCHAR        |                  |               |                 |                 |
| ApplicationNo | Application Number | NVARCHAR        |                  |               |                 |                 |
| ApplicationType | Application Type | NVARCHAR        |                  |               |                 |                 |
| Area          | Area            | NVARCHAR        |                  |               |                 |                 |
| BlockID       | Block ID        | NVARCHAR        |                  |               |                 |                 |
| ContactPerson | Contact Person  | NVARCHAR        |                  |               |                 |                 |
| ContactPersonCN | Contact Person (CN) | NVARCHAR        |                  |               |                 |                 |
| ContactPersonEN | Contact Person (EN) | NVARCHAR        |                  |               |                 |                 |
| ContactPersonEmail | Contact Person Email | NVARCHAR        |                  |               |                 |                 |
| ContactPersonTel | Contact Person Tel | NVARCHAR        |                  |               |                 |                 |
| DescriptionOfSchool | Description of School | NVARCHAR        |                  |               |                 |                 |
| District      | District        | NVARCHAR        |                  |               |                 |                 |
| EstimatedNoOfStudent | Estimated Number of Students | BIGINT/NVARCHAR        |                  |               |                 |
| FileReference | File Reference  | NVARCHAR        |                  |               |                 |                 |
| NameOfSchoolCN | Name of School (CN) | NVARCHAR        |                  |               |                 |                 |
| NameOfSchoolEN | Name of School (EN) | NVARCHAR        |                  |               |                 |                 |
| Region        | Region          | NVARCHAR        |                  |               |                 |                 |
| RelatedPremise | Related Premise | NVARCHAR        |                  |               |                 |                 |
| RelatedPremises | Related Premises | ARRAY           |                  |               |                 |                 |
| SelfCertification | Self Certification Data | OBJECT/NVARCHAR        |                  |               |                 |
| StructuralCalculation | Structural Calculation Data | OBJECT        |                  |               |                 |
| SubmissionType | Submission Type | NVARCHAR        |                  |               |                 |                 |
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| address       | Address Data    | OBJECT          |                  |               |                 |                 |
| assignedBS    | Assigned BS ID  | UNIQUEIDENTIFIER/NVARCHAR         |                  |               |                 | Y               |
| assignedGR    | Assigned GR ID  | UNIQUEIDENTIFIER/NVARCHAR         |                  |               |                 | Y               |
| assignedSBS   | Assigned SBS ID | NVARCHAR/NVARCHAR         |                  |               |                 |                 |
| createdAt     | Creation Timestamp | DATETIME2       |                  |               |                 |                 |
| updatedAt     | Update Timestamp | DATETIME2       |                  |               |                 |                 |

### 5.1.5. notifications

> Entity Name: notifications
>
> Description: Collection storing information about notifications.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| createdAt     | Creation Timestamp | DATETIME2       |                  |               |                 |                 |
| eminute       | E-minute ID     | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| notificationType | Notification Type | NVARCHAR        |                  |               |                 |                 |
| requireSendEmail | Require Send Email | BIT             |                  |               |                 |                 |
| task          | Task ID         | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| user          | User identifier | NVARCHAR        |                  |               |                 | Y               |

### 5.1.6. bsblocks

> Entity Name: bsblocks
>
> Description: Collection storing information about building services blocks.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| bdgis         | BDGIS identifier | NVARCHAR        |                  |               |                 |                 |
| blockId       | Block ID        | NVARCHAR        |                  |               |                 |                 |

### 5.1.7. cases

> Entity Name: cases
>
> Description: Collection storing information about cases.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| ActualReplyDate | Actual Reply Date | DATETIME2/NVARCHAR       |                  |               |                 |                 |
| Area          | Area            | NVARCHAR        |                  |               |                 |                 |
| AuditResult   | Audit Result    | NVARCHAR        |                  |               |                 |                 |
| CaseOfficer   | Case Officer    | NVARCHAR        |                  |               |                 |                 |
| Category      | Category        | NVARCHAR        |                  |               |                 |                 |
| District      | District        | NVARCHAR        |                  |               |                 |                 |
| FileReference | File Reference  | NVARCHAR        |                  |               |                 |                 |
| LAFileReference | LA File Reference | OBJECT          |                  |               |                 |                 |
| Nature        | Nature          | NVARCHAR        |                  |               |                 |                 |
| ObjectiontoLR | Objection to LR | NVARCHAR        |                  |               |                 |                 |
| ReceivedDate  | Received Date   | DATETIME2/NVARCHAR       |                  |               |                 |                 |
| Referrer      | Referrer Data   | OBJECT          |                  |               |                 |                 |
| Region        | Region          | NVARCHAR        |                  |               |                 |                 |
| Remarks       | Remarks         | NVARCHAR        |                  |               |                 |                 |
| Reminders     | Reminders       | ARRAY           |                  |               |                 |                 |
| SubmissionType | Submission Type | NVARCHAR        |                  |               |                 |                 |
| SubstantialReplyDate | Substantial Reply Date | DATETIME2/NVARCHAR       |                  |               |                 |
| TargetReplyDate | Target Reply Date | DATETIME2/NVARCHAR       |                  |               |                 |                 |
| ThreeTierReqt | Three Tier Requirement | NVARCHAR        |                  |               |                 |                 |
| ViaSCS        | Via SCS         | BIT             |                  |               |                 |                 |
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| application   | Application ID  | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| assignedBS    | Assigned BS ID  | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| assignedGR    | Assigned GR ID  | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| building_information | Building Information | OBJECT          |                  |               |                 |                 |
| caseDescription | Case Description | OBJECT          |                  |               |                 |                 |
| caseOfficerReceive | Case Officer Receive | NVARCHAR        |                  |               |                 |                 |
| caseOfficerReply | Case Officer Reply | NVARCHAR        |                  |               |                 |                 |
| createdAt     | Creation Timestamp | DATETIME2       |                  |               |                 |                 |
| deck_study    | Deck Study Data | OBJECT          |                  |               |                 |                 |
| documentChecklist | Document Checklist | OBJECT          |                  |               |                 |                 |
| dv            | DV Data         | OBJECT          |                  |               |                 |                 |
| frc           | FRC Data        | OBJECT          |                  |               |                 |                 |
| misc          | Miscellaneous Data | OBJECT          |                  |               |                 |                 |
| moe           | MOE Data        | OBJECT          |                  |               |                 |                 |
| seniorCaseOfficerReceive | Senior Case Officer Receive | NVARCHAR        |                  |               |                 |                 |
| seniorCaseOfficerReply | Senior Case Officer Reply | NVARCHAR        |                  |               |                 |                 |
| site_inspection | Site Inspection Data | OBJECT          |                  |               |                 |                 |
| structural_ccc_bs | Structural CCC BS Data | OBJECT          |                  |               |                 |                 |
| structural_schnlh | Structural SCHNLH Data | OBJECT          |                  |               |                 |                 |
| structural_schnlhkinds | Structural SCHNLH Kinds Data | OBJECT          |                  |               |                 |                 |
| team          | Team identifier | NVARCHAR        |                  |               |                 |                 |
| ubw           | UBW Data        | OBJECT          |                  |               |                 |                 |
| updatedAt     | Update Timestamp | DATETIME2       |                  |               |                 |                 |

### 5.1.8. oauthtokens

> Entity Name: oauthtokens
>
> Description: Collection storing information about OAuth tokens.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| accessToken   | Access Token    | NVARCHAR        |                  |               |                 |                 |
| accessTokenExpiresAt | Access Token Expiry | DATETIME2       |                  |               |                 |                 |
| client        | Client Data     | OBJECT          |                  |               |                 |                 |
| refreshToken  | Refresh Token   | NVARCHAR        |                  |               |                 |                 |
| refreshTokenExpiresAt | Refresh Token Expiry | DATETIME2       |                  |               |                 |                 |
| user          | User ID         | UNIQUEIDENTIFIER         |                  |               |                 | Y               |

### 5.1.9. sysfilerefs

> Entity Name: sysfilerefs
>
> Description: Collection storing system file references.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| createdDt     | Creation Date   | DATETIME2       |                  |               |                 |                 |
| createdName   | Created By Name | NVARCHAR        |                  |               |                 |                 |
| createdPost   | Created By Post | NVARCHAR        |                  |               |                 |                 |
| createdSection | Created By Section | NVARCHAR        |                  |               |                 |                 |
| display       | Display Value   | NVARCHAR        |                  |               |                 |                 |
| dvExceed      | DV Exceed Value | NVARCHAR        |                  |               |                 |                 |
| dvStatusDt    | DV Status Date  | DATETIME2/NVARCHAR       |                  |               |                 |                 |
| frefPref      | File Reference Prefix | NVARCHAR        |                  |               |                 |                 |
| frefSeq       | File Reference Sequence | NVARCHAR        |                  |               |                 |                 |
| frefSuf       | File Reference Suffix | NVARCHAR        |                  |               |                 |                 |
| frefYr        | File Reference Year | NVARCHAR        |                  |               |                 |                 |
| lastModifiedDt | Last Modified Date | DATETIME2       |                  |               |                 |                 |
| lastModifiedName | Last Modified By Name | NVARCHAR        |                  |               |                 |                 |
| lastModifiedPost | Last Modified By Post | NVARCHAR        |                  |               |                 |                 |
| lastModifiedSection | Last Modified By Section | NVARCHAR        |                  |               |                 |                 |
| sysFileRefId  | System File Reference ID | NVARCHAR        |                  |               |                 |                 |

### 5.1.10. attachments

> Entity Name: attachments
>
> Description: Collection storing information about attachments.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| application   | Application ID  | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| createdAt     | Creation Timestamp | DATETIME2       |                  |               |                 |                 |
| efolio        | Efolio identifier | NVARCHAR        |                  |               |                 |                 |
| file          | File Data       | OBJECT/NVARCHAR        |                  |               |                 |                 |
| filePartNo    | File Part Number | NVARCHAR        |                  |               |                 |                 |
| receivedDate  | Received Date   | DATETIME2       |                  |               |                 |                 |
| remarks       | Remarks         | NVARCHAR        |                  |               |                 |                 |
| subType       | Sub Type        | NVARCHAR        |                  |               |                 |                 |
| submissionCase| Submission Case ID | UNIQUEIDENTIFIER         |                  |               |                 | Y               |
| sysFileRefId  | System File Reference ID | NVARCHAR        |                  |               |                 |                 |
| type          | Attachment Type | NVARCHAR        |                  |               |                 |                 |
| updatedAt     | Update Timestamp | DATETIME2       |                  |               |                 |                 |

### 5.1.11. users

> Entity Name: users
>
> Description: Collection storing user information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| bdgis         | BDGIS identifier | NVARCHAR        |                  |               |                 |                 |
| begis         | BEGIS identifier | NVARCHAR        |                  |               |                 |                 |
| delegateTo    | Delegate To User | NVARCHAR        |                  |               |                 |                 |
| department    | Department      | NVARCHAR        |                  |               |                 |                 |
| email         | Email Address   | NVARCHAR        |                  |               |                 |                 |
| group         | Group identifier | NVARCHAR        |                  |               |                 |                 |
| lastLoginAt   | Last Login Timestamp | DATETIME2       |                  |               |                 |                 |
| letterLongPosition | Letter Long Position | NVARCHAR        |                  |               |                 |                 |
| letterLongPositionCn | Letter Long Position (CN) | NVARCHAR        |                  |               |                 |                 |
| letterName    | Letter Name     | NVARCHAR        |                  |               |                 |                 |
| letterNameCn  | Letter Name (CN) | NVARCHAR        |                  |               |                 |                 |
| letterPosition | Letter Position | NVARCHAR        |                  |               |                 |                 |
| letterPositionCn | Letter Position (CN) | NVARCHAR        |                  |               |                 |                 |
| lock          | Account Lock Status | BIT             |                  |               |                 |                 |
| luPostName    | LU Post Name    | NVARCHAR        |                  |               |                 |                 |
| name          | User Name       | NVARCHAR        |                  |               |                 |                 |
| notificationEmail | Notification Email | NVARCHAR        |                  |               |                 |                 |
| osdpEmail     | OSDP Email      | NVARCHAR        |                  |               |                 |                 |
| osdpLoginId   | OSDP Login ID   | NVARCHAR        |                  |               |                 |                 |
| password      | Password Hash   | NVARCHAR        |                  |               |                 |                 |
| phoneNumber   | Phone Number    | NVARCHAR        |                  |               |                 |                 |
| position      | Position        | NVARCHAR        |                  |               |                 |                 |
| role          | User Role       | NVARCHAR        |                  |               |                 |                 |
| team          | Team identifier | NVARCHAR        |                  |               |                 |                 |
| userType      | User Type       | NVARCHAR        |                  |               |                 |                 |

### 5.1.12. adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: Collection storing address block file references.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version field   | BIGINT          |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER         |                  |               | Y               |                 |
| adrBlkFileRefId | Address Block File Reference ID | NVARCHAR        |                  |               |                 |                 |
| adrBlkId      | Address Block ID | NVARCHAR        |                  |               |                 |                 |
| createdDt     | Creation Date   | DATETIME2       |                  |               |                 |                 |
| createdName   | Created By Name | NVARCHAR        |                  |               |                 |                 |
| createdPost   | Created By Post | NVARCHAR        |                  |               |                 |                 |
| createdSection | Created By Section | NVARCHAR        |                  |               |                 |                 |
| lastModifiedDt | Last Modified Date | DATETIME2       |                  |               |                 |                 |
| lastModifiedName | Last Modified By Name | NVARCHAR        |                  |               |                 |                 |
| lastModifiedPost | Last Modified By Post | NVARCHAR        |                  |               |                 |                 |
| lastModifiedSection | Last Modified By Section | NVARCHAR        |                  |               |                 |                 |
| sysFileRefId  | System File Reference ID | NVARCHAR        |                  |               |                 |                 |
