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
> [4.1.1. Collections 9](#collections)
>
> > [4.1.1.1. tasks 10](#tasks)
>
> > [4.1.1.2. eminutes 11](#eminutes)
>
> > [4.1.1.3. submissions 12](#submissions)
>
> > [4.1.1.4. applications 12](#applications)
>
> > [4.1.1.5. notifications 14](#notifications)
>
> > [4.1.1.6. bsblocks 15](#bsblocks)
>
> > [4.1.1.7. cases 15](#cases)
>
> > [4.1.1.8. oauthtokens 17](#oauthtokens)
>
> > [4.1.1.9. sysfilerefs 18](#sysfilerefs)
>
> > [4.1.1.10. attachments 19](#attachments)
>
> > [4.1.1.11. users 20](#users)
>
> > [4.1.1.12. adrblkfilerefs 21](#adrblkfilerefs)


# 1. Introduction

This document provides a description of data catalogue of the Combined
System Development Services of the LSCP of the Buildings Department. This data catalogue is based on the analysis of the database named **bd**. The database contains information related to the Licensing Self-Certification Portal (LSCP) and its associated functionalities.

# 2. Definitions

| Terms | Definitions          |
|-------|----------------------|
| BD    | Buildings Department |
| LSCP  | Licensing Self-Certification Portal |
| MB    | Megabytes            |
| KB    | Kilobytes            |
| ObjectId | MongoDB ObjectId, a 12-byte BSON type |
| String | Textual data |
| Int   | Integer number |
| Date  | Date and time information |
| Bool  | Boolean value (true/false) |
| Object | Complex data structure, potentially nested |
| Array | Ordered list of values |
| Null  | Absence of a value |

# 3. Data Entity Description

This section states all the entities (collections) in the LSCP Database (**bd**).

The following section describes how the LSCP entities are physically designed in the database.

-   Entities list for LSCP Data

| **Item** | **Entity Name** | **Entity Description** |
|----------|-----------------|------------------------|
| 1        | tasks           | Tasks related to applications or cases |
| 2        | eminutes        | Electronic minutes of meetings or discussions |
| 3        | submissions     | Application submissions |
| 4        | applications    | Applications for licensing self-certification |
| 5        | notifications   | System notifications for users |
| 6        | bsblocks        | Building blocks information |
| 7        | cases           | Cases related to applications, potentially for follow-up or audit |
| 8        | oauthtokens     | OAuth tokens for API authentication |
| 9        | sysfilerefs     | System file references, metadata for files |
| 10       | attachments     | File attachments associated with applications or cases |
| 11       | users           | User accounts and profiles |
| 12       | adrblkfilerefs  | Address block file references |

#

# 4. Equipment Configuration

This section details the data items for each database collection in the physical design. The explanation for columns is as follows.

Database-level validation is not utilized. Instead, validations are implemented on the server side.

> **Entity Name** - Name of database collection
>
> **Description** - Description of entity (collection)
>
> **Field Name** - Name of attribute (field) within a document
>
> **Field Format** - Type of the data item as identified in the database schema analysis. Mapped to general data types where applicable.
>
> BIGINT: The BIGINT data type is used to store larger integer value. e.g. from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.
>
> NVARCHAR: The NVARCHAR data type stores character data in a variable-length field.
>
> DATETIME2: "DATETIME2" data type is used to store date and time values.
>
> UNIQUEIDENTIFIER: A column or local variable of unique identifier data type can be initialized to a value. (Represents ObjectId in MongoDB context)
>
> BIT: BIT data type is used to represent a Boolean value.
>
> **Field Length** - Specify the max number of characters of string field (Variable for NVARCHAR, N/A for other types in this context)
>
> **Mandatory** - Specify if the data item is mandatory. ?Y? if true. (Information not available from schema analysis)
>
> **Primary Key** - Indicates if data item is part of the Primary Key. (Assumed '_id' is Primary Key)
>
> **Foreign Key** - Indicates if data item is likely a Foreign Key referencing another collection. (Inferred based on field names, may not be explicitly defined)

##

## 4.1 Objective

> Name Space: LSCP
>
> Description: LSCP Data Storage for **bd** database
>
> Storage Location: TBC (To Be Confirmed)
>
> File Name: TBC (To Be Confirmed)

### 4.1.1. Collections

This section describes the fields within each collection of the **bd** database.

#### 4.1.1.1. tasks

> Entity Name: tasks
>
> Description: Collection to store tasks related to applications or cases.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|------------------|------------------|---------------|-----------------|-----------------|
| __v             | Version field     | Int, ObjectId    | N/A              |               |                 |                 |
| _id             | Task ID         | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| application     | Application ID  | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| createdAt       | Creation Date   | DATETIME2        | N/A              |               |                 |                 |
| status          | Task Status     | NVARCHAR         | Variable         |               |                 |                 |
| submissionCase  | Case ID         | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| taskType        | Type of Task    | NVARCHAR         | Variable         |               |                 |                 |
| team            | Team assigned   | NVARCHAR         | Variable         |               |                 |                 |
| user            | User assigned   | NVARCHAR, UNIQUEIDENTIFIER | Variable/N/A   |               |                 | Y               |

#### 4.1.1.2. eminutes

> Entity Name: eminutes
>
> Description: Collection for electronic minutes, potentially for meetings or case discussions.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|------------------|------------------|---------------|-----------------|-----------------|
| __v             | Version field     | Int              | N/A              |               |                 |                 |
| _id             | Minute ID       | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| comment         | Comment content | NVARCHAR         | Variable         |               |                 |                 |
| content         | Minute content  | NVARCHAR         | Variable         |               |                 |                 |
| createdAt       | Creation Date   | DATETIME2        | N/A              |               |                 |                 |
| efolio          | Efolio reference| NVARCHAR         | Variable         |               |                 |                 |
| eminuteId       | Minute Identifier| NVARCHAR         | Variable         |               |                 |                 |
| from            | Sender ID       | UNIQUEIDENTIFIER, NVARCHAR | N/A/Variable   |               |                 | Y               |
| status          | Minute Status   | NVARCHAR         | Variable         |               |                 |                 |
| subject         | Minute Subject  | NVARCHAR         | Variable         |               |                 |                 |
| submissionCase  | Case ID         | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| sysFileRefId    | File Reference ID| NVARCHAR         | Variable         |               |                 | Y               |
| to              | Recipient ID    | UNIQUEIDENTIFIER, NVARCHAR | N/A/Variable   |               |                 | Y               |

#### 4.1.1.3. submissions

> Entity Name: submissions
>
> Description: Collection to store application submissions. Currently empty.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|------------------|------------------|---------------|-----------------|-----------------|
| *(No fields defined in schema analysis as collection is empty)* |                  |                  |                  |               |                 |                 |

#### 4.1.1.4. applications

> Entity Name: applications
>
> Description: Collection for storing applications for licensing self-certification.

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| APP13                   | APP13 data                  | Object, Array    | N/A              |               |                 |                 |
| AddressOfPremiseCN      | Premise Address (CN)        | NVARCHAR         | Variable         |               |                 |                 |
| AddressOfPremiseCNFloor | Premise Address Floor (CN)  | NVARCHAR         | Variable         |               |                 |                 |
| AddressOfPremiseCNUnit  | Premise Address Unit (CN)   | NVARCHAR         | Variable         |               |                 |                 |
| AddressOfPremiseEN      | Premise Address (EN)        | NVARCHAR         | Variable         |               |                 |                 |
| AddressOfPremiseENFloor | Premise Address Floor (EN)  | NVARCHAR         | Variable         |               |                 |                 |
| AddressOfPremiseENUnit  | Premise Address Unit (EN)   | NVARCHAR         | Variable         |               |                 |                 |
| AgeOfStudent            | Age of Student              | NVARCHAR, Null   | Variable         |               |                 |                 |
| ApplicantAddress        | Applicant Address           | NVARCHAR         | Variable         |               |                 |                 |
| ApplicantEmail          | Applicant Email             | NVARCHAR         | Variable         |               |                 |                 |
| ApplicantFax            | Applicant Fax               | NVARCHAR         | Variable         |               |                 |                 |
| ApplicantMobile         | Applicant Mobile            | NVARCHAR         | Variable         |               |                 |                 |
| ApplicantName           | Applicant Name              | NVARCHAR         | Variable         |               |                 |                 |
| ApplicantNameCN         | Applicant Name (CN)         | NVARCHAR         | Variable         |               |                 |                 |
| ApplicantNameEN         | Applicant Name (EN)         | NVARCHAR, Null   | Variable         |               |                 |                 |
| ApplicantTel            | Applicant Telephone         | NVARCHAR, Null   | Variable         |               |                 |                 |
| ApplicationNo           | Application Number          | NVARCHAR, Null   | Variable         |               |                 |                 |
| ApplicationType         | Application Type            | NVARCHAR         | Variable         |               |                 |                 |
| Area                    | Area                        | NVARCHAR         | Variable         |               |                 |                 |
| BlockID                 | Block ID                    | NVARCHAR         | Variable         |               |                 |                 |
| ContactPerson           | Contact Person Name         | NVARCHAR         | Variable         |               |                 |                 |
| ContactPersonCN         | Contact Person Name (CN)    | NVARCHAR         | Variable         |               |                 |                 |
| ContactPersonEN         | Contact Person Name (EN)    | NVARCHAR         | Variable         |               |                 |                 |
| ContactPersonEmail      | Contact Person Email        | NVARCHAR         | Variable         |               |                 |                 |
| ContactPersonTel        | Contact Person Telephone    | NVARCHAR         | Variable         |               |                 |                 |
| DescriptionOfSchool     | Description of School       | NVARCHAR, Null   | Variable         |               |                 |                 |
| District                | District                    | NVARCHAR         | Variable         |               |                 |                 |
| EstimatedNoOfStudent    | Estimated Number of Students| Int, Null        | N/A              |               |                 |                 |
| FileReference           | File Reference              | NVARCHAR         | Variable         |               |                 |                 |
| NameOfSchoolCN          | Name of School (CN)         | NVARCHAR         | Variable         |               |                 |                 |
| NameOfSchoolEN          | Name of School (EN)         | NVARCHAR         | Variable         |               |                 |                 |
| Region                  | Region                      | NVARCHAR         | Variable         |               |                 |                 |
| RelatedPremise          | Related Premise             | NVARCHAR         | Variable         |               |                 |                 |
| RelatedPremises         | Related Premises (Array)    | Array            | N/A              |               |                 |                 |
| SelfCertification      | Self Certification Data     | Object, Null     | N/A              |               |                 |                 |
| StructuralCalculation   | Structural Calculation Data | Object           | N/A              |               |                 |                 |
| SubmissionType          | Submission Type           | NVARCHAR         | Variable         |               |                 |                 |
| __v                     | Version field             | Int              | N/A              |               |                 |                 |
| _id                     | Application ID            | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| address                 | Address object            | Object           | N/A              |               |                 |                 |
| assignedBS              | Assigned Building Surveyor ID | UNIQUEIDENTIFIER, NVARCHAR, Null | N/A/Variable   |               |                 | Y               |
| assignedGR              | Assigned Geotechnical Engineer ID | UNIQUEIDENTIFIER, Null | N/A              |               |                 | Y               |
| assignedSBS             | Assigned Structural Engineer ID | NVARCHAR, Null   | Variable         |               |                 |                 |
| createdAt               | Creation Date             | DATETIME2        | N/A              |               |                 |                 |
| updatedAt               | Last Updated Date         | DATETIME2        | N/A              |               |                 |                 |

#### 4.1.1.5. notifications

> Entity Name: notifications
>
> Description: Collection for storing system notifications for users.

| **Field Name**     | **Description**         | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                  | Version field           | Int              | N/A              |               |                 |                 |
| _id                  | Notification ID       | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| createdAt            | Creation Date         | DATETIME2        | N/A              |               |                 |                 |
| eminute              | Eminute ID            | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| notificationType     | Type of Notification  | NVARCHAR         | Variable         |               |                 |                 |
| requireSendEmail     | Email Required Flag   | BIT              | N/A              |               |                 |                 |
| task                 | Task ID               | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| user                 | User ID               | NVARCHAR         | Variable         |               |                 | Y               |

#### 4.1.1.6. bsblocks

> Entity Name: bsblocks
>
> Description: Collection for building blocks information.

| **Field Name** | **Description**   | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v             | Version field     | Int              | N/A              |               |                 |                 |
| _id             | Block ID          | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| bdgis           | BDGIS identifier  | NVARCHAR         | Variable         |               |                 |                 |
| blockId         | Block Identifier  | NVARCHAR         | Variable         |               |                 |                 |

#### 4.1.1.7. cases

> Entity Name: cases
>
> Description: Collection for cases related to applications, potentially for follow-up or audit.

| **Field Name**              | **Description**                 | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------------|---------------------------------|------------------|------------------|---------------|-----------------|-----------------|
| ActualReplyDate           | Actual Reply Date               | DATETIME2, Null  | N/A              |               |                 |                 |
| Area                      | Area                            | NVARCHAR         | Variable         |               |                 |                 |
| AuditResult               | Audit Result                    | NVARCHAR         | Variable         |               |                 |                 |
| CaseOfficer               | Case Officer Name               | NVARCHAR         | Variable         |               |                 |                 |
| Category                  | Case Category                   | NVARCHAR         | Variable         |               |                 |                 |
| District                  | District                        | NVARCHAR         | Variable         |               |                 |                 |
| FileReference             | File Reference                  | NVARCHAR         | Variable         |               |                 |                 |
| LAFileReference           | LA File Reference               | Object           | N/A              |               |                 |                 |
| Nature                    | Case Nature                     | NVARCHAR, Null   | Variable         |               |                 |                 |
| ObjectiontoLR             | Objection to LR                 | NVARCHAR         | Variable         |               |                 |                 |
| ReceivedDate              | Date Received                   | DATETIME2, Null  | N/A              |               |                 |                 |
| Referrer                  | Case Referrer                   | Object           | N/A              |               |                 |                 |
| Region                    | Region                          | NVARCHAR         | Variable         |               |                 |                 |
| Remarks                   | Case Remarks                    | NVARCHAR         | Variable         |               |                 |                 |
| Reminders                 | Reminders (Array)               | Array            | N/A              |               |                 |                 |
| SubmissionType            | Submission Type                 | NVARCHAR         | Variable         |               |                 |                 |
| SubstantialReplyDate      | Substantial Reply Date          | DATETIME2, Null  | N/A              |               |                 |                 |
| TargetReplyDate           | Target Reply Date               | DATETIME2, Null  | N/A              |               |                 |                 |
| ThreeTierReqt             | Three Tier Requirement          | NVARCHAR         | Variable         |               |                 |                 |
| ViaSCS                    | Via SCS Flag                    | BIT              | N/A              |               |                 |                 |
| __v                       | Version field                   | Int              | N/A              |               |                 |                 |
| _id                       | Case ID                         | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| application               | Application ID                  | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| assignedBS                | Assigned Building Surveyor ID    | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| assignedGR                | Assigned Geotechnical Engineer ID| UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| building_information      | Building Information Object     | Object           | N/A              |               |                 |                 |
| caseDescription           | Case Description Object         | Object           | N/A              |               |                 |                 |
| caseOfficerReceive        | Case Officer Receive User ID    | NVARCHAR         | Variable         |               |                 | Y               |
| caseOfficerReply          | Case Officer Reply User ID      | NVARCHAR         | Variable         |               |                 | Y               |
| createdAt                 | Creation Date                   | DATETIME2        | N/A              |               |                 |                 |
| deck_study                | Deck Study Object               | Object           | N/A              |               |                 |                 |
| documentChecklist         | Document Checklist Object       | Object           | N/A              |               |                 |                 |
| dv                        | DV Object                       | Object           | N/A              |               |                 |                 |
| frc                       | FRC Object                      | Object           | N/A              |               |                 |                 |
| misc                      | Miscellaneous Object            | Object           | N/A              |               |                 |                 |
| moe                       | MOE Object                      | Object           | N/A              |               |                 |                 |
| seniorCaseOfficerReceive  | Senior Case Officer Receive User ID | NVARCHAR         | Variable         |               |                 | Y               |
| seniorCaseOfficerReply    | Senior Case Officer Reply User ID   | NVARCHAR         | Variable         |               |                 | Y               |
| site_inspection           | Site Inspection Object          | Object           | N/A              |               |                 |                 |
| structural_ccc_bs         | Structural CCC BS Object        | Object           | N/A              |               |                 |                 |
| structural_schnlh         | Structural SCHNLH Object        | Object           | N/A              |               |                 |                 |
| structural_schnlhkinds    | Structural SCHNLHKINDS Object   | Object           | N/A              |               |                 |                 |
| team                      | Team assigned                   | NVARCHAR         | Variable         |               |                 |                 |
| ubw                       | UBW Object                      | Object           | N/A              |               |                 |                 |
| updatedAt                 | Last Updated Date               | DATETIME2        | N/A              |               |                 |                 |

#### 4.1.1.8. oauthtokens

> Entity Name: oauthtokens
>
> Description: Collection for OAuth 2.0 access and refresh tokens.

| **Field Name**          | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                     | Version field               | Int              | N/A              |               |                 |                 |
| _id                     | Token ID                    | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| accessToken             | Access Token                | NVARCHAR         | Variable         |               |                 |                 |
| accessTokenExpiresAt    | Access Token Expiry Date    | DATETIME2        | N/A              |               |                 |                 |
| client                  | Client Object               | Object           | N/A              |               |                 |                 |
| refreshToken            | Refresh Token               | NVARCHAR         | Variable         |               |                 |                 |
| refreshTokenExpiresAt   | Refresh Token Expiry Date   | DATETIME2        | N/A              |               |                 |                 |
| user                    | User ID                     | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |

#### 4.1.1.9. sysfilerefs

> Entity Name: sysfilerefs
>
> Description: Collection for system file references, storing metadata about files.

| **Field Name**        | **Description**           | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------|---------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                   | Version field             | Int              | N/A              |               |                 |                 |
| _id                   | File Reference ID         | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| createdDt             | Creation Date             | DATETIME2        | N/A              |               |                 |                 |
| createdName           | Creator Name              | NVARCHAR, Null   | Variable         |               |                 |                 |
| createdPost           | Creator Post              | NVARCHAR, Null   | Variable         |               |                 |                 |
| createdSection        | Creator Section           | NVARCHAR, Null   | Variable         |               |                 |                 |
| display               | Display Name              | NVARCHAR         | Variable         |               |                 |                 |
| dvExceed              | DV Exceed Status          | NVARCHAR, Null   | Variable         |               |                 |                 |
| dvStatusDt            | DV Status Date            | DATETIME2, Null  | N/A              |               |                 |                 |
| frefPref              | File Reference Prefix     | NVARCHAR, Null   | Variable         |               |                 |                 |
| frefSeq               | File Reference Sequence   | NVARCHAR, Null   | Variable         |               |                 |                 |
| frefSuf               | File Reference Suffix     | NVARCHAR, Null   | Variable         |               |                 |                 |
| frefYr                | File Reference Year       | NVARCHAR, Null   | Variable         |               |                 |                 |
| lastModifiedDt        | Last Modified Date        | DATETIME2        | N/A              |               |                 |                 |
| lastModifiedName      | Last Modifier Name        | NVARCHAR, Null   | Variable         |               |                 |                 |
| lastModifiedPost      | Last Modifier Post        | NVARCHAR, Null   | Variable         |               |                 |                 |
| lastModifiedSection   | Last Modifier Section     | NVARCHAR, Null   | Variable         |               |                 |                 |
| sysFileRefId          | System File Reference ID  | NVARCHAR         | Variable         |               |                 |                 |

#### 4.1.1.10. attachments

> Entity Name: attachments
>
> Description: Collection for file attachments associated with applications or cases.

| **Field Name**    | **Description**       | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------|-----------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v               | Version field         | Int              | N/A              |               |                 |                 |
| _id               | Attachment ID       | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| application       | Application ID      | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| createdAt         | Creation Date       | DATETIME2        | N/A              |               |                 |                 |
| efolio            | Efolio reference    | NVARCHAR, Null   | Variable         |               |                 |                 |
| file              | File Object/String    | Object, NVARCHAR | N/A/Variable   |               |                 |                 |
| filePartNo        | File Part Number      | NVARCHAR         | Variable         |               |                 |                 |
| receivedDate      | Date Received       | DATETIME2        | N/A              |               |                 |                 |
| remarks           | Attachment Remarks  | NVARCHAR         | Variable         |               |                 |                 |
| subType           | Attachment Subtype  | NVARCHAR         | Variable         |               |                 |                 |
| submissionCase    | Case ID             | UNIQUEIDENTIFIER | N/A              |               |                 | Y               |
| sysFileRefId      | File Reference ID   | NVARCHAR         | Variable         |               |                 | Y               |
| type              | Attachment Type     | NVARCHAR         | Variable         |               |                 |                 |
| updatedAt         | Last Updated Date   | DATETIME2        | N/A              |               |                 |                 |

#### 4.1.1.11. users

> Entity Name: users
>
> Description: Collection for user accounts and profiles.

| **Field Name**        | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                   | Version field               | Int              | N/A              |               |                 |                 |
| _id                   | User ID                     | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| bdgis                 | BDGIS identifier            | NVARCHAR         | Variable         |               |                 |                 |
| begis                 | BEGIS identifier            | NVARCHAR         | Variable         |               |                 |                 |
| delegateTo            | Delegate To User ID         | NVARCHAR         | Variable         |               |                 | Y               |
| department            | Department                  | NVARCHAR         | Variable         |               |                 |                 |
| email                 | Email Address               | NVARCHAR         | Variable         |               |                 |                 |
| group                 | User Group                  | NVARCHAR         | Variable         |               |                 |                 |
| lastLoginAt           | Last Login Date             | DATETIME2        | N/A              |               |                 |                 |
| letterLongPosition    | Letter Long Position (EN)   | NVARCHAR         | Variable         |               |                 |                 |
| letterLongPositionCn  | Letter Long Position (CN)   | NVARCHAR         | Variable         |               |                 |                 |
| letterName            | Letter Name (EN)            | NVARCHAR         | Variable         |               |                 |                 |
| letterNameCn          | Letter Name (CN)            | NVARCHAR         | Variable         |               |                 |                 |
| letterPosition        | Letter Position (EN)        | NVARCHAR         | Variable         |               |                 |                 |
| letterPositionCn      | Letter Position (CN)        | NVARCHAR         | Variable         |               |                 |                 |
| lock                  | Account Lock Status         | BIT              | N/A              |               |                 |                 |
| luPostName            | LU Post Name                | NVARCHAR         | Variable         |               |                 |                 |
| name                  | User Name (EN)              | NVARCHAR         | Variable         |               |                 |                 |
| notificationEmail     | Notification Email Address  | NVARCHAR         | Variable         |               |                 |                 |
| osdpEmail             | OSDP Email Address          | NVARCHAR         | Variable         |               |                 |                 |
| osdpLoginId           | OSDP Login ID               | NVARCHAR         | Variable         |               |                 |                 |
| password              | Password (Hashed)           | NVARCHAR         | Variable         |               |                 |                 |
| phoneNumber           | Phone Number                | NVARCHAR         | Variable         |               |                 |                 |
| position              | Position (EN)               | NVARCHAR         | Variable         |               |                 |                 |
| role                  | User Role                   | NVARCHAR         | Variable         |               |                 |                 |
| team                  | Team assigned               | NVARCHAR         | Variable         |               |                 |                 |
| userType              | User Type                   | NVARCHAR         | Variable         |               |                 |                 |

#### 4.1.1.12. adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: Collection for address block file references.

| **Field Name**        | **Description**             | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------------|-----------------------------|------------------|------------------|---------------|-----------------|-----------------|
| __v                   | Version field               | Int              | N/A              |               |                 |                 |
| _id                   | Address Block File Ref ID   | UNIQUEIDENTIFIER | N/A              | Y             | Y               |                 |
| adrBlkFileRefId       | Address Block File Ref Identifier | NVARCHAR         | Variable         |               |                 |                 |
| adrBlkId            | Address Block ID            | NVARCHAR         | Variable         |               |                 | Y               |
| createdDt             | Creation Date             | DATETIME2        | N/A              |               |                 |                 |
| createdName           | Creator Name              | NVARCHAR, Null   | Variable         |               |                 |                 |
| createdPost           | Creator Post              | NVARCHAR         | Variable         |               |                 |                 |
| createdSection        | Creator Section           | NVARCHAR, Null   | Variable         |               |                 |                 |
| lastModifiedDt        | Last Modified Date        | DATETIME2        | N/A              |               |                 |                 |
| lastModifiedName      | Last Modifier Name        | NVARCHAR, Null   | Variable         |               |                 |                 |
| lastModifiedPost      | Last Modifier Post        | NVARCHAR         | Variable         |               |                 |                 |
| lastModifiedSection   | Last Modifier Section     | NVARCHAR, Null   | Variable         |               |                 |                 |
| sysFileRefId          | System File Reference ID  | NVARCHAR         | Variable         |               |                 | Y               |

---

**Note:**

- "Mandatory", "Field Length", and explicit "Foreign Key" relationships are not directly derived from the provided `database_schema.md`. "Mandatory" is left blank, "Field Length" is set to "Variable" for NVARCHAR types and "N/A" for others where applicable. "Foreign Key" is inferred based on field names and common database relationships, marked as 'Y' where likely, but should be verified against actual database constraints.
- "Field Format" is based on the "Types" listed in `database_schema.md` and mapped to more general data types where appropriate for clarity in a Data Catalogue.
- Descriptions for Entities and Fields are derived from the collection and field names provided in `database_schema.md`. They can be further refined for better clarity and business context.
- This Data Catalogue is based on the database schema analysis performed on 2025/3/4 ??10:10:39. Database schema changes after this date are not reflected in this document.
```