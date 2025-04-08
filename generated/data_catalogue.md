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

# 2. Definitions

| Terms | Definitions          |
|-------|----------------------|
| BD    | Buildings Department |
| LSCP  | Licensing Self-Certification Portal |
|       |                      |
|       |                      |
|       |                      |
|       |                      |
|       |                      |
|       |                      |

# 3. Data Entity Description

This section states all the entities in the LSCP Database.

The following section describes how the LSCP entities can be mapped onto
physical data design.

-   Entities list for LSCP Data

| **Item** | **Entity Name** | **Entity Description** |
|----------|-----------------|------------------------|
| 1        | tasks           | Task information       |
| 2        | eminutes        | E-minutes records      |
| 3        | submissions     | Submission data        |
| 4        | applications    | Application details    |
| 5        | notifications   | Notification records   |
| 6        | bsblocks        | Building blocks data   |
| 7        | cases           | Case management data   |
| 8        | oauthtokens     | OAuth tokens for authentication |
| 9        | sysfilerefs     | System file references |
| 10       | attachments     | File attachments       |
| 11       | users           | User accounts          |
| 12       | adrblkfilerefs  | Address block file references |

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
> Description: Task information

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version         | BIGINT          |                  | Y             |                 |                 |
| _id           | Task ID         | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| application   | Application ID  | UNIQUEIDENTIFIER|                  | Y             |                 | Y               |
| createdAt     | Created At      | DATETIME2       |                  | Y             |                 |                 |
| status        | Status          | NVARCHAR        | Variable        | Y             |                 |                 |
| submissionCase| Submission Case ID| UNIQUEIDENTIFIER|                  | Y             |                 | Y               |
| taskType      | Task Type       | NVARCHAR        | Variable        | Y             |                 |                 |
| team          | Team            | NVARCHAR        | Variable        |               |                 |                 |
| user          | User ID         | NVARCHAR / UNIQUEIDENTIFIER | Variable        |               |                 | Y               |

### 4.1.2. eminutes

> Entity Name: eminutes
>
> Description: E-minutes records

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version         | BIGINT          |                  | Y             |                 |                 |
| _id           | E-minute ID     | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| comment       | Comment         | NVARCHAR        | Variable        |               |                 |                 |
| content       | Content         | NVARCHAR        | Variable        | Y             |                 |                 |
| createdAt     | Created At      | DATETIME2       |                  | Y             |                 |                 |
| efolio        | Efolio          | NVARCHAR        | Variable        |               |                 |                 |
| eminuteId     | E-minute ID     | NVARCHAR        | Variable        | Y             |                 |                 |
| from          | From User ID    | UNIQUEIDENTIFIER / NVARCHAR | Variable        | Y             |                 | Y               |
| status        | Status          | NVARCHAR        | Variable        | Y             |                 |                 |
| subject       | Subject         | NVARCHAR        | Variable        | Y             |                 |                 |
| submissionCase| Submission Case ID| UNIQUEIDENTIFIER|                  | Y             |                 | Y               |
| sysFileRefId  | System File Reference ID | NVARCHAR        | Variable        |               |                 |                 |
| to            | To User ID      | UNIQUEIDENTIFIER / NVARCHAR | Variable        |               |                 | Y               |

### 4.1.3. submissions

> Entity Name: submissions
>
> Description: Submission data

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
|  *No Fields Defined* |  *No Fields Defined* |  *No Fields Defined* |  *No Fields Defined* |  *No Fields Defined* |  *No Fields Defined* |  *No Fields Defined* |

### 4.1.4. applications

