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

[1. Environment Description 4](#environment-description)

[2. Purpose 6](#purpose)

> [2.1 Schedule 6](#schedule)
>
> [2.2 Verification 6](#verification)

[3. Documentation 7](#documentation)

[4. Program Source Code 9](#program-source-code)

[5. Administration Accounts Checklist
10](#administration-accounts-checklist)

[6. Backup 11](#backup)

> [6.1 VM Backup 11](#vm-backup)
>
> [6.2 Database Backup 11](#database-backup)

[7. Outstanding Items/Issues 12](#outstanding-itemsissues)

[8. Licensed Software 13](#licensed-software)

# 1. Environment Description

Production and UAT environment:

[Will insert environment diagram here - refer to System Manual for architecture details]

List of machines and virtual machines:

**WKGO Production Environment:**

<table>
<thead>
<tr>
<th>Hostname (Physical Machine)</th>
<th>Hostname (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="14">prd-scs-admin-server-01</td>
<td>prd-scs-vcenter-01</td><td>vCenter Server</td><td>192.168.10.24 / 10.5.161.210</td>
</tr>
<tr>
<td>prd-scs-log-01</td><td>Kiwi Log Server</td><td>192.168.10.11 / 10.5.161.223</td>
</tr>
<tr>
<td>prd-scs-admin-api-01</td><td>API Server</td><td>192.168.12.11</td>
</tr>
<tr>
<td>prd-scs-admin-frontend-01</td><td>Frontend Server</td><td>192.168.12.12</td>
</tr>
<tr>
<td>prd-scs-admin-backend-01</td><td>Backend Server</td><td>192.168.12.13</td>
</tr>
<tr>
<td>prd-scs-db-01</td><td>Database Server (Primary)</td><td>192.168.12.14</td>
</tr>
<tr>
<td>prd-scs-filer</td><td>File Server</td><td>192.168.12.20</td>
</tr>
<tr>
<td>prd-scs-proxy</td><td>Reverse Proxy Server (Internal)</td><td>192.168.12.15 / 10.5.161.226</td>
</tr>
<tr>
<td>uat-scs-admin-api-01</td><td>UAT API Server</td><td>192.168.13.10</td>
</tr>
<tr>
<td>uat-scs-admin-frontend-01</td><td>UAT Frontend Server</td><td>192.168.13.11</td>
</tr>
<tr>
<td>uat-scs-admin-backend-01</td><td>UAT Backend Server</td><td>192.168.13.12</td>
</tr>
<tr>
<td>uat-scs-db-01</td><td>UAT Database Server</td><td>192.168.13.13</td>
</tr>
<tr>
<td>uat-scs-filer</td><td>UAT File Server</td><td>192.168.13.15</td>
</tr>
<tr>
<td>uat-scs-proxy</td><td>UAT Reverse Proxy Server (Internal)</td><td>192.168.13.14 / 10.5.161.224</td>
</tr>
<tr>
<td rowspan="10">prd-scs-admin-server-02</td>
<td>prd-scs-backup-01</td><td>Veeam Backup Server</td><td>192.168.10.25 / 10.5.161.211</td>
</tr>
<tr>
<td>prd-scs-esetnod32</td><td>NOD32 Anti-Virus Server</td><td>192.168.10.34 / 10.5.161.215</td>
</tr>
<tr>
<td>prd-scs-admin-api-02</td><td>API Server (Secondary)</td><td>192.168.12.16</td>
</tr>
<tr>
<td>prd-scs-admin-frontend-02</td><td>Frontend Server (Secondary)</td><td>192.168.12.17</td>
</tr>
<tr>
<td>prd-scs-admin-backend-02</td><td>Backend Server (Secondary)</td><td>192.168.12.18</td>
</tr>
<tr>
<td>prd-scs-db-02</td><td>Database Server (Secondary)</td><td>192.168.12.19</td>
</tr>
<tr>
<td>dev-scs-admin-api-01</td><td>DEV API Server</td><td>192.168.14.10</td>
</tr>
<tr>
<td>dev-scs-admin-frontend-01</td><td>DEV Frontend Server</td><td>192.168.14.11</td>
</tr>
<tr>
<td>dev-scs-admin-backend-01</td><td>DEV Backend Server</td><td>192.168.14.12</td>
</tr>
<tr>
<td>dev-scs-db-01</td><td>DEV Database Server</td><td>192.168.14.13</td>
</tr>
<tr>
<td>prd-scs-nas</td><td>N/A (Physical NAS)</td><td>NAS Storage</td><td>192.168.10.35, 10.5.161.218</td>
</tr>
<tr>
<td>PA-850-SCSPri</td><td>N/A (Physical Firewall)</td><td>Primary Firewall</td><td>192.168.10.12 / 10.5.161.205</td>
</tr>
<tr>
<td>PA-850-SCSSec</td><td>N/A (Physical Firewall)</td><td>Secondary Firewall</td><td>192.168.10.13 / 10.5.161.220</td>
</tr>
<tr>
<td>-</td><td>prd-scs-proxy</td><td>Reverse Proxy Server (External)</td><td>192.168.12.15 / 10.5.161.226</td>
</tr>
</tbody>
</table>

**GCIS Production Environment (P1):**

<table>
<thead>
<tr>
<th>Hostname (Physical Machine)</th>
<th>Hostname (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspwi</td><td>Reverse Proxy Server (Internet DMZ)</td><td>192.168.0.6 / 45.119.92.84</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspwg</td><td>Reverse Proxy Server (GNET DMZ)</td><td>192.168.4.6 / 10.160.11.211</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspad</td><td>Application Server (Trusted Zone)</td><td>192.168.8.6</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspdb</td><td>Database Server (Trusted Zone)</td><td>192.168.8.7</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspbk2</td><td>Veeam Backup Server (Trusted Zone)</td><td>192.168.8.9</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsplog</td><td>Kiwi Log Server (Trusted Zone)</td><td>192.168.8.10</td>
</tr>
</tbody>
</table>

**GCIS UAT Environment (T1):**

<table>
<thead>
<tr>
<th>Hostname (Physical Machine)</th>
<th>Hostname (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsuwi</td><td>UAT Reverse Proxy Server (Internet DMZ)</td><td>192.168.0.7 / 45.119.94.99</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsuwg</td><td>UAT Reverse Proxy Server (GNET DMZ)</td><td>192.168.4.7 / 10.148.11.220</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsuad</td><td>UAT Application Server (Trusted Zone)</td><td>192.168.8.9</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsudb</td><td>UAT Database Server (Trusted Zone)</td><td>192.168.8.10</td>
</tr>
</tbody>
</table>

**GCIS DEV Environment (T1):**

<table>
<thead>
<tr>
<th>Hostname (Physical Machine)</th>
<th>Hostname (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsdwi</td><td>DEV Reverse Proxy Server (Internet DMZ)</td><td>192.168.0.6 / 45.119.94.100</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsdwg</td><td>DEV Reverse Proxy Server (GNET DMZ)</td><td>192.168.4.6 / 10.148.11.220</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsdad</td><td>DEV Application Server (Trusted Zone)</td><td>192.168.8.7</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsddb</td><td>DEV Database Server (Trusted Zone)</td><td>192.168.8.8</td>
</tr>
</tbody>
</table>


DR environment:

[Will insert DR environment diagram here - refer to System Manual for architecture details]

List of machines and virtual machines:

**AIA DR Environment:**

<table>
<thead>
<tr>
<th>Hostname (Physical Machine)</th>
<th>Hostname (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="10">dr-scs-admin-server-01</td>
<td>dr-scs-vcenter-01</td><td>DR vCenter Server</td><td>192.168.20.18 / 10.5.174.225</td>
</tr>
<tr>
<td>dr-scs-backup-01</td><td>DR Veeam Backup Server</td><td>192.168.20.19 / 10.5.161.224</td>
</tr>
<tr>
<td>dr-scs-log-01</td><td>DR Kiwi Log Server</td><td>192.168.20.10</td>
</tr>
<tr>
<td>dr-scs-admin-api-01</td><td>DR API Server</td><td>192.168.22.11</td>
</tr>
<tr>
<td>dr-scs-admin-frontend-01</td><td>DR Frontend Server</td><td>192.168.22.12</td>
</tr>
<tr>
<td>dr-scs-admin-backend-01</td><td>DR Backend Server</td><td>192.168.22.13</td>
</tr>
<tr>
<td>dr-scs-db-01</td><td>DR Database Server</td><td>192.168.22.14</td>
</tr>
<tr>
<td>dr-scs-filer</td><td>DR File Server</td><td>192.168.22.16</td>
</tr>
<tr>
<td>dr-scs-proxy</td><td>DR Reverse Proxy Server (Internal)</td><td>192.168.22.15 / 10.5.174.228</td>
</tr>
<tr>
<td>dev-scs-filer</td><td>DEV File Server</td><td>192.168.14.15</td>
</tr>
<tr>
<td>dr-scs-nas</td><td>N/A (Physical NAS)</td><td>DR NAS Storage</td><td>192.168.20.35, 10.5.174.225</td>
</tr>
<tr>
<td>PA-850-SCSDR</td><td>N/A (Physical Firewall)</td><td>DR Firewall</td><td>192.168.20.12 / 10.5.174.215</td>
</tr>
<tr>
<td>-</td><td>scspwi</td><td>DR Reverse Proxy Server (Internet DMZ)</td><td>192.168.0.6 / 45.119.93.84</td>
</tr>
<tr>
<td>-</td><td>scspwg</td><td>DR Reverse Proxy Server (GNET DMZ)</td><td>192.168.4.6 / 10.160.139.211</td>
</tr>
</tbody>
</table>

**GCIS DR Environment (P2):**

<table>
<thead>
<tr>
<th>Hostname (Physical Machine)</th>
<th>Hostname (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspwi</td><td>DR Reverse Proxy Server (Internet DMZ)</td><td>192.168.0.6 / 45.119.93.84</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspwg</td><td>DR Reverse Proxy Server (GNET DMZ)</td><td>192.168.4.6 / 10.160.139.211</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspad</td><td>DR Application Server (Trusted Zone)</td><td>192.168.8.6</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspdb</td><td>DR Database Server (Trusted Zone)</td><td>192.168.8.7</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scspbk2</td><td>DR Veeam Backup Server (Trusted Zone)</td><td>192.168.8.9</td>
</tr>
<tr>
<td>N/A (GCIS Cloud)</td>
<td>scsplog</td><td>DR Kiwi Log Server (Trusted Zone)</td><td>192.168.8.10</td>
</tr>
</tbody>
</table>

Please refer to the **System Manual** for detailed network diagrams and rack diagrams.

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
>
> 2. Program Source code (Backend Application, Frontend Web App,
> Fronted Mobile App)
>
> 3. Administration Accounts
>
> 4. System backup
>
> 5. Hardware
>
> 6. Software Packages and Licenses

## 2.1 Schedule

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |

**Note:** Dates to be filled in upon agreement between MC and BD.

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

**Note:** File Names and Versions to be filled in upon handover. Ensure all documents listed are provided.

# 4. Program Source Code

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |  [TBD]   |  [TBD]    |
| Backend Application  |  [TBD]   |  [TBD]    |
| Database Scripts     |  [TBD]   |  [TBD]    |

**Note:** Machine and Directory information for source code repository to be provided upon handover.

# 5. Administration Accounts Checklist

In this section, it will list the user account for management in the
different areas.

<table>
<thead>
<tr>
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
<tr>
<td>Blade Servers</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>Hypervisiors</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>Windows Server</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>Hypervisior Controller (vCenter)</td>
<td>prd-scs-vcenter-01, dr-scs-vcenter-01</td>
<td>192.168.10.24, 192.168.20.18</td>
<td>10.5.161.210, 10.5.174.225</td>
<td>vSphere Client</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>Storage Server (SAN)</td>
<td>Dell PowerStore 500T</td>
<td>192.168.10.26, 192.168.20.20</td>
<td>[TBD]</td>
<td>Web Interface</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>Backup Appliance</td>
<td>Dell DataDomain 3300</td>
<td>192.168.10.20, 192.168.20.25</td>
<td>[TBD]</td>
<td>Web Interface</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>Firewall</td>
<td>PA-850-SCSPri, PA-850-SCSDR</td>
<td>192.168.10.12, 192.168.20.12</td>
<td>10.5.161.205, 10.5.174.215</td>
<td>Web Interface</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>Network Switch</td>
<td>[TBD]</td>
<td>192.168.10.14, 192.168.20.13</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>SQL Database</td>
<td>prd-scs-db-01, prd-scs-db-02, scspdb, dr-scs-db-01, scsudb, scsddb, uat-scs-db-01, dev-scs-db-01</td>
<td>Various (refer to Environment Description)</td>
<td>Various (refer to Environment Description)</td>
<td>SQL Server Management Studio</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>Symantec Endpoint Protection Manager (SEPM) / ESET Protect</td>
<td>prd-scs-esetnod32</td>
<td>192.168.10.34</td>
<td>10.5.161.215</td>
<td>Web Interface</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
<tr>
<td>Syslog (Kiwi Syslog)</td>
<td>prd-scs-log-01, scsplog, dr-scs-log-01</td>
<td>192.168.10.11, 192.168.8.10, 192.168.20.10</td>
<td>10.5.161.223</td>
<td>Kiwi Syslog Web Interface</td>
<td>[TBD]</td>
<td>[TBD]</td>
</tr>
</tbody>
</table>

**Note:** User accounts and Passwords to be provided securely during handover. Replace "[TBD]" with actual information.

**Administration Accounts on LSCP Application**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |
|             | Public User|              |          |

**Note:** Default application admin accounts and passwords to be provided securely during handover.

# 6. Backup

<span class="mark">\[RY Note: Following content needs to check\]</span>

## 6.1 VM Backup

Backup service is carried out by Veeam Backup & Replication server in both WKGO (prd-scs-backup-01) and DR site (dr-scs-backup-01).

Daily VM image backup is carried out and store in the backup storage. A
further copy of production VM images is copied to DR?s backup server (for WKGO VMs) and GCIS DR site (for GCIS VMs - managed by GCIS Backup Services).

Backup Schedule details:

* **PROD VM Backup Job 3 Daily**: Daily 12:01 AM (Full)
* **PROD VM Backup to Tape Job 3 Weekly**: Every Sunday 09:00 AM (Full)
* **PROD UAT VM Backup Job 1 Daily**: Daily 08:00 PM (Full)
* **PROD UAT VM Backup to Tape Job 1 Weekly**: Every Sunday 06:00 AM (Full)
* **PROD DEV VM Backup Job 2 Daily**: Daily 10:00 PM (Full)
* **PROD DEV VM Backup to Tape Job 2 Weekly**: Every Sunday 03:00 AM (Full)
* **PROD All jobs to DR Backup Copy Job 1**: After every PROD VM Backup Job 1, 2 and 3 Daily
* **DR VM Backup Job 4 Daily**: Daily 08:00 PM (Full)

## 6.2 Database Backup

Database full export backup: this type of backup contains full database
exported database objects including schemas, table structures, packages,
stored procedures and data.

Daily full export backup is done on DB servers, data stored on the DB
servers and further backed up by VM Backup.

Database backup directory on DB servers: `D:\backup\`

Database full export backup is scheduled daily at 18:45.

# 7. Outstanding Items/Issues

Nil.

# 8. Licensed Software

<span class="mark">\[RY Note: Items are for reference only. They are
incorrect\]</span>

| Item                                                                              | Amount | Expire At |
|-----------------------------------------------------------------------------------|--------|-----------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        | Perpetual |
| SQL 2019 Standard (2-Core) - Perpetual  (Note: System is using SQL 2022 Standard)                                          |        | Perpetual |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years) / ESET Server Security License (Perpetual)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription) / Kiwi Syslog Server NG License (Perpetual)                             |        | Perpetual |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

**Note:** License details and expiry dates to be confirmed and updated during handover. Please refer to the Software Inventory section in the System Manual for installed software versions.

\<\<\< End of document \>\>\>
```