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

[**2. Database Analysis and Optimization Opportunities 11**](#database-analysis-and-optimization-opportunities)

> [2.1 Database Statistics 11](#database-statistics)
>
> [2.2 Collection Overview and Analysis 12](#collection-overview-and-analysis)
>
> [2.3 Field Analysis and Potential Issues 13](#field-analysis-and-potential-issues)

[**3. Critical Online Transition Timing
14**](#critical-online-transition-timing)

[**4. Critical Batch Cycle Timing 15**](#critical-batch-cycle-timing)

[**5. Optimization changes 16**](#optimization-changes)

> [5.1 Optimization Actions 17](#optimization-actions)
>
> [5.1.1 Create stored procedures 17](#create-stored-procedures)
>
> [5.1.2 Create clustered indexes 17](#create-clustered-indexes)
>
> [5.2 Specific Optimization Recommendations 18](#specific-optimization-recommendations)

##

## 1. Introduction

The performance optimization of the system could be classified into
optimization of Online Transaction. This report outlines the analysis of the current database schema and proposes optimization strategies to enhance system performance for the Licensing Self-Certification Portal (LSCP).

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
    > burden.
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
|           | tasks          | 0.99 MB   |
|           | eminutes       | 0.03 MB   |
|           | submissions    | 0.00 MB   |
|           | applications   | 0.36 MB   |
|           | notifications  | 0.24 MB   |
|           | bsblocks       | 6.40 MB   |
|           | cases          | 1.17 MB   |
|           | oauthtokens    | 2.29 MB   |
|           | sysfilerefs    | 204.70 MB |
|           | attachments    | 0.13 MB   |
|           | users          | 0.04 MB   |
|           | adrblkfilerefs | 154.89 MB |

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
    > is 200ms.
-   Remote testing site will have **50% mark-up** time to the committed
    > response time.

### 1.4.1 Online Transaction

The programs in the following category are classified as online
transaction:

-   User Account Program
-   Form and Record Management Program

Online transactions can be classified into the following groups:

<span class="mark">\[RY Note: Needs user input/ refer to Load Test data
given by user]</span>

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

###

### 1.4.2 Online Reports

The programs in the following category are classified as online reports:

-   XXXXXXXXXXX

As the report is a standalone internal system for BD, the measurement
would only estimate when the concurrent users are not more than 20.

| On-line Reports | Committed Response Time |
|-----------------|-------------------------|
|                 |                         |
|                 |                         |

#

# 2. Database Analysis and Optimization Opportunities

This section provides an analysis of the database schema and identifies potential areas for performance optimization based on the provided database statistics and collection details.

## 2.1 Database Statistics

The following are the key statistics of the `bd` database as of 2025/3/4 ??10:10:39:

- **Database Size:** 88.10 MB
- **Collections:** 12
- **Total Documents:** 1,278,983
- **Total Data Size:** 371.24 MB

The database size and total data size indicate the storage footprint of the application. The number of collections and documents provides an overview of the data organization.

## 2.2 Collection Overview and Analysis

The database consists of 12 collections. The following table summarizes the document count and size of each collection:

| Collection Name   | Document Count | Size      | Average Document Size |
|-------------------|----------------|-----------|-----------------------|
| tasks             | 5,523          | 0.99 MB   | 0.18 KB               |
| eminutes          | 133            | 0.03 MB   | 0.24 KB               |
| submissions       | 0              | 0.00 MB   | 0.00 KB               |
| applications      | 381            | 0.36 MB   | 0.96 KB               |
| notifications     | 1,837          | 0.24 MB   | 0.13 KB               |
| bsblocks          | 98,397         | 6.40 MB   | 0.07 KB               |
| cases             | 451            | 1.17 MB   | 2.65 KB               |
| oauthtokens       | 3,019          | 2.29 MB   | 0.78 KB               |
| sysfilerefs       | 601,808        | 204.70 MB | 0.35 KB               |
| attachments       | 370            | 0.13 MB   | 0.37 KB               |
| users             | 116            | 0.04 MB   | 0.39 KB               |
| adrblkfilerefs    | 566,948        | 154.89 MB | 0.28 KB               |

**Analysis:**

- **Large Collections:** `sysfilerefs` and `adrblkfilerefs` are significantly larger in both document count and size compared to other collections. These collections should be prioritized for performance optimization, especially in terms of indexing and query optimization.
- **`bsblocks` Collection:** While smaller than `sysfilerefs` and `adrblkfilerefs`, `bsblocks` still holds a substantial number of documents and size, warranting attention for optimization.
- **`submissions` Collection:**  This collection has zero documents. It's important to verify if this is expected or if there's an issue preventing data from being stored in this collection. If submissions are expected, investigate potential data flow problems. If not, consider removing the collection to simplify the database.
- **`cases` Collection:**  Has a relatively high average document size (2.65 KB), suggesting potentially complex documents. Analyzing the structure and query patterns of this collection could reveal optimization opportunities.

## 2.3 Field Analysis and Potential Issues

The field analysis for each collection provides insights into data types and occurrences. Reviewing this detailed information can reveal potential areas for schema optimization and indexing strategies.

**Potential Issues Identified from Field Analysis:**

- **Mixed Data Types:**  Several fields exhibit mixed data types (e.g., `tasks.user`, `eminutes.from`, `eminutes.to`). While MongoDB is schema-less, inconsistent data types within a field can complicate querying and indexing.  It's recommended to standardize data types for fields used in queries and consider schema enforcement where beneficial.
- **High Cardinality String Fields:**  Many string fields are present across collections. For collections with a large number of documents like `sysfilerefs` and `adrblkfilerefs`, ensure that frequently queried string fields are appropriately indexed to improve search performance.
- **Date Fields:** Date fields like `createdAt`, `updatedAt`, `createdDt`, `lastModifiedDt` are common. Indexing these fields can be beneficial for time-based queries and data archival strategies.
- **Object and Array Types in `applications`:** The `applications` collection contains fields with `object` and `array` types (e.g., `APP13`, `RelatedPremises`, `address`).  Queries involving these complex types might require careful optimization and potentially indexing within embedded documents or arrays if frequently queried.

#

# 3. Critical Online Transition Timing

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
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</tbody>
</table>

#

#

# 4. Critical Batch Cycle Timing

The below are the list of batch programs. The cycle timing of the batch
is identified in the tables below.
They are different from modules in the last section whereas they will
run a thousand times everyday but the modules in this section probably
run once or twice daily. Moreover, most of the modules described in this
section are scheduled jobs running in backend, normally, the fluctuation
of performance in these items would not affect the end user. Except, the
generate report module, has a higher impact, thus it is the only item
required to optimize.

| **Program ID**    | **Program Name** | **Online Web** | **Mobile** | **Update Batch** | **Require Optimization?** | **Cycle Timing** |
|----------------|----------------|---------|---------|---------|---------|--------|
| **BATCH PROGRAM** |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |

# 5. Optimization changes

The optimization will **<u>only</u>** focus the performance on programs
and reports.

## 5.1 Optimization Actions

### 5.1.1 Create stored procedures

All reports are created by stored procedures. Stored procedures are
precompiled as opposed to the dynamic prepared statements that are
compiled whenever your application code invokes a call. Once you execute
a stored procedure, it remains in the cache, saving the execution time.
In addition, the stored procedures are mostly using primary key for
searching.  *(Note: This section seems to be based on SQL Server concepts. In MongoDB context, this would relate to optimized aggregation pipelines and efficient query design.)*

### 5.1.2 Create clustered indexes

When creating a primary key constraint, a unique clustered index on the
column or columns is automatically created if a clustered index on the
table does not already exist and you do not specify a unique
non-clustered index. The primary key column cannot allow NULL values. In
addition, when creating a unique constraint, a unique non-clustered
index is created to enforce a unique constraint by default. When
designing a clustered index, we have considered that the data types to
be used as clustering keys. For instance, the primary keys are BIGINT
data type which is the best choices as clustered index key. *(Note: This section is also based on SQL Server terminology. In MongoDB, we use indexes. Clustered indexes are not directly applicable, but the concept of indexing for efficient data retrieval is relevant.)*

## 5.2 Specific Optimization Recommendations

Based on the database analysis, the following specific optimization recommendations are proposed:

| **Table Name**   | **LSCP Entity** | **Key Nature** | **Index Field**      | **Recommendation**                                                                                                                               |
|----------------|-----------------|----------------|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| sysfilerefs    | File Reference  | High Cardinality | sysFileRefId         | **Index `sysFileRefId`**: Ensure an index exists on `sysFileRefId` as it seems to be a primary identifier and likely used in queries.          |
| sysfilerefs    | Date Range      | Time-based       | createdDt, lastModifiedDt | **Index `createdDt` and `lastModifiedDt`**: Create compound indexes on date fields if time-based queries are frequent (e.g., filtering by date ranges). |
| adrblkfilerefs | ADR Block File Ref | High Cardinality | adrBlkFileRefId      | **Index `adrBlkFileRefId`**:  Ensure an index exists on `adrBlkFileRefId` for efficient lookups.                                         |
| adrblkfilerefs | ADR Block ID    | High Cardinality | adrBlkId           | **Index `adrBlkId`**: If `adrBlkId` is frequently used in queries, create an index.                                                              |
| bsblocks       | Block ID        | High Cardinality | blockId            | **Index `blockId`**: Index `blockId` for faster lookups in `bsblocks` collection.                                                                 |
| tasks          | Application     | Foreign Key    | application        | **Index `application`**: Index `application` field for efficient retrieval of tasks related to specific applications.                               |
| tasks          | Submission Case | Foreign Key    | submissionCase     | **Index `submissionCase`**: Index `submissionCase` for efficient retrieval of tasks related to specific submission cases.                           |
| applications   | Application No  | High Cardinality | ApplicationNo      | **Index `ApplicationNo`**: Index `ApplicationNo` for faster searching and retrieval of applications by application number.                        |
| users          | User Login      | Unique         | osdpLoginId         | **Index `osdpLoginId` (Unique)**: Ensure a unique index on `osdpLoginId` for efficient user authentication and lookup.                             |
| eminutes       | Submission Case | Foreign Key    | submissionCase     | **Index `submissionCase`**: Index `submissionCase` for efficient retrieval of eminutes related to specific submission cases.                        |

<span class="mark">\<\< End of Document\>\></span>
```