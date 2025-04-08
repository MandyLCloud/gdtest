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
> [4.1.1. Tasks 9](#tasks)
>
> [4.1.2. Eminutes 10](#eminutes)
>
> [4.1.3. Submissions 11](#submissions)
>
> [4.1.4. Applications 11](#applications)
>
> [4.1.5. Notifications 13](#notifications)
>
> [4.1.6. Bsblocks 14](#bsblocks)
>
> [4.1.7. Cases 14](#cases)
>
> [4.1.8. Oauthtokens 16](#oauthtokens)
>
> [4.1.9. Sysfilerefs 17](#sysfilerefs)
>
> [4.1.10. Attachments 18](#attachments)
>
> [4.1.11. Users 19](#users)
>
> [4.1.12. Adrblkfilerefs 20](#adrblkfilerefs)

# 1. Introduction

This document provides a description of data catalogue of the Combined
System Development Services of the LSCP of the Buildings Department.

This data catalogue is based on the analysis of the `bd` database, last updated on 2025/3/4 ??10:10:39.

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
| ID    | Identifier           |
| Ref   | Reference            |
| Dt    | Date                 |
| No    | Number               |
| CN    | Chinese              |
| EN    | English              |
| GR    | General Referee      |
| BS    | Building Surveyor    |
| SBS   | Senior Building Surveyor |
| TBC   | To Be Confirmed      |

# 3. Data Entity Description

This section states all the entities in the LSCP Database.

The following section describes how the LSCP entities can be mapped onto
physical data design.

-   Entities list for LSCP Data

| **Item** | **Entity Name** | **Entity Description** |
|----------|-----------------|------------------------|
| 1        | tasks           | Tasks related to applications or cases. |
| 2        | eminutes        | Electronic minutes, likely for meeting records. |
| 3        | submissions     | Application submissions. |
| 4        | applications    | Applications for licensing self-certification. |
| 5        | notifications   | System notifications for users. |
| 6        | bsblocks        | Building blocks information, potentially geographical. |
| 7        | cases           | Cases related to building regulations or applications. |
| 8        | oauthtokens     | OAuth tokens for API authentication. |
| 9        | sysfilerefs     | System file references, metadata for uploaded files. |
| 10       | attachments     | Attachments to applications or other entities. |
| 11       | users           | User accounts and profiles. |
| 12       | adrblkfilerefs  | Address block file references, related to geographical data. |

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
> BIGINT: The BIGINT data type is used to store larger integer value. e.g. from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.
>
> NVARCHAR: The NVARCHAR data type stores character data in a variable-length field.
>
> DATETIME2: "DATETIME2" data type is used to store date and time values.
>
> UNIQUEIDENTIFIER: A column or local variable of unique identifier data type can be initialized to a value.
>
> BIT: BIT data type is used to represent a Boolean value.
>
> **Field Length** - Specify the max number of characters of string field
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

### 4.1.1. Tasks

> Entity Name: tasks
>
> Description: Tasks related to applications or cases.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v             | Version         | objectId, int   |                 |               | N               | N               |
| _id             | Task ID         | objectId        |                 | Y             | Y               | N               |
| application     | Application Ref | objectId        |                 |               | N               | Y               |
| createdAt       | Created Date    | date            |                 |               | N               | N               |
| status          | Task Status     | string          |                 |               | N               | N               |
| submissionCase  | Case Ref        | objectId        |                 |               | N               | Y               |
| taskType        | Task Type       | string          |                 |               | N               | N               |
| team            | Team            | string          |                 |               | N               | N               |
| user            | User Ref        | string, objectId|                 |               | N               | Y               |

### 4.1.2. Eminutes

> Entity Name: eminutes
>
> Description: Electronic minutes, likely for meeting records.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v             | Version         | int             |                 |               | N               | N               |
| _id             | Eminute ID      | objectId        |                 | Y             | Y               | N               |
| comment         | Comment         | string          |                 |               | N               | N               |
| content         | Content         | string          |                 |               | N               | N               |
| createdAt       | Created Date    | date            |                 |               | N               | N               |
| efolio          | Efolio Ref      | string          |                 |               | N               | N               |
| eminuteId       | Eminute ID      | string          |                 |               | N               | N               |
| from            | From User Ref   | objectId, string|                 |               | N               | Y               |
| status          | Status          | string          |                 |               | N               | N               |
| subject         | Subject         | string          |                 |               | N               | N               |
| submissionCase  | Case Ref        | objectId        |                 |               | N               | Y               |
| sysFileRefId    | File Ref ID     | string          |                 |               | N               | Y               |
| to              | To User Ref     | objectId, string|                 |               | N               | Y               |

### 4.1.3. Submissions

> Entity Name: submissions
>
> Description: Application submissions.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| *No Fields Defined* |                 |                  |                  |               |                 |                 |

### 4.1.4. Applications

> Entity Name: applications
>
> Description: Applications for licensing self-certification.

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|-----------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| APP13                   | APP13                       | object, array   |                 |               | N               | N               |
| AddressOfPremiseCN      | Premise Address CN          | string          |                 |               | N               | N               |
| AddressOfPremiseCNFloor | Premise Address CN Floor    | string          |                 |               | N               | N               |
| AddressOfPremiseCNUnit  | Premise Address CN Unit     | string          |                 |               | N               | N               |
| AddressOfPremiseEN      | Premise Address EN          | string          |                 |               | N               | N               |
| AddressOfPremiseENFloor | Premise Address EN Floor    | string          |                 |               | N               | N               |
| AddressOfPremiseENUnit  | Premise Address EN Unit     | string          |                 |               | N               | N               |
| AgeOfStudent            | Age of Student              | null, string    |                 |               | N               | N               |
| ApplicantAddress        | Applicant Address           | string          |                 |               | N               | N               |
| ApplicantEmail          | Applicant Email             | string          |                 |               | N               | N               |
| ApplicantFax            | Applicant Fax               | string          |                 |               | N               | N               |
| ApplicantMobile         | Applicant Mobile            | string          |                 |               | N               | N               |
| ApplicantName           | Applicant Name              | string          |                 |               | N               | N               |
| ApplicantNameCN         | Applicant Name CN           | string          |                 |               | N               | N               |
| ApplicantNameEN         | Applicant Name EN           | null, string    |                 |               | N               | N               |
| ApplicantTel            | Applicant Tel               | null, string    |                 |               | N               | N               |
| ApplicationNo           | Application Number          | null, string    |                 |               | N               | N               |
| ApplicationType         | Application Type            | string          |                 |               | N               | N               |
| Area                    | Area                        | string          |                 |               | N               | N               |
| BlockID                 | Block ID                    | string          |                 |               | N               | N               |
| ContactPerson           | Contact Person              | string          |                 |               | N               | N               |
| ContactPersonCN         | Contact Person CN           | string          |                 |               | N               | N               |
| ContactPersonEN         | Contact Person EN           | string          |                 |               | N               | N               |
| ContactPersonEmail      | Contact Person Email        | string          |                 |               | N               | N               |
| ContactPersonTel        | Contact Person Tel          | string          |                 |               | N               | N               |
| DescriptionOfSchool     | Description of School       | string, null    |                 |               | N               | N               |
| District                | District                    | string          |                 |               | N               | N               |
| EstimatedNoOfStudent    | Estimated Number of Student | int, null       |                 |               | N               | N               |
| FileReference           | File Reference              | string          |                 |               | N               | N               |
| NameOfSchoolCN          | Name of School CN           | string          |                 |               | N               | N               |
| NameOfSchoolEN          | Name of School EN           | string          |                 |               | N               | N               |
| Region                  | Region                      | string          |                 |               | N               | N               |
| RelatedPremise          | Related Premise             | string          |                 |               | N               | N               |
| RelatedPremises         | Related Premises            | array           |                 |               | N               | N               |
| SelfCertification      | Self Certification          | object, null    |                 |               | N               | N               |
| StructuralCalculation   | Structural Calculation      | object          |                 |               | N               | N               |
| SubmissionType          | Submission Type             | string          |                 |               | N               | N               |
| __v                     | Version                     | int             |                 |               | N               | N               |
| _id                     | Application ID              | objectId        |                 | Y             | Y               | N               |
| address                 | Address Object              | object          |                 |               | N               | N               |
| assignedBS              | Assigned Building Surveyor Ref | objectId, string, null |         |               | N               | Y               |
| assignedGR              | Assigned General Referee Ref| objectId, null  |                 |               | N               | Y               |
| assignedSBS             | Assigned Senior Building Surveyor Ref | string, null      |                 |               | N               | Y               |
| createdAt               | Created Date                | date            |                 |               | N               | N               |
| updatedAt               | Updated Date                | date            |                 |               | N               | N               |

### 4.1.5. Notifications

> Entity Name: notifications
>
> Description: System notifications for users.

| **Field Name**     | **Description**       | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-----------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                  | Version               | int             |                 |               | N               | N               |
| _id                  | Notification ID       | objectId        |                 | Y             | Y               | N               |
| createdAt            | Created Date          | date            |                 |               | N               | N               |
| eminute              | Eminute Ref         | objectId        |                 |               | N               | Y               |
| notificationType     | Notification Type     | string          |                 |               | N               | N               |
| requireSendEmail     | Require Send Email    | bool            |                 |               | N               | N               |
| task                 | Task Ref              | objectId        |                 |               | N               | Y               |
| user                 | User Ref              | string          |                 |               | N               | Y               |

### 4.1.6. Bsblocks

> Entity Name: bsblocks
>
> Description: Building blocks information, potentially geographical.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v             | Version         | int             |                 |               | N               | N               |
| _id             | BSBlock ID      | objectId        |                 | Y             | Y               | N               |
| bdgis           | BDGIS Code      | string          |                 |               | N               | N               |
| blockId         | Block ID        | string          |                 |               | N               | N               |

### 4.1.7. Cases

> Entity Name: cases
>
> Description: Cases related to building regulations or applications.

| **Field Name**              | **Description**                 | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------------|---------------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| ActualReplyDate             | Actual Reply Date               | null, date      |                 |               | N               | N               |
| Area                        | Area                            | string          |                 |               | N               | N               |
| AuditResult                 | Audit Result                    | string          |                 |               | N               | N               |
| CaseOfficer                 | Case Officer                    | string          |                 |               | N               | N               |
| Category                    | Category                        | string          |                 |               | N               | N               |
| District                    | District                        | string          |                 |               | N               | N               |
| FileReference               | File Reference                  | string          |                 |               | N               | N               |
| LAFileReference             | LA File Reference               | object          |                 |               | N               | N               |
| Nature                      | Nature                          | null, string    |                 |               | N               | N               |
| ObjectiontoLR               | Objection to LR                 | string          |                 |               | N               | N               |
| ReceivedDate                | Received Date                   | date, null      |                 |               | N               | N               |
| Referrer                    | Referrer                        | object          |                 |               | N               | N               |
| Region                      | Region                          | string          |                 |               | N               | N               |
| Remarks                     | Remarks                         | string          |                 |               | N               | N               |
| Reminders                   | Reminders                       | array           |                 |               | N               | N               |
| SubmissionType              | Submission Type                 | string          |                 |               | N               | N               |
| SubstantialReplyDate        | Substantial Reply Date          | null, date      |                 |               | N               | N               |
| TargetReplyDate             | Target Reply Date               | date, null      |                 |               | N               | N               |
| ThreeTierReqt               | Three Tier Requirement          | string          |                 |               | N               | N               |
| ViaSCS                      | Via SCS                         | bool            |                 |               | N               | N               |
| __v                         | Version                         | int             |                 |               | N               | N               |
| _id                         | Case ID                         | objectId        |                 | Y             | Y               | N               |
| application                 | Application Ref                 | objectId        |                 |               | N               | Y               |
| assignedBS                  | Assigned Building Surveyor Ref   | objectId        |                 |               | N               | Y               |
| assignedGR                  | Assigned General Referee Ref    | objectId        |                 |               | N               | Y               |
| building_information        | Building Information Object     | object          |                 |               | N               | N               |
| caseDescription             | Case Description Object         | object          |                 |               | N               | N               |
| caseOfficerReceive          | Case Officer Receive User       | string          |                 |               | N               | Y               |
| caseOfficerReply            | Case Officer Reply User         | string          |                 |               | N               | Y               |
| createdAt                   | Created Date                    | date            |                 |               | N               | N               |
| deck_study                  | Deck Study Object               | object          |                 |               | N               | N               |
| documentChecklist           | Document Checklist Object       | object          |                 |               | N               | N               |
| dv                          | DV Object                       | object          |                 |               | N               | N               |
| frc                         | FRC Object                      | object          |                 |               | N               | N               |
| misc                        | Miscellaneous Object            | object          |                 |               | N               | N               |
| moe                         | MOE Object                      | object          |                 |               | N               | N               |
| seniorCaseOfficerReceive    | Senior Case Officer Receive User| string          |                 |               | N               | Y               |
| seniorCaseOfficerReply      | Senior Case Officer Reply User  | string          |                 |               | N               | Y               |
| site_inspection             | Site Inspection Object          | object          |                 |               | N               | N               |
| structural_ccc_bs           | Structural CCC BS Object        | object          |                 |               | N               | N               |
| structural_schnlh           | Structural SCHNLH Object        | object          |                 |               | N               | N               |
| structural_schnlhkinds      | Structural SCHNLH Kinds Object  | object          |                 |               | N               | N               |
| team                        | Team                            | string          |                 |               | N               | N               |
| ubw                         | UBW Object                      | object          |                 |               | N               | N               |
| updatedAt                   | Updated Date                    | date            |                 |               | N               | N               |

### 4.1.8. Oauthtokens

> Entity Name: oauthtokens
>
> Description: OAuth tokens for API authentication.

| **Field Name**            | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------------|-----------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                         | Version                     | int             |                 |               | N               | N               |
| _id                         | OAuth Token ID              | objectId        |                 | Y             | Y               | N               |
| accessToken               | Access Token                | string          |                 |               | N               | N               |
| accessTokenExpiresAt      | Access Token Expires At     | date            |                 |               | N               | N               |
| client                      | Client Object               | object          |                 |               | N               | N               |
| refreshToken              | Refresh Token               | string          |                 |               | N               | N               |
| refreshTokenExpiresAt     | Refresh Token Expires At    | date            |                 |               | N               | N               |
| user                        | User Ref                    | objectId        |                 |               | N               | Y               |

### 4.1.9. Sysfilerefs

> Entity Name: sysfilerefs
>
> Description: System file references, metadata for uploaded files.

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|-----------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                     | Version                     | int             |                 |               | N               | N               |
| _id                     | SysFileRef ID               | objectId        |                 | Y             | Y               | N               |
| createdDt               | Created Date                | date            |                 |               | N               | N               |
| createdName             | Created By Name             | null, string    |                 |               | N               | N               |
| createdPost             | Created By Post             | null, string    |                 |               | N               | N               |
| createdSection          | Created By Section          | null, string    |                 |               | N               | N               |
| display                 | Display Name                | string          |                 |               | N               | N               |
| dvExceed                | DV Exceed                     | null, string    |                 |               | N               | N               |
| dvStatusDt              | DV Status Date              | null, date      |                 |               | N               | N               |
| frefPref                | File Ref Prefix             | string, null    |                 |               | N               | N               |
| frefSeq                 | File Ref Sequence           | null, string    |                 |               | N               | N               |
| frefSuf                 | File Ref Suffix             | null, string    |                 |               | N               | N               |
| frefYr                  | File Ref Year               | null, string    |                 |               | N               | N               |
| lastModifiedDt          | Last Modified Date          | date            |                 |               | N               | N               |
| lastModifiedName        | Last Modified By Name       | null, string    |                 |               | N               | N               |
| lastModifiedPost        | Last Modified By Post       | null, string    |                 |               | N               | N               |
| lastModifiedSection     | Last Modified By Section    | null            |                 |               | N               | N               |
| sysFileRefId            | System File Reference ID    | string          |                 |               | N               | N               |

### 4.1.10. Attachments

> Entity Name: attachments
>
> Description: Attachments to applications or other entities.

| **Field Name**     | **Description**       | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-----------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                  | Version               | int             |                 |               | N               | N               |
| _id                  | Attachment ID       | objectId        |                 | Y             | Y               | N               |
| application          | Application Ref       | objectId        |                 |               | N               | Y               |
| createdAt            | Created Date          | date            |                 |               | N               | N               |
| efolio               | Efolio Ref          | null, string    |                 |               | N               | N               |
| file                 | File Object/Path      | object, string  |                 |               | N               | N               |
| filePartNo           | File Part Number      | string          |                 |               | N               | N               |
| receivedDate         | Received Date         | date            |                 |               | N               | N               |
| remarks              | Remarks               | string          |                 |               | N               | N               |
| subType              | Sub Type              | string          |                 |               | N               | N               |
| submissionCase       | Case Ref            | objectId        |                 |               | N               | Y               |
| sysFileRefId         | SysFileRef Ref        | string          |                 |               | N               | Y               |
| type                 | Attachment Type     | string          |                 |               | N               | N               |
| updatedAt            | Updated Date          | date            |                 |               | N               | N               |

### 4.1.11. Users

> Entity Name: users
>
> Description: User accounts and profiles.

| **Field Name**          | **Description**           | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|---------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                     | Version                   | int             |                 |               | N               | N               |
| _id                     | User ID                   | objectId        |                 | Y             | Y               | N               |
| bdgis                   | BDGIS Code                | string          |                 |               | N               | N               |
| begis                   | BEGIS Code                | string          |                 |               | N               | N               |
| delegateTo              | Delegate To User Ref      | string          |                 |               | N               | Y               |
| department              | Department                | string          |                 |               | N               | N               |
| email                   | Email                     | string          |                 |               | N               | N               |
| group                   | Group                     | string          |                 |               | N               | N               |
| lastLoginAt             | Last Login Date           | date            |                 |               | N               | N               |
| letterLongPosition      | Letter Long Position      | string          |                 |               | N               | N               |
| letterLongPositionCn    | Letter Long Position CN   | string          |                 |               | N               | N               |
| letterName              | Letter Name               | string          |                 |               | N               | N               |
| letterNameCn            | Letter Name CN            | string          |                 |               | N               | N               |
| letterPosition          | Letter Position           | string          |                 |               | N               | N               |
| letterPositionCn        | Letter Position CN        | string          |                 |               | N               | N               |
| lock                    | Account Lock Status       | bool            |                 |               | N               | N               |
| luPostName              | LU Post Name              | string          |                 |               | N               | N               |
| name                    | Name                      | string          |                 |               | N               | N               |
| notificationEmail       | Notification Email        | string          |                 |               | N               | N               |
| osdpEmail               | OSDP Email                | string          |                 |               | N               | N               |
| osdpLoginId             | OSDP Login ID             | string          |                 |               | N               | N               |
| password                | Password (hashed)         | string          |                 |               | N               | N               |
| phoneNumber             | Phone Number              | string          |                 |               | N               | N               |
| position                | Position                  | string          |                 |               | N               | N               |
| role                    | Role                      | string          |                 |               | N               | N               |
| team                    | Team                      | string          |                 |               | N               | N               |
| userType                | User Type                 | string          |                 |               | N               | N               |

### 4.1.12. Adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: Address block file references, related to geographical data.

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|-----------------------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                     | Version                     | int             |                 |               | N               | N               |
| _id                     | AdrBlkFileRef ID            | objectId        |                 | Y             | Y               | N               |
| adrBlkFileRefId         | Address Block File Ref ID   | string          |                 |               | N               | N               |
| adrBlkId                | Address Block ID            | string          |                 |               | N               | N               |
| createdDt               | Created Date                | date            |                 |               | N               | N               |
| createdName             | Created By Name             | null, string    |                 |               | N               | N               |
| createdPost             | Created By Post             | string          |                 |               | N               | N               |
| createdSection          | Created By Section          | null, string    |                 |               | N               | N               |
| lastModifiedDt          | Last Modified Date          | date            |                 |               | N               | N               |
| lastModifiedName        | Last Modified By Name       | null, string    |                 |               | N               | N               |
| lastModifiedPost        | Last Modified By Post       | string          |                 |               | N               | N               |
| lastModifiedSection     | Last Modified By Section    | string, null    |                 |               | N               | N               |
| sysFileRefId            | SysFileRef Ref              | string          |                 |               | N               | Y               |
```