> Entity Name: applications
>
> Description: Application details

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|-----------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| APP13                   | APP13                       | NVARCHAR        | Variable        |               |                 |                 |
| AddressOfPremiseCN      | Address Of Premise CN       | NVARCHAR        | Variable        |               |                 |                 |
| AddressOfPremiseCNFloor | Address Of Premise CN Floor | NVARCHAR        | Variable        |               |                 |                 |
| AddressOfPremiseCNUnit  | Address Of Premise CN Unit  | NVARCHAR        | Variable        |               |                 |                 |
| AddressOfPremiseEN      | Address Of Premise EN       | NVARCHAR        | Variable        |               |                 |                 |
| AddressOfPremiseENFloor | Address Of Premise EN Floor | NVARCHAR        | Variable        |               |                 |                 |
| AddressOfPremiseENUnit  | Address Of Premise EN Unit  | NVARCHAR        | Variable        |               |                 |                 |
| AgeOfStudent            | Age Of Student              | NVARCHAR        | Variable        |               |                 |                 |
| ApplicantAddress        | Applicant Address           | NVARCHAR        | Variable        |               |                 |                 |
| ApplicantEmail          | Applicant Email             | NVARCHAR        | Variable        |               |                 |                 |
| ApplicantFax            | Applicant Fax               | NVARCHAR        | Variable        |               |                 |                 |
| ApplicantMobile         | Applicant Mobile            | NVARCHAR        | Variable        |               |                 |                 |
| ApplicantName           | Applicant Name              | NVARCHAR        | Variable        |               |                 |                 |
| ApplicantNameCN         | Applicant Name CN           | NVARCHAR        | Variable        |               |                 |                 |
| ApplicantNameEN         | Applicant Name EN           | NVARCHAR        | Variable        |               |                 |                 |
| ApplicantTel            | Applicant Tel             | NVARCHAR        | Variable        |               |                 |                 |
| ApplicationNo           | Application No              | NVARCHAR        | Variable        | Y             |                 |                 |
| ApplicationType         | Application Type            | NVARCHAR        | Variable        | Y             |                 |                 |
| Area                    | Area                        | NVARCHAR        | Variable        |               |                 |                 |
| BlockID                 | Block ID                    | NVARCHAR        | Variable        |               |                 |                 |
| ContactPerson           | Contact Person              | NVARCHAR        | Variable        |               |                 |                 |
| ContactPersonCN         | Contact Person CN           | NVARCHAR        | Variable        |               |                 |                 |
| ContactPersonEN         | Contact Person EN           | NVARCHAR        | Variable        |               |                 |                 |
| ContactPersonEmail      | Contact Person Email        | NVARCHAR        | Variable        |               |                 |                 |
| ContactPersonTel        | Contact Person Tel          | NVARCHAR        | Variable        |               |                 |                 |
| DescriptionOfSchool     | Description Of School       | NVARCHAR        | Variable        |               |                 |                 |
| District                | District                    | NVARCHAR        | Variable        |               |                 |                 |
| EstimatedNoOfStudent    | Estimated No Of Student     | BIGINT          |                  |               |                 |                 |
| FileReference           | File Reference              | NVARCHAR        | Variable        |               |                 |                 |
| NameOfSchoolCN          | Name Of School CN           | NVARCHAR        | Variable        |               |                 |                 |
| NameOfSchoolEN          | Name Of School EN           | NVARCHAR        | Variable        |               |                 |                 |
| Region                  | Region                      | NVARCHAR        | Variable        |               |                 |                 |
| RelatedPremise          | Related Premise             | NVARCHAR        | Variable        |               |                 |                 |
| RelatedPremises         | Related Premises (Array)    | NVARCHAR        | Variable        | Y             |                 |                 |
| SelfCertification      | Self Certification (Object) | NVARCHAR        | Variable        |               |                 |                 |
| StructuralCalculation   | Structural Calculation (Object)| NVARCHAR        | Variable        |               |                 |                 |
| SubmissionType          | Submission Type             | NVARCHAR        | Variable        |               |                 |                 |
| __v                     | Version                     | BIGINT          |                  | Y             |                 |                 |
| _id                     | Application ID              | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| address                 | Address (Object)            | NVARCHAR        | Variable        |               |                 |                 |
| assignedBS              | Assigned BS User ID         | UNIQUEIDENTIFIER / NVARCHAR | Variable        |               |                 | Y               |
| assignedGR              | Assigned GR User ID         | UNIQUEIDENTIFIER|                  |               |                 | Y               |
| assignedSBS             | Assigned SBS User ID        | NVARCHAR        | Variable        |               |                 |                 |
| createdAt               | Created At                  | DATETIME2       |                  | Y             |                 |                 |
| updatedAt               | Updated At                  | DATETIME2       |                  |               |                 |                 |

### 4.1.5. notifications

> Entity Name: notifications
>
> Description: Notification records

| **Field Name**     | **Description**         | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                | Version                 | BIGINT          |                  | Y             |                 |                 |
| _id                | Notification ID         | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| createdAt          | Created At              | DATETIME2       |                  | Y             |                 |                 |
| eminute            | E-minute ID             | UNIQUEIDENTIFIER|                  |               |                 | Y               |
| notificationType   | Notification Type       | NVARCHAR        | Variable        | Y             |                 |                 |
| requireSendEmail   | Require Send Email      | BIT             |                  | Y             |                 |                 |
| task               | Task ID                 | UNIQUEIDENTIFIER|                  |               |                 | Y               |
| user               | User ID                 | NVARCHAR        | Variable        | Y             |                 | Y               |

