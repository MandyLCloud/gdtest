```markdown
--- hp_o1.md ---
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

# 

# 

# 

#  

# 1. Environment Description

Production and UAT environment:

<img src="media/image2.png" style="width:6.62605in;height:5.91667in" />

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
<tr class="odd">
<th rowspan="2">prd-scs-admin-server-01</th>
<th>prd-scs-vcenter-01</th>
<th>vCenter</th>
<th><p>192.168.10.24 /</p>
<p>10.5.161.210</p></th>
</tr>
<tr class="header">
<th>prd-scs-log-01</th>
<th>Kiwi Log Server</th>
<th><p>192.168.10.11 /</p>
<p>10.5.161.223</p></th>
</tr>
<tr class="odd">
<th rowspan="3">prd-scs-admin-server-02</th>
<th>prd-scs-backup-01</th>
<th>Veeam Backup Server</th>
<th><p>192.168.10.25 /</p>
<p>10.5.161.211</p></th>
</tr>
<tr class="header">
<th>prd-scs-esetnod32</th>
<th>NOD32 Anti-Virus Server</th>
<th><p>192.168.10.34 /</p>
<p>10.5.161.215</p></th>
</tr>
<tr class="odd">
<th>dev-scs-admin-api-01</th>
<th>API Server (DEV)</th>
<th>192.168.14.10</th>
</tr>
<tr class="header">
<th rowspan="7">prd-scs-nas</th>
<th>prd-scs-admin-api-01</th>
<th>API Server (PRD)</th>
<th>192.168.12.11</th>
</tr>
<tr class="odd">
<th>prd-scs-admin-frontend-01</th>
<th>Frontend Server (PRD)</th>
<th>192.168.12.12</th>
</tr>
<tr class="header">
<th>prd-scs-admin-backend-01</th>
<th>Backend Server (PRD)</th>
<th>192.168.12.13</th>
</tr>
<tr class="odd">
<th>prd-scs-db-01</th>
<th>Database Server (PRD)</th>
<th>192.168.12.14</th>
</tr>
<tr class="header">
<th>prd-scs-filer</th>
<th>File Server (PRD)</th>
<th>192.168.12.20</th>
</tr>
<tr class="odd">
<th>prd-scs-proxy</th>
<th>Reverse Proxy Server (PRD)</th>
<th><p>192.168.12.15 /</p>
<p>10.5.161.226</p></th>
</tr>
<tr class="header">
<th>prd-scs-admin-api-02</th>
<th>API Server (PRD)</th>
<th>192.168.12.16</th>
</tr>
<tr class="odd">
<th></th>
<th>prd-scs-admin-frontend-02</th>
<th>Frontend Server (PRD)</th>
<th>192.168.12.17</th>
</tr>
<tr class="header">
<th></th>
<th>prd-scs-admin-backend-02</th>
<th>Backend Server (PRD)</th>
<th>192.168.12.18</th>
</tr>
<tr class="odd">
<th></th>
<th>prd-scs-db-02</th>
<th>Database Server (PRD)</th>
<th>192.168.12.19</th>
</tr>
<tr class="header">
<th></th>
<th>uat-scs-admin-api-01</th>
<th>API Server (UAT)</th>
<th>192.168.13.10</th>
</tr>
<tr class="odd">
<th></th>
<th>uat-scs-admin-frontend-01</th>
<th>Frontend Server (UAT)</th>
<th>192.168.13.11</th>
</tr>
<tr class="header">
<th></th>
<th>uat-scs-admin-backend-01</th>
<th>Backend Server (UAT)</th>
<th>192.168.13.12</th>
</tr>
<tr class="odd">
<th></th>
<th>uat-scs-db-01</th>
<th>Database Server (UAT)</th>
<th>192.168.13.13</th>
</tr>
<tr class="header">
<th></th>
<th>uat-scs-filer</th>
<th>File Server (UAT)</th>
<th>192.168.13.15</th>
</tr>
<tr class="odd">
<th></th>
<th>uat-scs-proxy</th>
<th>Reverse Proxy Server (UAT)</th>
<th><p>192.168.13.14 /</p>
<p>10.5.161.224</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

DR environment:

<img src="media/image5.png" style="width:6.62605in;height:6.44444in" />

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
<tr class="odd">
<th rowspan="2">dr-scs-admin-server-01</th>
<th>dr-scs-vcenter-01</th>
<th>vCenter</th>
<th><p>192.168.20.18 /</p>
<p>10.5.174.225</p></th>
</tr>
<tr class="header">
<th>dr-scs-log-01</th>
<th>Kiwi Log Server</th>
<th>192.168.20.10</th>
<th></th>
</tr>
<tr class="odd">
<th rowspan="7">dr-scs-nas</th>
<th>dr-scs-backup-01</th>
<th>Veeam Backup Server</th>
<th><p>192.168.20.19 /</p>
<p>10.5.161.224</p></th>
</tr>
<tr class="header">
<th>dr-scs-admin-api-01</th>
<th>API Server</th>
<th>192.168.22.11</th>
<th></th>
</tr>
<tr class="odd">
<th>dr-scs-admin-frontend-01</th>
<th>Frontend Server</th>
<th>192.168.22.12</th>
<th></th>
</tr>
<tr class="header">
<th>dr-scs-admin-backend-01</th>
<th>Backend Server</th>
<th>192.168.22.13</th>
<th></th>
</tr>
<tr class="odd">
<th>dr-scs-db-01</th>
<th>Database Server</th>
<th>192.168.22.14</th>
<th></th>
</tr>
<tr class="header">
<th>dr-scs-filer</th>
<th>File Server</th>
<th>192.168.22.16</th>
<th></th>
</tr>
<tr class="odd">
<th>dr-scs-proxy</th>
<th>Reverse Proxy Server</th>
<th><p>192.168.22.15 /</p>
<p>10.5.174.228</p></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th>scspwi</th>
<th>Reverse Proxy Server (GCIS)</th>
<th><p>192.168.0.6 /</p>
<p>45.119.93.84</p></th>
</tr>
<tr class="odd">
<th></th>
<th>scspwg</th>
<th>Reverse Proxy Server (GCIS)</th>
<th><p>192.168.4.6 /</p>
<p>10.160.139.211</p></th>
</tr>
<tr class="header">
<th></th>
<th>scspad</th>
<th>Apps Server (GCIS)</th>
<th>192.168.8.6</th>
</tr>
<tr class="odd">
<th></th>
<th>scspdb</th>
<th>Database Server (GCIS)</th>
<th>192.168.8.7</th>
</tr>
<tr class="header">
<th></th>
<th>scspbk2</th>
<th>Veeam Backup Server (GCIS)</th>
<th>192.168.8.9</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

# 

#  

# 2. Purpose

This document is a checklist of handover materials within project scope;
and it also provides relevant information to the support maintenance
staffs who will be maintaining this system in the future. All these
deliverables should be received from system implementation team of the
Licensing Self-Certification Portal (LSCP); to the Buildings Department
(BD) of the Government of the Hong Kong Special Administrative Region
(HKSARG or the Government).

The hand-over items of this project can be summarized into the following
4 items:

> 1\. Documentation
>
> 2\. Program Source code (Backend Application, Frontend Web App,
> Fronted Mobile App)
>
> 3\. Administration Accounts
>
> 4\. System backup
>
> 5\. Hardware
>
> 6\. Software Packages and Licenses

## 2.1 Schedule

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |

## 2.2 Verification

1.  The application URL verification

> The access link (URL) of each application should be verified by
> performing an access checking.

1.  Login accounts verification

> The login accounts of the applications and servers should be verified
> by processing login action.

#  

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
| System Manual                        | ?         | ?       |
| Program Manual                       | ?         | ?       |
| Project Evaluation Report            | ?         | ?       |

# 

#  

# 4. Program Source Code

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |
|                      |         |           |

#  

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
<th>prd-scs-admin-server-01<br>prd-scs-admin-server-02<br>dr-scs-admin-server-01</th>
<th>192.168.10.22<br>192.168.10.23<br>192.168.20.17</th>
<th>10.5.161.206<br>10.5.161.207<br>10.5.174.216</th>
<th>vSphere Client</th>
<th>administrator@vsphere.local</th>
<th></th>
</tr>
<tr class="header">
<th>Hypervisiors</th>
<th>prd-scs-admin-server-01<br>prd-scs-admin-server-02<br>dr-scs-admin-server-01</th>
<th>192.168.10.22<br>192.168.10.23<br>192.168.20.17</th>
<th>10.5.161.206<br>10.5.161.207<br>10.5.174.216</th>
<th>ESXi Web UI, SSH</th>
<th>root</th>
<th></th>
</tr>
<tr class="odd">
<th>Windows Server</th>
<th>prd-scs-nas<br>dr-scs-nas<br>prd-scs-backup-01<br>prd-scs-log-01<br>prd-scs-esetnod32<br>prd-scs-admin-api-01<br>prd-scs-admin-api-02<br>prd-scs-admin-frontend-01<br>prd-scs-admin-frontend-02<br>prd-scs-admin-backend-01<br>prd-scs-admin-backend-02<br>prd-scs-db-01<br>prd-scs-db-02<br>prd-scs-filer<br>prd-scs-proxy<br>uat-scs-admin-api-01<br>uat-scs-admin-frontend-01<br>uat-scs-admin-backend-01<br>uat-scs-db-01<br>uat-scs-filer<br>uat-scs-proxy<br>dev-scs-admin-api-01<br>dev-scs-admin-frontend-01<br>dev-scs-admin-backend-01<br>dev-scs-db-01<br>dev-scs-filer<br>dev-scs-proxy<br>dr-scs-backup-01<br>dr-scs-log-01<br>dr-scs-admin-api-01<br>dr-scs-admin-frontend-01<br>dr-scs-admin-backend-01<br>dr-scs-db-01<br>dr-scs-filer<br>dr-scs-proxy<br>scspbk2<br>scsplog<br>scspwi<br>scspwg<br>scspad<br>scspdb<br>scsuwi<br>scsuwg<br>scsuad<br>scsudb<br>scsdwi<br>scsdwg<br>scsdad<br>scsddb</th>
<th>See Section 1</th>
<th>See Section 1</th>
<th>RDP</th>
<th>administrator</th>
<th></th>
</tr>
<tr class="header">
<th>Hypervisior Controller</th>
<th>prd-scs-vcenter-01<br>dr-scs-vcenter-01</th>
<th>192.168.10.24<br>192.168.20.18</th>
<th>10.5.161.210<br>10.5.174.225</th>
<th>vSphere Client</th>
<th>administrator@vsphere.local</th>
<th></th>
</tr>
<tr class="odd">
<th>Storage Server</th>
<th>Dell PowerStore 500T (PS500T-Cluster1, PS500T-Cluster2)<br>Dell DataDomain 3300 (prd-scs-backupstorage-01, dr-scs-backupstorage-01)</th>
<th>192.168.10.26<br>192.168.20.20<br>192.168.10.20<br>192.168.20.25</th>
<th>N/A</th>
<th>Web UI</th>
<th>admin</th>
<th></th>
</tr>
<tr class="header">
<th>Firewall</th>
<th>PA-850-SCSPri<br>PA-850-SCSSec<br>PA-850-SCSDR</th>
<th>192.168.10.12<br>192.168.10.13<br>192.168.20.12</th>
<th>10.5.161.205<br>10.5.161.220<br>10.5.174.215</th>
<th>Web UI</th>
<th>admin</th>
<th></th>
</tr>
<tr class="odd">
<th>Network Switch</th>
<th>Catalyst (192.168.10.14, 192.168.10.15, 192.168.20.13)</th>
<th>192.168.10.14<br>192.168.10.15<br>192.168.20.13</th>
<th>N/A</th>
<th>Web UI, Console</th>
<th>admin</th>
<th></th>
</tr>
<tr class="header">
<th>SQL Database</th>
<th>prd-scs-db-01<br>prd-scs-db-02<br>uat-scs-db-01<br>dev-scs-db-01<br>dr-scs-db-01<br>scspdb<br>scsudb<br>scsddb</th>
<th>See Section 1</th>
<th>See Section 1</th>
<th>SQL Management Studio</th>
<th>sa</th>
<th></th>
</tr>
<tr class="odd">
<th>Symantec Endpoint Protection Manager (SEPM) / ESET PROTECT Server</th>
<th>prd-scs-esetnod32</th>
<th>192.168.10.34</th>
<th>10.5.161.215</th>
<th>Web UI</th>
<th>administrator</th>
<th></th>
</tr>
<tr class="header">
<th>Syslog</th>
<th>prd-scs-log-01<br>dr-scs-log-01<br>scsplog</th>
<th>192.168.10.11<br>192.168.20.10<br>192.168.8.10</th>
<th>10.5.161.223<br>N/A<br>N/A</th>
<th>Web UI</th>
<th>admin</th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

# 

Administration Accounts on LSCP

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  | BDAdmin      |          |
| PRD / DR    | BD Admin  | BDAdmin      |          |
|             |           |              |          |

# 6. Backup

<span class="mark">\[RY Note: Following content needs to check\]</span>

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

# 

#  

# 7. Outstanding Items/Issues

Nil.

#  

# 8. Licensed Software

<span class="mark">\[RY Note: Items are for reference only. They are
incorrect\]</span>

| Item                                                                              | Amount | Expire At |
|------------------------|------------------------|------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual                                            |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

\<\<\< End of document \>\>\>
```