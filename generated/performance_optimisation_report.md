# Performance Optimization Report
**For Licensing Self-Certification Portal of Buildings Department**

**Version 0.1**
**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

## Distribution

| Copy No. | Holder                                          |
|---------|-------------------------------------------------|
| 1       | Buildings Department (BD)                       |
| 2       | Master Concept (Hong Kong) Limited (MC)        |

## Amendment History

| Change Number | Revision Description | Pages Affected | Revision/ Version Number | Date       |
|---------------|----------------------|----------------|--------------------------|------------|
| 1             | 1st draft            | All            | 0.1                      | 16/01/2025 |
|               |                      |                |                          |            |
|               |                      |                |                          |            |
|               |                      |                |                          |            |
|               |                      |                |                          |            |

## Table of Contents

1.  [Introduction](#introduction)
    *   [1.1 Goal of Performance Optimization](#goal-of-performance-optimization)
        *   [1.1.1 Server Loading](#server-loading)
        *   [1.1.2 Bandwidth Usage](#bandwidth-usage)
        *   [1.1.3 Better user experience](#better-user-experience)
    *   [1.2 Performance Optimisation Actions](#performance-optimisation-actions)
    *   [1.3 Storage Allocation](#storage-allocation)
    *   [1.4 Required Response Time](#required-response-time)
        *   [1.4.1 Online Transaction](#online-transaction)
        *   [1.4.2 Online Reports](#online-reports)
2.  [Critical online transition timing](#critical-online-transition-timing)
3.  [Critical Batch Cycle Timing](#critical-batch-cycle-timing)
4.  [Optimization changes](#optimization-changes)
    *   [4.1 Optimization Actions](#optimization-actions)
        *   [4.1.1 Create stored procedures](#create-stored-procedures)
        *   [4.1.2 Create clustered indexes](#create-clustered-indexes)
5.  [Database Analysis](#database-analysis)

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

*   Optimize the programming and query logic to reduce server loading burden.
*   Optimize the page size and image size to reduce bandwidth burden.
*   Improve resourcing retrieval speed by indexing and hashing.
*   Cache frequently used resources.
*   Pre-generate resource that required heavy instant server loading.
*   Improve resourcing retrieval speed by indexing and hashing.
*   Reduce waiting time of third-party services.
*   Archive expired records to keep the size of active datastore minimal

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

*   Maximum number of Concurrent users is 100.
*   Minimal bandwidth is 2Mb/s per testing machine.
*   Maximum network round-trip latency (ping) to the Integrated system is 200ms.
*   Remote testing site will have **50% mark-up** time to the committed response time.

### 1.4.1 Online Transaction

The programs in the following category are classified as online transaction:

*   User Account Program
*   Form and Record Management Program

Online transactions can be classified into the following groups:

| Transaction Complexity | Number of Concurrent Users |            |          |     |
|----------------------|----------------------------|------------|----------|-----|
|                        | 40                         | 80         | 100      |     |
| Simple                 | < 1 sec                    | < 2 sec    | < 3 sec  |     |
| Medium                 | < 2 sec                    | < 3 sec    | < 4 sec  |     |
| Complex                | < 2.5 sec                  | < 3.5 sec  | < 5 sec  |     |

Online transactions can also be classified as follows:

| Online transactions         | Description                                                                       |
|-----------------------------|-----------------------------------------------------------------------------------|
| Online Update Transactions  | Used to update records in LSCP, for example, create supervision plan              |
| Online Enquiry Transactions | Used to retrieve records from LSCP, for example, filter site monitoring records   |
| Full-text Search            | Used to search for records with given key words, for example, search assigned TCP |

### 1.4.2 Online Reports

The programs in the following category are classified as online reports:

*   XXXXXXXXXXX

As the report is a standalone internal system for BD, the measurement would only estimate when the concurrent users are not more than 20.

| On-line Reports | Committed Response Time |
|-----------------|-------------------------|
|                 |                         |
|                 |                         |

## 2. Critical Online Transition Timing

The following matrix is the list of programs with the complexity and transaction type being marked.

Offline module helps users save information in local devices when Internet connectivity is not available. Once Internet connectivity is back, it will submit the data and store it in the database. The major difference between offline modules with other modules is that the offline module is asynchronous. It will not submit immediately but will wait until the Internet is available. For the asynchronous handling logic, we included it in the functional test. On the other hand, the data sending logic is no different with other API, thus we would not have a separate section for offline module in critical online transition timing.

| **Module ID** | **Program ID** | **Program Name** | **Complexity (Simple / Medium / Complex)** | **Online Transaction Program** | **Report Program** | **Type of transactions** | **Mobile Apps** |
|---------------|----------------|------------------|------------------------------------------|--------------------------------|--------------------|--------------------------|-----------------|
|               |                |                  |                                          |                                |                    |                          |                 |
| **USER ACCOUNT PROGRAM** |                  |                |            |                  |                           |                  |                           |
|               |                |                  |                                          |                                |                    |                          |                 |
|               |                |                  |                                          |                                |                    |                          |                 |
|               |                |                  |                                          |                                |                    |                          |                 |
|               |                |                  |                                          |                                |                    |                          |                 |
|               |                |                  |                                          |                                |                    |                          |                 |
|               |                |                  |                                          |                                |                    |                          |                 |

## 3. Critical Batch Cycle Timing

The below are the list of batch programs. The cycle timing of the batch is identified in the tables below.
They are different from modules in the last section whereas they will run a thousand times everyday but the modules in this section probably run once or twice daily. Moreover, most of the modules described in this section are scheduled jobs running in backend, normally, the fluctuation of performance in these items would not affect the end user. Except, the generate report module, has a higher impact, thus it is the only item required to optimize.

| **Program ID** | **Program Name** | **Online Web** | **Mobile** | **Update Batch** | **Require Optimization?** | **Cycle Timing** |
|----------------|----------------|----------------|------------|------------------|---------------------------|----------------|
| **BATCH PROGRAM** |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |

## 4. Optimization changes

The optimization will **<u>only</u>** focus the performance on programs and reports.

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

## 5. Database Analysis

### Database Statistics
- Database Name: bd
- Last Updated: 2025/3/4 ??10:10:39
- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1278983
- Total Data Size: 371.24 MB

### Collections Overview
| Collection      | Document Count | Size (MB) |
|-----------------|----------------|-----------|
| tasks           | 5523           | 0.99      |
| eminutes        | 133            | 0.03      |
| submissions     | 0              | 0.00      |
| applications    | 381            | 0.36      |
| notifications   | 1837           | 0.24      |
| bsblocks        | 98397          | 6.40      |
| cases           | 451            | 1.17      |
| oauthtokens     | 3019           | 2.29      |
| sysfilerefs     | 601808         | 204.70    |
| attachments     | 370            | 0.13      |
| users           | 116            | 0.04      |
| adrblkfilerefs  | 566948         | 154.89    |

### Collection Analysis

#### Collection: tasks
- Document Count: 5523
- Size: 0.99 MB
- Average Document Size: 0.18 KB

**Field Analysis:**

| Field          | Types              | Occurrences |
|----------------|--------------------|-------------|
| \_\_v          | objectId, int      | 1000        |
| \_id           | objectId           | 1000        |
| application    | objectId           | 998         |
| createdAt      | date               | 1000        |
| status         | string             | 1000        |
| submissionCase | objectId           | 998         |
| taskType       | string             | 998         |
| team           | string             | 835         |
| user           | string, objectId   | 713         |

**Potential Optimization:** Consider indexing the `application`, `submissionCase` and `user` fields if they are frequently used in queries.

#### Collection: eminutes
- Document Count: 133
- Size: 0.03 MB
- Average Document Size: 0.24 KB

**Field Analysis:**

| Field          | Types              | Occurrences |
|----------------|--------------------|-------------|
| \_\_v          | int                | 133         |
| \_id           | objectId           | 133         |
| comment        | string             | 64          |
| content        | string             | 133         |
| createdAt      | date               | 133         |
| efolio         | string             | 100         |
| eminuteId      | string             | 133         |
| from           | objectId, string   | 133         |
| status         | string             | 133         |
| subject        | string             | 133         |
| submissionCase | objectId           | 133         |
| sysFileRefId   | string             | 65          |
| to             | objectId, string   | 129         |

**Potential Optimization:** Consider indexing `submissionCase`, `from`, and `to` fields if used in queries.

#### Collection: submissions
- Document Count: 0
- Size: 0.00 MB
- Average Document Size: 0.00 KB

**Note:** This collection is currently empty.

#### Collection: applications
- Document Count: 381
- Size: 0.36 MB
- Average Document Size: 0.96 KB

**Field Analysis:** (Partial - Showing only a few fields for brevity)

| Field                     | Types               | Occurrences |
|---------------------------|---------------------|-------------|
| APP13                     | object, array       | 172         |
| AddressOfPremiseCN        | string              | 267         |
| AddressOfPremiseEN        | string              | 271         |
| AgeOfStudent              | null, string        | 328         |
| ApplicantAddress          | string              | 335         |
| ApplicantEmail            | string              | 289         |
| ApplicationNo             | null, string        | 381         |
| ApplicationType           | string              | 356         |
| RelatedPremises           | array               | 381         |
| \_\_v                     | int                 | 381         |
| \_id                      | objectId            | 381         |
| assignedBS                | objectId, string, null| 364         |
| createdAt                 | date                | 381         |
| updatedAt                 | date                | 194         |

**Potential Optimization:**  Indexing `ApplicationNo`, `ApplicationType`, and `assignedBS` would likely improve query performance.  Consider indexing other fields based on common search criteria.  The `RelatedPremises` array might benefit from specific indexing strategies if its contents are frequently queried.

#### Collection: notifications
- Document Count: 1837
- Size: 0.24 MB
- Average Document Size: 0.13 KB

**Field Analysis:**

| Field            | Types        | Occurrences |
|------------------|--------------|-------------|
| \_\_v            | int          | 1000        |
| \_id             | objectId     | 1000        |
| createdAt        | date         | 1000        |
| eminute          | objectId     | 58          |
| notificationType | string       | 1000        |
| requireSendEmail | bool         | 1000        |
| task             | objectId     | 942         |
| user             | string       | 991         |

**Potential Optimization:** Indexing `task` and `user` fields is recommended.

#### Collection: bsblocks
- Document Count: 98397
- Size: 6.40 MB
- Average Document Size: 0.07 KB

**Field Analysis:**

| Field     | Types  | Occurrences |
|-----------|--------|-------------|
| \_\_v     | int    | 1000        |
| \_id      | objectId| 1000        |
| bdgis     | string | 1000        |
| blockId   | string | 1000        |

**Potential Optimization:** Indexing `blockId` and `bdgis` is recommended.

#### Collection: cases
- Document Count: 451
- Size: 1.17 MB
- Average Document Size: 2.65 KB

**Field Analysis:** (Partial - Showing only a few fields for brevity)

| Field               | Types        | Occurrences |
|---------------------|--------------|-------------|
| ActualReplyDate     | null, date   | 39          |
| Category            | string       | 384         |
| ReceivedDate        | date, null   | 375         |
| \_\_v               | int          | 451         |
| \_id                | objectId     | 451         |
| application         | objectId     | 450         |
| assignedBS          | objectId     | 274         |
| assignedGR          | objectId     | 137         |
| createdAt           | date         | 451         |
| team                | string       | 374         |
| updatedAt           | date         | 16          |

**Potential Optimization:** Index `application`, `assignedBS`, `assignedGR`, `Category`, and `team`.

#### Collection: oauthtokens
- Document Count: 3019
- Size: 2.29 MB
- Average Document Size: 0.78 KB

**Field Analysis:**

| Field                 | Types    | Occurrences |
|-----------------------|----------|-------------|
| \_\_v                 | int      | 1000        |
| \_id                  | objectId | 1000        |
| accessToken           | string   | 1000        |
| accessTokenExpiresAt  | date     | 1000        |
| client                | object   | 1000        |
| refreshToken          | string   | 1000        |
| refreshTokenExpiresAt | date     | 1000        |
| user                  | objectId | 1000        |

**Potential Optimization:** Index `user`, `accessToken`, and `refreshToken`.

#### Collection: sysfilerefs
- Document Count: 601808
- Size: 204.70 MB
- Average Document Size: 0.35 KB

**Field Analysis:** (Partial - Showing only a few fields for brevity)

| Field            | Types       | Occurrences |
|------------------|-------------|-------------|
| \_\_v            | int         | 1000        |
| \_id             | objectId    | 1000        |
| createdDt        | date        | 1000        |
| createdName      | null, string| 1000        |
| sysFileRefId     | string      | 1000        |

**Potential Optimization:** Index `sysFileRefId`. Consider indexing `createdDt` and `createdName` based on query patterns.

#### Collection: attachments
- Document Count: 370
- Size: 0.13 MB
- Average Document Size: 0.37 KB

**Field Analysis:**

| Field          | Types              | Occurrences |
|----------------|--------------------|-------------|
| \_\_v          | int                | 370         |
| \_id           | objectId           | 370         |
| application    | objectId           | 364         |
| createdAt      | date               | 370         |
| efolio         | null, string       | 351         |
| file           | object, string     | 247         |
| submissionCase | objectId           | 350         |
| sysFileRefId   | string             | 67          |
| type           | string             | 348         |

**Potential Optimization:** Index `application`, `submissionCase`, `type`, and `sysFileRefId`.

#### Collection: users
- Document Count: 116
- Size: 0.04 MB
- Average Document Size: 0.39 KB

**Field Analysis:** (Partial - Showing only a few fields for brevity)

| Field             | Types  | Occurrences |
|-------------------|--------|-------------|
| \_\_v             | int    | 116         |
| \_id              | objectId| 116         |
| department        | string | 116         |
| email             | string | 109         |
| osdpLoginId       | string | 102         |
| role              | string | 112         |
| userType          | string | 116         |

**Potential Optimization:** Index `email`, `osdpLoginId`, and `role`.

#### Collection: adrblkfilerefs
- Document Count: 566948
- Size: 154.89 MB
- Average Document Size: 0.28 KB

**Field Analysis:**

| Field             | Types  | Occurrences |
|-------------------|--------|-------------|
| \_\_v             | int    | 1000        |
| \_id              | objectId| 1000        |
| adrBlkFileRefId   | string | 1000        |
| adrBlkId          | string | 1000        |
| createdDt         | date   | 1000        |
| createdName       | null, string| 1000        |
| createdPost       | string | 1000        |
| sysFileRefId      | string | 1000        |

**Potential Optimization:** Index `adrBlkFileRefId`, `adrBlkId`, and `sysFileRefId`.

\<End of Document\>