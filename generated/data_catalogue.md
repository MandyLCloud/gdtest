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
| 1                     | 1st draft based on Database Schema | All                                  | 0.1                       | 16/01/2025 |                    |
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
> [4.1.8. oauthtokens 17](#oauthtokens)
>
> [4.1.9. sysfilerefs 18](#sysfilerefs)
>
> [4.1.10. attachments 19](#attachments)
>
> [4.1.11. users 20](#users)
>
> [4.1.12. adrblkfilerefs 22](#adrblkfilerefs)

# 1. Introduction

This document provides a description of data catalogue of the Combined
System Development Services of the LSCP of the Buildings Department.

This data catalogue is based on the analysis of the 'bd' database, last updated on 2025/3/4 ??10:10:39.

**Database Statistics:**
- Database Name: bd
- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1278983
- Total Data Size: 371.24 MB

# 2. Definitions

| Terms | Definitions          |
|-------|----------------------|
| BD    | Buildings Department |
| LSCP  | Licensing Self-Certification Portal |
| MB    | Megabytes            |
| KB    | Kilobytes            |
| ObjectId | Unique identifier used in database |
| Date  | Date and time value  |
| String| Textual data         |
| Int   | Integer number       |
| Bool  | Boolean value (true/false) |
| Object| Complex data structure |
| Array | List of data items  |
| Null  | Absence of value     |

# 3. Data Entity Description

This section states all the entities in the LSCP Database.

The following section describes how the LSCP entities can be mapped onto
physical data design.

-   Entities list for LSCP Data

| **Item** | **Entity Name** | **Entity Description** |
|----------|-----------------|------------------------|
| 1        | tasks           | Tasks Collection       |
| 2        | eminutes        | E-minutes Collection     |
| 3        | submissions     | Submissions Collection |
| 4        | applications    | Applications Collection|
| 5        | notifications   | Notifications Collection|
| 6        | bsblocks        | BS Blocks Collection   |
| 7        | cases           | Cases Collection       |
| 8        | oauthtokens     | OAuth Tokens Collection|
| 9        | sysfilerefs     | System File References Collection |
| 10       | attachments     | Attachments Collection |
| 11       | users           | Users Collection       |
| 12       | adrblkfilerefs  | ADR Block File References Collection |

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
> Description: Collection to store tasks.
>
> **Collection Statistics:**
> - Document Count: 5523
> - Size: 0.99 MB
> - Average Document Size: 0.18 KB

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|------------------|------------------|---------------|-----------------|-----------------|
| __v           | Version         | BIGINT/UNIQUEIDENTIFIER |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| application   | Application ID  | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| createdAt     | Creation Time   | DATETIME2        |                  |               |                 |                 |
| status        | Task Status     | NVARCHAR         |                  |               |                 |                 |
| submissionCase| Submission Case ID| UNIQUEIDENTIFIER |                  |               |                 | Y               |
| taskType      | Task Type       | NVARCHAR         |                  |               |                 |                 |
| team          | Team            | NVARCHAR         |                  |               |                 |                 |
| user          | User ID         | NVARCHAR/UNIQUEIDENTIFIER |                  |               |                 | Y               |

### 4.1.2. eminutes

> Entity Name: eminutes
>
> Description: Collection to store e-minutes.
>
> **Collection Statistics:**
> - Document Count: 133
> - Size: 0.03 MB
> - Average Document Size: 0.24 KB

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|------------------|------------------|---------------|-----------------|-----------------|
| __v           | Version         | BIGINT           |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| comment       | Comment         | NVARCHAR         |                  |               |                 |                 |
| content       | Content         | NVARCHAR         |                  |               |                 |                 |
| createdAt     | Creation Time   | DATETIME2        |                  |               |                 |                 |
| efolio        | E-folio ID      | NVARCHAR         |                  |               |                 |                 |
| eminuteId     | E-minute ID     | NVARCHAR         |                  |               |                 |                 |
| from          | Sender User ID  | UNIQUEIDENTIFIER/NVARCHAR |                  |               |                 | Y               |
| status        | Status          | NVARCHAR         |                  |               |                 |                 |
| subject       | Subject         | NVARCHAR         |                  |               |                 |                 |
| submissionCase| Submission Case ID| UNIQUEIDENTIFIER |                  |               |                 | Y               |
| sysFileRefId  | System File Reference ID | NVARCHAR         |                  |               |                 |                 |
| to            | Recipient User ID| UNIQUEIDENTIFIER/NVARCHAR |                  |               |                 | Y               |

### 4.1.3. submissions

> Entity Name: submissions
>
> Description: Collection to store submissions.
>
> **Collection Statistics:**
> - Document Count: 0
> - Size: 0.00 MB
> - Average Document Size: 0.00 KB

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|------------------|------------------|---------------|-----------------|-----------------|
| *No fields defined in schema analysis* |                 |                  |                  |               |                 |                 |

### 4.1.4. applications

> Entity Name: applications
>
> Description: Collection to store applications.
>
> **Collection Statistics:**
> - Document Count: 381
> - Size: 0.36 MB
> - Average Document Size: 0.96 KB

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| APP13                   | APP13                       | OBJECT/ARRAY     |                  |               |                 |                 |
| AddressOfPremiseCN      | Address Of Premise CN       | NVARCHAR         |                  |               |                 |                 |
| AddressOfPremiseCNFloor | Address Of Premise CN Floor | NVARCHAR         |                  |               |                 |                 |
| AddressOfPremiseCNUnit  | Address Of Premise CN Unit  | NVARCHAR         |                  |               |                 |                 |
| AddressOfPremiseEN      | Address Of Premise EN       | NVARCHAR         |                  |               |                 |                 |
| AddressOfPremiseENFloor | Address Of Premise EN Floor | NVARCHAR         |                  |               |                 |                 |
| AddressOfPremiseENUnit  | Address Of Premise EN Unit  | NVARCHAR         |                  |               |                 |                 |
| AgeOfStudent            | Age Of Student              | NVARCHAR         |                  |               |                 |                 |
| ApplicantAddress        | Applicant Address           | NVARCHAR         |                  |               |                 |                 |
| ApplicantEmail          | Applicant Email             | NVARCHAR         |                  |               |                 |                 |
| ApplicantFax            | Applicant Fax               | NVARCHAR         |                  |               |                 |                 |
| ApplicantMobile         | Applicant Mobile            | NVARCHAR         |                  |               |                 |                 |
| ApplicantName           | Applicant Name              | NVARCHAR         |                  |               |                 |                 |
| ApplicantNameCN         | Applicant Name CN           | NVARCHAR         |                  |               |                 |                 |
| ApplicantNameEN         | Applicant Name EN           | NVARCHAR         |                  |               |                 |                 |
| ApplicantTel            | Applicant Tel               | NVARCHAR         |                  |               |                 |                 |
| ApplicationNo           | Application No              | NVARCHAR         |                  |               |                 |                 |
| ApplicationType         | Application Type            | NVARCHAR         |                  |               |                 |                 |
| Area                    | Area                        | NVARCHAR         |                  |               |                 |                 |
| BlockID                 | Block ID                    | NVARCHAR         |                  |               |                 |                 |
| ContactPerson           | Contact Person              | NVARCHAR         |                  |               |                 |                 |
| ContactPersonCN         | Contact Person CN           | NVARCHAR         |                  |               |                 |                 |
| ContactPersonEN         | Contact Person EN           | NVARCHAR         |                  |               |                 |                 |
| ContactPersonEmail      | Contact Person Email        | NVARCHAR         |                  |               |                 |                 |
| ContactPersonTel        | Contact Person Tel          | NVARCHAR         |                  |               |                 |                 |
| DescriptionOfSchool     | Description Of School       | NVARCHAR         |                  |               |                 |                 |
| District                | District                    | NVARCHAR         |                  |               |                 |                 |
| EstimatedNoOfStudent    | Estimated No Of Student     | BIGINT/NVARCHAR  |                  |               |                 |                 |
| FileReference           | File Reference              | NVARCHAR         |                  |               |                 |                 |
| NameOfSchoolCN          | Name Of School CN           | NVARCHAR         |                  |               |                 |                 |
| NameOfSchoolEN          | Name Of School EN           | NVARCHAR         |                  |               |                 |                 |
| Region                  | Region                      | NVARCHAR         |                  |               |                 |                 |
| RelatedPremise          | Related Premise             | NVARCHAR         |                  |               |                 |                 |
| RelatedPremises         | Related Premises            | ARRAY            |                  |               |                 |                 |
| SelfCertification       | Self Certification          | OBJECT           |                  |               |                 |                 |
| StructuralCalculation   | Structural Calculation      | OBJECT           |                  |               |                 |                 |
| SubmissionType          | Submission Type             | NVARCHAR         |                  |               |                 |                 |
| __v                     | Version                     | BIGINT           |                  |               |                 |                 |
| _id                     | Document ID                 | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| address                 | Address                     | OBJECT           |                  |               |                 |                 |
| assignedBS              | Assigned BS                 | UNIQUEIDENTIFIER/NVARCHAR |                  |               |                 | Y               |
| assignedGR              | Assigned GR                 | UNIQUEIDENTIFIER/NVARCHAR |                  |               |                 | Y               |
| assignedSBS             | Assigned SBS                | NVARCHAR         |                  |               |                 |                 |
| createdAt               | Creation Time               | DATETIME2        |                  |               |                 |                 |
| updatedAt               | Update Time                 | DATETIME2        |                  |               |                 |                 |

### 4.1.5. notifications

> Entity Name: notifications
>
> Description: Collection to store notifications.
>
> **Collection Statistics:**
> - Document Count: 1837
> - Size: 0.24 MB
> - Average Document Size: 0.13 KB

| **Field Name**     | **Description**         | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                | Version                 | BIGINT           |                  |               |                 |                 |
| _id                | Document ID             | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| createdAt          | Creation Time           | DATETIME2        |                  |               |                 |                 |
| eminute            | E-minute ID             | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| notificationType   | Notification Type       | NVARCHAR         |                  |               |                 |                 |
| requireSendEmail   | Require Send Email      | BIT              |                  |               |                 |                 |
| task               | Task ID                 | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| user               | User ID                 | NVARCHAR         |                  |               |                 |                 |

### 4.1.6. bsblocks

> Entity Name: bsblocks
>
> Description: Collection to store BS Blocks information.
>
> **Collection Statistics:**
> - Document Count: 98397
> - Size: 6.40 MB
> - Average Document Size: 0.07 KB

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|------------------|------------------|---------------|-----------------|-----------------|
| __v           | Version         | BIGINT           |                  |               |                 |                 |
| _id           | Document ID     | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| bdgis         | BDGIS Code      | NVARCHAR         |                  |               |                 |                 |
| blockId       | Block ID        | NVARCHAR         |                  |               |                 |                 |

### 4.1.7. cases

> Entity Name: cases
>
> Description: Collection to store cases.
>
> **Collection Statistics:**
> - Document Count: 451
> - Size: 1.17 MB
> - Average Document Size: 2.65 KB

| **Field Name**              | **Description**               | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------------|-------------------------------|------------------|------------------|---------------|-----------------|-----------------|
| ActualReplyDate             | Actual Reply Date             | DATETIME2        |                  |               |                 |                 |
| Area                        | Area                          | NVARCHAR         |                  |               |                 |                 |
| AuditResult                 | Audit Result                  | NVARCHAR         |                  |               |                 |                 |
| CaseOfficer                 | Case Officer                  | NVARCHAR         |                  |               |                 |                 |
| Category                    | Category                      | NVARCHAR         |                  |               |                 |                 |
| District                    | District                      | NVARCHAR         |                  |               |                 |                 |
| FileReference               | File Reference                | NVARCHAR         |                  |               |                 |                 |
| LAFileReference             | LA File Reference             | OBJECT           |                  |               |                 |                 |
| Nature                      | Nature                        | NVARCHAR         |                  |               |                 |                 |
| ObjectiontoLR               | Objection to LR               | NVARCHAR         |                  |               |                 |                 |
| ReceivedDate                | Received Date                 | DATETIME2        |                  |               |                 |                 |
| Referrer                    | Referrer                      | OBJECT           |                  |               |                 |                 |
| Region                      | Region                        | NVARCHAR         |                  |               |                 |                 |
| Remarks                     | Remarks                       | NVARCHAR         |                  |               |                 |                 |
| Reminders                   | Reminders                     | ARRAY            |                  |               |                 |                 |
| SubmissionType              | Submission Type               | NVARCHAR         |                  |               |                 |                 |
| SubstantialReplyDate        | Substantial Reply Date        | DATETIME2        |                  |               |                 |                 |
| TargetReplyDate             | Target Reply Date             | DATETIME2        |                  |               |                 |                 |
| ThreeTierReqt               | Three Tier Requirement        | NVARCHAR         |                  |               |                 |                 |
| ViaSCS                      | Via SCS                       | BIT              |                  |               |                 |                 |
| __v                         | Version                       | BIGINT           |                  |               |                 |                 |
| _id                         | Document ID                   | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| application                 | Application ID                | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| assignedBS                  | Assigned BS                   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| assignedGR                  | Assigned GR                   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| building_information        | Building Information          | OBJECT           |                  |               |                 |                 |
| caseDescription             | Case Description              | OBJECT           |                  |               |                 |                 |
| caseOfficerReceive          | Case Officer Receive User ID  | NVARCHAR         |                  |               |                 |                 |
| caseOfficerReply            | Case Officer Reply User ID    | NVARCHAR         |                  |               |                 |                 |
| createdAt                   | Creation Time                 | DATETIME2        |                  |               |                 |                 |
| deck_study                  | Deck Study Data               | OBJECT           |                  |               |                 |                 |
| documentChecklist           | Document Checklist Data       | OBJECT           |                  |               |                 |                 |
| dv                          | DV Data                       | OBJECT           |                  |               |                 |                 |
| frc                         | FRC Data                      | OBJECT           |                  |               |                 |                 |
| misc                        | Miscellaneous Data            | OBJECT           |                  |               |                 |                 |
| moe                         | MOE Data                      | OBJECT           |                  |               |                 |                 |
| seniorCaseOfficerReceive    | Senior Case Officer Receive User ID | NVARCHAR         |                  |               |                 |                 |
| seniorCaseOfficerReply      | Senior Case Officer Reply User ID   | NVARCHAR         |                  |               |                 |                 |
| site_inspection             | Site Inspection Data          | OBJECT           |                  |               |                 |                 |
| structural_ccc_bs           | Structural CCC BS Data        | OBJECT           |                  |               |                 |                 |
| structural_schnlh           | Structural SCHNLH Data        | OBJECT           |                  |               |                 |                 |
| structural_schnlhkinds      | Structural SCHNLH Kinds Data  | OBJECT           |                  |               |                 |                 |
| team                        | Team                          | NVARCHAR         |                  |               |                 |                 |
| ubw                         | UBW Data                      | OBJECT           |                  |               |                 |                 |
| updatedAt                   | Update Time                   | DATETIME2        |                  |               |                 |                 |

### 4.1.8. oauthtokens

> Entity Name: oauthtokens
>
> Description: Collection to store OAuth tokens.
>
> **Collection Statistics:**
> - Document Count: 3019
> - Size: 2.29 MB
> - Average Document Size: 0.78 KB

| **Field Name**            | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                       | Version                     | BIGINT           |                  |               |                 |                 |
| _id                       | Document ID                 | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| accessToken               | Access Token                | NVARCHAR         |                  |               |                 |                 |
| accessTokenExpiresAt      | Access Token Expiry Time    | DATETIME2        |                  |               |                 |                 |
| client                    | Client Information          | OBJECT           |                  |               |                 |                 |
| refreshToken              | Refresh Token               | NVARCHAR         |                  |               |                 |                 |
| refreshTokenExpiresAt     | Refresh Token Expiry Time   | DATETIME2        |                  |               |                 |                 |
| user                      | User ID                     | UNIQUEIDENTIFIER |                  |               |                 | Y               |

### 4.1.9. sysfilerefs

> Entity Name: sysfilerefs
>
> Description: Collection to store system file references.
>
> **Collection Statistics:**
> - Document Count: 601808
> - Size: 204.70 MB
> - Average Document Size: 0.35 KB

| **Field Name**        | **Description**           | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|---------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                   | Version                   | BIGINT           |                  |               |                 |                 |
| _id                   | Document ID               | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| createdDt             | Creation Date             | DATETIME2        |                  |               |                 |                 |
| createdName           | Creator Name              | NVARCHAR         |                  |               |                 |                 |
| createdPost           | Creator Post              | NVARCHAR         |                  |               |                 |                 |
| createdSection        | Creator Section           | NVARCHAR         |                  |               |                 |                 |
| display               | Display Name              | NVARCHAR         |                  |               |                 |                 |
| dvExceed              | DV Exceed Status          | NVARCHAR         |                  |               |                 |                 |
| dvStatusDt            | DV Status Date            | DATETIME2        |                  |               |                 |                 |
| frefPref              | File Reference Prefix     | NVARCHAR         |                  |               |                 |                 |
| frefSeq               | File Reference Sequence   | NVARCHAR         |                  |               |                 |                 |
| frefSuf               | File Reference Suffix     | NVARCHAR         |                  |               |                 |                 |
| frefYr                | File Reference Year       | NVARCHAR         |                  |               |                 |                 |
| lastModifiedDt        | Last Modified Date        | DATETIME2        |                  |               |                 |                 |
| lastModifiedName      | Last Modified Name        | NVARCHAR         |                  |               |                 |                 |
| lastModifiedPost      | Last Modified Post        | NVARCHAR         |                  |               |                 |                 |
| lastModifiedSection   | Last Modified Section     | NVARCHAR         |                  |               |                 |                 |
| sysFileRefId          | System File Reference ID  | NVARCHAR         |                  |               |                 |                 |

### 4.1.10. attachments

> Entity Name: attachments
>
> Description: Collection to store attachments.
>
> **Collection Statistics:**
> - Document Count: 370
> - Size: 0.13 MB
> - Average Document Size: 0.37 KB

| **Field Name**     | **Description**         | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                | Version                 | BIGINT           |                  |               |                 |                 |
| _id                | Document ID             | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| application        | Application ID          | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| createdAt          | Creation Time           | DATETIME2        |                  |               |                 |                 |
| efolio             | E-folio ID              | NVARCHAR         |                  |               |                 |                 |
| file               | File Information        | OBJECT/NVARCHAR  |                  |               |                 |                 |
| filePartNo         | File Part Number        | NVARCHAR         |                  |               |                 |                 |
| receivedDate       | Received Date           | DATETIME2        |                  |               |                 |                 |
| remarks            | Remarks                 | NVARCHAR         |                  |               |                 |                 |
| subType            | Sub Type                | NVARCHAR         |                  |               |                 |                 |
| submissionCase     | Submission Case ID      | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| sysFileRefId       | System File Reference ID | NVARCHAR         |                  |               |                 |                 |
| type               | Attachment Type         | NVARCHAR         |                  |               |                 |                 |
| updatedAt          | Update Time             | DATETIME2        |                  |               |                 |                 |

### 4.1.11. users

> Entity Name: users
>
> Description: Collection to store user information.
>
> **Collection Statistics:**
> - Document Count: 116
> - Size: 0.04 MB
> - Average Document Size: 0.39 KB

| **Field Name**        | **Description**           | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|---------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                   | Version                   | BIGINT           |                  |               |                 |                 |
| _id                   | Document ID               | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| bdgis                 | BDGIS Code                | NVARCHAR         |                  |               |                 |                 |
| begis                 | BEGIS Code                | NVARCHAR         |                  |               |                 |                 |
| delegateTo            | Delegate To User ID       | NVARCHAR         |                  |               |                 |                 |
| department            | Department                | NVARCHAR         |                  |               |                 |                 |
| email                 | Email Address             | NVARCHAR         |                  |               |                 |                 |
| group                 | Group                     | NVARCHAR         |                  |               |                 |                 |
| lastLoginAt           | Last Login Time           | DATETIME2        |                  |               |                 |                 |
| letterLongPosition    | Letter Long Position      | NVARCHAR         |                  |               |                 |                 |
| letterLongPositionCn  | Letter Long Position (CN)| NVARCHAR         |                  |               |                 |                 |
| letterName            | Letter Name               | NVARCHAR         |                  |               |                 |                 |
| letterNameCn          | Letter Name (CN)          | NVARCHAR         |                  |               |                 |                 |
| letterPosition        | Letter Position           | NVARCHAR         |                  |               |                 |                 |
| letterPositionCn      | Letter Position (CN)      | NVARCHAR         |                  |               |                 |                 |
| lock                  | Account Lock Status       | BIT              |                  |               |                 |                 |
| luPostName            | LU Post Name              | NVARCHAR         |                  |               |                 |                 |
| name                  | Name                      | NVARCHAR         |                  |               |                 |                 |
| notificationEmail     | Notification Email        | NVARCHAR         |                  |               |                 |                 |
| osdpEmail             | OSDP Email                | NVARCHAR         |                  |               |                 |                 |
| osdpLoginId           | OSDP Login ID             | NVARCHAR         |                  |               |                 |                 |
| password              | Password (hashed)         | NVARCHAR         |                  |               |                 |                 |
| phoneNumber           | Phone Number              | NVARCHAR         |                  |               |                 |                 |
| position              | Position                  | NVARCHAR         |                  |               |                 |                 |
| role                  | Role                      | NVARCHAR         |                  |               |                 |                 |
| team                  | Team                      | NVARCHAR         |                  |               |                 |                 |
| userType              | User Type                 | NVARCHAR         |                  |               |                 |                 |

### 4.1.12. adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: Collection to store ADR Block File References.
>
> **Collection Statistics:**
> - Document Count: 566948
> - Size: 154.89 MB
> - Average Document Size: 0.28 KB

| **Field Name**        | **Description**               | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-------------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                   | Version                       | BIGINT           |                  |               |                 |                 |
| _id                   | Document ID                   | UNIQUEIDENTIFIER |                  | Y             | Y               |                 |
| adrBlkFileRefId       | ADR Block File Reference ID   | NVARCHAR         |                  |               |                 |                 |
| adrBlkId              | ADR Block ID                  | NVARCHAR         |                  |               |                 |                 |
| createdDt             | Creation Date                 | DATETIME2        |                  |               |                 |                 |
| createdName           | Creator Name                  | NVARCHAR         |                  |               |                 |                 |
| createdPost           | Creator Post                  | NVARCHAR         |                  |               |                 |                 |
| createdSection        | Creator Section               | NVARCHAR         |                  |               |                 |                 |
| lastModifiedDt        | Last Modified Date            | DATETIME2        |                  |               |                 |                 |
| lastModifiedName      | Last Modified Name            | NVARCHAR         |                  |               |                 |                 |
| lastModifiedPost      | Last Modified Post            | NVARCHAR         |                  |               |                 |                 |
| lastModifiedSection   | Last Modified Section         | NVARCHAR         |                  |               |                 |                 |
| sysFileRefId          | System File Reference ID      | NVARCHAR         |                  |               |                 |                 |
```