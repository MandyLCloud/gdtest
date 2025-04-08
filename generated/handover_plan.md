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

---

# 1. Environment Description

This section describes the Production, UAT, and DR environments for the Licensing Self-Certification Portal (LSCP). The system is deployed across two datacenters: On-premise (WKGO) and Government Cloud Infrastructure Services (GCIS).

**Production and UAT Environment (WKGO):**

[Production and UAT environment diagram is expected here, refer to original document for placeholders]

List of machines and virtual machines:

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 20%" />
<col style="width: 35%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Hostname</p>
<p>(Physical Machine)</p></th>
<th><p>Hostname</p>
<p>(Virtual Machine)</p></th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<th rowspan="2">prd-scs-admin-server-01</th>
<td>prd-scs-vcenter-01</td>
<td>vCenter Server</td>
<td>192.168.10.24 / 10.5.161.210</td>
</tr>
<tr class="even">
<td>prd-scs-log-01</td>
<td>Kiwi Log Server</td>
<td>192.168.10.11 / 10.5.161.223</td>
</tr>
<tr class="odd">
<th rowspan="7">prd-scs-admin-server-02</th>
<td>prd-scs-backup-01</td>
<td>Veeam Backup Server</td>
<td>192.168.10.25 / 10.5.161.211</td>
</tr>
<tr class="even">
<td>prd-scs-esetnod32</td>
<td>NOD32 Anti-Virus Server</td>
<td>192.168.10.34 / 10.5.161.215</td>
</tr>
<tr class="odd">
<td>prd-scs-admin-api-02</td>
<td>API Server (Admin)</td>
<td>192.168.12.16</td>
</tr>
<tr class="even">
<td>prd-scs-admin-frontend-02</td>
<td>Frontend Server (Admin)</td>
<td>192.168.12.17</td>
</tr>
<tr class="odd">
<td>prd-scs-admin-backend-02</td>
<td>Backend Server (Admin)</td>
<td>192.168.12.18</td>
</tr>
<tr class="even">
<td>prd-scs-db-02</td>
<td>Database Server (Secondary)</td>
<td>192.168.12.19</td>
</tr>
<tr class="odd">
<td>dev-scs-proxy</td>
<td>Reverse Proxy Server (DEV)</td>
<td>192.168.14.14 / 10.5.161.225</td>
</tr>
<tr class="even">
<th rowspan="7">prd-scs-admin-server-01</th>
<td>prd-scs-admin-api-01</td>
<td>API Server (Admin)</td>
<td>192.168.12.11</td>
</tr>
<tr class="odd">
<td>prd-scs-admin-frontend-01</td>
<td>Frontend Server (Admin)</td>
<td>192.168.12.12</td>
</tr>
<tr class="even">
<td>prd-scs-admin-backend-01</td>
<td>Backend Server (Admin)</td>
<td>192.168.12.13</td>
</tr>
<tr class="odd">
<td>prd-scs-db-01</td>
<td>Database Server (Primary)</td>
<td>192.168.12.14</td>
</tr>
<tr class="even">
<td>prd-scs-proxy</td>
<td>Reverse Proxy Server (Production)</td>
<td>192.168.12.15 / 10.5.161.226</td>
</tr>
<tr class="odd">
<td>prd-scs-filer</td>
<td>File Server (Production)</td>
<td>192.168.12.20</td>
</tr>
<tr class="even">
<td>uat-scs-proxy</td>
<td>Reverse Proxy Server (UAT)</td>
<td>192.168.13.14 / 10.5.161.224</td>
</tr>
</tbody>
</table>

**Production and UAT Environment (GCIS):**

