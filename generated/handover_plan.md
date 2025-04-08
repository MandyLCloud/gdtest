```markdown
<img src="media/image1.jpg" style="width:2.03125in;height:1.52083in"
alt="BDlogo" />

**HANDOVER PLAN**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">COMBINED SYSTEM DEVELOPMENT SERVICES</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">BUILDINGS DEPARTMENT</span>**

**Version: 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of, and may not be
reproduced in whole

or in part without the express permission of the Government of the
HKSAR.

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

**TABLE OF CONTENTS**

[1. Environment Description](#environment-description)
[2. Purpose](#purpose)
    [2.1 Schedule](#schedule)
    [2.2 Verification](#verification)
[3. Documentation](#documentation)
[4. Program Source Code](#program-source-code)
[5. Administration Accounts Checklist](#administration-accounts-checklist)
[6. Backup](#backup)
    [6.1 VM Backup](#vm-backup)
    [6.2 Database Backup](#database-backup)
[7. Outstanding Items/Issues](#outstanding-itemsissues)
[8. Licensed Software](#licensed-software)

# 1. Environment Description

Production and UAT environment:

\[Production and UAT Environment Diagram - To be inserted here. Refer to System Manual for details. e.g., media/image2.png, media/image3.png]

List of machines and virtual machines:

**WKGO - Production Environment**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                     | IP                 |
|-----------------------------|----------------------------|-----------------------------|--------------------|
| Dell PowerEdge R750 Server  | prd-scs-vcenter-01         | vCenter                     | 192.168.10.24 / 10.5.161.210 |
|                               | prd-scs-backup-01          | Veeam Backup Server         | 192.168.10.25 / 10.5.161.211 |
|                               | prd-scs-log-01             | Kiwi Log Server             | 192.168.10.11 / 10.5.161.223 |
|                               | prd-scs-esetnod32          | NOD32 Anti-Virus Server     | 192.168.10.34 / 10.5.161.215 |
|                               | prd-scs-admin-api-01       | API Server                  | 192.168.12.11        |
|                               | prd-scs-admin-frontend-01  | Frontend Server             | 192.168.12.12        |
|                               | prd-scs-admin-backend-01   | Backend Server              | 192.168.12.13        |
|                               | prd-scs-db-01              | Database Server             | 192.168.12.14        |
|                               | prd-scs-filer              | File Server                 | 192.168.12.20        |
|                               | prd-scs-proxy              | Reverse Proxy Server        | 192.168.12.15 / 10.5.161.226 |
| Dell PowerEdge R750 Server  | prd-scs-admin-api-02       | API Server                  | 192.168.12.16        |
|                               | prd-scs-admin-frontend-02  | Frontend Server             | 192.168.12.17        |
|                               | prd-scs-admin-backend-02   | Backend Server              | 192.168.12.18        |
|                               | prd-scs-db-02              | Database Server             | 192.168.12.19        |
|                               | -                          | -                           | -                    |
|                               | -                          | -                           | -                    |

**GCIS P1 - Production Environment**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                     | IP                  |
|-----------------------------|----------------------------|-----------------------------|---------------------|
| GCIS Infrastructure         | scspwi                     | Reverse Proxy Server (iDMZ) | 192.168.0.6 / 45.119.92.84  |
|                               | scspwg                     | Reverse Proxy Server (gDMZ) | 192.168.4.6 / 10.160.11.211 |
|                               | scspad                     | Apps Server (Trust Zone)    | 192.168.8.6         |
|                               | scspdb                     | Database Server (Trust Zone)| 192.168.8.7         |
|                               | scspbk2                    | Veeam Backup Server         | 192.168.8.9         |
|                               | scsplog                    | Kiwi Log Server             | 192.168.8.10        |
|                               | -                          | -                           | -                     |
|                               | -                          | -                           | -                     |

**WKGO - UAT Environment**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                     | IP                 |
|-----------------------------|----------------------------|-----------------------------|--------------------|
| Dell PowerEdge R750 Server  | uat-scs-admin-api-01       | API Server                  | 192.168.13.10        |
|                               | uat-scs-admin-frontend-01  | Frontend Server             | 192.168.13.11        |
|                               | uat-scs-admin-backend-01   | Backend Server              | 192.168.13.12        |
|                               | uat-scs-db-01              | Database Server             | 192.168.13.13        |
|                               | uat-scs-filer              | File Server                 | 192.168.13.15        |
|                               | uat-scs-proxy              | Reverse Proxy Server        | 192.168.13.14 / 10.5.161.224 |
|                               | -                          | -                           | -                    |
|                               | -                          | -                           | -                    |

**GCIS T1 - UAT Environment**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                     | IP                  |
|-----------------------------|----------------------------|-----------------------------|---------------------|
| GCIS Infrastructure         | scsuwi                     | Reverse Proxy Server (iDMZ) | 192.168.0.7 / 45.119.94.99  |
|                               | scsuwg                     | Reverse Proxy Server (gDMZ) | 192.168.4.7 / 10.148.11.220 |
|                               | scsuad                     | Apps Server (Trust Zone)    | 192.168.8.9         |
|                               | scsudb                     | Database Server (Trust Zone)| 192.168.8.10        |
|                               | -                          | -                           | -                     |
|                               | -                          | -                           | -                     |

**WKGO - DEV Environment**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                     | IP                 |
|-----------------------------|----------------------------|-----------------------------|--------------------|
| Dell PowerEdge R750 Server  | dev-scs-admin-api-01       | API Server                  | 192.168.14.10        |
|                               | dev-scs-admin-frontend-01  | Frontend Server             | 192.168.14.11        |
|                               | dev-scs-admin-backend-01   | Backend Server              | 192.168.14.12        |
|                               | dev-scs-db-01              | Database Server             | 192.168.14.13        |
|                               | dev-scs-filer              | File Server                 | 192.168.14.15        |
|                               | dev-scs-proxy              | Reverse Proxy Server        | 192.168.14.14 / 10.5.161.225 |
|                               | -                          | -                           | -                    |
|                               | -                          | -                           | -                    |

**GCIS T1 - DEV Environment**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                     | IP                  |
|-----------------------------|----------------------------|-----------------------------|---------------------|
| GCIS Infrastructure         | scsdwi                     | Reverse Proxy Server (iDMZ) | 192.168.0.6 / 45.119.94.100 |
|                               | scsdwg                     | Reverse Proxy Server (gDMZ) | 192.168.4.6 / 10.148.11.220 |
|                               | scsdad                     | Apps Server (Trust Zone)    | 192.168.8.7         |
|                               | scsddb                     | Database Server (Trust Zone)| 192.168.8.8         |
|                               | -                          | -                           | -                     |
|                               | -                          | -                           | -                     |


DR environment:

\[DR Environment Diagram - To be inserted here. Refer to System Manual for details. e.g., media/image5.png]

List of machines and virtual machines:

**AIA - DR Environment**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                     | IP                 |
|-----------------------------|----------------------------|-----------------------------|--------------------|
| Dell PowerEdge R750Server   | dr-scs-vcenter-01          | vCenter                     | 192.168.20.18 / 10.5.174.225 |
|                               | dr-scs-backup-01           | Veeam Backup Server         | 192.168.20.19 / 10.5.161.224 |
|                               | dr-scs-log-01              | Kiwi Log Server             | 192.168.20.10        |
|                               | dr-scs-admin-api-01        | API Server                  | 192.168.22.11        |
|                               | dr-scs-admin-frontend-01   | Frontend Server             | 192.168.22.12        |
|                               | dr-scs-admin-backend-01    | Backend Server              | 192.168.22.13        |
|                               | dr-scs-db-01               | Database Server             | 192.168.22.14        |
|                               | dr-scs-filer               | File Server                 | 192.168.22.16        |
|                               | dr-scs-proxy               | Reverse Proxy Server        | 192.168.22.15 / 10.5.174.228 |
|                               | -                          | -                           | -                    |
|                               | -                          | -                           | -                    |
|                               | -                          | -                           | -                    |

**GCIS P2 - DR Environment (Replicated from P1)**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                     | IP                  |
|-----------------------------|----------------------------|-----------------------------|---------------------|
| GCIS Infrastructure         | scspwi                     | Reverse Proxy Server (iDMZ) | 192.168.0.6 / 45.119.93.84  |
|                               | scspwg                     | Reverse Proxy Server (gDMZ) | 192.168.4.6 / 10.160.139.211|
|                               | scspad                     | Apps Server (Trust Zone)    | 192.168.8.6         |
|                               | scspdb                     | Database Server (Trust Zone)| 192.168.8.7         |
|                               | scspbk2                    | Veeam Backup Server         | 192.168.8.9         |
|                               | scsplog                    | Kiwi Log Server             | 192.168.8.10        |
|                               | -                          | -                           | -                     |
|                               | -                          | -                           | -                     |


# 2. Purpose

This document is a checklist of handover materials within project scope;
and it also provides relevant information to the support maintenance
staffs who will be maintaining this system in the future. All these
deliverables should be received from system implementation team of the
Licensing Self-Certification Portal (LSCP); to the Buildings Department
(BD) of the Government of the Hong Kong Special Administrative Region
(HKSARG or the Government).

The hand-over items of this project can be summarized into the following
6 items:

> 1. Documentation
> 2. Program Source code (Backend Application, Frontend Web App, Fronted Mobile App)
> 3. Administration Accounts
> 4. System backup
> 5. Hardware
> 6. Software Packages and Licenses

## 2.1 Schedule

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |

## 2.2 Verification

1.  The application URL verification

> The access link (URL) of each application should be verified by
> performing an access checking.

2.  Login accounts verification

> The login accounts of the applications and servers should be verified
> by processing login action.

# 3. Documentation

| Document                             | File Name | Version |
|--------------------------------------|-----------|---------|
| SA&D Report                          |           |         |
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
| Computer Operation Procedures Manual |           |         |
| Data Manual                          |           |         |
| System Maintenance Plan              |           |         |
| User Procedures Manual               |           |         |
| Security Incident Handling Procedure |           |         |
| Handover Plan                        |           |         |
| System Manual                        |           |         |
| Program Manual                       |           |         |
| Project Evaluation Report            |           |         |

# 4. Program Source Code

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |
|                      |         |           |

# 5. Administration Accounts Checklist

In this section, it will list the user account for management in the
different areas.

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
<th><blockquote>
<p>Internal IP Address</p>
</blockquote></th>
<th><blockquote>
<p>BD Network IP Address</p>
</blockquote></th>
<th>Access method</th>
<th>User account</th>
<th>Password</th>
</tr>
<tr class="odd">
<th>Blade Servers</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>Hypervisiors</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>Windows Server</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>Hypervisior Controller</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>Storage Server</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>Firewall</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>Network Switch</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>SQL Database</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>Symantec Endpoint Protection Manager (SEPM)</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>Syslog</th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

**Administration Accounts on LSCP**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |
|             |           |              |          |

# 6. Backup

<span class="mark">\[RY Note: Following content needs to check]</span>

## 6.1 VM Backup

Backup service is carried out by backup server.

Daily VM image backup is carried out and store in the backup servers. A
further copy of production VM images is copied to DR?s backuper server.

## 6.2 Database Backup

Database full export backup: this type of backup contains full database
exported database objects including schemas, table structures, packages,
stored procedures and data.

Daily full export backup is done on DB servers, data stored on the DB
servers and further backed up by VM Backup.

For detailed backup strategy, please refer to Section 8.6 "Database Backup Strategy" of the System Manual.

# 7. Outstanding Items/Issues

Nil.

# 8. Licensed Software

<span class="mark">\[RY Note: Items are for reference only. They are
incorrect]</span>

| Item                                                                              | Amount | Expire At |
|-----------------------------------------------------------------------------------|--------|-----------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual (Note: Should be SQL 2022 Standard based on System Manual Section 7.2)  |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years) (Note: Should be ESET Server Security and Bitdefender based on System Manual Section 7.2)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

\<\<\< End of document \>\>\>
```