### 4.1.6. bsblocks

> Entity Name: bsblocks
>
> Description: Building blocks data

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v           | Version         | BIGINT          |                  | Y             |                 |                 |
| _id           | BS Block ID     | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| bdgis         | BDGIS Code      | NVARCHAR        | Variable        | Y             |                 |                 |
| blockId       | Block ID        | NVARCHAR        | Variable        | Y             |                 |                 |

### 4.1.7. cases

> Entity Name: cases
>
> Description: Case management data

| **Field Name**            | **Description**               | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------------|-------------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| ActualReplyDate           | Actual Reply Date             | DATETIME2       |                  |               |                 |                 |
| Area                      | Area                          | NVARCHAR        | Variable        |               |                 |                 |
| AuditResult               | Audit Result                  | NVARCHAR        | Variable        |               |                 |                 |
| CaseOfficer               | Case Officer                  | NVARCHAR        | Variable        |               |                 |                 |
| Category                  | Category                      | NVARCHAR        | Variable        | Y             |                 |                 |
| District                  | District                      | NVARCHAR        | Variable        |               |                 |                 |
| FileReference             | File Reference                | NVARCHAR        | Variable        |               |                 |                 |
| LAFileReference           | LA File Reference (Object)    | NVARCHAR        | Variable        |               |                 |                 |
| Nature                    | Nature                        | NVARCHAR        | Variable        |               |                 |                 |
| ObjectiontoLR             | Objection to LR               | NVARCHAR        | Variable        |               |                 |                 |
| ReceivedDate              | Received Date                 | DATETIME2       |                  |               |                 |                 |
| Referrer                  | Referrer (Object)             | NVARCHAR        | Variable        |               |                 |                 |
| Region                    | Region                        | NVARCHAR        | Variable        |               |                 |                 |
| Remarks                   | Remarks                       | NVARCHAR        | Variable        |               |                 |                 |
| Reminders                 | Reminders (Array)             | NVARCHAR        | Variable        |               |                 |                 |
| SubmissionType            | Submission Type               | NVARCHAR        | Variable        |               |                 |                 |
| SubstantialReplyDate      | Substantial Reply Date        | DATETIME2       |                  |               |                 |                 |
| TargetReplyDate           | Target Reply Date             | DATETIME2       |                  |               |                 |                 |
| ThreeTierReqt             | Three Tier Requirement        | NVARCHAR        | Variable        |               |                 |                 |
| ViaSCS                    | Via SCS                       | BIT             |                  |               |                 |                 |
| __v                       | Version                       | BIGINT          |                  | Y             |                 |                 |
| _id                       | Case ID                       | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| application               | Application ID                | UNIQUEIDENTIFIER|                  | Y             |                 | Y               |
| assignedBS                | Assigned BS User ID           | UNIQUEIDENTIFIER|                  |               |                 | Y               |
| assignedGR                | Assigned GR User ID           | UNIQUEIDENTIFIER|                  |               |                 | Y               |
| building_information      | Building Information (Object) | NVARCHAR        | Variable        |               |                 |                 |
| caseDescription           | Case Description (Object)     | NVARCHAR        | Variable        |               |                 |                 |
| caseOfficerReceive        | Case Officer Receive User ID  | NVARCHAR        | Variable        |               |                 | Y               |
| caseOfficerReply          | Case Officer Reply User ID    | NVARCHAR        | Variable        |               |                 | Y               |
| createdAt                 | Created At                    | DATETIME2       |                  | Y             |                 |                 |
| deck_study                | Deck Study (Object)           | NVARCHAR        | Variable        | Y             |                 |                 |
| documentChecklist         | Document Checklist (Object)   | NVARCHAR        | Variable        |               |                 |                 |
| dv                        | DV (Object)                   | NVARCHAR        | Variable        | Y             |                 |                 |
| frc                       | FRC (Object)                  | NVARCHAR        | Variable        | Y             |                 |                 |
| misc                      | MISC (Object)                 | NVARCHAR        | Variable        | Y             |                 |                 |
| moe                       | MOE (Object)                  | NVARCHAR        | Variable        | Y             |                 |                 |
| seniorCaseOfficerReceive  | Senior Case Officer Receive User ID | NVARCHAR        | Variable        |               |                 | Y               |
| seniorCaseOfficerReply    | Senior Case Officer Reply User ID   | NVARCHAR        | Variable        |               |                 | Y               |
| site_inspection           | Site Inspection (Object)      | NVARCHAR        | Variable        |               |                 |                 |
| structural_ccc_bs         | Structural CCC BS (Object)    | NVARCHAR        | Variable        | Y             |                 |                 |
| structural_schnlh         | Structural SCHNLH (Object)    | NVARCHAR        | Variable        | Y             |                 |                 |
| structural_schnlhkinds    | Structural SCHNLHKINDS (Object)| NVARCHAR        | Variable        | Y             |                 |                 |
| team                      | Team                          | NVARCHAR        | Variable        | Y             |                 |                 |
| ubw                       | UBW (Object)                  | NVARCHAR        | Variable        | Y             |                 |                 |
| updatedAt                 | Updated At                    | DATETIME2       |                  |               |                 |                 |

