```markdown
<img src="media/image1.jpg" style="width:2.02569in;height:1.51944in"
alt="BDlogo" />**<span class="smallcaps">
</span>**

**<span class="smallcaps">PERFORMANCE OPTIMIZATION REPORT</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">COMBINED SYSTEM DEVELOPMENT SERVICES</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**<span class="smallcaps">OF</span>**

**<span class="smallcaps">BUILDINGS DEPARTMENT</span>**

**Version 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR.

<table>
<colgroup>
<col style="width: 28%" />
<col style="width: 71%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Distribution</strong></th>
</tr>
<tr class="odd">
<th>Copy No.</th>
<th>Holder</th>
</tr>
<tr class="header">
<th>1</th>
<th><blockquote>
<p>Buildings Department (BD)</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>2</th>
<th><blockquote>
<p>Master Concept (Hong Kong) Limited (MC)</p>
</blockquote></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

| Amendment History |                      |                |                          |            |
|---------|------------------------------|-----------|----------|-------------|
| Change Number     | Revision Description | Pages Affected | Revision/ Version Number | Date       |
| 1                 | 1st draft            | All            | 0.1                      | 16/01/2025 |
|                   |                      |                |                          |            |
|                   |                      |                |                          |            |
|                   |                      |                |                          |            |
|                   |                      |                |                          |            |

**TABLE OF CONTENTS**

[**1. Introduction 5**](#introduction)

> [1.1 Goal of Performance Optimization
> 6](#goal-of-performance-optimization)
>
> [1.1.1 Server Loading 6](#server-loading)
>
> [1.1.2 Bandwidth Usage 6](#bandwidth-usage)
>
> [1.1.3 Better user experience 6](#better-user-experience)
>
> [1.2 Performance Optimisation Actions
> 7](#performance-optimisation-actions)
>
> [1.3 Storage Allocation 8](#storage-allocation)
>
> [1.4 Required Response Time 9](#required-response-time)
>
> [1.4.1 Online Transaction 9](#online-transaction)
>
> [1.4.2 Online Reports 10](#online-reports)
>
> [1.5 Database Overview](#database-overview)

[**2. Critical online transition timing
11**](#critical-online-transition-timing)

[**3. Critical Batch Cycle Timing 12**](#critical-batch-cycle-timing)

[**4. Optimization changes 13**](#optimization-changes)

> [4.1 Optimization Actions 14](#optimization-actions)
>
> [4.1.1 Create stored procedures 14](#create-stored-procedures)
>
> [4.1.2 Create clustered indexes 14](#create-clustered-indexes)
>
> [4.2 Database Performance Analysis](#database-performance-analysis)

## 1. Introduction

The performance optimization of the system could be classified into
optimization of Online Transaction. This report outlines the performance optimization strategies for the Licensing Self-Certification Portal (LSCP) system, considering both application and database aspects.

## 1.1 Goal of Performance Optimization

The main goal of performance optimization is to improve the response
time of the system to users. In order to achieve better response time,
the program implementation should take the following areas into
consideration.

### 1.1.1 Server Loading

The Capacity of Server Loading is a fixed variable of a system. An
increase in server loading would increase the response time of the
system. Server loading is affected by

1.  the number of system users; and

2.  the efficiency of the programming code.

When the number of system users increases, the server loading increases
and hence there is less resource for running programming code for each
system user. The response of the program would be slower as there is
less server resource for the program to utilize.

On the other hand, if the programming code could use fewer server
resources, there is less server loading and hence the server could
respond to users quicker and serve more users simultaneously.

Therefore, response time could be reduced if the programming code could
be optimized to use fewer server resources.

### 1.1.2 Bandwidth Usage

Capacity of Bandwidth Usage is a fixed variable of a system. An increase
in bandwidth usage would decrease the response time of the system.
Bandwidth loading is affected by

1.  the number of system users; and

2.  the size of transmitting resource.

When the number of system users increases, the bandwidth usage increases
and hence there is less bandwidth resource for transmitting data to each
system user. The response time would be slower as there is less
bandwidth for each user to utilize.

On the other hand, if the size of transmitting data is smaller, there is
less bandwidth usage and hence the fixed network bandwidth could serve
more users simultaneously.

Therefore, response time could be reduced if the size of the
transmitting resource could be optimized to use less server resources.

### 1.1.3 Better User Experience

This application will be used by the public, in order words, it
represents the department. If it performs well, the department can take
credit from it, the image of the department may be affected if this
application performs bad or causes other problems, for example very slow
or no response.

## 1.2 Performance Optimisation Actions

To serve more users simultaneously with better response time, the system
and the programs should be optimized to use the server loading and
bandwidth resource more efficiently. The followings are the possible
measures that could be taken generally:

-   Optimize the programming and query logic to reduce server loading
    burden.
-   Optimize the page size and image size to reduce bandwidth burden.
-   Improve resourcing retrieval speed by indexing and hashing.
-   Cache frequently used resources.
-   Pre-generate resource that required heavy instant server loading.
-   Improve resourcing retrieval speed by indexing and hashing.
-   Reduce waiting time of third-party services.
-   Archive expired records to keep the size of active datastore minimal

## 1.3 Storage Allocation

The storage of the database data will be stored as following:

i\. System data ? Store in the ?Database? server in the Integrated
system.

ii\. Textual data ? Store in the ?Database? server in the Integrated
system.

All the required system and textual data will be logical stored in
various filegroup of <u>Microsoft SQL Server</u>
<span class="mark"></span>database. The following table shows the logic
data storage in Microsoft SQL Server database.

| FileGroup | TableName      | TableSize |
|-----------|----------------|-----------|
| PRIMARY   | tasks          | 0.99 MB   |
| PRIMARY   | eminutes       | 0.03 MB   |
| PRIMARY   | submissions    | 0.00 MB   |
| PRIMARY   | applications   | 0.36 MB   |
| PRIMARY   | notifications  | 0.24 MB   |
| PRIMARY   | bsblocks       | 6.40 MB   |
| PRIMARY   | cases          | 1.17 MB   |
| PRIMARY   | oauthtokens    | 2.29 MB   |
| PRIMARY   | sysfilerefs    | 204.70 MB |
| PRIMARY   | attachments    | 0.13 MB   |
| PRIMARY   | users          | 0.04 MB   |
| PRIMARY   | adrblkfilerefs | 154.89 MB |

The filegroup growth size has set to meet the recommendation for below
256 MB for data files.

## 1.4 Required Response Time

The required response time is defined according to 2 pre-defined
categories. They are Online Transaction and Online Report. All of the
programs and reports that require to interact and provide immediate
response to users are categorized. The categorized programs and reports
should respond to the user within required response time. The required response time should be defined according to the complexity of the
programs. The required response time and the complexity will be
discussed in the coming section.

For those procedures or reports that could not able to optimize to have
immediate response, some part of the program that take a lot of
processing time will be swapped to batch job.

95% of all online functions should meet the committed response time.

The committed response time is affected by the network status of the
site. The environment of testing site should meet an agreed network
health level. The following criteria define the agreed network health
level.

-   Maximum number of Concurrent users is 100.
-   Minimal bandwidth is 2Mb/s per testing machine.
-   Maximum network round-trip latency (ping) to the Integrated system
    is 200ms.
-   Remote testing site will have **50% mark-up** time to the committed
    response time.

### 1.4.1 Online Transaction

The programs in the following category are classified as online
transaction:

-   User Account Program
-   Form and Record Management Program

Online transactions can be classified into the following groups:

<span class="mark">\[RY Note: Needs user input/ refer to Load Test data
given by user\]</span>

| Transaction Complexity | Number of Concurrent Users |            |          |     |
|---------------------|-----------------|-----------------|-----------------|--|
|                        | 40                         | 80         | 100      |     |
| Simple                 | \< 1 sec                   | \< 2 sec   | \< 3 sec |     |
| Medium                 | \< 2 sec                   | \< 3 sec   | \< 4 sec |     |
| Complex                | \< 2.5 sec                 | \< 3.5 sec | \< 5 sec |     |

Online transactions can also be classified as follows:

| Online transactions         | Description                                                                       |
|---------------------------------|---------------------------------------|
| Online Update Transactions  | Used to update records in LSCP, for example, create supervision plan              |
| Online Enquiry Transactions | Used to retrieve records from LSCP, for example, filter site monitoring records   |
| Full-text Search            | Used to search for records with given key words, for example, search assigned TCP |

### 1.4.2 Online Reports

The programs in the following category are classified as online reports:

-   XXXXXXXXXXX

As the report is a standalone internal system for BD, the measurement
would only estimate when the concurrent users are not more than 20.

| On-line Reports | Committed Response Time |
|-----------------|-------------------------|
|                 | \[To be defined]        |
|                 | \[To be defined]        |

### 1.5 Database Overview

This section provides an overview of the database "bd" as analyzed on 2025/3/4 ??10:10:39.

**Database Statistics:**

- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1278983
- Total Data Size: 371.24 MB

**Collections Overview:**

The database consists of 12 collections. The collections "sysfilerefs" and "adrblkfilerefs" are the largest in terms of size and document count, contributing significantly to the overall database size.

- **Large Collections (by Document Count):**
    - sysfilerefs: 601808 documents
    - adrblkfilerefs: 566948 documents
    - bsblocks: 98397 documents

- **Large Collections (by Size):**
    - sysfilerefs: 204.70 MB
    - adrblkfilerefs: 154.89 MB
    - bsblocks: 6.40 MB

- **Collections with No Documents:**
    - submissions: 0 documents

The "submissions" collection currently contains no documents. It's important to monitor this collection in the future to understand its data growth and potential performance impact.

The "tasks", "eminutes", "applications", "notifications", "cases", "oauthtokens", "attachments", and "users" collections are relatively smaller in size and document count compared to "sysfilerefs" and "adrblkfilerefs".

# 2. Critical Online Transition Timing

The following matrix is the list of programs with the complexity and
transaction type being marked.

Offline module helps users save information in local devices when
Internet connectivity is not available. Once Internet connectivity is
back, it will submit the data and store it in the database. The major
difference between offline modules with other modules is that the
offline module is asynchronous. It will not submit immediately but will
wait until the Internet is available. For the asynchronous handling
logic, we included it in the functional test. On the other hand, the
data sending logic is no different with other API, thus we would not
have a separate section for offline module in critical online transition
timing.

<table>
<colgroup>
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 16%" />
<col style="width: 13%" />
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 12%" />
<col style="width: 18%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Module ID</strong></th>
<th><strong>Program ID</strong></th>
<th><strong>Program Name</strong></th>
<th><blockquote>
<p><strong>Complexity<br />
(Simple / Medium / Complex)</strong></p>
</blockquote></th>
<th><blockquote>
<p><strong>Online Transaction Program</strong></p>
</blockquote></th>
<th><blockquote>
<p><strong>Report Program</strong></p>
</blockquote></th>
<th><strong>Type of transactions</strong></th>
<th><blockquote>
<p><strong>Mobile Apps</strong></p>
</blockquote></th>
</tr>
<tr class="odd">
<th colspan="6"><strong>USER ACCOUNT PROGRAM</strong></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>UA-01</th>
<th>UA_CREATE</th>
<th>Create User Account</th>
<th>Simple</th>
<th>?</th>
<th></th>
<th>Online Update Transactions</th>
<th></th>
</tr>
<tr class="odd">
<th>UA-02</th>
<th>UA_UPDATE</th>
<th>Update User Account</th>
<th>Medium</th>
<th>?</th>
<th></th>
<th>Online Update Transactions</th>
<th></th>
</tr>
<tr class="header">
<th>UA-03</th>
<th>UA_DELETE</th>
<th>Delete User Account</th>
<th>Simple</th>
<th>?</th>
<th></th>
<th>Online Update Transactions</th>
<th></th>
</tr>
<tr class="odd">
<th>UA-04</th>
<th>UA_SEARCH</th>
<th>Search User Account</th>
<th>Medium</th>
<th>?</th>
<th></th>
<th>Online Enquiry Transactions, Full-text Search</th>
<th></th>
</tr>
<tr class="header">
<th>UA-05</th>
<th>UA_LIST</th>
<th>List User Accounts</th>
<th>Simple</th>
<th>?</th>
<th></th>
<th>Online Enquiry Transactions</th>
<th></th>
</tr>
<tr class="odd">
<th colspan="6"><strong>FORM AND RECORD MANAGEMENT PROGRAM</strong></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>FR-01</th>
<th>FR_CREATE_APP</th>
<th>Create Application Form</th>
<th>Complex</th>
<th>?</th>
<th></th>
<th>Online Update Transactions</th>
<th>?</th>
</tr>
<tr class="odd">
<th>FR-02</th>
<th>FR_UPDATE_APP</th>
<th>Update Application Form</th>
<th>Complex</th>
<th>?</th>
<th></th>
<th>Online Update Transactions</th>
<th>?</th>
</tr>
<tr class="header">
<th>FR-03</th>
<th>FR_VIEW_APP</th>
<th>View Application Form</th>
<th>Medium</th>
<th>?</th>
<th></th>
<th>Online Enquiry Transactions</th>
<th>?</th>
</tr>
<tr class="odd">
<th>FR-04</th>
<th>FR_SEARCH_CASE</th>
<th>Search Case Record</th>
<th>Complex</th>
<th>?</th>
<th></th>
<th>Online Enquiry Transactions, Full-text Search</th>
<th></th>
</tr>
<tr class="header">
<th>FR-05</th>
<th>FR_LIST_CASES</th>
<th>List Case Records</th>
<th>Medium</th>
<th>?</th>
<th></th>
<th>Online Enquiry Transactions</th>
<th></th>
</tr>
</tbody>
</table>

# 3. Critical Batch Cycle Timing

The below are the list of batch programs. The cycle timing of the batch
is identified in the tables below.
They are different from modules in the last section whereas they will
run a thousand times everyday but the modules in this section probably
run once or twice daily. Moreover, most of the modules described in this
section are scheduled jobs running in backend, normally, the fluctuation
of performance in these items would not affect the end user. Except, the
generate report module, has a higher impact, thus it is the only item
required to optimize.

| **Program ID**    | **Program Name**           | **Online Web** | **Mobile** | **Update Batch** | **Require Optimization?** | **Cycle Timing** |
|----------------|--------------------------|---------|---------|---------|---------|--------|
| **BATCH-01**   | Daily Data Archiving     |         |            | ?       | Yes                     | Daily    |
| **BATCH-02**   | Weekly Report Generation |         |            | ?       | Yes                     | Weekly   |
| **BATCH-03**   | Monthly System Backup    |         |            | ?       | No                      | Monthly  |
| **BATCH-04**   | Notification Processing  | ?       | ?          | ?       | No                      | Hourly   |
| **BATCH-05**   | OAuth Token Cleanup      |         |            | ?       | No                      | Daily    |
| **BATCH-06**   | SysFileRef Cleanup       |         |            | ?       | Yes                     | Daily    |
| **BATCH-07**   | ADRBlkFileRef Cleanup    |         |            | ?       | Yes                     | Daily    |
| **BATCH-08**   | Submission Status Update | ?       | ?          | ?       | No                      | 15 Minutes|

# 4. Optimization changes

The optimization will **<u>only</u>** focus the performance on programs
and reports.

## 4.1 Optimization Actions

### 4.1.1 Create stored procedures

All reports are created by stored procedures. Stored procedures are
precompiled as opposed to the dynamic prepared statements that are
compiled whenever your application code invokes a call. Once you execute
a stored procedure, it remains in the cache, saving the execution time.
In addition, the stored procedures are mostly using primary key for
searching.

### 4.1.2 Create clustered indexes

When creating a primary key constraint, a unique clustered index on the
column or columns is automatically created if a clustered index on the
table does not already exist and you do not specify a unique
non-clustered index. The primary key column cannot allow NULL values. In
addition, when creating a unique constraint, a unique non-clustered
index is created to enforce a unique constraint by default. When
designing a clustered index, we have considered that the data types to
be used as clustering keys. For instance, the primary keys are BIGINT
data type which is the best choices as clustered index key.

| **Table ID** | **Table Name**     | **LSCP Entity** | **Key Nature** | **Index Field** |
|--------------|--------------------|-----------------|----------------|-----------------|
| TBL-01       | tasks              | Task            | Primary Key    | _id             |
| TBL-02       | eminutes           | E-Minute        | Primary Key    | _id             |
| TBL-03       | submissions        | Submission      | Primary Key    | _id             |
| TBL-04       | applications       | Application     | Primary Key    | _id             |
| TBL-05       | notifications      | Notification    | Primary Key    | _id             |
| TBL-06       | bsblocks           | BS Block        | Primary Key    | _id             |
| TBL-07       | cases              | Case            | Primary Key    | _id             |
| TBL-08       | oauthtokens        | OAuth Token     | Primary Key    | _id             |
| TBL-09       | sysfilerefs        | Sys File Ref    | Primary Key    | _id             |
| TBL-10       | attachments        | Attachment      | Primary Key    | _id             |
| TBL-11       | users              | User            | Primary Key    | _id             |
| TBL-12       | adrblkfilerefs     | ADR Blk File Ref| Primary Key    | _id             |

## 4.2 Database Performance Analysis

Based on the database schema analysis, the following points are relevant to performance optimization:

- **Large Collections**: The `sysfilerefs` and `adrblkfilerefs` collections are significantly larger than others. Optimizing queries and operations on these collections will have the most impact on overall database performance. Consider indexing frequently queried fields in these collections beyond the primary key.

- **`sysfilerefs` and `adrblkfilerefs` Field Analysis**: Review the field analysis for `sysfilerefs` and `adrblkfilerefs` in the `database_schema.md` for potential indexing opportunities. Fields like `sysFileRefId`, `adrBlkFileRefId`, `createdDt`, and `lastModifiedDt` appear to be commonly used and could benefit from indexing if they are frequently used in queries.

- **Mixed Data Types**: In the `tasks` collection, the `user` field has mixed types (string, objectId). While MongoDB is flexible, consistent data types can improve query performance and indexing efficiency. Investigate if this mixed type is intentional and if it can be standardized for better performance. Similarly, the `from` and `to` fields in `eminutes` and `assignedBS`, `assignedGR`, `assignedSBS` in `applications` also have mixed types. Review these for potential standardization.

- **`applications` Collection - Array and Object Types**: The `applications` collection contains fields with `object` and `array` types (e.g., `APP13`, `RelatedPremises`, `address`, `SelfCertification`, `StructuralCalculation`). Queries involving these complex types might be less efficient than those on simple data types. Analyze query patterns on these fields and consider optimization strategies if needed, such as indexing within arrays or embedded documents.

- **`cases` Collection - Nested Objects**: The `cases` collection has numerous nested object fields (e.g., `LAFileReference`, `Referrer`, `building_information`, `caseDescription`, `deck_study`, etc.).  Similar to arrays and objects in `applications`, complex queries on these nested fields might require optimization.

- **`submissions` Collection - Zero Documents**: While currently empty, understand the purpose of the `submissions` collection and anticipate its future data volume and query patterns for proactive performance planning.

- **Indexing Strategy**:  The report mentions creating clustered indexes. In MongoDB, indexes are crucial for query performance.  Review the existing indexes in the database (not provided in the input, but should be checked in the actual database). Ensure that indexes are created for fields frequently used in query filters, sorting, and joins (if applicable). Consider compound indexes for queries involving multiple fields.

- **Query Optimization**: Analyze slow queries using database profiling tools. Optimize these queries by reviewing query structure, using appropriate indexes, and potentially restructuring data or queries if necessary.

- **Data Archiving**: Implement the "Daily Data Archiving" batch job (BATCH-01) effectively, especially for the large `sysfilerefs` and `adrblkfilerefs` collections, to keep the active data size manageable and improve query performance on recent data.

<span class="mark">\<\< End of Document\>\></span>
```