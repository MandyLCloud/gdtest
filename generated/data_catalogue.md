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
> [4.1.4. applications 11](#applications)
>
> [4.1.5. notifications 13](#notifications)
>
> [4.1.6. bsblocks 14](#bsblocks)
>
> [4.1.7. cases 14](#cases)
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

This data catalogue is based on the analysis of the 'bd' database, last updated on 2025/3/4 ??10:10:39.

**Database Statistics:**
- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1278983
- Total Data Size: 371.24 MB

# 2. Definitions

| Terms | Definitions          |
|-------|----------------------|
| BD    | Buildings Department |
| LSCP  | Licensing Self-Certification Portal |
| MB    | Megabyte             |
| KB    | Kilobyte             |
| GB    | Gigabyte             |
| ID    | Identifier           |
| No.   | Number               |
| CN    | Chinese              |
| EN    | English              |
| TBC   | To Be Confirmed      |
| MS SQL| Microsoft SQL Server |

# 3. Data Entity Description

This section states all the entities in the LSCP Database.

The following section describes how the LSCP entities can be mapped onto
physical data design.

-   Entities list for LSCP Data

| **Item** | **Entity Name** | **Entity Description**                                  |
|----------|-----------------|-------------------------------------------------------|
| 1        | tasks           | Stores information about tasks within the system.       |
| 2        | eminutes        | Stores electronic minutes of meetings or discussions. |
| 3        | submissions     | Stores data related to submissions (currently empty). |
| 4        | applications    | Stores application forms and related details.         |
| 5        | notifications   | Stores system notifications for users.                 |
| 6        | bsblocks        | Stores information about building blocks.             |
| 7        | cases           | Stores information about cases or applications.       |
| 8        | oauthtokens     | Stores OAuth tokens for authentication.               |
| 9        | sysfilerefs     | Stores system file references.                        |
| 10       | attachments     | Stores attachments related to applications or cases.  |
| 11       | users           | Stores user account information.                      |
| 12       | adrblkfilerefs  | Stores address block file references.                 |

# 

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
> Description: Stores information about tasks within the system, potentially related to applications and submissions.

| **Field Name** | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|----------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v            | Version field               | objectId, int    | N/A              | N             | N               | N               |
| _id            | Task ID                     | objectId         | N/A              | Y             | Y               | N               |
| application    | Reference to application    | objectId         | N/A              | N             | N               | Y               |
| createdAt      | Task creation timestamp     | date             | N/A              | N             | N               | N               |
| status         | Task status                 | string           | Variable         | N             | N               | N               |
| submissionCase | Reference to submission case| objectId         | N/A              | N             | N               | Y               |
| taskType       | Type of task                | string           | Variable         | N             | N               | N               |
| team           | Team assigned to task       | string           | Variable         | N             | N               | N               |
| user           | User related to task        | string, objectId | Variable/N/A     | N             | N               | Y               |

### 4.1.2. eminutes

> Entity Name: eminutes
>
> Description: Stores electronic minutes of meetings or discussions, potentially related to cases and efolios.

| **Field Name** | **Description**         | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|----------------|-------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v            | Version field           | int              | N/A              | N             | N               | N               |
| _id            | Eminute ID              | objectId         | N/A              | Y             | Y               | N               |
| comment        | Comment in eminute      | string           | Variable         | N             | N               | N               |
| content        | Content of eminute      | string           | Variable         | N             | N               | N               |
| createdAt      | Eminute creation timestamp| date             | N/A              | N             | N               | N               |
| efolio         | Efolio reference        | string           | Variable         | N             | N               | N               |
| eminuteId      | Eminute Identifier      | string           | Variable         | N             | N               | N               |
| from           | Sender of eminute       | objectId, string | N/A/Variable     | N             | N               | Y               |
| status         | Eminute status          | string           | Variable         | N             | N               | N               |
| subject        | Subject of eminute      | string           | Variable         | N             | N               | N               |
| submissionCase | Submission case reference| objectId         | N/A              | N             | N               | Y               |
| sysFileRefId   | System file reference ID| string           | Variable         | N             | N               | Y               |
| to             | Recipient of eminute    | objectId, string | N/A/Variable     | N             | N               | Y               |

### 4.1.3. submissions

> Entity Name: submissions
>
> Description: Stores data related to submissions. Currently, this collection is empty.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|----------------|-----------------|------------------|------------------|---------------|-----------------|-----------------|
| *No fields defined* |                 |                  |                  |               |                 |                 |

### 4.1.4. applications

> Entity Name: applications
>
> Description: Stores application forms and related details, including various fields related to premise address, applicant information, school details, and assigned personnel.

| **Field Name**          | **Description**                 | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|---------------------------------|------------------|------------------|---------------|-----------------|-----------------|
| APP13                   | Application field 13            | object, array    | N/A              | N             | N               | N               |
| AddressOfPremiseCN      | Address of premise in Chinese   | string           | Variable         | N             | N               | N               |
| AddressOfPremiseCNFloor | Premise floor in Chinese        | string           | Variable         | N             | N               | N               |
| AddressOfPremiseCNUnit  | Premise unit in Chinese         | string           | Variable         | N             | N               | N               |
| AddressOfPremiseEN      | Address of premise in English   | string           | Variable         | N             | N               | N               |
| AddressOfPremiseENFloor | Premise floor in English        | string           | Variable         | N             | N               | N               |
| AddressOfPremiseENUnit  | Premise unit in English         | string           | Variable         | N             | N               | N               |
| AgeOfStudent            | Age of student                  | null, string     | Variable         | N             | N               | N               |
| ApplicantAddress        | Applicant address               | string           | Variable         | N             | N               | N               |
| ApplicantEmail          | Applicant email                 | string           | Variable         | N             | N               | N               |
| ApplicantFax            | Applicant fax number            | string           | Variable         | N             | N               | N               |
| ApplicantMobile         | Applicant mobile number         | string           | Variable         | N             | N               | N               |
| ApplicantName           | Applicant name                  | string           | Variable         | N             | N               | N               |
| ApplicantNameCN         | Applicant name in Chinese       | string           | Variable         | N             | N               | N               |
| ApplicantNameEN         | Applicant name in English       | null, string     | Variable         | N             | N               | N               |
| ApplicantTel            | Applicant telephone number      | null, string     | Variable         | N             | N               | N               |
| ApplicationNo           | Application number              | null, string     | Variable         | N             | N               | N               |
| ApplicationType         | Application type                | string           | Variable         | N             | N               | N               |
| Area                    | Area of premise                 | string           | Variable         | N             | N               | N               |
| BlockID                 | Block ID                        | string           | Variable         | N             | N               | N               |
| ContactPerson           | Contact person name             | string           | Variable         | N             | N               | N               |
| ContactPersonCN         | Contact person name in Chinese  | string           | Variable         | N             | N               | N               |
| ContactPersonEN         | Contact person name in English  | string           | Variable         | N             | N               | N               |
| ContactPersonEmail      | Contact person email            | string           | Variable         | N             | N               | N               |
| ContactPersonTel        | Contact person telephone        | string           | Variable         | N             | N               | N               |
| DescriptionOfSchool     | Description of school           | string, null     | Variable         | N             | N               | N               |
| District                | District of premise             | string           | Variable         | N             | N               | N               |
| EstimatedNoOfStudent    | Estimated number of students    | int, null        | N/A              | N             | N               | N               |
| FileReference           | File reference number           | string           | Variable         | N             | N               | N               |
| NameOfSchoolCN          | Name of school in Chinese       | string           | Variable         | N             | N               | N               |
| NameOfSchoolEN          | Name of school in English       | string           | Variable         | N             | N               | N               |
| Region                  | Region of premise               | string           | Variable         | N             | N               | N               |
| RelatedPremise          | Related premise information     | string           | Variable         | N             | N               | N               |
| RelatedPremises         | Array of related premises       | array            | N/A              | N             | N               | N               |
| SelfCertification      | Self-certification details      | object, null     | N/A              | N             | N               | N               |
| StructuralCalculation   | Structural calculation details  | object           | N/A              | N             | N               | N               |
| SubmissionType          | Submission type                 | string           | Variable         | N             | N               | N               |
| __v                     | Version field                   | int              | N/A              | N             | N               | N               |
| _id                     | Application ID                  | objectId         | N/A              | Y             | Y               | N               |
| address                 | Address object                  | object           | N/A              | N             | N               | N               |
| assignedBS              | Assigned Building Surveyor      | objectId, string, null| N/A/Variable     | N             | N               | Y               |
| assignedGR              | Assigned Geotechnical Engineer  | objectId, null   | N/A/Variable     | N             | N               | Y               |
| assignedSBS             | Assigned Structural Engineer    | string, null     | Variable         | N             | N               | N               |
| createdAt               | Application creation timestamp  | date             | N/A              | N             | N               | N               |
| updatedAt               | Application update timestamp    | date             | N/A              | N             | N               | N               |

### 4.1.5. notifications

> Entity Name: notifications
>
> Description: Stores system notifications for users, potentially related to tasks and eminutes.

| **Field Name**     | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                | Version field               | int              | N/A              | N             | N               | N               |
| _id                | Notification ID             | objectId         | N/A              | Y             | Y               | N               |
| createdAt          | Notification creation timestamp| date             | N/A              | N             | N               | N               |
| eminute            | Reference to eminute        | objectId         | N/A              | N             | N               | Y               |
| notificationType   | Type of notification        | string           | Variable         | N             | N               | N               |
| requireSendEmail   | Flag to send email          | bool             | N/A              | N             | N               | N               |
| task               | Reference to task           | objectId         | N/A              | N             | N               | Y               |
| user               | User receiving notification | string           | Variable         | N             | N               | Y               |

### 4.1.6. bsblocks

> Entity Name: bsblocks
>
> Description: Stores information about building blocks, likely related to geographical information.

| **Field Name** | **Description**       | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|----------------|-----------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v            | Version field         | int              | N/A              | N             | N               | N               |
| _id            | BSBlock ID            | objectId         | N/A              | Y             | Y               | N               |
| bdgis          | BDGIS identifier      | string           | Variable         | N             | N               | N               |
| blockId        | Block Identifier      | string           | Variable         | N             | N               | N               |

### 4.1.7. cases

> Entity Name: cases
>
> Description: Stores information about cases or applications, including details about case officers, dates, categories, and related objects.

| **Field Name**            | **Description**                   | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------------|-----------------------------------|------------------|------------------|---------------|-----------------|-----------------|
| ActualReplyDate           | Actual reply date                 | null, date       | N/A              | N             | N               | N               |
| Area                      | Area of case                      | string           | Variable         | N             | N               | N               |
| AuditResult               | Audit result of case              | string           | Variable         | N             | N               | N               |
| CaseOfficer               | Case officer assigned             | string           | Variable         | N             | N               | N               |
| Category                  | Case category                     | string           | Variable         | N             | N               | N               |
| District                  | District of case                  | string           | Variable         | N             | N               | N               |
| FileReference             | File reference for case           | string           | Variable         | N             | N               | N               |
| LAFileReference           | LA file reference                 | object           | N/A              | N             | N               | N               |
| Nature                    | Nature of case                    | null, string     | Variable         | N             | N               | N               |
| ObjectiontoLR             | Objection to LR                   | string           | Variable         | N             | N               | N               |
| ReceivedDate              | Date case received                | date, null       | N/A              | N             | N               | N               |
| Referrer                  | Case referrer                     | object           | N/A              | N             | N               | N               |
| Region                    | Region of case                    | string           | Variable         | N             | N               | N               |
| Remarks                   | Case remarks                      | string           | Variable         | N             | N               | N               |
| Reminders                 | Case reminders                    | array            | N/A              | N             | N               | N               |
| SubmissionType            | Submission type of case           | string           | Variable         | N             | N               | N               |
| SubstantialReplyDate      | Substantial reply date            | null, date       | N/A              | N             | N               | N               |
| TargetReplyDate           | Target reply date                 | date, null       | N/A              | N             | N               | N               |
| ThreeTierReqt             | Three tier requirement            | string           | Variable         | N             | N               | N               |
| ViaSCS                    | Via SCS flag                      | bool             | N/A              | N             | N               | N               |
| __v                       | Version field                     | int              | N/A              | N             | N               | N               |
| _id                       | Case ID                           | objectId         | N/A              | Y             | Y               | N               |
| application               | Reference to application          | objectId         | N/A              | N             | N               | Y               |
| assignedBS                | Assigned Building Surveyor          | objectId         | N/A              | N             | N               | Y               |
| assignedGR                | Assigned Geotechnical Engineer      | objectId         | N/A              | N             | N               | Y               |
| building_information      | Building information object       | object           | N/A              | N             | N               | N               |
| caseDescription           | Case description object           | object           | N/A              | N             | N               | N               |
| caseOfficerReceive        | Case officer receive information  | string           | Variable         | N             | N               | N               |
| caseOfficerReply          | Case officer reply information    | string           | Variable         | N             | N               | N               |
| createdAt                 | Case creation timestamp           | date             | N/A              | N             | N               | N               |
| deck_study                | Deck study object                 | object           | N/A              | N             | N               | N               |
| documentChecklist         | Document checklist object         | object           | N/A              | N             | N               | N               |
| dv                        | DV object                         | object           | N/A              | N             | N               | N               |
| frc                       | FRC object                        | object           | N/A              | N             | N               | N               |
| misc                      | Miscellaneous object              | object           | N/A              | N             | N               | N               |
| moe                       | MOE object                        | object           | N/A              | N             | N               | N               |
| seniorCaseOfficerReceive  | Senior case officer receive info  | string           | Variable         | N             | N               | N               |
| seniorCaseOfficerReply    | Senior case officer reply info    | string           | Variable         | N             | N               | N               |
| site_inspection           | Site inspection object            | object           | N/A              | N             | N               | N               |
| structural_ccc_bs         | Structural CCC BS object          | object           | N/A              | N             | N               | N               |
| structural_schnlh         | Structural SCHNLH object          | object           | N/A              | N             | N               | N               |
| structural_schnlhkinds    | Structural SCHNLH Kinds object     | object           | N/A              | N             | N               | N               |
| team                      | Team assigned to case             | string           | Variable         | N             | N               | N               |
| ubw                       | UBW object                        | object           | N/A              | N             | N               | N               |
| updatedAt                 | Case update timestamp             | date             | N/A              | N             | N               | N               |

### 4.1.8. oauthtokens

> Entity Name: oauthtokens
>
> Description: Stores OAuth tokens for authentication, related to users and clients.

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                     | Version field               | int              | N/A              | N             | N               | N               |
| _id                     | OAuth Token ID              | objectId         | N/A              | Y             | Y               | N               |
| accessToken             | Access token value          | string           | Variable         | N             | N               | N               |
| accessTokenExpiresAt    | Access token expiry timestamp| date             | N/A              | N             | N               | N               |
| client                  | Client information          | object           | N/A              | N             | N               | N               |
| refreshToken            | Refresh token value         | string           | Variable         | N             | N               | N               |
| refreshTokenExpiresAt   | Refresh token expiry timestamp| date             | N/A              | N             | N               | N               |
| user                    | Reference to user           | objectId         | N/A              | N             | N               | Y               |

### 4.1.9. sysfilerefs

> Entity Name: sysfilerefs
>
> Description: Stores system file references, including details about creation, modification, and file identifiers.

| **Field Name**        | **Description**               | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-------------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                   | Version field                 | int              | N/A              | N             | N               | N               |
| _id                   | SysFileRef ID                 | objectId         | N/A              | Y             | Y               | N               |
| createdDt             | Creation timestamp            | date             | N/A              | N             | N               | N               |
| createdName           | Creator name                  | null, string     | Variable         | N             | N               | N               |
| createdPost           | Creator post                  | null, string     | Variable         | N             | N               | N               |
| createdSection        | Creator section               | null, string     | Variable         | N             | N               | N               |
| display               | Display name                  | string           | Variable         | N             | N               | N               |
| dvExceed              | DV exceed information         | null, string     | Variable         | N             | N               | N               |
| dvStatusDt            | DV status timestamp           | null, date       | N/A              | N             | N               | N               |
| frefPref              | File reference prefix         | string, null     | Variable         | N             | N               | N               |
| frefSeq               | File reference sequence       | null, string     | Variable         | N             | N               | N               |
| frefSuf               | File reference suffix         | null, string     | Variable         | N             | N               | N               |
| frefYr                | File reference year           | null, string     | Variable         | N             | N               | N               |
| lastModifiedDt        | Last modification timestamp   | date             | N/A              | N             | N               | N               |
| lastModifiedName      | Last modifier name            | null, string     | Variable         | N             | N               | N               |
| lastModifiedPost      | Last modifier post            | null, string     | Variable         | N             | N               | N               |
| lastModifiedSection   | Last modifier section         | null             | N/A              | N             | N               | N               |
| sysFileRefId          | System File Reference Identifier| string           | Variable         | N             | N               | N               |

### 4.1.10. attachments

> Entity Name: attachments
>
> Description: Stores attachments related to applications or cases, including file details and references to applications and submission cases.

| **Field Name**   | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v              | Version field               | int              | N/A              | N             | N               | N               |
| _id              | Attachment ID               | objectId         | N/A              | Y             | Y               | N               |
| application      | Reference to application    | objectId         | N/A              | N             | N               | Y               |
| createdAt        | Attachment creation timestamp| date             | N/A              | N             | N               | N               |
| efolio           | Efolio reference            | null, string     | Variable         | N             | N               | N               |
| file             | File details                | object, string   | N/A/Variable     | N             | N               | N               |
| filePartNo       | File part number            | string           | Variable         | N             | N               | N               |
| receivedDate     | Date file received          | date             | N/A              | N             | N               | N               |
| remarks          | Attachment remarks          | string           | Variable         | N             | N               | N               |
| subType          | Attachment subtype          | string           | Variable         | N             | N               | N               |
| submissionCase   | Reference to submission case| objectId         | N/A              | N             | N               | Y               |
| sysFileRefId     | System file reference ID    | string           | Variable         | N             | N               | Y               |
| type             | Attachment type             | string           | Variable         | N             | N               | N               |
| updatedAt        | Attachment update timestamp  | date             | N/A              | N             | N               | N               |

### 4.1.11. users

> Entity Name: users
>
> Description: Stores user account information, including personal details, department, role, and login information.

| **Field Name**        | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                   | Version field               | int              | N/A              | N             | N               | N               |
| _id                   | User ID                     | objectId         | N/A              | Y             | Y               | N               |
| bdgis                 | BDGIS identifier            | string           | Variable         | N             | N               | N               |
| begis                 | BEGIS identifier            | string           | Variable         | N             | N               | N               |
| delegateTo            | User delegated to           | string           | Variable         | N             | N               | N               |
| department            | User department             | string           | Variable         | N             | N               | N               |
| email                 | User email                  | string           | Variable         | N             | N               | N               |
| group                 | User group                  | string           | Variable         | N             | N               | N               |
| lastLoginAt           | Last login timestamp        | date             | N/A              | N             | N               | N               |
| letterLongPosition    | Long position in letter      | string           | Variable         | N             | N               | N               |
| letterLongPositionCn  | Long position in letter (CN)| string           | Variable         | N             | N               | N               |
| letterName            | Name in letter              | string           | Variable         | N             | N               | N               |
| letterNameCn          | Name in letter (CN)         | string           | Variable         | N             | N               | N               |
| letterPosition        | Position in letter          | string           | Variable         | N             | N               | N               |
| letterPositionCn      | Position in letter (CN)     | string           | Variable         | N             | N               | N               |
| lock                  | Account lock status         | bool             | N/A              | N             | N               | N               |
| luPostName            | LU Post name                | string           | Variable         | N             | N               | N               |
| name                  | User name                   | string           | Variable         | N             | N               | N               |
| notificationEmail     | Notification email address    | string           | Variable         | N             | N               | N               |
| osdpEmail             | OSDP email                  | string           | Variable         | N             | N               | N               |
| osdpLoginId           | OSDP login ID               | string           | Variable         | N             | N               | N               |
| password              | User password (hashed)      | string           | Variable         | N             | N               | N               |
| phoneNumber           | User phone number           | string           | Variable         | N             | N               | N               |
| position              | User position               | string           | Variable         | N             | N               | N               |
| role                  | User role                   | string           | Variable         | N             | N               | N               |
| team                  | User team                   | string           | Variable         | N             | N               | N               |
| userType              | User type                   | string           | Variable         | N             | N               | N               |

### 4.1.12. adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: Stores address block file references, linking address blocks to system file references.

| **Field Name**        | **Description**                 | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|---------------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                   | Version field                   | int              | N/A              | N             | N               | N               |
| _id                   | ADRBlkFileRef ID              | objectId         | N/A              | Y             | Y               | N               |
| adrBlkFileRefId       | Address Block File Reference ID | string           | Variable         | N             | N               | N               |
| adrBlkId              | Address Block ID                | string           | Variable         | N             | N               | N               |
| createdDt             | Creation timestamp            | date             | N/A              | N             | N               | N               |
| createdName           | Creator name                  | null, string     | Variable         | N             | N               | N               |
| createdPost           | Creator post                  | string           | Variable         | N             | N               | N               |
| createdSection        | Creator section               | null, string     | Variable         | N             | N               | N               |
| lastModifiedDt        | Last modification timestamp   | date             | N/A              | N             | N               | N               |
| lastModifiedName      | Last modifier name            | null, string     | Variable         | N             | N               | N               |
| lastModifiedPost      | Last modifier post            | string           | Variable         | N             | N               | N               |
| lastModifiedSection   | Last modifier section         | string, null     | Variable/N/A     | N             | N               | N               |
| sysFileRefId          | System file reference ID      | string           | Variable         | N             | N               | Y               |
```