### 4.1.8. oauthtokens

> Entity Name: oauthtokens
>
> Description: OAuth tokens for authentication

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|-----------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                     | Version                     | BIGINT          |                  | Y             |                 |                 |
| _id                     | OAuth Token ID              | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| accessToken             | Access Token                | NVARCHAR        | Variable        | Y             |                 |                 |
| accessTokenExpiresAt    | Access Token Expires At     | DATETIME2       |                  | Y             |                 |                 |
| client                  | Client (Object)             | NVARCHAR        | Variable        | Y             |                 |                 |
| refreshToken            | Refresh Token               | NVARCHAR        | Variable        | Y             |                 |                 |
| refreshTokenExpiresAt   | Refresh Token Expires At    | DATETIME2       |                  | Y             |                 |                 |
| user                    | User ID                     | UNIQUEIDENTIFIER|                  | Y             |                 | Y               |

### 4.1.9. sysfilerefs

> Entity Name: sysfilerefs
>
> Description: System file references

| **Field Name**        | **Description**           | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|---------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                   | Version                   | BIGINT          |                  | Y             |                 |                 |
| _id                   | System File Reference ID  | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| createdDt             | Created Date              | DATETIME2       |                  | Y             |                 |                 |
| createdName           | Created By Name           | NVARCHAR        | Variable        |               |                 |                 |
| createdPost           | Created By Post           | NVARCHAR        | Variable        |               |                 |                 |
| createdSection        | Created By Section        | NVARCHAR        | Variable        |               |                 |                 |
| display               | Display Name              | NVARCHAR        | Variable        | Y             |                 |                 |
| dvExceed              | DV Exceed                 | NVARCHAR        | Variable        |               |                 |                 |
| dvStatusDt            | DV Status Date            | DATETIME2       |                  |               |                 |                 |
| frefPref              | File Reference Prefix     | NVARCHAR        | Variable        |               |                 |                 |
| frefSeq               | File Reference Sequence   | NVARCHAR        | Variable        |               |                 |                 |
| frefSuf               | File Reference Suffix     | NVARCHAR        | Variable        |               |                 |                 |
| frefYr                | File Reference Year       | NVARCHAR        | Variable        |               |                 |                 |
| lastModifiedDt        | Last Modified Date        | DATETIME2       |                  | Y             |                 |                 |
| lastModifiedName      | Last Modified By Name     | NVARCHAR        | Variable        |               |                 |                 |
| lastModifiedPost      | Last Modified By Post     | NVARCHAR        | Variable        |               |                 |                 |
| lastModifiedSection   | Last Modified Section     | NVARCHAR        | Variable        |               |                 |                 |
| sysFileRefId          | System File Reference ID  | NVARCHAR        | Variable        | Y             |                 |                 |

### 4.1.10. attachments

> Entity Name: attachments
>
> Description: File attachments

| **Field Name**     | **Description**         | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                | Version                 | BIGINT          |                  | Y             |                 |                 |
| _id                | Attachment ID           | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| application        | Application ID          | UNIQUEIDENTIFIER|                  | Y             |                 | Y               |
| createdAt          | Created At              | DATETIME2       |                  | Y             |                 |                 |
| efolio             | Efolio                  | NVARCHAR        | Variable        |               |                 |                 |
| file               | File (Object/String)      | NVARCHAR        | Variable        |               |                 |                 |
| filePartNo         | File Part Number        | NVARCHAR        | Variable        |               |                 |                 |
| receivedDate       | Received Date           | DATETIME2       |                  | Y             |                 |                 |
| remarks            | Remarks                 | NVARCHAR        | Variable        |               |                 |                 |
| subType            | Sub Type                | NVARCHAR        | Variable        |               |                 |                 |
| submissionCase     | Submission Case ID      | UNIQUEIDENTIFIER|                  |               |                 | Y               |
| sysFileRefId       | System File Reference ID | NVARCHAR        | Variable        |               |                 |                 |
| type               | Type                    | NVARCHAR        | Variable        | Y             |                 |                 |
| updatedAt          | Updated At              | DATETIME2       |                  |               |                 |                 |