List of machines and virtual machines:

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 20%" />
<col style="width: 35%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Hostname</p>
<p>(Physical Machine)</p></th>
<th><p>Hostname</p>
<p>(Virtual Machine)</p></th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<th>GCIS P1</th>
<td>scspwi</td>
<td>Reverse Proxy Server (Internet DMZ)</td>
<td>192.168.0.6 / 45.119.92.84</td>
</tr>
<tr class="even">
<th>GCIS P1</th>
<td>scspwg</td>
<td>Reverse Proxy Server (GNET DMZ)</td>
<td>192.168.4.6 / 10.160.11.211</td>
</tr>
<tr class="odd">
<th>GCIS P1</th>
<td>scspad</td>
<td>Application Server (Trust Zone)</td>
<td>192.168.8.6</td>
</tr>
<tr class="even">
<th>GCIS P1</th>
<td>scspdb</td>
<td>Database Server (Trust Zone)</td>
<td>192.168.8.7</td>
</tr>
<tr class="odd">
<th>GCIS P1</th>
<td>scspbk2</td>
<td>Veeam Backup Server (Trust Zone)</td>
<td>192.168.8.9</td>
</tr>
<tr class="even">
<th>GCIS P1</th>
<td>scsplog</td>
<td>Kiwi Log Server (Trust Zone)</td>
<td>192.168.8.10</td>
</tr>
<tr class="odd">
<th>GCIS T1</th>
<td>scsuwi</td>
<td>Reverse Proxy Server (Internet DMZ - UAT)</td>
<td>192.168.0.7 / 45.119.94.99</td>
</tr>
<tr class="even">
<th>GCIS T1</th>
<td>scsuwg</td>
<td>Reverse Proxy Server (GNET DMZ - UAT)</td>
<td>192.168.4.7 / 10.148.11.220</td>
</tr>
<tr class="odd">
<th>GCIS T1</th>
<td>scsuad</td>
<td>Application Server (Trust Zone - UAT)</td>
<td>192.168.8.9</td>
</tr>
<tr class="even">
<th>GCIS T1</th>
<td>scsudb</td>
<td>Database Server (Trust Zone - UAT)</td>
<td>192.168.8.10</td>
</tr>
<tr class="odd">
<th>GCIS T1</th>
<td>scsdwi</td>
<td>Reverse Proxy Server (Internet DMZ - DEV)</td>
<td>192.168.0.6 / 45.119.94.100</td>
</tr>
<tr class="even">
<th>GCIS T1</th>
<td>scsdwg</td>
<td>Reverse Proxy Server (GNET DMZ - DEV)</td>
<td>192.168.4.6 / 10.148.11.220</td>
</tr>
<tr class="odd">
<th>GCIS T1</th>
<td>scsdad</td>
<td>Application Server (Trust Zone - DEV)</td>
<td>192.168.8.7</td>
</tr>
<tr class="even">
<th>GCIS T1</th>
<td>scsddb</td>
<td>Database Server (Trust Zone - DEV)</td>
<td>192.168.8.8</td>
</tr>
</tbody>
</table>

**DR environment (AIA):**

[DR environment diagram is expected here, refer to original document for placeholders]

