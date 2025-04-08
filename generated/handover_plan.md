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
reproduced in whole or in part without the express permission of the Government of the HKSAR.

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
<tr class="odd">
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
[9. Log Management](#log-management)

# 1. Environment Description

Production and UAT environment:

\[an image here]

Refer to the System Manual - Section 5.2 System Architecture and Section 6 Equipment Configuration for detailed environment diagrams and configurations.

**List of machines and virtual machines:**

**WKGO - Production Environment**

Please refer to System Manual - Section 6.1.2 Guest Servers Components - Production guest servers for detailed information.

| **Role**             | **Host Name**        | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses**                  | **Data Center** | **Host Server / Zone**   |
|----------------------|----------------------|----------|--------------|---------------|-----------------------------------|-----------------|--------------------------|
| vCenter              | prd-scs-vcenter-01   | 16       | 39           | 1.33TB        | 192.168.10.24 / 10.5.161.210      | WKGO            | prd-scs-admin-server-01  |
| Veeam Backup Server  | prd-scs-backup-01    | 8        | 24           | 300 + 1TB     | 192.168.10.25 / 10.5.161.211      | WKGO            | prd-scs-admin-server-02  |
| Kiwi Log Server      | prd-scs-log-01       | 4        | 16           | 300 + 500     | 192.168.10.11 / 10.5.161.223      | WKGO            | prd-scs-admin-server-01  |
| NOD32 Anti-Virus Server | prd-scs-esetnod32    | 4        | 16           | 300           | 192.168.10.34 / 10.5.161.215      | WKGO            | prd-scs-admin-server-02  |
| API Server           | prd-scs-admin-api-01 | 2        | 4            | 100           | 192.168.12.11                       | WKGO            | prd-scs-admin-server-01  |
| Frontend Server      | prd-scs-admin-frontend-01 | 2        | 4            | 100           | 192.168.12.12                       | WKGO            | prd-scs-admin-server-01  |
| Backend Server       | prd-scs-admin-backend-01 | 2        | 4            | 100           | 192.168.12.13                       | WKGO            | prd-scs-admin-server-01  |
| Database Server      | prd-scs-db-01        | 8        | 16           | 100 + 500     | 192.168.12.14                       | WKGO            | prd-scs-admin-server-01  |
| File Server          | prd-scs-filer        | 2        | 4            | 100 + 1TB     | 192.168.12.20                       | WKGO            | prd-scs-admin-server-01  |
| Reverse Proxy Server | prd-scs-proxy        | 2        | 4            | 100           | 192.168.12.15 / 10.5.161.226      | WKGO            | prd-scs-admin-server-01  |
| API Server           | prd-scs-admin-api-02 | 2        | 4            | 100           | 192.168.12.16                       | WKGO            | prd-scs-admin-server-02  |
| Frontend Server      | prd-scs-admin-frontend-02 | 2        | 4            | 100           | 192.168.12.17                       | WKGO            | prd-scs-admin-server-02  |
| Backend Server       | prd-scs-admin-backend-02 | 2        | 4            | 100           | 192.168.12.18                       | WKGO            | prd-scs-admin-server-02  |
| Database Server      | prd-scs-db-02        | 8        | 16           | 100 + 500     | 192.168.12.19                       | WKGO            | prd-scs-admin-server-02  |
| Reverse Proxy Server | scspwi               | 2        | 8            | 100           | 192.168.0.6 / 45.119.92.84        | GCIS P1         | iDMZ                     |
| Reverse Proxy Server | scspwg               | 2        | 8            | 100           | 192.168.4.6 / 10.160.11.211       | GCIS P1         | gDMZ                     |
| Apps Server          | scspad               | 4        | 16           | 100 + 500     | 192.168.8.6                         | GCIS P1         | Trust Zone               |
| Database Server      | scspdb               | 4        | 16           | 100 + 200     | 192.168.8.7                         | GCIS P1         | Trust Zone               |
| Veeam Backup Server  | scspbk2              | 4        | 16           | 100 + 1TB     | 192.168.8.9                         | GCIS P1         | Trust Zone               |
| Kiwi Log Server      | scsplog              | 2        | 8            | 100 + 100     | 192.168.8.10                        | GCIS P1         | Trust Zone               |

**WKGO - UAT Environment**

Please refer to System Manual - Section 6.1.2 Guest Servers Components - UAT guest servers for detailed information.

| **Role**             | **Host Name**        | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses**                  | **Data Center** | **Host Server / Zone**   |
|----------------------|----------------------|----------|--------------|---------------|-----------------------------------|-----------------|--------------------------|
| API Server           | uat-scs-admin-api-01 | 2        | 4            | 100           | 192.168.13.10                       | WKGO            | prd-scs-admin-server-01  |
| Frontend Server      | uat-scs-admin-frontend-01 | 2        | 4            | 100           | 192.168.13.11                       | WKGO            | prd-scs-admin-server-01  |
| Backend Server       | uat-scs-admin-backend-01 | 2        | 4            | 100           | 192.168.13.12                       | WKGO            | prd-scs-admin-server-01  |
| Database Server      | uat-scs-db-01        | 2        | 4            | 100           | 192.168.13.13                       | WKGO            | prd-scs-admin-server-01  |
| File Server          | uat-scs-filer        | 2        | 4            | 100 + 200     | 192.168.13.15                       | WKGO            | prd-scs-admin-server-01  |
| Reverse Proxy Server | uat-scs-proxy        | 2        | 4            | 100           | 192.168.13.14 / 10.5.161.224      | WKGO            | prd-scs-admin-server-01  |
| Reverse Proxy Server | scsuwi               | 2        | 8            | 100           | 192.168.0.7 / 45.119.94.99        | GCIS T1         | iDMZ                     |
| Reverse Proxy Server | scsuwg               | 2        | 8            | 100           | 192.168.4.7 / 10.148.11.220       | GCIS T1         | gDMZ                     |
| Apps Server          | scsuad               | 4        | 16           | 100 + 200     | 192.168.8.9                         | GCIS T1         | Trust Zone               |
| Database Server      | scsudb               | 4        | 16           | 100 + 100     | 192.168.8.10                        | GCIS T1         | Trust Zone               |

**WKGO - DEV Environment**

Please refer to System Manual - Section 6.1.2 Guest Servers Components - DEV guest servers for detailed information.

| **Role**             | **Host Name**        | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses**                  | **Data Center** | **Host Server / Zone**   |
|----------------------|----------------------|----------|--------------|---------------|-----------------------------------|-----------------|--------------------------|
| API Server           | dev-scs-admin-api-01 | 2        | 4            | 100           | 192.168.14.10                       | WKGO            | prd-scs-admin-server-02  |
| Frontend Server      | dev-scs-admin-frontend-01 | 2        | 4            | 100           | 192.168.14.11                       | WKGO            | prd-scs-admin-server-02  |
| Backend Server       | dev-scs-admin-backend-01 | 2        | 4            | 100           | 192.168.14.12                       | WKGO            | prd-scs-admin-server-02  |
| Database Server      | dev-scs-db-01        | 2        | 4            | 100           | 192.168.14.13                       | WKGO            | prd-scs-admin-server-02  |
| File Server          | dev-scs-filer        | 2        | 4            | 100 + 200     | 192.168.14.15                       | WKGO            | prd-scs-admin-server-02  |
| Reverse Proxy Server | dev-scs-proxy        | 2        | 4            | 100           | 192.168.14.14 / 10.5.161.225      | WKGO            | prd-scs-admin-server-02  |
| Reverse Proxy Server | scsdwi               | 2        | 8            | 100           | 192.168.0.6 / 45.119.94.100       | GCIS T1         | iDMZ                     |
| Reverse Proxy Server | scsdwg               | 2        | 8            | 100           | 192.168.4.6 / 10.148.11.220       | GCIS T1         | gDMZ                     |
| Apps Server          | scsdad               | 4        | 16           | 100 + 200     | 192.168.8.7                         | GCIS T1         | Trust Zone               |
| Database Server      | scsddb               | 4        | 16           | 100 + 100     | 192.168.8.8                         | GCIS T1         | Trust Zone               |

**DR environment:**

\[image here]

Refer to the System Manual - Section 5.2 System Architecture and Section 6 Equipment Configuration for detailed environment diagrams and configurations.

**List of machines and virtual machines:**

**AIA - DR Environment**

Please refer to System Manual - Section 6.1.2 Guest Servers Components - Disaster Recovery guest servers for detailed information.

| **Role**             | **Host Name**        | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses**                  | **Data Center** | **Host Server / Zone**   |
|----------------------|----------------------|----------|--------------|---------------|-----------------------------------|-----------------|--------------------------|
| vCenter              | dr-scs-vcenter-01    | 16       | 39           | 1.33TB        | 192.168.20.18 / 10.5.174.225      | AIA             | dr-scs-admin-server-01   |
| Veeam Backup Server  | dr-scs-backup-01     | 8        | 24           | 300 + 1TB     | 192.168.20.19 / 10.5.161.224      | AIA             | dr-scs-admin-server-01   |
| Kiwi Log Server      | dr-scs-log-01        | 4        | 8            | 300 + 500     | 192.168.20.10                       | AIA             | dr-scs-admin-server-01   |
| API Server           | dr-scs-admin-api-01  | 2        | 8            | 90            | 192.168.22.11                       | AIA             | dr-scs-admin-server-01   |
| Frontend Server      | dr-scs-admin-frontend-01 | 2        | 8            | 90            | 192.168.22.12                       | AIA             | dr-scs-admin-server-01   |
| Backend Server       | dr-scs-admin-backend-01 | 2        | 8            | 90            | 192.168.22.13                       | AIA             | dr-scs-admin-server-01   |
| Database Server      | dr-scs-db-01         | 2        | 8            | 90 + 500      | 192.168.22.14                       | AIA             | dr-scs-admin-server-01   |
| File Server          | dr-scs-filer         | 2        | 8            | 90 + 1TB      | 192.168.22.16                       | AIA             | dr-scs-admin-server-01   |
| Reverse Proxy Server | dr-scs-proxy         | 2        | 4            | 90            | 192.168.22.15 / 10.5.174.228      | AIA             | dr-scs-admin-server-01   |
| Reverse Proxy Server | scspwi               | 2        | 8            | 100           | 192.168.0.6 / 45.119.93.84        | GCIS P2         | iDMZ                     |
| Reverse Proxy Server | scspwg               | 2        | 8            | 100           | 192.168.4.6 / 10.160.139.211      | GCIS P2         | gDMZ                     |
| Apps Server          | scspad               | 4        | 16           | 100 + 500     | 192.168.8.6                         | GCIS P2         | Trust Zone               |
| Database Server      | scspdb               | 4        | 16           | 100 + 200     | 192.168.8.7                         | GCIS P2         | Trust Zone               |
| Veeam Backup Server  | scspbk2              | 4        | 16           | 100 + 1TB     | 192.168.8.9                         | GCIS P2         | Trust Zone               |
| Kiwi Log Server      | scsplog              | 2        | 8            | 100 + 100     | 192.168.8.10                        | GCIS P2         | Trust Zone               |


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
| System Manual                        | `sm_i1.md`  | 0.1     |
| Program Manual                       | ?         | ?       |
| Project Evaluation Report            | ?         | ?       |

# 4. Program Source Code

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |
|                      |         |           |

*Note: Please refer to Program Manual for detailed directory structure and repository information.*

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

*Note: Please refer to Security Management Plan and System Manual for default account details and password management procedures.*

# 6. Backup

<span class="mark">\[RY Note: Following content needs to check]</span>

Refer to System Manual - Section 8.2 Backup and Section 8.6 Database Backup Strategy for detailed backup procedures and schedules.

## 6.1 VM Backup

Backup service is carried out by backup server.

Daily VM image backup is carried out and store in the backup servers. A
further copy of production VM images is copied to DR?s backuper server.

Production, UAT and DEV environments on WKGO and DR on AIA will be
backed up by the backup servers (prd-scs-backup-01 and dr-scs-backup-01).

Production environments on GCIS P1 will be backed up by backup services
that are provided by GCIS with offsite copy and replicated to DR GCIS
P2. UAT and DEV environments on GCIS will be backup by backup services that
are provided by GCIS.

## 6.2 Database Backup

Database full export backup: this type of backup contains full database
exported database objects including schemas, table structures, packages,
stored procedures and data.

Daily full export backup is done on DB servers, data stored on the DB
servers and further backed up by VM Backup.

Daily full export backup is done on DB servers (uat-db-01,
prd-db-01, prd-db-02, dr-db-01) at 18:45, data stored on the DB servers?
directory: `D:\backup\\`.

# 7. Outstanding Items/Issues

Nil.

# 8. Licensed Software

<span class="mark">\[RY Note: Items are for reference only. They are
incorrect]</span>

| Item                                                                              | Amount | Expire At |
|-----------------------------------------------------------------------------------|--------|-----------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual                                            |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

*Note: Please refer to Software Inventory in System Manual - Section 7.2 Inventory of System Software and Software Package for a comprehensive list of software.*

# 9. Log Management

Refer to System Manual - Section 10. Log Management for detailed log management procedures and retention policy.

1.  Following activities shall include in the log:

> ? Attempts for log-in
>
> ? Unauthorised update/access
>
> ? Failed attempts for privileges elevation
>
> ? Attempts for password changes
>
> ? Access attempts to critical files (e.g., software configuration
> files, password and key files, etc.)
>
> ? Actions taken by privileged users
>
> ? Use of privileged rights such as addition and deletion of user
> accounts
>
> ? Security related system failures and alerts
>
> ? Changes to user access rights
>
> ? Failed access attempts to systems and files identified as critical
> to the system
>
> ? Computer services such as file copying or searching
>
> ? Modification to audit policy
>
> ? Activation and de-activation of protection systems, such as
> anti-malware systems and intrusion detection systems

2.  Logs shall be retained for **180 days** and centralised and managed
by Syslog server. Unauthorised access is restricted.

3.  Logs will be reviewed regularly.

4.  Logs shall not be used to profile the activity of a particular user
unless it relates to a necessary audit activity supported by a
Directorate rank officer.

\<\<\< End of document \>\>\>
```