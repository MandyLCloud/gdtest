# Handover Plan - DRAFT

## Introduction

This Handover Plan outlines the transfer of the Licensing Self-Certification Portal (LSCP) system from Master Concept (Hong Kong) Limited (MC) to the Buildings Department (BD).  This document serves as a checklist of handover materials and provides essential information for the support and maintenance staff. This is a draft version and requires review and completion before finalization.

<!-- Consider adding a project overview/brief description here -->

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
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>1st draft</td>
<td>All</td>
<td>0.1</td>
<td>16/01/2024</td>
<td></td>
</tr>
</tbody>
</table>

## Table of Contents

- [1. Environment Description](#environment-description)
- [2. Purpose](#purpose)
    - [2.1 Schedule](#schedule)
    - [2.2 Verification](#verification)
- [3. Documentation](#documentation)
- [4. Program Source Code](#program-source-code)
- [5. Administration Accounts Checklist](#administration-accounts-checklist)
- [6. Backup](#backup)
    - [6.1 VM Backup](#vm-backup)
    - [6.2 Database Backup](#database-backup)
- [7. Outstanding Items/Issues](#outstanding-itemsissues)
- [8. Licensed Software](#licensed-software)
- [9. System Summary](#system-summary) <!-- Added from System Manual -->
    - [9.1 Objective](#objective)
    - [9.2 System Architecture](#system-architecture)
    - [9.3 System Functions](#system-functions)
- [10. Equipment Configuration](#equipment-configuration)
- [11. Software Inventories](#software-inventories)
- [12. Security and Backup](#security-and-backup)
- [13. Database Administration](#database-administration)
- [14. Log Management](#log-management)


## 1. Environment Description

<!-- Placeholder images need to be replaced with actual diagrams -->

**Production and UAT environment:**

![Production and UAT Environment Diagram](placeholder_production_uat.png) <!-- Replace placeholder -->

List of machines and virtual machines:

<!-- Complete the table with appropriate data -->
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
<!-- Add rows here -->
</tbody>
</table>

**DR environment:**

![DR Environment Diagram](placeholder_dr.png)  <!-- Replace placeholder -->

List of machines and virtual machines:

<!-- Complete the table with appropriate data -->
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
<!-- Add rows here -->
</tbody>
</table>


## 2. Purpose

This document serves as a checklist of handover materials within the project scope and provides relevant information to the support and maintenance staff.  All deliverables should be received by BD from the LSCP implementation team (MC).

The handover items can be summarized as follows:

1. Documentation
2. Program Source Code (Backend Application, Frontend Web App, Frontend Mobile App)
3. Administration Accounts
4. System Backup
5. Hardware
6. Software Packages and Licenses


## 2.1 Schedule

<!-- Add dates and confirm action parties -->
| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |


## 2.2 Verification

1. **Application URL Verification:** The access link (URL) of each application should be verified.
2. **Login Accounts Verification:** The login accounts for applications and servers should be verified.


## 3. Documentation

<!-- Add file names and versions for each document -->
| Document                             | File Name | Version |
|--------------------------------------|-----------|---------|
| SA&D Report                          | ?         | ?       |
| Project Initiation Document (PID)    |           |         |
| ...                                   | ...       | ...     |
| Project Evaluation Report            |           |         |


## 4. Program Source Code

<!-- Complete table with machine and directory information -->
| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |
| Mobile Application   |         |           | <!-- Added Mobile App -->



## 5. Administration Accounts Checklist

<!-- Complete the table with account details.  **IMPORTANT:**  Consider security implications of including passwords in this document.  Recommend using a separate secure channel for password transfer. -->
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
<!-- Add rows here -->
</tbody>
</table>

**Administration Accounts on LSCP**

<!--  **IMPORTANT:**  Consider security implications of including passwords in this document.  Recommend using a separate secure channel for password transfer. -->
| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |


## 6. Backup

<!-- Review and confirm the following backup information -->

### 6.1 VM Backup

Backup service is carried out by the backup server. Daily VM image backups are performed and stored on the backup servers. A further copy of production VM images is copied to the DR backup server.

### 6.2 Database Backup

Daily full database export backups are performed, including schemas, table structures, packages, stored procedures, and data.


## 7. Outstanding Items/Issues

Nil.  <!-- List any outstanding items or issues here -->


## 8. Licensed Software

<!-- Verify and update the licensed software information. Include license keys if necessary (consider security implications) -->
| Item                                                                              | Amount | Expire At | License Key (Secure Transfer Recommended) |
|------------------------|--------|-----------|-----------------------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |                                         |
| ...                                                                                | ...    | ...       | ...                                     |


## 9. System Summary  <!-- From System Manual -->

### 9.1 Objective

The LSCP aims to provide an electronic platform for site inspection and site monitoring personnel (BD Officers and public users) to provide, manage, and review inspection and monitoring records.

### 9.2 System Architecture

<!-- Include the diagrams and descriptions from the System Manual.  Consider combining or streamlining redundant information. -->
<!--  Diagrams are already embedded in the System Manual content, so no need to add separate image links here. -->
<!-- System Architecture text from System Manual inserted here -->
<!-- ... (Insert content from sm_i1.md, sections 5.2 and 5.3) ... -->


## 10. Equipment Configuration  <!-- From System Manual -->

<!-- ... (Insert content from sm_i1.md, section 6) ... -->

## 11. Software Inventories  <!-- From System Manual -->

<!-- ... (Insert content from sm_i1.md, section 7) ... -->

## 12. Security and Backup  <!-- From System Manual -->

<!-- ... (Insert content from sm_i1.md, section 8) ... -->

## 13. Database Administration  <!-- From System Manual -->

<!-- ... (Insert content from sm_i1.md, section 9) ... -->


## 14. Log Management  <!-- From System Manual -->

<!-- ... (Insert content from sm_i1.md, section 10) ... -->


<!-- End of Document -->