List of machines and virtual machines:

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 20%" />
<col style="width: 35%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Hostname</p>
<p>(Physical Machine)</p></th>
<th><p>Hostname</p>
<p>(Virtual Machine)</p></th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<th rowspan="2">dr-scs-admin-server-01</th>
<td>dr-scs-vcenter-01</td>
<td>vCenter Server (DR)</td>
<td>192.168.20.18 / 10.5.174.225</td>
</tr>
<tr class="even">
<td>dr-scs-log-01</td>
<td>Kiwi Log Server (DR)</td>
<td>192.168.20.10</td>
</tr>
<tr class="odd">
<th rowspan="7">dr-scs-admin-server-01</th>
<td>dr-scs-backup-01</td>
<td>Veeam Backup Server (DR)</td>
<td>192.168.20.19 / 10.5.161.224</td>
</tr>
<tr class="even">
<td>dr-scs-admin-api-01</td>
<td>API Server (Admin - DR)</td>
<td>192.168.22.11</td>
</tr>
<tr class="odd">
<td>dr-scs-admin-frontend-01</td>
<td>Frontend Server (Admin - DR)</td>
<td>192.168.22.12</td>
</tr>
<tr class="even">
<td>dr-scs-admin-backend-01</td>
<td>Backend Server (Admin - DR)</td>
<td>192.168.22.13</td>
</tr>
<tr class="odd">
<td>dr-scs-db-01</td>
<td>Database Server (DR)</td>
<td>192.168.22.14</td>
</tr>
<tr class="even">
<td>dr-scs-proxy</td>
<td>Reverse Proxy Server (DR)</td>
<td>192.168.22.15 / 10.5.174.228</td>
</tr>
<tr class="odd">
<td>dr-scs-filer</td>
<td>File Server (DR)</td>
<td>192.168.22.16</td>
</tr>
<tr class="even">
<th>GCIS P2</th>
<td>scspwi</td>
<td>Reverse Proxy Server (Internet DMZ - DR)</td>
<td>192.168.0.6 / 45.119.93.84</td>
</tr>
<tr class="odd">
<th>GCIS P2</th>
<td>scspwg</td>
<td>Reverse Proxy Server (GNET DMZ - DR)</td>
<td>192.168.4.6 / 10.160.139.211</td>
</tr>
<tr class="even">
<th>GCIS P2</th>
<td>scspad</td>
<td>Application Server (Trust Zone - DR)</td>
<td>192.168.8.6</td>
</tr>
<tr class="odd">
<th>GCIS P2</th>
<td>scspdb</td>
<td>Database Server (Trust Zone - DR)</td>
<td>192.168.8.7</td>
</tr>
<tr class="even">
<th>GCIS P2</th>
<td>scspbk2</td>
<td>Veeam Backup Server (Trust Zone - DR)</td>
<td>192.168.8.9</td>
</tr>
<tr class="odd">
<th>GCIS P2</th>
<td>scsplog</td>
<td>Kiwi Log Server (Trust Zone - DR)</td>
<td>192.168.8.10</td>
</tr>
</tbody>
</table>

---

# 2. Purpose

This document serves as a checklist for handover materials within the project scope. It also provides essential information for the support and maintenance staff who will be responsible for the ongoing maintenance of the Licensing Self-Certification Portal (LSCP) system.

All deliverables outlined in this plan are to be transferred from the system implementation team of the LSCP to the Buildings Department (BD) of the Government of the Hong Kong Special Administrative Region (HKSARG or the Government).

The handover items for this project are categorized into the following key areas:

1. Documentation
2. Program Source Code (Backend Application, Frontend Web App, Frontend Mobile App)
3. Administration Accounts
4. System Backup
5. Hardware (Refer to System Manual for details)
6. Software Packages and Licenses (Refer to System Manual for details)

## 2.1 Schedule

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |

## 2.2 Verification

The verification process will include the following steps to ensure a successful handover:

1.  **Application URL Verification**:
    > Access links (URLs) for each application will be verified by performing access checks to ensure they are functional and reachable.

2.  **Login Accounts Verification**:
    > Login accounts for applications and servers will be verified by successfully logging in to confirm credentials and access permissions.

---

# 3. Documentation

The following documents are to be handed over as part of the system handover.

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

---

# 4. Program Source Code

The program source code for the LSCP system components will be handed over, including the following:

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |
| Frontend Mobile App   |         |           |

**Note**: Specific machine and directory details for the source code will be provided separately.

---

# 5. Administration Accounts Checklist

This section lists the user accounts required for system administration across different areas of the LSCP infrastructure.

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
</thead>
<tbody>
<tr class="odd">
<th>Blade Servers</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<th>Hypervisiors</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<th>Windows Server</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<th>Hypervisior Controller</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<th>Storage Server</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<th>Firewall</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<th>Network Switch</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<th>SQL Database</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<th>Symantec Endpoint Protection Manager (SEPM)</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<th>Syslog</th>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

**Administration Accounts on LSCP Application**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |

