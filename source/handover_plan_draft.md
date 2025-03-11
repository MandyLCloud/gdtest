# Handover Plan - DRAFT

## Introduction

This Handover Plan outlines the transfer of the Licensing Self-Certification Portal (LSCP) system from Master Concept (Hong Kong) Limited (MC) to the Buildings Department (BD). This document serves as a checklist of handover materials and provides essential information for the support and maintenance staff.  This draft version consolidates information from various sources and requires review and refinement before finalization.

<!-- Consider adding a project overview/background section here -->

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

[1. Environment Description](#environment-description)

[2. Purpose](#purpose)

[3. Schedule](#schedule)

[4. Verification](#verification)

[5. Documentation](#documentation)

[6. Program Source Code](#program-source-code)

[7. Administration Accounts Checklist](#administration-accounts-checklist)

[8. Backup](#backup)

[9. Outstanding Items/Issues](#outstanding-itemsissues)

[10. Licensed Software](#licensed-software)

[11. System Summary](#system-summary)

[12. System Architecture](#system-architecture)

[13. System Functions](#system-functions)

[14. Equipment Configuration](#equipment-configuration)

[15. Software Inventories](#software-inventories)

[16. Security and Backup](#security-and-backup-1)

[17. Database Administration](#database-administration-1)

[18. Log Management](#log-management)


## 1. Environment Description

<!-- Placeholder for environment diagrams. Replace the bracketed placeholders with actual diagrams -->

**Production and UAT Environment:**

![Production and UAT Environment Diagram](media/image2.png) <!-- Add image for Production and UAT -->

**List of Machines and Virtual Machines (Production and UAT):**

<!-- Populate the table below with accurate information -->
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

**DR Environment:**

![DR Environment Diagram](media/image5.png) <!-- Add image for DR -->

**List of Machines and Virtual Machines (DR):**

<!-- Populate the table below with accurate information -->
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

This document serves as a checklist for the handover of the Licensing Self-Certification Portal (LSCP) from the system implementation team to the Buildings Department (BD). It provides crucial information for the support and maintenance staff who will manage the system.  The handover encompasses documentation, program source code (backend, frontend web app, frontend mobile app), administration accounts, system backups, hardware, and software packages with licenses.


## 3. Schedule

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |  <!-- Add Date -->    | MC/BD          |
| Verification |  <!-- Add Date -->    | BD             |


## 4. Verification

1. **Application URL Verification:** Access links (URLs) for each application will be verified through access checks.
2. **Login Accounts Verification:** Login accounts for applications and servers will be verified by attempting logins.


## 5. Documentation

<!-- Add filenames and versions for each document -->

| Document                             | File Name | Version |
|--------------------------------------|-----------|---------|
| SA&D Report                          | ?         | ?       |
| Project Initiation Document (PID)    |           |         |
| Physical Data Design                 |           |         |
| ...                                  |           |         |
| Project Evaluation Report            |           |         |


## 6. Program Source Code

<!-- Add machine and directory information -->

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |


## 7. Administration Accounts Checklist

<!-- Populate the tables below with account details.  **IMPORTANT:** Consider security implications of including passwords in this document. Explore alternatives like secure password vaults. -->

**Server Accounts:**

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

**LSCP Application Accounts:**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |


## 8. Backup

<!-- Review and update the backup information based on sm_i1.md -->

### VM Backup

Daily VM image backups are performed by the backup server and stored on the backup servers. Production VM images are also copied to the DR backup server.  See section 16 for more details.

### Database Backup

Daily full database backups are performed on the DB servers. Data is stored on the DB servers and further backed up via VM backups. See section 16 for more details.


## 9. Outstanding Items/Issues

Nil.  <!-- Update if needed -->


## 10. Licensed Software

<!-- Verify and update the license information -->

| Item                                                                              | Amount | Expire At |
|------------------------|------------------------|------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| ...                                                                                |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |


## 11. System Summary

The LSCP caters to BD Officers and public users involved in site inspection and monitoring. It aims to provide an electronic platform for managing and reviewing inspection and monitoring records.


## 12. System Architecture

<!-- Include the system architecture diagrams and descriptions from sm_i1.md -->

![System Architecture Diagram](media/image2.png)
![System Architecture Diagram 2](media/image3.png)

<!-- Add the detailed descriptions of the system components and integrations from sm_i1.md -->


## 13. System Functions

<!-- Include the table of system functions from sm_i1.md -->

|               |                                                         |
|---------------|---------------------------------------------------------|
| Function ID   | Function Name                                           |
| ...           | ...                                                     |
| UF-WEB-004-9  | Import SMIS Excel into CDPSS                            |



## 14. Equipment Configuration

<!-- Include the hardware and software configuration details from sm_i1.md -->

<!-- ... (Hardware Components, Guest Servers Components, Gateway and SMTPX Configuration, Database Configuration, Detailed Server and Network Configurations) ... -->


## 15. Software Inventories

<!-- Include the software inventory details from sm_i1.md -->

<!-- ... (Inventory of Application Programs, Inventory of System Software and Software Package) ... -->



## 16. Security and Backup (Detailed)


<!-- Consolidate and expand the security and backup information from both documents -->

<!-- Include details on System Control, Backup, Security (Data Transmission, Data Storage, System, Physical, Password, Account Control), Change Control, Disaster Recovery, and Database Backup Strategy from sm_i1.md -->


## 17. Database Administration

<!-- Include the database administration details from sm_i1.md -->

<!-- ... (Clean Database Transaction Logs, Database Backup, System Constraints and Limitations) ... -->


## 18. Log Management

<!-- Include the log management details from sm_i1.md -->


<!--  End of document -->
