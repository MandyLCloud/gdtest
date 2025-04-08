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

[**2. Critical online transition timing
11**](#critical-online-transition-timing)

[**3. Critical Batch Cycle Timing 12**](#critical-batch-cycle-timing)

[**4. Optimization changes 13**](#optimization-changes)

> [4.1 Optimization Actions 14](#optimization-actions)
>
> [4.1.1 Create stored procedures 14](#create-stored-procedures)
>
> [4.1.2 Create clustered indexes 14](#create-clustered-indexes)

## 1. Introduction

This Performance Optimization Report is prepared for the Combined System Development Services for the Licensing Self-Certification Portal of the Buildings Department. This report outlines the strategies and considerations for optimizing the system's performance to ensure efficiency, responsiveness, and a positive user experience.

The performance optimization of the system is primarily focused on enhancing Online Transaction processing. This report will analyze key areas such as server loading, bandwidth usage, storage allocation, and response times, drawing insights from the database schema analysis to identify potential areas for improvement.

**Database Analysis Summary (from database_schema.md):**

The system database, named `bd`, was last analyzed on 2025/3/4 ??10:10:39. Key statistics include:

- **Database Size:** 88.10 MB
- **Collections:** 12
- **Total Documents:** 1,278,983
- **Total Data Size:** 371.24 MB

The database comprises 12 collections, with `sysfilerefs` and `adrblkfilerefs` being the largest in terms of document count and data size. These collections, along with `bsblocks`, contribute significantly to the overall database size and should be considered for optimization strategies, especially in terms of indexing and query efficiency.

## 1.1 Goal of Performance Optimization

The primary goal of performance optimization is to enhance the system's response time for users. Achieving a better response time involves considering the following critical areas:

### 1.1.1 Server Loading

Server loading is a crucial factor influencing system performance. Increased server load directly impacts response times. Server load is primarily affected by:

1.  **Number of System Users:** A higher number of concurrent users increases server load, potentially slowing down response times for individual users.
2.  **Efficiency of Programming Code:** Inefficient code consumes more server resources, contributing to higher server load and slower response times.

Optimizing programming code to minimize server resource usage is essential for reducing server load, improving response times, and enabling the server to handle more users concurrently.

### 1.1.2 Bandwidth Usage

Bandwidth capacity is another fixed system variable. Increased bandwidth usage can degrade response times. Bandwidth load is affected by:

1.  **Number of System Users:** More concurrent users increase bandwidth usage, potentially limiting bandwidth availability for each user.
2.  **Size of Transmitting Resource:** Larger data transmissions consume more bandwidth, impacting response times, especially under high user loads.

Optimizing the size of transmitted data is crucial for efficient bandwidth utilization. Reducing the size of transmitting resources allows the network to serve more users simultaneously and improves overall response times.

### 1.1.3 Better User Experience

The Licensing Self-Certification Portal is a public-facing application representing the Buildings Department.  System performance directly impacts the department's image and user satisfaction.  Poor performance, such as slow or unresponsive applications, can negatively affect user perception and the department's reputation.  Therefore, performance optimization is vital for ensuring a positive user experience and upholding the department's image.

## 1.2 Performance Optimisation Actions

To enhance system performance, serve more users concurrently, and improve response times, the following general optimization measures should be considered:

-   **Optimize Programming and Query Logic:** Refine code and database queries to minimize server processing and resource consumption.
-   **Optimize Page and Image Sizes:** Reduce the size of web pages and images to decrease bandwidth usage and improve loading times.
-   **Improve Resource Retrieval Speed:** Implement indexing and hashing techniques to expedite data retrieval from the database.
-   **Cache Frequently Used Resources:** Utilize caching mechanisms to store and quickly access frequently accessed data, reducing database load.
-   **Pre-generate Resource-Intensive Content:** Pre-calculate or generate resources that require significant server processing in advance to minimize real-time load.
-   **Reduce Waiting Time for Third-Party Services:** Optimize interactions with external services to minimize delays and improve overall response times.
-   **Archive Expired Records:** Regularly archive or remove outdated data to maintain a minimal active dataset size, improving query performance and reducing storage needs.

## 1.3 Storage Allocation

Database storage for the system will be allocated as follows:

i.  **System data:** Stored in the "Database" server within the Integrated system.
ii. **Textual data:** Stored in the "Database" server within the Integrated system.

All system and textual data will be logically stored within various filegroups of the Microsoft SQL Server database.

| FileGroup | TableName | TableSize |
|-----------|-----------|-----------|
| *To be determined based on SQL Server Filegroup configuration* | *To be determined based on SQL Server Table allocation to Filegroups* | *To be determined based on SQL Server Table sizes* |
|           |           |           |
|           |           |           |
|           |           |           |
|           |           |           |
|           |           |           |

*Note: The table above is a placeholder and needs to be populated with details of FileGroup and Table allocations within the Microsoft SQL Server database, if applicable. The current database analysis is based on a schema that resembles a NoSQL database (like MongoDB), as indicated by collection names and ObjectId types. If the system is indeed using SQL Server, a separate analysis of SQL Server database objects and filegroups will be required to populate this table accurately.*

The filegroup growth size is set to meet the recommendation of being below 256 MB for data files.

## 1.4 Required Response Time

Required response times are categorized into two types: Online Transactions and Online Reports. Programs and reports requiring immediate user interaction and response fall into these categories and should meet defined response time targets. These targets are determined by program complexity.

For operations that cannot be optimized for immediate response, time-consuming parts will be offloaded to batch jobs.

**Target:** 95% of all online functions should meet the committed response time.

Committed response times are influenced by network conditions. The testing environment should adhere to the following network health criteria:

-   **Maximum Concurrent Users:** 100
-   **Minimal Bandwidth:** 2Mb/s per testing machine
-   **Maximum Network Round-Trip Latency (ping) to Integrated System:** 200ms
-   **Remote Testing Site Mark-up:** A 50% mark-up will be applied to the committed response time for remote testing sites.

### 1.4.1 Online Transaction

Programs classified as online transactions include:

-   User Account Program
-   Form and Record Management Program

Online transactions are further classified by complexity:

**\[RY Note: Needs user input/ refer to Load Test data given by user]**

| Transaction Complexity | Number of Concurrent Users |            |          |     |
|---------------------|-----------------|-----------------|-----------------|--|
|                        | 40                         | 80         | 100      |     |
| Simple                 | \< 1 sec                   | \< 2 sec   | \< 3 sec |     |
| Medium                 | \< 2 sec                   | \< 3 sec   | \< 4 sec |     |
| Complex                | \< 2.5 sec                 | \< 3.5 sec | \< 5 sec |     |

Online transactions are also categorized by type:

| Online transactions         | Description                                                                       |
|---------------------------------|---------------------------------------|
| Online Update Transactions  | Used to update records in LSCP, for example, create supervision plan              |
| Online Enquiry Transactions | Used to retrieve records from LSCP, for example, filter site monitoring records   |
| Full-text Search            | Used to search for records with given key words, for example, search assigned TCP |

### 1.4.2 Online Reports

Programs classified as online reports include:

-   XXXXXXXXXXX (*To be defined based on system functionalities*)

For online reports, performance estimation is based on a maximum of 20 concurrent users, as the report system is primarily for internal Buildings Department use.

| On-line Reports | Committed Response Time |
|-----------------|-------------------------|
| *Report Name 1* | *To be defined*         |
| *Report Name 2* | *To be defined*         |
| ...             | ...                     |

# 2. Critical Online Transition Timing

The following table outlines programs with their complexity and transaction types.

*Note: This section requires input to populate the table with specific program details, complexity assessments, and transaction types for the Licensing Self-Certification Portal.*

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
<th>*Module Specific ID*</th>
<th>*Program Name*</th>
<th>*Simple/Medium/Complex*</th>
<th>*Yes/No*</th>
<th>*Yes/No*</th>
<th>*Update/Enquiry/Search*</th>
<th>*Yes/No*</th>
</tr>
<tr class="odd">
<th colspan="6"><strong>FORM AND RECORD MANAGEMENT PROGRAM</strong></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th>*Module Specific ID*</th>
<th>*Program Name*</th>
<th>*Simple/Medium/Complex*</th>
<th>*Yes/No*</th>
<th>*Yes/No*</th>
<th>*Update/Enquiry/Search*</th>
<th>*Yes/No*</th>
</tr>
</tbody>
</table>

# 3. Critical Batch Cycle Timing

The table below lists batch programs and their cycle timings. Optimization is primarily focused on the "generate report" module due to its potential impact on user experience.

*Note: This section requires input to populate the table with specific batch program details, cycle timings, and optimization requirements.*

| **Program ID**    | **Program Name** | **Online Web** | **Mobile** | **Update Batch** | **Require Optimization?** | **Cycle Timing** |
|----------------|----------------|---------|---------|---------|---------|--------|
| **BATCH PROGRAM** |                  |                |            |                  |                           |                  |
| *Batch Program ID* | *Batch Program Name* | *Yes/No*       | *Yes/No*   | *Yes/No*         | *Yes/No*                  | *Timing Details* |
|                   |                  |                |            |                  |                           |                  |
|                   |                  |                |            |                  |                           |                  |

# 4. Optimization changes

Performance optimization efforts will primarily focus on programs and reports to improve response times and efficiency.

## 4.1 Optimization Actions

### 4.1.1 Create stored procedures

All reports are recommended to be implemented using stored procedures. Stored procedures offer performance benefits as they are precompiled and cached, reducing execution time compared to dynamically compiled statements.  Stored procedures are also expected to utilize primary keys for efficient data retrieval.

### 4.1.2 Create clustered indexes

Creating clustered indexes, especially on primary key columns, is a key optimization strategy.  Primary key constraints automatically create clustered indexes (or unique non-clustered if a clustered index already exists).  Choosing appropriate data types for clustering keys, such as BIGINT for primary keys, is crucial for index performance.

*Note: The table below is a placeholder and needs to be populated with specific table and index recommendations based on application usage patterns and query analysis. Based on the database schema analysis, collections with high document counts like `sysfilerefs`, `adrblkfilerefs`, and `bsblocks` should be prioritized for index optimization.*

| **Table ID** | **Table Name** | **LSCP Entity** | **Key Nature** | **Index Field** |
|--------|----------------------|---------------|--------|--------------------|
| *Table/Collection ID* | *Table/Collection Name* | *Entity Description* | *Primary/Foreign Key* | *Field to Index* |
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