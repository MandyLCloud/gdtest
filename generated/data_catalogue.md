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

# 3. Data Entity Description

This section states all the entities in the LSCP Database.

The following section describes how the LSCP entities can be mapped onto
physical data design.

-   Entities list for LSCP Data

| **Item** | **Entity Name** | **Entity Description** |
|----------|-----------------|------------------------|
| 1        | tasks           | Details in section 4.1.1 |
| 2        | eminutes        | Details in section 4.1.2 |
| 3        | submissions     | Details in section 4.1.3 |
| 4        | applications    | Details in section 4.1.4 |
| 5        | notifications   | Details in section 4.1.5 |
| 6        | bsblocks        | Details in section 4.1.6 |
| 7        | cases           | Details in section 4.1.7 |
| 8        | oauthtokens     | Details in section 4.1.8 |
| 9        | sysfilerefs     | Details in section 4.1.9 |
| 10       | attachments     | Details in section 4.1.10 |
| 11       | users           | Details in section 4.1.11 |
| 12       | adrblkfilerefs  | Details in section 4.1.12 |

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

### 4.1.1. <a name="tasks"></a>tasks

> Entity Name: tasks
>
> Description: Collection for storing task information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v            | To be defined   | BIGINT, UNIQUEIDENTIFIER |                  |               |                 |                 |
| _id            | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| application    | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| createdAt      | To be defined   | DATETIME2        |                  |               |                 |                 |
| status         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| submissionCase | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| taskType       | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| team           | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| user           | To be defined   | NVARCHAR(MAX), UNIQUEIDENTIFIER |                  |               |                 |                 |

### 4.1.2. <a name="eminutes"></a>eminutes

> Entity Name: eminutes
>
> Description: Collection for storing electronic minutes information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v            | To be defined   | BIGINT           |                  |               |                 |                 |
| _id            | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| comment        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| content        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| createdAt      | To be defined   | DATETIME2        |                  |               |                 |                 |
| efolio         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| eminuteId      | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| from           | To be defined   | UNIQUEIDENTIFIER, NVARCHAR(MAX) |                  |               |                 | Y?              |
| status         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| subject        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| submissionCase | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| sysFileRefId   | To be defined   | NVARCHAR(MAX)    |                  |               |                 | Y?              |
| to             | To be defined   | UNIQUEIDENTIFIER, NVARCHAR(MAX) |                  |               |                 | Y?              |

### 4.1.3. <a name="submissions"></a>submissions

> Entity Name: submissions
>
> Description: Collection for storing submission information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| *(No fields defined in input)* |                 |                  |                  |               |                 |                 |

### 4.1.4. <a name="applications"></a>applications

> Entity Name: applications
>
> Description: Collection for storing application information.

| **Field Name**          | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| APP13                   | To be defined   | NVARCHAR(MAX), NVARCHAR(MAX)[] |                  |               |                 |                 |
| AddressOfPremiseCN      | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| AddressOfPremiseCNFloor | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| AddressOfPremiseCNUnit  | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| AddressOfPremiseEN      | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| AddressOfPremiseENFloor | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| AddressOfPremiseENUnit  | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| AgeOfStudent            | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| ApplicantAddress        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ApplicantEmail          | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ApplicantFax            | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ApplicantMobile         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ApplicantName           | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ApplicantNameCN         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ApplicantNameEN         | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| ApplicantTel            | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| ApplicationNo           | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| ApplicationType         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| Area                    | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| BlockID                 | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ContactPerson           | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ContactPersonCN         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ContactPersonEN         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ContactPersonEmail      | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ContactPersonTel        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| DescriptionOfSchool     | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| District                | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| EstimatedNoOfStudent    | To be defined   | BIGINT, NULL     |                  |               |                 |                 |
| FileReference           | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| NameOfSchoolCN          | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| NameOfSchoolEN          | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| Region                  | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| RelatedPremise          | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| RelatedPremises         | To be defined   | NVARCHAR(MAX)[]  |                  |               |                 |                 |
| SelfCertification      | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| StructuralCalculation   | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| SubmissionType          | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| __v                     | To be defined   | BIGINT           |                  |               |                 |                 |
| _id                     | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| address                 | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| assignedBS              | To be defined   | UNIQUEIDENTIFIER, NVARCHAR(MAX), NULL |                  |               |                 | Y?              |
| assignedGR              | To be defined   | UNIQUEIDENTIFIER, NULL |                  |               |                 | Y?              |
| assignedSBS             | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| createdAt               | To be defined   | DATETIME2        |                  |               |                 |                 |
| updatedAt               | To be defined   | DATETIME2        |                  |               |                 |                 |

### 4.1.5. <a name="notifications"></a>notifications

> Entity Name: notifications
>
> Description: Collection for storing notification information.

| **Field Name**     | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                | To be defined   | BIGINT           |                  |               |                 |                 |
| _id                | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| createdAt          | To be defined   | DATETIME2        |                  |               |                 |                 |
| eminute            | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| notificationType   | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| requireSendEmail   | To be defined   | BIT              |                  |               |                 |                 |
| task               | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| user               | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |

### 4.1.6. <a name="bsblocks"></a>bsblocks

> Entity Name: bsblocks
>
> Description: Collection for storing building structure block information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v            | To be defined   | BIGINT           |                  |               |                 |                 |
| _id            | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| bdgis          | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| blockId        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |

### 4.1.7. <a name="cases"></a>cases

> Entity Name: cases
>
> Description: Collection for storing case information.