**Note**: Specific account details and passwords will be provided securely through a separate channel.

---

# 6. Backup

\[RY Note: Following content needs to be checked]

## 6.1 VM Backup

VM Backup services are managed by dedicated backup servers within each environment.

- **WKGO & AIA:** Daily VM image backups are performed and stored on backup servers. Production VM images are also copied to the DR backup server located in AIA for redundancy.
- **GCIS:** Backup services for GCIS environments (P1, T1, DEV, P2) are provided by GCIS, including offsite copies and replication to DR GCIS P2.

Backup Schedule Details:

- **PROD VM Backup Job 3 Daily**: Daily 12:01 AM (Full)
- **PROD VM Backup to Tape Job 3 Weekly**: Every Sunday 09:00 AM (Full)
- **PROD UAT VM Backup Job 1 Daily**: Daily 08:00 PM (Full)
- **PROD UAT VM Backup to Tape Job 1 Weekly**: Every Sunday 06:00 AM (Full)
- **PROD DEV VM Backup Job 2 Daily**: Daily 10:00 PM (Full)
- **PROD DEV VM Backup to Tape Job 2 Weekly**: Every Sunday 03:00 AM (Full)
- **PROD All jobs to DR Backup Copy Job 1**: After every PROD VM Backup Job 1, 2 and 3 Daily
- **DR VM Backup Job 4 Daily**: Daily 08:00 PM (Full)

## 6.2 Database Backup

Database backup strategy includes full export backups to ensure comprehensive data recovery.

- **WKGO & AIA:** Daily full export backups are performed on database servers at 18:45 daily. Backed up data is stored on the DB servers and further protected by VM backups, including replication to DR. The backup directory is `D:\backup\\` on DB servers.
- **GCIS:** Production database server on GCIS P1 performs local database backups stored locally and additionally backed up by Veeam backup server (scspbk2). GCIS also provides backup services for databases within its environment.

**Recovery:**

Recovery procedures are defined for various failure scenarios to minimize downtime. Expected recovery times are outlined below:

| # | Failure Scenario                                         | Impact                                                              | System Recovery                                  | Total down time |
|---|----------------------------------------------------------|---------------------------------------------------------------------|---------------------------------------------------|-----------------|
| 1 | System (hardware) failure of the primary database server | Production BDSCS services not available; All BDSCS users cannot use BDSCS | Pilot BDSCS needs to be setup using standby DB   | ~1 hour         |
| 2 | Electricity shortage on primary site                     | Production BDSCS services not available; All BDSCS users cannot use BDSCS | BDSCS needs to be setup using DR site             | ~half day       |
| 3 | System failure of either one of the App servers on primary site | According to the number of concurrent user, the performance may be degraded. | No effect on system availability                | N/A             |
| 4 | System failure of ALL App servers on primary site         | Production BDSCS Web services not available; ALL BDSCS Web users cannot use BDSCS | BDSCS needs to be restored using App servers VM image backup | ~half day       |
| 5 | Database connection failure since SQL database instance down | BDSCS services not available; ALL BDSCS users cannot use BDSCS       | Restart SQL database instance                    | ~1 hour         |
| 6 | Primary database crushed                                 | No impact as it will failover to the secondary database                | BDSCS needs to be setup using secondary DB       | ~1 hour         |
| 7 | System failure (hardware failure) on one of the VM servers | No impact as all VM Server is formed in cluster. If one have failure hardware failover will proceed automatically. | N/A                                               | N/A             |

---

# 7. Outstanding Items/Issues

Nil.

---

# 8. Licensed Software

\[RY Note: Items are for reference only. They are incorrect]

The following is a list of licensed software used in the LSCP system. Please refer to the software inventories in the System Manual for detailed and accurate software information.

| Item                                                                              | Amount | Expire At |
|-----------------------------------------------------------------------------------|--------|-----------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual                                            |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

\<\<\< End of document \>\>\>
```