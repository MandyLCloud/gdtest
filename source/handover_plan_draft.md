# Handover Plan - DRAFT

## Introduction

This Handover Plan outlines the transfer of the Licensing Self-Certification Portal (LSCP) system from Master Concept (Hong Kong) Limited (MC) to the Buildings Department (BD) of the Government of the Hong Kong Special Administrative Region (HKSARG). This document serves as a checklist of handover materials and provides essential information for the support and maintenance staff.  This is a draft version (v0.1) and requires review and completion before finalization.

<!-- Consider adding a more detailed description of the LSCP system and its purpose. -->

<img src="media/image1.jpg" style="width:2.03125in;height:1.52083in" alt="BDlogo" />

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
<th colspan="6"><blockquote>
<p><strong>Amendment History</strong></p>
</blockquote></th>
</tr>
<tr class="odd">
<th>Change Number</th>
<th>Revision Description</th>
<th><p>Pages</p>
<p>Affected</p></th>
<th><p>Revision</p>
<p>Number</p></th>
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

[1. Environment Description](#environment-description)

[2. Purpose](#purpose)

> [2.1 Schedule](#schedule)
>
> [2.2 Verification](#verification)

[3. Documentation](#documentation)

[4. Program Source Code](#program-source-code)

[5. Administration Accounts Checklist](#administration-accounts-checklist)

[6. Backup](#backup)

> [6.1 VM Backup](#vm-backup)
>
> [6.2 Database Backup](#database-backup)

[7. Outstanding Items/Issues](#outstanding-itemsissues)

[8. Licensed Software](#licensed-software)

[9. System Summary](#system-summary)

> [9.1 Objective](#objective)
>
> [9.2 System Architecture](#system-architecture)
>
> [9.3 System Functions](#system-functions)

[10. Equipment Configuration](#equipment-configuration)

> [10.1 Computer Hardware](#computer-hardware)

[11. Software Inventories](#software-inventories)

[12. Security and Backup](#security-and-backup)

[13. Database Administration](#database-administration)

[14. Log Management](#log-management)


## 1. Environment Description

<!-- Complete the tables with the necessary information.  Replace placeholders like "[an image here]" with actual images. -->

**Production and UAT environment:**

![Production and UAT Environment Diagram](media/image2.png) <!-- Assuming image2.png represents the Production and UAT environment -->

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
|  |  |  |  |


**DR environment:**

![DR Environment Diagram](media/image5.png) <!-- Assuming image5.png represents the DR environment -->

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
|  |  |  |  |


## 2. Purpose

This document serves as a checklist of handover materials within the project scope and provides relevant information to the support maintenance staff. All deliverables should be received by BD from MC. The key handover items include:

1. Documentation
2. Program Source Code (Backend Application, Frontend Web App, Frontend Mobile App)
3. Administration Accounts
4. System Backup
5. Hardware
6. Software Packages and Licenses

## 2.1 Schedule

<!-- Add dates and clarify action parties. -->

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |

## 2.2 Verification

1. **Application URL Verification:** The access link (URL) of each application should be verified.
2. **Login Accounts Verification:**  The login accounts for applications and servers should be verified.


## 3. Documentation

<!-- Complete the table with file names and versions. -->

| Document                             | File Name | Version |
|--------------------------------------|-----------|---------|
| SA&D Report                          | ?         | ?       |
| ... | ... | ... |
| Project Evaluation Report            | ?         | ?       |


## 4. Program Source Code

<!-- Complete the table with machine and directory information. -->

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |


## 5. Administration Accounts Checklist

<!-- Complete the tables with user accounts and passwords.  Consider security implications of including passwords directly in the document.  Perhaps use a separate secure document or encrypted method for password transfer. -->

**Server Administration Accounts:**

| User Type | Hostname | Internal IP Address | BD Network IP Address | Access method | User account | Password |
|---|---|---|---|---|---|---|
| Blade Servers |  |  |  |  |  |  |
| ... | ... | ... | ... | ... | ... | ... |
| Syslog |  |  |  |  |  |  |


**LSCP Administration Accounts:**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |


## 6. Backup

<!-- Review and update the following content as needed. -->

### 6.1 VM Backup

Backup service is carried out by the backup server. Daily VM image backups are stored on the backup servers. A further copy of production VM images is copied to the DR backup server.

### 6.2 Database Backup

Daily full export backups of the database are performed, including schemas, table structures, packages, stored procedures, and data.


## 7. Outstanding Items/Issues

Nil.  <!-- Update if any outstanding items/issues exist. -->


## 8. Licensed Software

<!-- Review and update the following items and amounts. -->

| Item                                                                              | Amount | Expire At |
|------------------------|------------------------|------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| ... | ... | ... |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |


## 9. System Summary

### 9.1 Objective

The LSCP aims to provide an electronic platform for site inspection and site monitoring personnel (BD Officers and public users) to provide, manage, and review inspection and monitoring records.

### 9.2 System Architecture

<!-- Include the system architecture diagrams and descriptions from sm_i1.md.  Ensure image paths are correct. -->

![System Architecture Overview](media/image2.png)

![LSCP Architecture for Production and UAT](media/image3.png)

<!-- Include the detailed descriptions of each system component (External Application Server, External Web Server, etc.) from sm_i1.md. -->

### 9.3 System Functions

<!-- Include the system functions table from sm_i1.md. -->

| Function ID | Function Name |
|---|---|
| UF-WEB-001-1 | Public User Authentication with Password |
| ... | ... |
| UF-WEB-004-9 | Import SMIS Excel into CDPSS |


## 10. Equipment Configuration

### 10.1 Computer Hardware

<!-- Include the hardware configuration tables and details from sm_i1.md.  Ensure consistency and accuracy of information. -->

<!-- ... (Hardware details from sm_i1.md) ... -->

## 11. Software Inventories

<!-- Include the software inventory tables from sm_i1.md. -->

<!-- ... (Software inventory details from sm_i1.md) ... -->


## 12. Security and Backup

<!-- Include the security and backup information from sm_i1.md, consolidating with existing information from hp_i1.md.  Pay attention to potential conflicts or inconsistencies and resolve them. -->

<!-- ... (Security and Backup details from sm_i1.md) ... -->


## 13. Database Administration

<!-- Include the database administration information from sm_i1.md. -->

<!-- ... (Database Administration details from sm_i1.md) ... -->


## 14. Log Management

<!-- Include the log management information from sm_i1.md. -->

<!-- ... (Log Management details from sm_i1.md) ... -->


<!-- End of document -->