### 4.1.11. users

> Entity Name: users
>
> Description: User accounts

| **Field Name**        | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-----------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                   | Version                     | BIGINT          |                  | Y             |                 |                 |
| _id                   | User ID                     | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| bdgis                 | BDGIS Code                  | NVARCHAR        | Variable        |               |                 |                 |
| begis                 | BEGIS Code                  | NVARCHAR        | Variable        |               |                 |                 |
| delegateTo            | Delegate To User ID         | NVARCHAR        | Variable        |               |                 | Y               |
| department            | Department                  | NVARCHAR        | Variable        | Y             |                 |                 |
| email                 | Email                       | NVARCHAR        | Variable        |               |                 |                 |
| group                 | Group                       | NVARCHAR        | Variable        |               |                 |                 |
| lastLoginAt           | Last Login At               | DATETIME2       |                  |               |                 |                 |
| letterLongPosition    | Letter Long Position        | NVARCHAR        | Variable        |               |                 |                 |
| letterLongPositionCn  | Letter Long Position CN     | NVARCHAR        | Variable        |               |                 |                 |
| letterName            | Letter Name                 | NVARCHAR        | Variable        |               |                 |                 |
| letterNameCn          | Letter Name CN              | NVARCHAR        | Variable        |               |                 |                 |
| letterPosition        | Letter Position             | NVARCHAR        | Variable        |               |                 |                 |
| letterPositionCn      | Letter Position CN          | NVARCHAR        | Variable        |               |                 |                 |
| lock                  | Lock Status                 | BIT             |                  | Y             |                 |                 |
| luPostName            | LU Post Name                | NVARCHAR        | Variable        |               |                 |                 |
| name                  | Name                        | NVARCHAR        | Variable        |               |                 |                 |
| notificationEmail     | Notification Email          | NVARCHAR        | Variable        |               |                 |                 |
| osdpEmail             | OSDP Email                  | NVARCHAR        | Variable        |               |                 |                 |
| osdpLoginId           | OSDP Login ID               | NVARCHAR        | Variable        |               |                 |                 |
| password              | Password                    | NVARCHAR        | Variable        |               |                 |                 |
| phoneNumber           | Phone Number                | NVARCHAR        | Variable        |               |                 |                 |
| position              | Position                    | NVARCHAR        | Variable        |               |                 |                 |
| role                  | Role                        | NVARCHAR        | Variable        | Y             |                 |                 |
| team                  | Team                        | NVARCHAR        | Variable        |               |                 |                 |
| userType              | User Type                   | NVARCHAR        | Variable        | Y             |                 |                 |

### 4.1.12. adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: Address block file references

| **Field Name**        | **Description**               | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-------------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                   | Version                       | BIGINT          |                  | Y             |                 |                 |
| _id                   | Address Block File Ref ID     | UNIQUEIDENTIFIER|                  | Y             | Y               |                 |
| adrBlkFileRefId       | Address Block File Ref ID     | NVARCHAR        | Variable        | Y             |                 |                 |
| adrBlkId              | Address Block ID              | NVARCHAR        | Variable        | Y             |                 |                 |
| createdDt             | Created Date                  | DATETIME2       |                  | Y             |                 |                 |
| createdName           | Created By Name               | NVARCHAR        | Variable        |               |                 |                 |
| createdPost           | Created By Post               | NVARCHAR        | Variable        | Y             |                 |                 |
| createdSection        | Created By Section            | NVARCHAR        | Variable        |               |                 |                 |
| lastModifiedDt        | Last Modified Date            | DATETIME2       |                  | Y             |                 |                 |
| lastModifiedName      | Last Modified By Name         | NVARCHAR        | Variable        |               |                 |                 |
| lastModifiedPost      | Last Modified By Post         | NVARCHAR        | Variable        | Y             |                 |                 |
| lastModifiedSection   | Last Modified Section         | NVARCHAR        | Variable        |               |                 |                 |
| sysFileRefId          | System File Reference ID      | NVARCHAR        | Variable        | Y             |                 | Y               |