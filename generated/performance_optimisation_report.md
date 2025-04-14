# Performance Optimization Report

**For Combined System Development Services for Licensing Self-Certification Portal of Buildings Department**

**Version 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

| Amendment History |                      |                |                          |            |
|-----------------|------------------------------|-----------------|--------------------------|-----------------|
| Change Number     | Revision Description | Pages Affected | Revision/ Version Number | Date       |
| 1                 | 1st draft            | All            | 0.1                      | 16/01/2025 |
|                   |                      |                |                          |            |
|                   |                      |                |                          |            |
|                   |                      |                |                          |            |
|                   |                      |                |                          |            |

**TABLE OF CONTENTS**

[**1. Introduction**](#introduction)

> [1.1 Goal of Performance Optimization](#goal-of-performance-optimization)
>
> [1.1.1 Server Loading](#server-loading)
>
> [1.1.2 Bandwidth Usage](#bandwidth-usage)
>
> [1.1.3 Better user experience](#better-user-experience)
>
> [1.2 Performance Optimisation Actions](#performance-optimisation-actions)
>
> [1.3 Storage Allocation](#storage-allocation)
>
> [1.4 Required Response Time](#required-response-time)
>
> [1.4.1 Online Transaction](#online-transaction)
>
> [1.4.2 Online Reports](#online-reports)

[**2. Critical online transition timing**](#critical-online-transition-timing)

[**3. Critical Batch Cycle Timing**](#critical-batch-cycle-timing)

[**4. Optimization changes**](#optimization-changes)

> [4.1 Optimization Actions](#optimization-actions)
>
> [4.1.1 Create stored procedures](#create-stored-procedures)
>
> [4.1.2 Create clustered indexes](#create-clustered-indexes)

## 1. Introduction

The performance optimization of the system could be classified into optimization of Online Transaction.

## 1.1 Goal of Performance Optimization

The main goal of performance optimization is to improve the response time of the system to users. In order to achieve better response time, the program implementation should take the following areas into consideration.

### 1.1.1 Server Loading

The Capacity of Server Loading is a fixed variable of a system. An increase in server loading would increase the response time of the system. Server loading is affected by:

1.  The number of system users; and
2.  The efficiency of the programming code.

When the number of system users increases, the server loading increases and hence there is less resource for running programming code for each system user. The response of the program would be slower as there is less server resource for the program to utilize.

On the other hand, if the programming code could use fewer server resources, there is less server loading and hence the server could respond to users quicker and serve more users simultaneously.

Therefore, response time could be reduced if the programming code could be optimized to use fewer server resources.

### 1.1.2 Bandwidth Usage

Capacity of Bandwidth Usage is a fixed variable of a system. An increase in bandwidth usage would decrease the response time of the system. Bandwidth loading is affected by:

1.  The number of system users; and
2.  The size of transmitting resource.

When the number of system users increases, the bandwidth usage increases and hence there is less bandwidth resource for transmitting data to each system user. The response time would be slower as there is less bandwidth for each user to utilize.

On the other hand, if the size of transmitting data is smaller, there is less bandwidth usage and hence the fixed network bandwidth could serve more users simultaneously.

Therefore, response time could be reduced if the size of the transmitting resource could be optimized to use less server resources.

### 1.1.3 Better User Experience

This application will be used by the public, in order words, it represents the department. If it performs well, the department can take credit from it, the image of the department may be affected if this application performs bad or causes other problems, for example very slow or no response.

## 1.2 Performance Optimisation Actions

To serve more users simultaneously with better response time, the system and the programs should be optimized to use the server loading and bandwidth resource more efficiently. The followings are the possible measures that could be taken generally:

-   Optimize the programming and query logic to reduce server loading burden.

-   Optimize the page size and image size to reduce bandwidth burden.

-   Improve resourcing retrieval speed by indexing and hashing.

-   Cache frequently used resources.

-   Pre-generate resource that required heavy instant server loading.

-   Improve resourcing retrieval speed by indexing and hashing.

-   Reduce waiting time of third-party services.

-   Archive expired records to keep the size of active datastore minimal

## 1.3 Storage Allocation

The storage of the database data will be stored as following:

i. System data ? Store in the ?Database? server in the Integrated system.

ii. Textual data ? Store in the ?Database? server in the Integrated system.

All the required system and textual data will be logical stored in various filegroup of Microsoft SQL Server database. The following table shows the logic data storage in Microsoft SQL Server database.

| FileGroup | TableName | TableSize |
|-----------|-----------|-----------|
|           |           |           |
|           |           |           |
|           |           |           |
|           |           |           |
|           |           |           |

The filegroup growth size has set to meet the recommendation for below 256 MB for data files.

## 1.4 Required Response Time

The required response time is defined according to 2 pre-defined categories. They are Online Transaction and Online Report. All of the programs and reports that require to interact and provide immediate response to users are categorized. The categorized programs and reports should respond to the user within required response time. The required response time should be defined according to the complexity of the programs. The required response time and the complexity will be discussed in the coming section.

For those procedures or reports that could not able to optimize to have immediate response, some part of the program that take a lot of processing time will be swapped to batch job.

95% of all online functions should meet the committed response time.

The committed response time is affected by the network status of the site. The environment of testing site should meet an agreed network health level. The following criteria define the agreed network health level.

-   Maximum number of Concurrent users is 100.

-   Minimal bandwidth is 2Mb/s per testing machine.

-   Maximum network round-trip latency (ping) to the Integrated system is 200ms.

-   Remote testing site will have **50% mark-up** time to the committed response time.

### 1.4.1 Online Transaction

The programs in the following category are classified as online transaction:

-   User Account Program

-   Form and Record Management Program

Online transactions can be classified into the following groups:

| Transaction Complexity | Number of Concurrent Users |            |          |     |
|---------------------|-----------------|-----------------|-----------------|--|
|                        | 40                         | 80         | 100      |     |
| Simple                 | < 1 sec                   | < 2 sec   | < 3 sec |     |
| Medium                 | < 2 sec                   | < 3 sec   | < 4 sec |     |
| Complex                | < 2.5 sec                 | < 3.5 sec | < 5 sec |     |

Online transactions can also be classified as follows:

| Online transactions         | Description                                                                       |
|---------------------------------|---------------------------------------|
| Online Update Transactions  | Used to update records in LSCP, for example, create supervision plan              |
| Online Enquiry Transactions | Used to retrieve records from LSCP, for example, filter site monitoring records   |
| Full-text Search            | Used to search for records with given key words, for example, search assigned TCP |

### 1.4.2 Online Reports

The programs in the following category are classified as online reports:

-   XXXXXXXXXXX

As the report is a standalone internal system for BD, the measurement would only estimate when the concurrent users are not more than 20.

| On-line Reports | Committed Response Time |
|-----------------|-------------------------|
|                 |                         |
|                 |                         |

## 2. Critical Online Transition Timing

The following matrix is the list of programs with the complexity and transaction type being marked.

Offline module helps users save information in local devices when Internet connectivity is not available. Once Internet connectivity is back, it will submit the data and store it in the database. The major difference between offline modules with other modules is that the offline module is asynchronous. It will not submit immediately but will wait until the Internet is available. For the asynchronous handling logic, we included it in the functional test. On the other hand, the data sending logic is no different with other API, thus we would not have a separate section for offline module in critical online transition timing.

| **Module ID** | **Program ID** | **Program Name** | **Complexity (Simple / Medium / Complex)** | **Online Transaction Program** | **Report Program** | **Type of transactions** | **Mobile Apps** |
|---------------|----------------|------------------|-------------------------------------------|--------------------------------|------------------|--------------------------|-----------------|
| **USER ACCOUNT PROGRAM** |                  |                  |                                           |                                |                  |                          |                 |
|               |                |                  |                                           |                                |                  |                          |                 |
|               |                |                  |                                           |                                |                  |                          |                 |
|               |                |                  |                                           |                                |                  |                          |                 |
|               |                |                  |                                           |                                |                  |                          |                 |
|               |                |                  |                                           |                                |                  |                          |                 |
|               |                |                  |                                           |                                |                  |                          |                 |

## 3. Critical Batch Cycle Timing

The below are the list of batch programs. The cycle timing of the batch is identified in the tables below.
They are different from modules in the last section whereas they will run a thousand times everyday but the modules in this section probably run once or twice daily. Moreover, most of the modules described in this section are scheduled jobs running in backend, normally, the fluctuation of performance in these items would not affect the end user. Except, the generate report module, has a higher impact, thus it is the only item required to optimize.

| **Program ID**    | **Program Name** | **Online Web** | **Mobile** | **Update Batch** | **Require Optimization?** | **Cycle Timing** |
|----------------|----------------|----------------|------------|------------------|---------------------------|----------------|
| **BATCH PROGRAM** |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |

## 4. Optimization changes

The optimization will **only** focus the performance on programs and reports.

## 4.1 Optimization Actions

### 4.1.1 Create stored procedures

All reports are created by stored procedures. Stored procedures are precompiled as opposed to the dynamic prepared statements that are compiled whenever your application code invokes a call. Once you execute a stored procedure, it remains in the cache, saving the execution time. In addition, the stored procedures are mostly using primary key for searching.

### 4.1.2 Create clustered indexes

When creating a primary key constraint, a unique clustered index on the column or columns is automatically created if a clustered index on the table does not already exist and you do not specify a unique non-clustered index. The primary key column cannot allow NULL values. In addition, when creating a unique constraint, a unique non-clustered index is created to enforce a unique constraint by default. When designing a clustered index, we have considered that the data types to be used as clustering keys. For instance, the primary keys are BIGINT data type which is the best choices as clustered index key.

| **Table ID** | **Table Name** | **LSCP Entity** | **Key Nature** | **Index Field** |
|--------------|----------------|-----------------|----------------|-----------------|
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |
|              |                |                 |                |                 |

<< End of Document >>

---

**Appendix: Database Analysis (bd)**

Last Updated: 2025/3/4 ??10:10:39

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

## Collection Details and Potential Optimization Areas

The following section provides a detailed analysis of each collection, highlighting potential areas for optimization based on data size, document count, and field analysis.  This analysis informs the recommendations in Section 4 regarding indexing and other optimization strategies.

### Collection: tasks

----------------------------------------

#### Collection Statistics

- Document Count: 5523
- Size: 0.99 MB
- Average Document Size: 0.18 KB

#### Field Analysis

__v
- Types: objectId, int
- Occurrences: 1000

_id
- Types: objectId
- Occurrences: 1000

application
- Types: objectId
- Occurrences: 998

createdAt
- Types: date
- Occurrences: 1000

status
- Types: string
- Occurrences: 1000

submissionCase
- Types: objectId
- Occurrences: 998

taskType
- Types: string
- Occurrences: 998

team
- Types: string
- Occurrences: 835

user
- Types: string, objectId
- Occurrences: 713

**Potential Optimization Areas:**

*   Consider indexing `application`, `submissionCase`, and `user` fields if they are frequently used in queries.  The mixed types in the `user` field might require special consideration during indexing.

### Collection: eminutes

----------------------------------------

#### Collection Statistics

- Document Count: 133
- Size: 0.03 MB
- Average Document Size: 0.24 KB

#### Field Analysis

__v
- Types: int
- Occurrences: 133

_id
- Types: objectId
- Occurrences: 133

comment
- Types: string
- Occurrences: 64

content
- Types: string
- Occurrences: 133

createdAt
- Types: date
- Occurrences: 133

efolio
- Types: string
- Occurrences: 100

eminuteId
- Types: string
- Occurrences: 133

from
- Types: objectId, string
- Occurrences: 133

status
- Types: string
- Occurrences: 133

subject
- Types: string
- Occurrences: 133

submissionCase
- Types: objectId
- Occurrences: 133

sysFileRefId
- Types: string
- Occurrences: 65

to
- Types: objectId, string
- Occurrences: 129

**Potential Optimization Areas:**

*   Indexing `submissionCase`, `from`, and `to` fields might improve query performance. The mixed types in `from` and `to` require careful index design.

### Collection: submissions

----------------------------------------

#### Collection Statistics

- Document Count: 0
- Size: 0.00 MB
- Average Document Size: 0.00 KB

#### Field Analysis

*   No documents exist. No optimization is currently needed.

### Collection: applications

----------------------------------------

#### Collection Statistics

- Document Count: 381
- Size: 0.36 MB
- Average Document Size: 0.96 KB

#### Field Analysis

APP13
- Types: object, array
- Occurrences: 172

AddressOfPremiseCN
- Types: string
- Occurrences: 267

AddressOfPremiseCNFloor
- Types: string
- Occurrences: 147

AddressOfPremiseCNUnit
- Types: string
- Occurrences: 147

AddressOfPremiseEN
- Types: string
- Occurrences: 271

AddressOfPremiseENFloor
- Types: string
- Occurrences: 155

AddressOfPremiseENUnit
- Types: string
- Occurrences: 154

AgeOfStudent
- Types: null, string
- Occurrences: 328

ApplicantAddress
- Types: string
- Occurrences: 335

ApplicantEmail
- Types: string
- Occurrences: 289

ApplicantFax
- Types: string
- Occurrences: 21

ApplicantMobile
- Types: string
- Occurrences: 288

ApplicantName
- Types: string
- Occurrences: 189

ApplicantNameCN
- Types: string
- Occurrences: 28

ApplicantNameEN
- Types: null, string
- Occurrences: 148

ApplicantTel
- Types: null, string
- Occurrences: 307

ApplicationNo
- Types: null, string
- Occurrences: 381

ApplicationType
- Types: string
- Occurrences: 356

Area
- Types: string
- Occurrences: 28

BlockID
- Types: string
- Occurrences: 178

ContactPerson
- Types: string
- Occurrences: 95

ContactPersonCN
- Types: string
- Occurrences: 6

ContactPersonEN
- Types: string
- Occurrences: 6

ContactPersonEmail
- Types: string
- Occurrences: 6

ContactPersonTel
- Types: string
- Occurrences: 6

DescriptionOfSchool
- Types: string, null
- Occurrences: 329

District
- Types: string
- Occurrences: 33

EstimatedNoOfStudent
- Types: int, null
- Occurrences: 328

FileReference
- Types: string
- Occurrences: 35

NameOfSchoolCN
- Types: string
- Occurrences: 323

NameOfSchoolEN
- Types: string
- Occurrences: 350

Region
- Types: string
- Occurrences: 29

RelatedPremise
- Types: string
- Occurrences: 62

RelatedPremises
- Types: array
- Occurrences: 381

SelfCertification
- Types: object, null
- Occurrences: 65

StructuralCalculation
- Types: object
- Occurrences: 18

SubmissionType
- Types: string
- Occurrences: 187

__v
- Types: int
- Occurrences: 381

_id
- Types: objectId
- Occurrences: 381

address
- Types: object
- Occurrences: 69

assignedBS
- Types: objectId, string, null
- Occurrences: 364

assignedGR
- Types: objectId, null
- Occurrences: 64

assignedSBS
- Types: string, null
- Occurrences: 53

createdAt
- Types: date
- Occurrences: 381

updatedAt
- Types: date
- Occurrences: 194

**Potential Optimization Areas:**

*   This collection has many string fields.  Consider indexing fields frequently used in search or filtering, such as `ApplicationNo`, `NameOfSchoolEN`, `ApplicantName`, `assignedBS`, `assignedGR`, and `SubmissionType`.  The mixed types in `assignedBS` require careful index design.

### Collection: notifications

----------------------------------------

#### Collection Statistics

- Document Count: 1837
- Size: 0.24 MB
- Average Document Size: 0.13 KB

#### Field Analysis

__v
- Types: int
- Occurrences: 1000

_id
- Types: objectId
- Occurrences: 1000

createdAt
- Types: date
- Occurrences: 1000

eminute
- Types: objectId
- Occurrences: 58

notificationType
- Types: string
- Occurrences: 1000

requireSendEmail
- Types: bool
- Occurrences: 1000

task
- Types: objectId
- Occurrences: 942

user
- Types: string
- Occurrences: 991

**Potential Optimization Areas:**

*   Indexing `task`, `user`, and `notificationType` is recommended if these fields are used in queries.

### Collection: bsblocks

----------------------------------------

#### Collection Statistics

- Document Count: 98397
- Size: 6.40 MB
- Average Document Size: 0.07 KB

#### Field Analysis

__v
- Types: int
- Occurrences: 1000

_id
- Types: objectId
- Occurrences: 1000

bdgis
- Types: string
- Occurrences: 1000

blockId
- Types: string
- Occurrences: 1000

**Potential Optimization Areas:**

*   Indexing `blockId` and `bdgis` is crucial for efficient lookups in this relatively large collection.

### Collection: cases

----------------------------------------

#### Collection Statistics

- Document Count: 451
- Size: 1.17 MB
- Average Document Size: 2.65 KB

#### Field Analysis

ActualReplyDate
- Types: null, date
- Occurrences: 39

Area
- Types: string
- Occurrences: 26

AuditResult
- Types: string
- Occurrences: 11

CaseOfficer
- Types: string
- Occurrences: 108

Category
- Types: string
- Occurrences: 384

District
- Types: string
- Occurrences: 37

FileReference
- Types: string
- Occurrences: 60

LAFileReference
- Types: object
- Occurrences: 17

Nature
- Types: null, string
- Occurrences: 382

ObjectiontoLR
- Types: string
- Occurrences: 12

ReceivedDate
- Types: date, null
- Occurrences: 375

Referrer
- Types: object
- Occurrences: 43

Region
- Types: string
- Occurrences: 32

Remarks
- Types: string
- Occurrences: 7

Reminders
- Types: array
- Occurrences: 55

SubmissionType
- Types: string
- Occurrences: 8

SubstantialReplyDate
- Types: null, date
- Occurrences: 42

TargetReplyDate
- Types: date, null
- Occurrences: 111

ThreeTierReqt
- Types: string
- Occurrences: 12

ViaSCS
- Types: bool
- Occurrences: 17

__v
- Types: int
- Occurrences: 451

_id
- Types: objectId
- Occurrences: 451

application
- Types: objectId
- Occurrences: 450

assignedBS
- Types: objectId
- Occurrences: 274

assignedGR
- Types: objectId
- Occurrences: 137

building_information
- Types: object
- Occurrences: 14

caseDescription
- Types: object
- Occurrences: 9

caseOfficerReceive
- Types: string
- Occurrences: 172

caseOfficerReply
- Types: string
- Occurrences: 72

createdAt
- Types: date
- Occurrences: 451

deck_study
- Types: object
- Occurrences: 451

documentChecklist
- Types: object
- Occurrences: 2

dv
- Types: object
- Occurrences: 197

frc
- Types: object
- Occurrences: 451

misc
- Types: object
- Occurrences: 451

moe
- Types: object
- Occurrences: 451

seniorCaseOfficerReceive
- Types: string
- Occurrences: 54

seniorCaseOfficerReply
- Types: string
- Occurrences: 41

site_inspection
- Types: object
- Occurrences: 7

structural_ccc_bs
- Types: object
- Occurrences: 451

structural_schnlh
- Types: object
- Occurrences: 152

structural_schnlhkinds
- Types: object
- Occurrences: 301

team
- Types: string
- Occurrences: 374

ubw
- Types: object
- Occurrences: 451

updatedAt
- Types: date
- Occurrences: 16

**Potential Optimization Areas:**

*   Given the relatively large average document size, indexing is important. Consider indexing `application`, `assignedBS`, `assignedGR`, `Category`, `CaseOfficer`, `ReceivedDate`, and `team`.

### Collection: oauthtokens

----------------------------------------

#### Collection Statistics

- Document Count: 3019
- Size: 2.29 MB
- Average Document Size: 0.78 KB

#### Field Analysis

__v
- Types: int
- Occurrences: 1000

_id
- Types: objectId
- Occurrences: 1000

accessToken
- Types: string
- Occurrences: 1000

accessTokenExpiresAt
- Types: date
- Occurrences: 1000

client
- Types: object
- Occurrences: 1000

refreshToken
- Types: string
- Occurrences: 1000

refreshTokenExpiresAt
- Types: date
- Occurrences: 1000

user
- Types: objectId
- Occurrences: 1000

**Potential Optimization Areas:**

*   Indexing `accessToken`, `refreshToken`, and `user` is crucial for authentication and authorization performance.

### Collection: sysfilerefs

----------------------------------------

#### Collection Statistics

- Document Count: 601808
- Size: 204.70 MB
- Average Document Size: 0.35 KB

#### Field Analysis

__v
- Types: int
- Occurrences: 1000

_id
- Types: objectId
- Occurrences: 1000

createdDt
- Types: date
- Occurrences: 1000

createdName
- Types: null, string
- Occurrences: 1000

createdPost
- Types: null, string
- Occurrences: 1000

createdSection
- Types: null, string
- Occurrences: 1000

display
- Types: string
- Occurrences: 1000

dvExceed
- Types: null, string
- Occurrences: 1000

dvStatusDt
- Types: null, date
- Occurrences: 1000

frefPref
- Types: string, null
- Occurrences: 1000

frefSeq
- Types: null, string
- Occurrences: 1000

frefSuf
- Types: null, string
- Occurrences: 1000

frefYr
- Types: null, string
- Occurrences: 1000

lastModifiedDt
- Types: date
- Occurrences: 1000

lastModifiedName
- Types: null, string
- Occurrences: 1000

lastModifiedPost
- Types: null, string
- Occurrences: 1000

lastModifiedSection
- Types: null
- Occurrences: 1000

sysFileRefId
- Types: string
- Occurrences: 1000

**Potential Optimization Areas:**

*   This is the largest collection. Indexing `sysFileRefId` is essential. Consider compound indexes on `frefPref`, `frefSeq`, and `frefYr` if these are frequently used together in queries. Indexing `createdDt` and `lastModifiedDt` may also be beneficial depending on query patterns.

### Collection: attachments

----------------------------------------

#### Collection Statistics

- Document Count: 370
- Size: 0.13 MB
- Average Document Size: 0.37 KB

#### Field Analysis

__v
- Types: int
- Occurrences: 370

_id
- Types: objectId
- Occurrences: 370

application
- Types: objectId
- Occurrences: 364

createdAt
- Types: date
- Occurrences: 370

efolio
- Types: null, string
- Occurrences: 351

file
- Types: object, string
- Occurrences: 247

filePartNo
- Types: string
- Occurrences: 216

receivedDate
- Types: date
- Occurrences: 352

remarks
- Types: string
- Occurrences: 216

subType
- Types: string
- Occurrences: 203

submissionCase
- Types: objectId
- Occurrences: 350

sysFileRefId
- Types: string
- Occurrences: 67

type
- Types: string
- Occurrences: 348

updatedAt
- Types: date
- Occurrences: 3

**Potential Optimization Areas:**

*   Indexing `application`, `submissionCase`, `sysFileRefId`, and `type` is recommended. The mixed types in `file` require careful index design.

### Collection: users

----------------------------------------

#### Collection Statistics

- Document Count: 116
- Size: 0.04 MB
- Average Document Size: 0.39 KB

#### Field Analysis

__v
- Types: int
- Occurrences: 116

_id
- Types: objectId
- Occurrences: 116

bdgis
- Types: string
- Occurrences: 29

begis
- Types: string
- Occurrences: 1

delegateTo
- Types: string
- Occurrences: 8

department
- Types: string
- Occurrences: 116

email
- Types: string
- Occurrences: 109

group
- Types: string
- Occurrences: 17

lastLoginAt
- Types: date
- Occurrences: 41

letterLongPosition
- Types: string
- Occurrences: 11

letterLongPositionCn
- Types: string
- Occurrences: 12

letterName
- Types: string
- Occurrences: 76

letterNameCn
- Types: string
- Occurrences: 75

letterPosition
- Types: string
- Occurrences: 79

letterPositionCn
- Types: string
- Occurrences: 1

lock
- Types: bool
- Occurrences: 116

luPostName
- Types: string
- Occurrences: 78

name
- Types: string
- Occurrences: 80

notificationEmail
- Types: string
- Occurrences: 23

osdpEmail
- Types: string
- Occurrences: 62

osdpLoginId
- Types: string
- Occurrences: 102

password
- Types: string
- Occurrences: 108

phoneNumber
- Types: string
- Occurrences: 65

position
- Types: string
- Occurrences: 85

role
- Types: string
- Occurrences: 112

team
- Types: string
- Occurrences: 52

userType
- Types: string
- Occurrences: 116

**Potential Optimization Areas:**

*   Indexing `osdpLoginId`, `email`, `role`, and `team` is critical for user authentication, authorization, and role-based access control.

### Collection: adrblkfilerefs

----------------------------------------

#### Collection Statistics

- Document Count: 566948
- Size: 154.89 MB
- Average Document Size: 0.28 KB

#### Field Analysis

__v
- Types: int
- Occurrences: 1000

_id
- Types: objectId
- Occurrences: 1000

adrBlkFileRefId
- Types: string
- Occurrences: 1000

adrBlkId
- Types: string
- Occurrences: 1000

createdDt
- Types: date
- Occurrences: 1000

createdName
- Types: null, string
- Occurrences: 1000

createdPost
- Types: string
- Occurrences: 1000

createdSection
- Types: null, string
- Occurrences: 1000

lastModifiedDt
- Types: date
- Occurrences: 1000

lastModifiedName
- Types: null, string
- Occurrences: 1000

lastModifiedPost
- Types: string
- Occurrences: 1000

lastModifiedSection
- Types: string, null
- Occurrences: 1000

sysFileRefId
- Types: string
- Occurrences: 1000

**Potential Optimization Areas:**

*   This is a large collection. Indexing `adrBlkFileRefId`, `adrBlkId`, and `sysFileRefId` is essential.

---

**Recommendations based on Database Analysis:**

Based on the database analysis, the following recommendations are made to improve performance:

1.  **Indexing:**  Implement indexes on frequently queried