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

[**3. Data Entity Description 7**](#data-entity-description)

[**4. Equipment Configuration 8**](#equipment-configuration)

> [4.1 Objective 9](#objective)
>
> [4.1.1. tasks 9](#tasks)
>
> [4.1.2. eminutes 10](#eminutes)
>
> [4.1.3. submissions 11](#submissions)
>
> [4.1.4. applications 12](#applications)
>
> [4.1.5. notifications 13](#notifications)
>
> [4.1.6. bsblocks 14](#bsblocks)
>
> [4.1.7. cases 15](#cases)
>
> [4.1.8. oauthtokens 16](#oauthtokens)
>
> [4.1.9. sysfilerefs 17](#sysfilerefs)
>
> [4.1.10. attachments 18](#attachments)
>
> [4.1.11. users 19](#users)
>
> [4.1.12. adrblkfilerefs 20](#adrblkfilerefs)

# 1. Introduction

This document provides a description of data catalogue of the Combined
System Development Services of the LSCP of the Buildings Department.

# 2. Definitions

| Terms | Definitions          |
|-------|----------------------|
| BD    | Buildings Department |
| LSCP  | Licensing Self-Certification Portal |
| tasks | Collection for storing tasks related information |
| eminutes | Collection for storing e-minutes information |
| submissions | Collection for storing submissions information |
| applications | Collection for storing applications information |
| notifications | Collection for storing notifications information |
| bsblocks | Collection for storing building blocks information |
| cases | Collection for storing cases information |
| oauthtokens | Collection for storing OAuth tokens information |
| sysfilerefs | Collection for storing system file references information |
| attachments | Collection for storing attachments information |
| users | Collection for storing users information |
| adrblkfilerefs | Collection for storing address block file references information |
| ObjectId | MongoDB's 12-byte unique identifier |
| String | Textual data |
| Date | Date and time information |
| Int | Integer number |
| Bool | Boolean value (true/false) |
| Object | Complex data structure, similar to JSON object |
| Array | Ordered list of values |
| Null | Absence of a value |

# 3. Data Entity Description

This section states all the entities in the LSCP Database.

The following section describes how the LSCP entities can be mapped onto
physical data design.

-   Entities list for LSCP Data

| **Item** | **Entity Name** | **Entity Description** |
|----------|-----------------|------------------------|
| 1        | tasks           | Stores tasks related to the system. |
| 2        | eminutes        | Stores electronic minutes of meetings or records. |
| 3        | submissions     | Manages submissions within the system. |
| 4        | applications    | Handles application forms and related data. |
| 5        | notifications   | Stores system notifications for users. |
| 6        | bsblocks        | Contains information about building blocks. |
| 7        | cases           | Manages cases or incidents within the system. |
| 8        | oauthtokens     | Stores OAuth tokens for authentication. |
| 9        | sysfilerefs     | References to system files. |
| 10       | attachments     | Manages attached files to various entities. |
| 11       | users           | Stores user account information. |
| 12       | adrblkfilerefs  | References to address block files. |

# 4. Equipment Configuration

This section is to package all of the details related to data items in
physical including Data Item, description, format and storage length so
as to ensure that data item details are maintained centrally.

The following tables describe the data items for each database table in
the physical design. The explanation for columns is as follows.

Database-level validation is not utilized in MS SQL. Instead, all
validations have been implemented on the server side within the code
behind.

> **Entity Name** - Name of database object
>
> **Description** - Description of entity
>
> **Field Name** - Name of object attributes
>
> **Field Format** - Type of the data item:
>
> BIGINT:
>
> The BIGINT data type is used to store larger integer value. e.g. from
> -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.
>
> NVARCHAR:
>
> The NVARCHAR data type stores character data in a variable-length
> field.
>
> DATETIME2:
>
> "DATETIME2" data type is used to store date and time values.
>
> UNIQUEIDENTIFIER:
>
> A column or local variable of unique identifier data type can be
> initialized to a value.
>
> BIT:
>
> BIT data type is used to represent a Boolean value.
>
> **Field Length** - Specify the max number of characters of string
> field
>
> **Mandatory** - Specify if the data item is mandatory. ?Y? if true.
>
> **Primary Key** - Indicates if data item is part of the Primary Key
>
> **Foreign Key** - Indicates if data item is part of the Foreign Key

## 

## 4.1 Objective

> Name Space: LSCP
>
> Description: LSCP Data Storage
>
> Storage Location: TBC
>
> File Name: TBC

### 4.1.1. tasks

> Entity Name: tasks
>
> Description: Stores tasks related to the system.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v            | Version field    | BIGINT/UNIQUEIDENTIFIER |                  | N             | N               | N               |
| _id            | Unique ID        | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| application    | Application ID   | UNIQUEIDENTIFIER  |                  | N             | N               | Y               |
| createdAt      | Creation Timestamp | DATETIME2       |                  | Y             | N               | N               |
| status         | Task Status      | NVARCHAR        | Variable        | Y             | N               | N               |
| submissionCase | Submission Case ID | UNIQUEIDENTIFIER  |                  | N             | N               | Y               |
| taskType       | Type of Task     | NVARCHAR        | Variable        | Y             | N               | N               |
| team           | Team ID          | NVARCHAR        | Variable        | N             | N               | N               |
| user           | User ID          | NVARCHAR/UNIQUEIDENTIFIER | Variable        | N             | N               | Y               |

### 4.1.2. eminutes

> Entity Name: eminutes
>
> Description: Stores electronic minutes of meetings or records.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v            | Version field    | BIGINT          |                  | N             | N               | N               |
| _id            | Unique ID        | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| comment        | Comment          | NVARCHAR        | Variable        | N             | N               | N               |
| content        | Content          | NVARCHAR        | Variable        | Y             | N               | N               |
| createdAt      | Creation Timestamp | DATETIME2       |                  | Y             | N               | N               |
| efolio         | E-folio ID       | NVARCHAR        | Variable        | N             | N               | N               |
| eminuteId      | E-minute ID      | NVARCHAR        | Variable        | Y             | N               | N               |
| from           | From User/ID     | UNIQUEIDENTIFIER/NVARCHAR | Variable        | Y             | N               | Y               |
| status         | Status           | NVARCHAR        | Variable        | Y             | N               | N               |
| subject        | Subject          | NVARCHAR        | Variable        | Y             | N               | N               |
| submissionCase | Submission Case ID | UNIQUEIDENTIFIER  |                  | Y             | N               | Y               |
| sysFileRefId   | System File Ref ID | NVARCHAR        | Variable        | N             | N               | N               |
| to             | To User/ID       | UNIQUEIDENTIFIER/NVARCHAR | Variable        | N             | N               | Y               |

### 4.1.3. submissions

> Entity Name: submissions
>
> Description: Manages submissions within the system.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| *No fields defined yet as collection is empty* |                 |                  |                  |               |                 |                 |

### 4.1.4. applications

> Entity Name: applications
>
> Description: Handles application forms and related data.

| **Field Name**         | **Description**          | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|----------------------|--------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| APP13                  | APP13 Data               | Object/Array      |                  | N             | N               | N               |
| AddressOfPremiseCN     | Address of Premise (CN)  | NVARCHAR        | Variable        | N             | N               | N               |
| AddressOfPremiseCNFloor| Address of Premise Floor (CN) | NVARCHAR        | Variable        | N             | N               | N               |
| AddressOfPremiseCNUnit | Address of Premise Unit (CN)  | NVARCHAR        | Variable        | N             | N               | N               |
| AddressOfPremiseEN     | Address of Premise (EN)  | NVARCHAR        | Variable        | N             | N               | N               |
| AddressOfPremiseENFloor| Address of Premise Floor (EN) | NVARCHAR        | Variable        | N             | N               | N               |
| AddressOfPremiseENUnit | Address of Premise Unit (EN)  | NVARCHAR        | Variable        | N             | N               | N               |
| AgeOfStudent           | Age of Student           | NVARCHAR        | Variable        | N             | N               | N               |
| ApplicantAddress       | Applicant Address        | NVARCHAR        | Variable        | N             | N               | N               |
| ApplicantEmail         | Applicant Email          | NVARCHAR        | Variable        | N             | N               | N               |
| ApplicantFax           | Applicant Fax            | NVARCHAR        | Variable        | N             | N               | N               |
| ApplicantMobile        | Applicant Mobile         | NVARCHAR        | Variable        | N             | N               | N               |
| ApplicantName          | Applicant Name           | NVARCHAR        | Variable        | N             | N               | N               |
| ApplicantNameCN        | Applicant Name (CN)      | NVARCHAR        | Variable        | N             | N               | N               |
| ApplicantNameEN        | Applicant Name (EN)      | NVARCHAR        | Variable        | N             | N               | N               |
| ApplicantTel           | Applicant Telephone      | NVARCHAR        | Variable        | N             | N               | N               |
| ApplicationNo          | Application Number       | NVARCHAR        | Variable        | Y             | N               | N               |
| ApplicationType        | Application Type         | NVARCHAR        | Variable        | Y             | N               | N               |
| Area                   | Area                     | NVARCHAR        | Variable        | N             | N               | N               |
| BlockID                | Block ID                 | NVARCHAR        | Variable        | N             | N               | N               |
| ContactPerson          | Contact Person           | NVARCHAR        | Variable        | N             | N               | N               |
| ContactPersonCN        | Contact Person (CN)      | NVARCHAR        | Variable        | N             | N               | N               |
| ContactPersonEN        | Contact Person (EN)      | NVARCHAR        | Variable        | N             | N               | N               |
| ContactPersonEmail     | Contact Person Email     | NVARCHAR        | Variable        | N             | N               | N               |
| ContactPersonTel       | Contact Person Tel       | NVARCHAR        | Variable        | N             | N               | N               |
| DescriptionOfSchool    | Description of School    | NVARCHAR        | Variable        | N             | N               | N               |
| District               | District                 | NVARCHAR        | Variable        | N             | N               | N               |
| EstimatedNoOfStudent   | Estimated No. of Student | BIGINT          |                  | N             | N               | N               |
| FileReference          | File Reference           | NVARCHAR        | Variable        | N             | N               | N               |
| NameOfSchoolCN         | Name of School (CN)      | NVARCHAR        | Variable        | N             | N               | N               |
| NameOfSchoolEN         | Name of School (EN)      | NVARCHAR        | Variable        | N             | N               | N               |
| Region                 | Region                   | NVARCHAR        | Variable        | N             | N               | N               |
| RelatedPremise         | Related Premise          | NVARCHAR        | Variable        | N             | N               | N               |
| RelatedPremises        | Related Premises         | Array           |                  | Y             | N               | N               |
| SelfCertification     | Self Certification Data  | Object          |                  | N             | N               | N               |
| StructuralCalculation  | Structural Calculation Data | Object          |                  | N             | N               | N               |
| SubmissionType         | Submission Type          | NVARCHAR        | Variable        | Y             | N               | N               |
| __v                    | Version field            | BIGINT          |                  | N             | N               | N               |
| _id                    | Unique ID                | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| address                | Address Data             | Object          |                  | N             | N               | N               |
| assignedBS             | Assigned BS User ID      | UNIQUEIDENTIFIER/NVARCHAR | Variable        | N             | N               | Y               |
| assignedGR             | Assigned GR User ID      | UNIQUEIDENTIFIER  |                  | N             | N               | Y               |
| assignedSBS            | Assigned SBS User ID     | NVARCHAR        | Variable        | N             | N               | N               |
| createdAt              | Creation Timestamp       | DATETIME2       |                  | Y             | N               | N               |
| updatedAt              | Update Timestamp         | DATETIME2       |                  | N             | N               | N               |

### 4.1.5. notifications

> Entity Name: notifications
>
> Description: Stores system notifications for users.

| **Field Name**     | **Description**        | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|------------------|------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v              | Version field          | BIGINT          |                  | N             | N               | N               |
| _id              | Unique ID              | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| createdAt        | Creation Timestamp     | DATETIME2       |                  | Y             | N               | N               |
| eminute          | E-minute ID            | UNIQUEIDENTIFIER  |                  | N             | N               | Y               |
| notificationType | Notification Type      | NVARCHAR        | Variable        | Y             | N               | N               |
| requireSendEmail | Require Send Email Flag| BIT             |                  | Y             | N               | N               |
| task             | Task ID                | UNIQUEIDENTIFIER  |                  | N             | N               | Y               |
| user             | User ID                | NVARCHAR        | Variable        | Y             | N               | N               |

### 4.1.6. bsblocks

> Entity Name: bsblocks
>
> Description: Contains information about building blocks.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v            | Version field    | BIGINT          |                  | N             | N               | N               |
| _id            | Unique ID        | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| bdgis          | BDGIS ID         | NVARCHAR        | Variable        | Y             | N               | N               |
| blockId        | Block ID         | NVARCHAR        | Variable        | Y             | N               | N               |

### 4.1.7. cases

> Entity Name: cases
>
> Description: Manages cases or incidents within the system.

| **Field Name**             | **Description**              | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------------|------------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| ActualReplyDate          | Actual Reply Date            | DATETIME2       |                  | N             | N               | N               |
| Area                     | Area                         | NVARCHAR        | Variable        | N             | N               | N               |
| AuditResult              | Audit Result                 | NVARCHAR        | Variable        | N             | N               | N               |
| CaseOfficer              | Case Officer                 | NVARCHAR        | Variable        | N             | N               | N               |
| Category                 | Category                     | NVARCHAR        | Variable        | Y             | N               | N               |
| District                 | District                     | NVARCHAR        | Variable        | N             | N               | N               |
| FileReference            | File Reference               | NVARCHAR        | Variable        | N             | N               | N               |
| LAFileReference          | LA File Reference            | Object          |                  | N             | N               | N               |
| Nature                   | Nature                       | NVARCHAR        | Variable        | N             | N               | N               |
| ObjectiontoLR            | Objection to LR              | NVARCHAR        | Variable        | N             | N               | N               |
| ReceivedDate             | Received Date                | DATETIME2       |                  | N             | N               | N               |
| Referrer                 | Referrer                     | Object          |                  | N             | N               | N               |
| Region                   | Region                       | NVARCHAR        | Variable        | N             | N               | N               |
| Remarks                  | Remarks                      | NVARCHAR        | Variable        | N             | N               | N               |
| Reminders                | Reminders                    | Array           |                  | N             | N               | N               |
| SubmissionType           | Submission Type              | NVARCHAR        | Variable        | N             | N               | N               |
| SubstantialReplyDate     | Substantial Reply Date       | DATETIME2       |                  | N             | N               | N               |
| TargetReplyDate          | Target Reply Date            | DATETIME2       |                  | N             | N               | N               |
| ThreeTierReqt            | Three Tier Requirement       | NVARCHAR        | Variable        | N             | N               | N               |
| ViaSCS                   | Via SCS Flag                 | BIT             |                  | Y             | N               | N               |
| __v                      | Version field                | BIGINT          |                  | N             | N               | N               |
| _id                      | Unique ID                    | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| application              | Application ID               | UNIQUEIDENTIFIER  |                  | Y             | N               | Y               |
| assignedBS               | Assigned BS User ID          | UNIQUEIDENTIFIER  |                  | N             | N               | Y               |
| assignedGR               | Assigned GR User ID          | UNIQUEIDENTIFIER  |                  | N             | N               | Y               |
| building_information     | Building Information Data    | Object          |                  | N             | N               | N               |
| caseDescription          | Case Description Data        | Object          |                  | N             | N               | N               |
| caseOfficerReceive       | Case Officer Receive User ID | NVARCHAR        | Variable        | N             | N               | N               |
| caseOfficerReply         | Case Officer Reply User ID   | NVARCHAR        | Variable        | N             | N               | N               |
| createdAt                | Creation Timestamp           | DATETIME2       |                  | Y             | N               | N               |
| deck_study               | Deck Study Data              | Object          |                  | Y             | N               | N               |
| documentChecklist        | Document Checklist Data      | Object          |                  | N             | N               | N               |
| dv                       | DV Data                      | Object          |                  | Y             | N               | N               |
| frc                      | FRC Data                     | Object          |                  | Y             | N               | N               |
| misc                     | Miscellaneous Data           | Object          |                  | Y             | N               | N               |
| moe                      | MOE Data                     | Object          |                  | Y             | N               | N               |
| seniorCaseOfficerReceive | Senior Case Officer Receive User ID | NVARCHAR        | Variable        | N             | N               | N               |
| seniorCaseOfficerReply   | Senior Case Officer Reply User ID | NVARCHAR        | Variable        | N             | N               | N               |
| site_inspection          | Site Inspection Data         | Object          |                  | N             | N               | N               |
| structural_ccc_bs        | Structural CCC BS Data       | Object          |                  | Y             | N               | N               |
| structural_schnlh        | Structural SCHNLH Data       | Object          |                  | Y             | N               | N               |
| structural_schnlhkinds   | Structural SCHNLHKINDS Data  | Object          |                  | Y             | N               | N               |
| team                     | Team ID                      | NVARCHAR        | Variable        | Y             | N               | N               |
| ubw                      | UBW Data                     | Object          |                  | Y             | N               | N               |
| updatedAt                | Update Timestamp             | DATETIME2       |                  | N             | N               | N               |

### 4.1.8. oauthtokens

> Entity Name: oauthtokens
>
> Description: Stores OAuth tokens for authentication.

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-----------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                   | Version field               | BIGINT          |                  | N             | N               | N               |
| _id                   | Unique ID                   | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| accessToken           | Access Token                | NVARCHAR        | Variable        | Y             | N               | N               |
| accessTokenExpiresAt  | Access Token Expiry Timestamp | DATETIME2       |                  | Y             | N               | N               |
| client                | Client Data                 | Object          |                  | Y             | N               | N               |
| refreshToken          | Refresh Token               | NVARCHAR        | Variable        | Y             | N               | N               |
| refreshTokenExpiresAt | Refresh Token Expiry Timestamp| DATETIME2       |                  | Y             | N               | N               |
| user                  | User ID                     | UNIQUEIDENTIFIER  |                  | Y             | N               | Y               |

### 4.1.9. sysfilerefs

> Entity Name: sysfilerefs
>
> Description: References to system files.

| **Field Name**        | **Description**           | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------|---------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                 | Version field             | BIGINT          |                  | N             | N               | N               |
| _id                 | Unique ID                 | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| createdDt           | Creation Timestamp        | DATETIME2       |                  | Y             | N               | N               |
| createdName         | Created By Name           | NVARCHAR        | Variable        | N             | N               | N               |
| createdPost         | Created By Post           | NVARCHAR        | Variable        | N             | N               | N               |
| createdSection      | Created By Section        | NVARCHAR        | Variable        | N             | N               | N               |
| display             | Display Name              | NVARCHAR        | Variable        | Y             | N               | N               |
| dvExceed            | DV Exceed Status          | NVARCHAR        | Variable        | N             | N               | N               |
| dvStatusDt          | DV Status Timestamp       | DATETIME2       |                  | N             | N               | N               |
| frefPref            | File Reference Prefix     | NVARCHAR        | Variable        | N             | N               | N               |
| frefSeq             | File Reference Sequence   | NVARCHAR        | Variable        | N             | N               | N               |
| frefSuf             | File Reference Suffix     | NVARCHAR        | Variable        | N             | N               | N               |
| frefYr              | File Reference Year       | NVARCHAR        | Variable        | N             | N               | N               |
| lastModifiedDt      | Last Modified Timestamp   | DATETIME2       |                  | Y             | N               | N               |
| lastModifiedName    | Last Modified By Name     | NVARCHAR        | Variable        | N             | N               | N               |
| lastModifiedPost    | Last Modified By Post     | NVARCHAR        | Variable        | N             | N               | N               |
| lastModifiedSection | Last Modified By Section  | NVARCHAR        | Variable        | N             | N               | N               |
| sysFileRefId        | System File Reference ID  | NVARCHAR        | Variable        | Y             | N               | N               |

### 4.1.10. attachments

> Entity Name: attachments
>
> Description: Manages attached files to various entities.

| **Field Name**     | **Description**        | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|------------------|------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v              | Version field          | BIGINT          |                  | N             | N               | N               |
| _id              | Unique ID              | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| application      | Application ID         | UNIQUEIDENTIFIER  |                  | N             | N               | Y               |
| createdAt        | Creation Timestamp     | DATETIME2       |                  | Y             | N               | N               |
| efolio           | E-folio ID             | NVARCHAR        | Variable        | N             | N               | N               |
| file             | File Data/Path         | Object/NVARCHAR   | Variable        | N             | N               | N               |
| filePartNo       | File Part Number       | NVARCHAR        | Variable        | N             | N               | N               |
| receivedDate     | Received Date          | DATETIME2       |                  | N             | N               | N               |
| remarks          | Remarks                | NVARCHAR        | Variable        | N             | N               | N               |
| subType          | Attachment Subtype     | NVARCHAR        | Variable        | N             | N               | N               |
| submissionCase   | Submission Case ID     | UNIQUEIDENTIFIER  |                  | N             | N               | Y               |
| sysFileRefId     | System File Reference ID | NVARCHAR        | Variable        | N             | N               | N               |
| type             | Attachment Type        | NVARCHAR        | Variable        | Y             | N               | N               |
| updatedAt        | Update Timestamp       | DATETIME2       |                  | N             | N               | N               |

### 4.1.11. users

> Entity Name: users
>
> Description: Stores user account information.

| **Field Name**         | **Description**            | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|----------------------|----------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                  | Version field              | BIGINT          |                  | N             | N               | N               |
| _id                  | Unique ID                  | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| bdgis                | BDGIS ID                   | NVARCHAR        | Variable        | N             | N               | N               |
| begis                | BEGIS ID                   | NVARCHAR        | Variable        | N             | N               | N               |
| delegateTo           | Delegate To User ID        | NVARCHAR        | Variable        | N             | N               | N               |
| department           | Department                 | NVARCHAR        | Variable        | Y             | N               | N               |
| email                | Email Address              | NVARCHAR        | Variable        | Y             | N               | N               |
| group                | Group                      | NVARCHAR        | Variable        | N             | N               | N               |
| lastLoginAt          | Last Login Timestamp       | DATETIME2       |                  | N             | N               | N               |
| letterLongPosition   | Letter Long Position       | NVARCHAR        | Variable        | N             | N               | N               |
| letterLongPositionCn | Letter Long Position (CN)  | NVARCHAR        | Variable        | N             | N               | N               |
| letterName           | Letter Name                | NVARCHAR        | Variable        | N             | N               | N               |
| letterNameCn         | Letter Name (CN)           | NVARCHAR        | Variable        | N             | N               | N               |
| letterPosition       | Letter Position            | NVARCHAR        | Variable        | N             | N               | N               |
| letterPositionCn     | Letter Position (CN)       | NVARCHAR        | Variable        | N             | N               | N               |
| lock                 | Account Lock Status        | BIT             |                  | Y             | N               | N               |
| luPostName           | LU Post Name               | NVARCHAR        | Variable        | N             | N               | N               |
| name                 | User Name                  | NVARCHAR        | Variable        | N             | N               | N               |
| notificationEmail    | Notification Email Address | NVARCHAR        | Variable        | N             | N               | N               |
| osdpEmail            | OSDP Email Address         | NVARCHAR        | Variable        | N             | N               | N               |
| osdpLoginId          | OSDP Login ID              | NVARCHAR        | Variable        | Y             | N               | N               |
| password             | Password (hashed)          | NVARCHAR        | Variable        | Y             | N               | N               |
| phoneNumber          | Phone Number               | NVARCHAR        | Variable        | N             | N               | N               |
| position             | Position                   | NVARCHAR        | Variable        | N             | N               | N               |
| role                 | User Role                  | NVARCHAR        | Variable        | Y             | N               | N               |
| team                 | Team ID                    | NVARCHAR        | Variable        | N             | N               | N               |
| userType             | User Type                  | NVARCHAR        | Variable        | Y             | N               | N               |

### 4.1.12. adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: References to address block files.

| **Field Name**        | **Description**           | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------|---------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                 | Version field             | BIGINT          |                  | N             | N               | N               |
| _id                 | Unique ID                 | UNIQUEIDENTIFIER  |                  | Y             | Y               | N               |
| adrBlkFileRefId     | Address Block File Ref ID | NVARCHAR        | Variable        | Y             | N               | N               |
| adrBlkId            | Address Block ID          | NVARCHAR        | Variable        | Y             | N               | N               |
| createdDt           | Creation Timestamp        | DATETIME2       |                  | Y             | N               | N               |
| createdName         | Created By Name           | NVARCHAR        | Variable        | N             | N               | N               |
| createdPost         | Created By Post           | NVARCHAR        | Variable        | Y             | N               | N               |
| createdSection      | Created By Section        | NVARCHAR        | Variable        | N             | N               | N               |
| lastModifiedDt      | Last Modified Timestamp   | DATETIME2       |                  | Y             | N               | N               |
| lastModifiedName    | Last Modified By Name     | NVARCHAR        | Variable        | N             | N               | N               |
| lastModifiedPost    | Last Modified By Post     | NVARCHAR        | Variable        | Y             | N               | N               |
| lastModifiedSection | Last Modified By Section  | NVARCHAR        | Variable        | N             | N               | N               |
| sysFileRefId        | System File Reference ID  | NVARCHAR        | Variable        | Y             | N               | N               |
```