| **Field Name**              | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| ActualReplyDate             | To be defined   | DATETIME2, NULL  |                  |               |                 |                 |
| Area                        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| AuditResult                 | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| CaseOfficer                 | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| Category                    | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| District                    | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| FileReference               | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| LAFileReference             | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| Nature                      | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| ObjectiontoLR               | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ReceivedDate                | To be defined   | DATETIME2, NULL  |                  |               |                 |                 |
| Referrer                    | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| Region                      | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| Remarks                     | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| Reminders                   | To be defined   | NVARCHAR(MAX)[]  |                  |               |                 |                 |
| SubmissionType              | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| SubstantialReplyDate        | To be defined   | DATETIME2, NULL  |                  |               |                 |                 |
| TargetReplyDate             | To be defined   | DATETIME2, NULL  |                  |               |                 |                 |
| ThreeTierReqt               | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ViaSCS                      | To be defined   | BIT              |                  |               |                 |                 |
| __v                         | To be defined   | BIGINT           |                  |               |                 |                 |
| _id                         | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| application                 | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| assignedBS                  | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| assignedGR                  | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| building_information        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| caseDescription             | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| caseOfficerReceive          | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| caseOfficerReply            | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| createdAt                   | To be defined   | DATETIME2        |                  |               |                 |                 |
| deck_study                  | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| documentChecklist           | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| dv                          | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| frc                         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| misc                        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| moe                         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| seniorCaseOfficerReceive    | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| seniorCaseOfficerReply      | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| site_inspection             | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| structural_ccc_bs           | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| structural_schnlh           | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| structural_schnlhkinds      | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| team                        | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| ubw                         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| updatedAt                   | To be defined   | DATETIME2        |                  |               |                 |                 |

### 4.1.8. <a name="oauthtokens"></a>oauthtokens

> Entity Name: oauthtokens
>
> Description: Collection for storing OAuth token information.

| **Field Name**          | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-------------------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                     | To be defined   | BIGINT           |                  |               |                 |                 |
| _id                     | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| accessToken             | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| accessTokenExpiresAt    | To be defined   | DATETIME2        |                  |               |                 |                 |
| client                  | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| refreshToken            | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| refreshTokenExpiresAt   | To be defined   | DATETIME2        |                  |               |                 |                 |
| user                    | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |

### 4.1.9. <a name="sysfilerefs"></a>sysfilerefs

> Entity Name: sysfilerefs
>
> Description: Collection for storing system file reference information.

| **Field Name**        | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                   | To be defined   | BIGINT           |                  |               |                 |                 |
| _id                   | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| createdDt             | To be defined   | DATETIME2        |                  |               |                 |                 |
| createdName           | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| createdPost           | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| createdSection        | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| display               | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| dvExceed              | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| dvStatusDt            | To be defined   | DATETIME2, NULL  |                  |               |                 |                 |
| frefPref              | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| frefSeq               | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| frefSuf               | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| frefYr                | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| lastModifiedDt        | To be defined   | DATETIME2        |                  |               |                 |                 |
| lastModifiedName      | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| lastModifiedPost      | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| lastModifiedSection   | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| sysFileRefId          | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |

### 4.1.10. <a name="attachments"></a>attachments

> Entity Name: attachments
>
> Description: Collection for storing attachment information.

| **Field Name**     | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|--------------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                | To be defined   | BIGINT           |                  |               |                 |                 |
| _id                | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| application        | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| createdAt          | To be defined   | DATETIME2        |                  |               |                 |                 |
| efolio             | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| file               | To be defined   | NVARCHAR(MAX), NVARCHAR(MAX) |                  |               |                 |                 |
| filePartNo         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| receivedDate       | To be defined   | DATETIME2        |                  |               |                 |                 |
| remarks            | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| subType            | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| submissionCase     | To be defined   | UNIQUEIDENTIFIER |                  |               |                 | Y               |
| sysFileRefId       | To be defined   | NVARCHAR(MAX)    |                  |               |                 | Y               |
| type               | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| updatedAt          | To be defined   | DATETIME2        |                  |               |                 |                 |

### 4.1.11. <a name="users"></a>users

> Entity Name: users
>
> Description: Collection for storing user information.

| **Field Name**         | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|------------------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                    | To be defined   | BIGINT           |                  |               |                 |                 |
| _id                    | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| bdgis                  | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| begis                  | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| delegateTo             | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| department             | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| email                  | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| group                  | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| lastLoginAt            | To be defined   | DATETIME2        |                  |               |                 |                 |
| letterLongPosition     | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| letterLongPositionCn   | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| letterName             | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| letterNameCn           | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| letterPosition         | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| letterPositionCn       | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| lock                   | To be defined   | BIT              |                  |               |                 |                 |
| luPostName             | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| name                   | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| notificationEmail      | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| osdpEmail              | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| osdpLoginId            | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| password               | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| phoneNumber            | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| position               | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| role                   | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| team                   | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| userType               | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |

### 4.1.12. <a name="adrblkfilerefs"></a>adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: Collection for storing address block file reference information.

| **Field Name**        | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|-----------------------|-----------------|-----------------|-----------------|---------------|-----------------|-----------------|
| __v                   | To be defined   | BIGINT           |                  |               |                 |                 |
| _id                   | To be defined   | UNIQUEIDENTIFIER |                  |               | Y               |                 |
| adrBlkFileRefId       | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| adrBlkId            | To be defined   | NVARCHAR(MAX)    |                  |               |                 |                 |
| createdDt             | To be defined   | DATETIME2        |                  |               |                 |                 |
| createdName           | To be defined   | NVARCHAR(MAX), NULL |                  |               |                 |                 |
| createdPost           | To