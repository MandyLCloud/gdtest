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

This data catalogue is based on the analysis of the 'bd' database, last updated on 2025/3/4 ??10:10:39. The database consists of 12 collections and a total of 1,278,983 documents, with a total data size of 371.24 MB. The database size is 88.10 MB. This document details the structure and fields of each collection within the 'bd' database.

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
| 1        | tasks           | Tasks Collection       |
| 2        | eminutes        | Eminutes Collection    |
| 3        | submissions     | Submissions Collection |
| 4        | applications    | Applications Collection|
| 5        | notifications   | Notifications Collection|
| 6        | bsblocks        | Bsblocks Collection    |
| 7        | cases           | Cases Collection       |
| 8        | oauthtokens     | Oauthtokens Collection |
| 9        | sysfilerefs     | Sysfilerefs Collection |
| 10       | attachments     | Attachments Collection |
| 11       | users           | Users Collection       |
| 12       | adrblkfilerefs  | Adrblkfilerefs Collection|
|          |                 |                        |
|          |                 |                        |
|          |                 |                        |

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
> Description: Collection for storing task information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v           |           | objectId, int |          |               |                 |                 |
| _id           |           | objectId   |          |               |                 |                 |
| application   |           | objectId   |          |               |                 |                 |
| createdAt     |           | date       |          |               |                 |                 |
| status        |           | string     |          |               |                 |                 |
| submissionCase|           | objectId   |          |               |                 |                 |
| taskType      |           | string     |          |               |                 |                 |
| team          |           | string     |          |               |                 |                 |
| user          |           | string, objectId |          |               |                 |                 |

### 4.1.2. eminutes

> Entity Name: eminutes
>
> Description: Collection for storing electronic minutes information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v           |           | int        |          |               |                 |                 |
| _id           |           | objectId   |          |               |                 |                 |
| comment       |           | string     |          |               |                 |                 |
| content       |           | string     |          |               |                 |                 |
| createdAt     |           | date       |          |               |                 |                 |
| efolio        |           | string     |          |               |                 |                 |
| eminuteId     |           | string     |          |               |                 |                 |
| from          |           | objectId, string |          |               |                 |                 |
| status        |           | string     |          |               |                 |                 |
| subject       |           | string     |          |               |                 |                 |
| submissionCase|           | objectId   |          |               |                 |                 |
| sysFileRefId  |           | string     |          |               |                 |                 |
| to            |           | objectId, string |          |               |                 |                 |

### 4.1.3. submissions

> Entity Name: submissions
>
> Description: Collection for storing submission information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
|  *No Fields Defined*              |           |              |          |               |                 |                 |

### 4.1.4. applications

> Entity Name: applications
>
> Description: Collection for storing application information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| APP13             |           | object, array |          |               |                 |                 |
| AddressOfPremiseCN|           | string     |          |               |                 |                 |
| AddressOfPremiseCNFloor|      | string     |          |               |                 |                 |
| AddressOfPremiseCNUnit|       | string     |          |               |                 |                 |
| AddressOfPremiseEN|           | string     |          |               |                 |                 |
| AddressOfPremiseENFloor|      | string     |          |               |                 |                 |
| AddressOfPremiseENUnit|       | string     |          |               |                 |                 |
| AgeOfStudent      |           | null, string |          |               |                 |                 |
| ApplicantAddress  |           | string     |          |               |                 |                 |
| ApplicantEmail    |           | string     |          |               |                 |                 |
| ApplicantFax      |           | string     |          |               |                 |                 |
| ApplicantMobile   |           | string     |          |               |                 |                 |
| ApplicantName     |           | string     |          |               |                 |                 |
| ApplicantNameCN   |           | string     |          |               |                 |                 |
| ApplicantNameEN   |           | null, string |          |               |                 |                 |
| ApplicantTel      |           | null, string |          |               |                 |                 |
| ApplicationNo     |           | null, string |          |               |                 |                 |
| ApplicationType   |           | string     |          |               |                 |                 |
| Area              |           | string     |          |               |                 |                 |
| BlockID           |           | string     |          |               |                 |                 |
| ContactPerson     |           | string     |          |               |                 |                 |
| ContactPersonCN   |           | string     |          |               |                 |                 |
| ContactPersonEN   |           | string     |          |               |                 |                 |
| ContactPersonEmail|           | string     |          |               |                 |                 |
| ContactPersonTel  |           | string     |          |               |                 |                 |
| DescriptionOfSchool|          | string, null |          |               |                 |                 |
| District          |           | string     |          |               |                 |                 |
| EstimatedNoOfStudent|         | int, null  |          |               |                 |                 |
| FileReference     |           | string     |          |               |                 |                 |
| NameOfSchoolCN    |           | string     |          |               |                 |                 |
| NameOfSchoolEN    |           | string     |          |               |                 |                 |
| Region            |           | string     |          |               |                 |                 |
| RelatedPremise    |           | string     |          |               |                 |                 |
| RelatedPremises   |           | array      |          |               |                 |                 |
| SelfCertification|           | object, null |          |               |                 |                 |
| StructuralCalculation|       | object     |          |               |                 |                 |
| SubmissionType    |           | string     |          |               |                 |                 |
| __v               |           | int        |          |               |                 |                 |
| _id               |           | objectId   |          |               |                 |                 |
| address           |           | object     |          |               |                 |                 |
| assignedBS        |           | objectId, string, null |          |               |                 |                 |
| assignedGR        |           | objectId, null |          |               |                 |                 |
| assignedSBS       |           | string, null |          |               |                 |                 |
| createdAt         |           | date       |          |               |                 |                 |
| updatedAt         |           | date       |          |               |                 |                 |

