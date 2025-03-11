# Handover Plan - DRAFT

## Introduction

This Handover Plan outlines the transfer of the Licensing Self-Certification Portal (LSCP) system from Master Concept (Hong Kong) Limited (MC) to the Buildings Department (BD). This document serves as a checklist of handover materials and provides essential information for the support and maintenance staff.  This draft version consolidates information from various sources and requires review and refinement before finalization.

<!-- Note: The introduction might need to be expanded with more context about the project. -->

<img src="media/image1.jpg" alt="BDlogo" style="width:2.03125in;height:1.52083in" />

**HANDOVER PLAN**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**

**LICENSING SELF-CERTIFICATION PORTAL**

**FOR**

**BUILDINGS DEPARTMENT**

**Version: 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of, and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

| **Distribution** |                                         |
|------------------|-----------------------------------------|
| Copy No.         | Holder                                  |
| 1                | Buildings Department (BD)               |
| 2                | Master Concept (Hong Kong) Limited (MC) |

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 22%" />
<col style="width: 22%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 15%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="6"><strong>Amendment History</strong></th>
</tr>
<tr class="odd">
<th>Change Number</th>
<th>Revision Description</th>
<th>Pages Affected</th>
<th>Revision Number</th>
<th>Date</th>
<th>Approved Reference</th>
</tr>
<tr class="header">
<th>1</th>
<th>1st draft</th>
<th>All</th>
<th>0.1</th>
<th>16/01/2024</th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## Table of Contents

* [1. Environment Description](#environment-description)
* [2. Purpose](#purpose)
    * [2.1 Schedule](#schedule)
    * [2.2 Verification](#verification)
* [3. Documentation](#documentation)
* [4. Program Source Code](#program-source-code)
* [5. Administration Accounts Checklist](#administration-accounts-checklist)
* [6. Backup](#backup)
    * [6.1 VM Backup](#vm-backup)
    * [6.2 Database Backup](#database-backup)
* [7. Outstanding Items/Issues](#outstanding-itemsissues)
* [8. Licensed Software](#licensed-software)
* [9. System Summary](#system-summary) <!-- Added from sm_i1.md -->
    * [9.1 Objective](#objective)
    * [9.2 System Architecture](#system-architecture)
    * [9.3 System Functions](#system-functions)
* [10. Equipment Configuration](#equipment-configuration)
* [11. Software Inventories](#software-inventories)
* [12. Security and Backup](#security-and-backup)
* [13. Database Administration](#database-administration)
* [14. Log Management](#log-management)


## 1. Environment Description

<!-- Note: Placeholder images need to be replaced with actual diagrams.  Table data needs to be populated. -->

**Production and UAT environment:**

\[an image here - Replace with actual diagram]

**List of machines and virtual machines:**

<!-- The following table needs to be populated with the correct data from both hp_i1.md and sm_i1.md -->
<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 20%" />
<col style="width: 35%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Hostname (Physical Machine)</th>
<th>Hostname (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
</tbody>
</table>


**DR environment:**

\[image here - Replace with actual diagram]

**List of machines and virtual machines:**

<!-- The following table needs to be populated with the correct data from both hp_i1.md and sm_i1.md -->
<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 20%" />
<col style="width: 35%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Hostname (Physical Machine)</th>
<th>Hostname (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
</tbody>
</table>



## 2. Purpose

This document is a checklist of handover materials within project scope and provides relevant information to the support maintenance staff. All deliverables should be received by BD from the LSCP implementation team.  The handover encompasses documentation, program source code (backend application, frontend web app, frontend mobile app), administration accounts, system backups, hardware, and software packages with licenses.


## 2.1 Schedule

<!-- Note: Dates need to be filled in. -->

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |


## 2.2 Verification

1. **Application URL verification:** Access links (URLs) will be verified.
2. **Login accounts verification:** Login accounts for applications and servers will be verified.


## 3. Documentation

<!-- Note: File names and versions need to be completed. Consider adding locations where these documents can be found. -->

| Document                             | File Name | Version |
|--------------------------------------|-----------|---------|
| SA&D Report                          | ?         | ?       |
| Project Initiation Document (PID)    |           |         |
| Physical Data Design                 |           |         |
| Process Data Interface               |           |         |
| Data Catalogue                       |           |         |
| Program Specifications               |           |         |
| Performance Optimization Report      |           |         |
| System Test Plan, Spec and Results   |           |         |
| Unit Test Cases and Results          |           |         |
| Load Test Plan and Result            |           |         |
| Training Plan                        |           |         |
| User Manual                          |           |         |
| System Installation Plan Report      |           |         |
| DR Plan                              |           |         |
| DR Drill Test result Report          |           |         |
| WCAG                                 |           |         |
| UAT Plan and Results                 |           |         |
| Application Operation manual         |           |         |
| Computer Operation Procedures Manual | ?         | ?       |
| Data Manual                          | ?         | ?       |
| System Maintenance Plan              | ?         | ?       |
| User Procedures Manual               | ?         | ?       |
| Security Incident Handling Procedure | ?         | ?       |
| Handover Plan                        | ?         | ?       |
| System Manual                        | ?         | ?       |
| Program Manual                       | ?         | ?       |
| Project Evaluation Report            | ?         | ?       |



## 4. Program Source Code

<!-- Note: Machine, directory information needs to be completed.  Consider specifying the version control system used (e.g., Git) and repository location. -->

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |


## 5. Administration Accounts Checklist

<!-- Note: Table needs to be populated with account details.  Consider security implications of including passwords in this document.  Best practice is to handle passwords separately and securely. -->

**Administration Accounts on different areas:**

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 18%" />
<col style="width: 13%" />
<col style="width: 13%" />
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
</colgroup>
<thead>
<tr class="header">
<th>User Type</th>
<th>Hostname</th>
<th>Internal IP Address</th>
<th>BD Network IP Address</th>
<th>Access method</th>
<th>User account</th>
<th>Password</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

**Administration Accounts on LSCP:**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |


## 6. Backup


## 6.1 VM Backup

Backup service is carried out by backup server. Daily VM image backup is carried out and stored in the backup servers. A further copy of production VM images is copied to DR?s backup server.


## 6.2 Database Backup

Daily full export backup is done on DB servers. Data is stored on the DB servers and further backed up by VM Backup.


## 7. Outstanding Items/Issues

Nil.


## 8. Licensed Software

<!-- Note:  Information needs to be verified and completed. -->

| Item                                                                              | Amount | Expire At |
|------------------------|------------------------|------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual                                            |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |


## 9. System Summary  <!-- From sm_i1.md -->

### 9.1 Objective

The LSCP aims to provide an electronic platform for site inspection and site monitoring personnel (BD Officers and public users) to provide, manage, and review inspection and monitoring records.

### 9.2 System Architecture

<!-- Note: All image placeholders from sm_i1.md need to be replaced with the actual images/diagrams.  Descriptions should be reviewed for clarity and consistency. -->

[Include System Architecture diagrams and descriptions from sm_i1.md here]


### 9.3 System Functions

[Include System Functions table from sm_i1.md here]


## 10. Equipment Configuration

[Include Equipment Configuration details from sm_i1.md here]


## 11. Software Inventories

[Include Software Inventories details from sm_i1.md here]


## 12. Security and Backup

[Include Security and Backup details from sm_i1.md here]


## 13. Database Administration

[Include Database Administration details from sm_i1.md here]


## 14. Log Management

[Include Log Management details from sm_i1.md here]


<!-- End of Document Marker -->
<<< End of document >>> 
