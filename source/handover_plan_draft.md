# Handover Plan - DRAFT

## Introduction

This Handover Plan outlines the transfer of the Licensing Self-Certification Portal (LSCP) system from Master Concept (Hong Kong) Limited (MC) to the Buildings Department (BD). This document serves as a checklist of handover materials and provides essential information for the support and maintenance staff.  This draft version consolidates information from various sources and requires further review and refinement before finalization.

<!-- Note: The introduction might need to be expanded to include a brief overview of the project and its objectives. -->

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
</table>


## Table of Contents

1. [Environment Description](#environment-description)
2. [Purpose](#purpose)
    * [Schedule](#schedule)
    * [Verification](#verification)
3. [Documentation](#documentation)
4. [Program Source Code](#program-source-code)
5. [Administration Accounts Checklist](#administration-accounts-checklist)
6. [Backup](#backup)
    * [VM Backup](#vm-backup)
    * [Database Backup](#database-backup)
7. [Outstanding Items/Issues](#outstanding-itemsissues)
8. [Licensed Software](#licensed-software)
9. [System Summary](#system-summary) <!-- Added from sm_i1.md -->
    * [Objective](#objective)
    * [System Architecture](#system-architecture)
    * [System Functions](#system-functions)
10. [Equipment Configuration](#equipment-configuration) <!-- Added from sm_i1.md -->
    * [Computer Hardware](#computer-hardware)
11. [Software Inventories](#software-inventories)  <!-- Added from sm_i1.md -->
12. [Security and Backup (Detailed)](#security-and-backup-detailed) <!-- Expanded from original and sm_i1.md -->
13. [Database Administration](#database-administration)  <!-- Added from sm_i1.md -->
14. [Log Management](#log-management) <!-- Added from sm_i1.md -->


## 1. Environment Description

<!-- Note: Placeholder images need to be replaced with actual diagrams.  Table needs to be populated with data. -->

**Production and UAT environment:**

\[an image here - Replace with actual diagram]

**List of machines and virtual machines:**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
|  |  |  |  |


**DR environment:**

\[image here - Replace with actual diagram]

**List of machines and virtual machines:**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
|  |  |  |  |



## 2. Purpose

This document serves as a checklist of handover materials within the project scope and provides relevant information to the support maintenance staff. All deliverables should be received by BD from the LSCP system implementation team (MC).  The key handover items include Documentation, Program Source Code, Administration Accounts, System Backup, Hardware, and Software Packages and Licenses.


## 2.1 Schedule

<!-- Note: Dates need to be filled in. -->

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |


## 2.2 Verification

1. **Application URL verification:** The access link (URL) of each application should be verified.
2. **Login accounts verification:** The login accounts for applications and servers should be verified.



## 3. Documentation

<!-- Note: File names and versions need to be completed. -->

| Document                             | File Name | Version |
|--------------------------------------|-----------|---------|
| SA&D Report                          | ?         | ?       |
| Project Initiation Document (PID)    |           |         |
| ... | ... | ... |
| Project Evaluation Report            | ?         | ?       |



## 4. Program Source Code

<!-- Note: Machine and directory information needs to be completed. -->

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |
|                      |         |           |



## 5. Administration Accounts Checklist

<!-- Note: Tables need to be populated with account details.  Consider security implications of including passwords in this document.  Perhaps a separate secure handover process for credentials is necessary. -->

**Server Administration Accounts:**

| User Type | Hostname | Internal IP Address | BD Network IP Address | Access method | User account | Password |
|---|---|---|---|---|---|---|
| ... | ... | ... | ... | ... | ... | ... |


**LSCP Administration Accounts:**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |
|             |           |              |          |



## 6. Backup

<!-- Note: Content needs to be verified and potentially expanded. -->

### 6.1 VM Backup

Backup service is carried out by the backup server. Daily VM image backups are stored on the backup servers. A further copy of production VM images is copied to the DR backup server.


### 6.2 Database Backup

Daily full export backups are performed on DB servers. Data is stored on the DB servers and further backed up by VM Backup.



## 7. Outstanding Items/Issues

Nil.


## 8. Licensed Software

<!-- Note: Items and details need to be verified and corrected. -->

| Item                                                                              | Amount | Expire At |
|------------------------|------------------------|------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| ... | ... | ... |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |



## 9. System Summary

<!-- Content from sm_i1.md -->

### 9.1 Objective

The LSCP serves BD Officers and public users involved in site inspection and monitoring.  Its primary objective is to provide an electronic platform for providing, managing, and reviewing inspection and monitoring records.

### 9.2 System Architecture

<!-- Include diagrams and descriptions from sm_i1.md -->
<!-- Note:  Consider consolidating the architecture descriptions from hp_i1.md and sm_i1.md to avoid redundancy. -->
[Insert System Architecture diagrams and descriptions from sm_i1.md]

### 9.3 System Functions

<!-- Include the table of system functions from sm_i1.md -->
[Insert System Functions table from sm_i1.md]



## 10. Equipment Configuration

<!-- Content from sm_i1.md -->

### 10.1 Computer Hardware

<!-- Include all hardware details from sm_i1.md -->
[Insert Hardware details from sm_i1.md]



## 11. Software Inventories

<!-- Content from sm_i1.md -->

<!-- Include all software inventory details from sm_i1.md -->
[Insert Software Inventories from sm_i1.md]



## 12. Security and Backup (Detailed)

<!-- Combine and expand security and backup information from hp_i1.md and sm_i1.md -->

<!-- Include details on System Control, Backup, Security (Data Transmission, Data Storage, System, Physical, Password, Account Control), Change Control, and Disaster Recovery from both documents. -->
[Insert and consolidate Security and Backup details from hp_i1.md and sm_i1.md]


## 13. Database Administration

<!-- Content from sm_i1.md -->

<!-- Include details on cleaning transaction logs and database backup procedures. -->
[Insert Database Administration details from sm_i1.md]



## 14. Log Management

<!-- Content from sm_i1.md -->

<!-- Include details on log management procedures. -->
[Insert Log Management details from sm_i1.md]



<!-- End of document -->