### 4.1.5. notifications

> Entity Name: notifications
>
> Description: Collection for storing notification information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v               |           | int        |          |               |                 |                 |
| _id               |           | objectId   |          |               |                 |                 |
| createdAt         |           | date       |          |               |                 |                 |
| eminute           |           | objectId   |          |               |                 |                 |
| notificationType  |           | string     |          |               |                 |                 |
| requireSendEmail  |           | bool       |          |               |                 |                 |
| task              |           | objectId   |          |               |                 |                 |
| user              |           | string     |          |               |                 |                 |

### 4.1.6. bsblocks

> Entity Name: bsblocks
>
> Description: Collection for storing building blocks information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v           |           | int        |          |               |                 |                 |
| _id           |           | objectId   |          |               |                 |                 |
| bdgis         |           | string     |          |               |                 |                 |
| blockId       |           | string     |          |               |                 |                 |

### 4.1.7. cases

> Entity Name: cases
>
> Description: Collection for storing case information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| ActualReplyDate       |           | null, date |          |               |                 |                 |
| Area                |           | string     |          |               |                 |                 |
| AuditResult         |           | string     |          |               |                 |                 |
| CaseOfficer         |           | string     |          |               |                 |                 |
| Category            |           | string     |          |               |                 |                 |
| District            |           | string     |          |               |                 |                 |
| FileReference       |           | string     |          |               |                 |                 |
| LAFileReference     |           | object     |          |               |                 |                 |
| Nature              |           | null, string |          |               |                 |                 |
| ObjectiontoLR       |           | string     |          |               |                 |                 |
| ReceivedDate        |           | date, null |          |               |                 |                 |
| Referrer            |           | object     |          |               |                 |                 |
| Region              |           | string     |          |               |                 |                 |
| Remarks             |           | string     |          |               |                 |                 |
| Reminders           |           | array      |          |               |                 |                 |
| SubmissionType      |           | string     |          |               |                 |                 |
| SubstantialReplyDate|           | null, date |          |               |                 |                 |
| TargetReplyDate       |           | date, null |          |               |                 |                 |
| ThreeTierReqt       |           | string     |          |               |                 |                 |
| ViaSCS              |           | bool       |          |               |                 |                 |
| __v                 |           | int        |          |               |                 |                 |
| _id                 |           | objectId   |          |               |                 |                 |
| application         |           | objectId   |          |               |                 |                 |
| assignedBS          |           | objectId   |          |               |                 |                 |
| assignedGR          |           | objectId   |          |               |                 |                 |
| building_information|           | object     |          |               |                 |                 |
| caseDescription     |           | object     |          |               |                 |                 |
| caseOfficerReceive  |           | string     |          |               |                 |                 |
| caseOfficerReply    |           | string     |          |               |                 |                 |
| createdAt           |           | date       |          |               |                 |                 |
| deck_study          |           | object     |          |               |                 |                 |
| documentChecklist   |           | object     |          |               |                 |                 |
| dv                  |           | object     |          |               |                 |                 |
| frc                 |           | object     |          |               |                 |                 |
| misc                |           | object     |          |               |                 |                 |
| moe                 |           | object     |          |               |                 |                 |
| seniorCaseOfficerReceive|      | string     |          |               |                 |                 |
| seniorCaseOfficerReply|        | string     |          |               |                 |                 |
| site_inspection     |           | object     |          |               |                 |                 |
| structural_ccc_bs   |           | object     |          |               |                 |                 |
| structural_schnlh   |           | object     |          |               |                 |                 |
| structural_schnlhkinds|        | object     |          |               |                 |                 |
| team                |           | string     |          |               |                 |                 |
| ubw                 |           | object     |          |               |                 |                 |
| updatedAt           |           | date       |          |               |                 |                 |

### 4.1.8. oauthtokens

> Entity Name: oauthtokens
>
> Description: Collection for storing OAuth tokens information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v                   |           | int        |          |               |                 |                 |
| _id                   |           | objectId   |          |               |                 |                 |
| accessToken           |           | string     |          |               |                 |                 |
| accessTokenExpiresAt  |           | date       |          |               |                 |                 |
| client              |           | object     |          |               |                 |                 |
| refreshToken          |           | string     |          |               |                 |                 |
| refreshTokenExpiresAt |           | date       |          |               |                 |                 |
| user                  |           | objectId   |          |               |                 |                 |

### 4.1.9. sysfilerefs

> Entity Name: sysfilerefs
>
> Description: Collection for storing system file references information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v               |           | int        |          |               |                 |                 |
| _id               |           | objectId   |          |               |                 |                 |
| createdDt         |           | date       |          |               |                 |                 |
| createdName       |           | null, string |          |               |                 |                 |
| createdPost       |           | null, string |          |               |                 |                 |
| createdSection    |           | null, string |          |               |                 |                 |
| display           |           | string     |          |               |                 |                 |
| dvExceed          |           | null, string |          |               |                 |                 |
| dvStatusDt        |           | null, date |          |               |                 |                 |
| frefPref          |           | string, null |          |               |                 |                 |
| frefSeq           |           | null, string |          |               |                 |                 |
| frefSuf           |           | null, string |          |               |                 |                 |
| frefYr            |           | null, string |          |               |                 |                 |
| lastModifiedDt    |           | date       |          |               |                 |                 |
| lastModifiedName  |           | null, string |          |               |                 |                 |
| lastModifiedPost  |           | null, string |          |               |                 |                 |
| lastModifiedSection|          | null       |          |               |                 |                 |
| sysFileRefId      |           | string     |          |               |                 |                 |

### 4.1.10. attachments

> Entity Name: attachments
>
> Description: Collection for storing attachment information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v               |           | int        |          |               |                 |                 |
| _id               |           | objectId   |          |               |                 |                 |
| application       |           | objectId   |          |               |                 |                 |
| createdAt         |           | date       |          |               |                 |                 |
| efolio            |           | null, string |          |               |                 |                 |
| file              |           | object, string |          |               |                 |                 |
| filePartNo        |           | string     |          |               |                 |                 |
| receivedDate      |           | date       |          |               |                 |                 |
| remarks           |           | string     |          |               |                 |                 |
| subType           |           | string     |          |               |                 |                 |
| submissionCase    |           | objectId   |          |               |                 |                 |
| sysFileRefId      |           | string     |          |               |                 |                 |
| type              |           | string     |          |               |                 |                 |
| updatedAt         |           | date       |          |               |                 |                 |

### 4.1.11. users

> Entity Name: users
>
> Description: Collection for storing user information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v               |           | int        |          |               |                 |                 |
| _id               |           | objectId   |          |               |                 |                 |
| bdgis             |           | string     |          |               |                 |                 |
| begis             |           | string     |          |               |                 |                 |
| delegateTo        |           | string     |          |               |                 |                 |
| department        |           | string     |          |               |                 |                 |
| email             |           | string     |          |               |                 |                 |
| group             |           | string     |          |               |                 |                 |
| lastLoginAt       |           | date       |          |               |                 |                 |
| letterLongPosition|           | string     |          |               |                 |                 |
| letterLongPositionCn|        | string     |          |               |                 |                 |
| letterName        |           | string     |          |               |                 |                 |
| letterNameCn      |           | string     |          |               |                 |                 |
| letterPosition    |           | string     |          |               |                 |                 |
| letterPositionCn  |           | string     |          |               |                 |                 |
| lock              |           | bool       |          |               |                 |                 |
| luPostName        |           | string     |          |               |                 |                 |
| name              |           | string     |          |               |                 |                 |
| notificationEmail |           | string     |          |               |                 |                 |
| osdpEmail         |           | string     |          |               |                 |                 |
| osdpLoginId       |           | string     |          |               |                 |                 |
| password          |           | string     |          |               |                 |                 |
| phoneNumber       |           | string     |          |               |                 |                 |
| position          |           | string     |          |               |                 |                 |
| role              |           | string     |          |               |                 |                 |
| team              |           | string     |          |               |                 |                 |
| userType          |           | string     |          |               |                 |                 |

### 4.1.12. adrblkfilerefs

> Entity Name: adrblkfilerefs
>
> Description: Collection for storing address block file references information.

| **Field Name** | **Description** | **Field Format** | **Field Length** | **Mandatory** | **Primary Key** | **Foreign Key** |
|---------------|-----------|----------|----------|-----------|----------|---------|
| __v               |           | int        |          |               |                 |                 |
| _id               |           | objectId   |          |               |                 |                 |
| adrBlkFileRefId   |           | string     |          |               |                 |                 |
| adrBlkId          |           | string     |          |               |                 |                 |
| createdDt         |           | date       |          |               |                 |                 |
| createdName       |           | null, string |          |               |                 |                 |
| createdPost       |           | string     |          |               |                 |                 |
| createdSection    |           | null, string |          |               |                 |                 |
| lastModifiedDt    |           | date       |          |               |                 |                 |
| lastModifiedName  |           | null, string |          |               |                 |                 |
| lastModifiedPost  |           | string     |          |               |                 |                 |
| lastModifiedSection|          | string, null |          |               |                 |                 |
| sysFileRefId      |           | string     |          |               |                 |                 |
```