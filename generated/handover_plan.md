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

[1. Environment Description](#environment-description)
    * [1.1 Production and UAT Environment](#production-and-uat-environment)
    * [1.2 DR Environment](#dr-environment)
[2. Purpose](#purpose)
    * [2.1 Schedule](#schedule)
    * [2.2 Verification](#verification)
[3. Documentation](#documentation)
[4. Program Source Code](#program-source-code)
[5. Administration Accounts Checklist](#administration-accounts-checklist)
[6. Backup](#backup)
    * [6.1 VM Backup](#vm-backup)
    * [6.2 Database Backup](#database-backup)
    * [6.3 Database Backup Strategy](#database-backup-strategy)
    * [6.4 Recovery](#recovery)
    * [6.5 Backup Schedule](#backup-schedule)
[7. Outstanding Items/Issues](#outstanding-itemsissues)
[8. Licensed Software](#licensed-software)
[9. Equipment Configuration](#equipment-configuration)
    * [9.1 Computer Hardware](#computer-hardware)
        * [9.1.1 Hardware Components](#hardware-components)
        * [9.1.2 Guest Servers Components](#guest-servers-components)
        * [9.1.3 Gateway and SMTPX Configuration](#gateway-and-smtpx-configuration)
        * [9.1.4 Database Configuration](#database-configuration)
        * [9.1.5 Detailed Server and Network Configurations](#detailed-server-and-network-configurations)
[10. Software Inventories](#software-inventories)
    * [10.1 Inventory of Application Programs](#inventory-of-application-programs)
    * [10.2 Inventory of System Software and Software Package](#inventory-of-system-software-and-software-package)
[11. Security and Backup](#security-and-backup)
    * [11.1 System Control](#system-control)
    * [11.2 Security](#security)
        * [11.2.1 Data Transmission Security](#data-transmission-security)
        * [11.2.2 Data Storage and Auditing Security](#data-storage-and-auditing-security)
        * [11.2.3 System Security](#system-security)
        * [11.2.4 Physical Security](#physical-security)
        * [11.2.5 Password and Group Control](#password-and-group-control)
        * [11.2.6 Control Procedure of Application User Account and Production Support Account](#control-procedure-of-application-user-account-and-production-support-account)
    * [11.3 Change Control](#change-control)
    * [11.4 Disaster Recovery](#disaster-recovery)
[12. Database Administration](#database-administration)
    * [12.1 Clean Database Transaction Logs](#clean-database-transaction-logs)
    * [12.2 Database Backup](#database-backup-admin)
    * [12.3 System Constraints and Limitations](#system-constraints-and-limitations)
[13. Log Management](#log-management)

# 1. Environment Description

## 1.1 Production and UAT Environment

Production and UAT environment:

\[an image here]

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
<th rowspan="2"></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th rowspan="3"></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th rowspan="7"></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 1.2 DR Environment

DR environment:

\[image here]

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
<th rowspan="2"></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th rowspan="7"></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

# 2. Purpose

This document is a checklist of handover materials within project scope;
and it also provides relevant information to the support maintenance
staffs who will be maintaining this system in the future. All these
deliverables should be received from system implementation team of the
Licensing Self-Certification Portal (LSCP); to the Buildings Department
(BD) of the Government of the Hong Kong Special Administrative Region
(HKSARG or the Government).

The hand-over items of this project can be summarized into the following
items:

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
| System Manual                        | ?         | ?       |
| Program Manual                       | ?         | ?       |
| Project Evaluation Report            | ?         | ?       |

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

#

Administration Accounts on LSCP

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

## 6.3 Database Backup Strategy

Beside DB server VM backup, database full export backup will be carried out as well. This type
of backup contains full database export database objects including
schemas, table structures, packages, stored procedures and data at 18:45
daily.

The daily full export backup is done on DB servers (uat-db-01,
prd-db-01, prd-db-02, dr-db-01), data stored on the DB servers?
directory: D:\backup\\

## 6.4 Recovery

The table below shows the impact, system recovery and the expected
duration before the BDSCS is resumed to normal operation when various
system failures occur.

<table>
<colgroup>
<col style="width: 5%" />
<col style="width: 31%" />
<col style="width: 26%" />
<col style="width: 20%" />
<col style="width: 15%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#</td>
<td>Failure Scenario</td>
<td>Impact</td>
<td>System Recovery</td>
<td>Total down time</td>
</tr>
<tr class="even">
<td>1</td>
<td>System (hardware) failure of the primary database server</td>
<td><p>Production BDSCS services not available;</p>
<p>All BDSCS users cannot use BDSCS</p></td>
<td>Pilot BDSCS needs to be setup using standby DB</td>
<td>~1 hour</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Electricity shortage on primary site</td>
<td><p>Production BDSCS services not available;</p>
<p>All BDSCS users cannot use BDSCS</p></td>
<td>BDSCSneeds to be setup using DR site</td>
<td>~half day</td>
</tr>
<tr class="even">
<td>3</td>
<td>System failure of either one of the App servers on primary site</td>
<td>According to the number of concurrent user, the performance may be
degraded.</td>
<td>No effect on system availability</td>
<td>N/A</td>
</tr>
<tr class="odd">
<td>4</td>
<td>System failure of ALL App servers on primary site</td>
<td><p>Production BDSCS Web services not available;</p>
<p>ALL BDSCS Web users cannot use BDSCS</p></td>
<td>BDSCS needs to be restored using App servers VM image backup</td>
<td>~half day</td>
</tr>
<tr class="even">
<td>5</td>
<td>Database connection failure since SQL database instance down</td>
<td><p>BDSCS services not available;</p>
<p>ALL BDSCS users cannot use BDSCS</p></td>
<td>Restart SQL database instance</td>
<td>~1 hour</td>
</tr>
<tr class="odd">
<td>6</td>
<td>Primary database crushed</td>
<td>No impact as it will failover to the secondary database</td>
<td>BDSCS needs to be setup using secondary DB</td>
<td>~1 hour</td>
</tr>
<tr class="even">
<td>7</td>
<td>System failure (hardware failure) on one of the VM servers</td>
<td>No impact as all VM Server is formed in cluster. If one have failure
hardware failover will proceed automatically.</td>
<td>N/A</td>
<td>N/A</td>
</tr>
</tbody>
</table>

## 6.5 Backup Schedule

|                                         |                                                 |
|-------------------------------------|-----------------------------------|
| Name                                    | Schedule                                        |
| PROD VM Backup Job 3 Daily              | Daily 12:01 AM (Full)                           |
| PROD VM Backup to Tape Job 3 Weekly     | Every Sunday 09:00 AM (Full)                    |
| PROD UAT VM Backup Job 1 Daily          | Daily 08:00 PM (Full)                           |
| PROD UAT VM Backup to Tape Job 1 Weekly | Every Sunday 06:00 AM (Full)                    |
| PROD DEV VM Backup Job 2 Daily          | Daily 10:00 PM (Full)                           |
| PROD DEV VM Backup to Tape Job 2 Weekly | Every Sunday 03:00 AM (Full)                    |
| PROD All jobs to DR Backup Copy Job 1   | After every PROD VM Backup Job 1, 2 and 3 Daily |
| DR VM Backup Job 4 Daily                | Daily 08:00 PM (Full)                           |

# 7. Outstanding Items/Issues

Nil.

# 8. Licensed Software

<span class="mark">\[RY Note: Items are for reference only. They are
incorrect]</span>

| Item                                                                              | Amount | Expire At |
|------------------------|------------------------|------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual                                            |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

# 9. Equipment Configuration

## 9.1 Computer Hardware

### 9.1.1 Hardware Components

The Configuration of Physical Server in Production

|                            |                         |                             |                |                        |
|----------------------------|-------------------------|-----------------------------|----------------|------------------------|
| **Model**                  | **Host Name**           | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750 Server | prd-scs-admin-server-01 | 192.168.10.22, 10.5.161.206 | F646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-admin-server-02 | 192.168.10.23, 10.5.161.207 | D646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-nas             | 192.168.10.35, 10.5.161.218 | ???            | ???                    |

The Configuration of SAN storage in Production

|             |                      |                |                       |                                                            |
|----------------|---------------|--------------|--------------|---------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CC    | N/A                   | 192.168.10.16                                              |
| SAN Switch  | Dell DS6610B         | FRC1924T0CD    | N/A                   | 192.168.10.17                                              |
| SAN Storage | Dell PowerStore 500T | HV1NBX3        | 11                    | 192.168.10.26, 192.168.10.27, 192.168.10.28, 192.168.10.29 |

The Configuration of Backup storage in Production

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|----------------|---------------|--------------|--------------|---------------|
| Backup Appliance | Dell DataDomain 3300 | 17XMBX3        | 15TB            | 192.168.10.20  |

The Configuration of Tape Library in Production

| **Type**     | **Model** | **Serial No.** | **No. of slots** | **IP Address** |
|--------------|-----------|----------------|------------------|----------------|
| Tape Library | Dell ML3  | 3555L3A7801YY0 | 35               | 192.168.10.20  |

The Configuration of Firewalls in Production

|               |                 |                 |                  |                |
|--------------|-------------|-------------|---------------|-----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSPri | 192.168.10.12   | 10.5.161.205    | Palo Alto PA-850 | 11901063047    |
| PA-850-SCSSec | 192.168.10.13   | 10.5.161.220    | Palo Alto PA-850 | 11901063049    |

The Configuration of switches in Production

| **Host Name** | **Internal IP** | **Model** | **Serial No.** |
|---------------|-----------------|-----------|----------------|
|               | 192.168.10.14   | Catalyst  |                |
|               | 192.168.10.15   | Catalyst  |                |

The Configuration of KVM in Production

|            |                |
|------------|----------------|
| **Model**  | **Serial No.** |
| Cyber View |                |

The Configuration of UPS in Production

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010008 | 192.168.11.20  |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010004 | 192.168.11.21  |

Hardware Components of Production Servers

<table>
<colgroup>
<col style="width: 5%" />
<col style="width: 35%" />
<col style="width: 52%" />
<col style="width: 6%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Item</strong></td>
<td><strong>Hardware Component</strong></td>
<td><strong>Configuration</strong></td>
<td><strong>Qty</strong></td>
</tr>
<tr class="even">
<td rowspan="5">1</td>
<td rowspan="5"><p>ESXi Hypervisor Server</p>
<p>(prd-scs-admin-server-01)</p></td>
<td>Dell PowerEdge R750</td>
<td>1</td>
</tr>
<tr class="odd">
<td>Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz</td>
<td>1</td>
</tr>
<tr class="even">
<td>32GB DDR4 Synchronous Registered (Buffered)</td>
<td>8</td>
</tr>
<tr class="odd">
<td>1.2TB SAS HDD</td>
<td>3</td>
</tr>
<tr class="even">
<td>ESXi 8.0.3</td>
<td>1</td>
</tr>
<tr class="odd">
<td rowspan="5">2</td>
<td rowspan="5"><p>ESXi Hypervisor Server</p>
<p>(prd-scs-admin-server-02)</p></td>
<td>Dell PowerEdge R750</td>
<td>1</td>
</tr>
<tr class="even">
<td>Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz</td>
<td>1</td>
</tr>
<tr class="odd">
<td>32GB DDR4 Synchronous Registered (Buffered)</td>
<td>8</td>
</tr>
<tr class="even">
<td>1.2TB SAS HDD</td>
<td>3</td>
</tr>
<tr class="odd">
<td>ESXi 8.0.3</td>
<td>1</td>
</tr>
<tr class="even">
<td rowspan="5">3</td>
<td rowspan="5"><p>NAS</p>
<p>(prd-scs-nas)</p></td>
<td>Dell PowerEdge R750</td>
<td>1</td>
</tr>
<tr class="odd">
<td>CPU???</td>
<td>???</td>
</tr>
<tr class="even">
<td>RAM???</td>
<td>???</td>
</tr>
<tr class="odd">
<td>HDD???</td>
<td>???</td>
</tr>
<tr class="even">
<td>Windows Server 2022</td>
<td>???</td>
</tr>
<tr class="odd">
<td rowspan="2">4</td>
<td rowspan="2"><p>SAN Switch</p>
<p>(prd-scs-sw-01)</p></td>
<td>Dell DS6610B</td>
<td>1</td>
</tr>
<tr class="even">
<td>Ports</td>
<td>16</td>
</tr>
<tr class="odd">
<td rowspan="2">5</td>
<td rowspan="2"><p>SAN Switch</p>
<p>(prd-scs-sw-02)</p></td>
<td>Dell DS6610B</td>
<td>1</td>
</tr>
<tr class="even">
<td>Ports</td>
<td>16</td>
</tr>
<tr class="odd">
<td rowspan="2">6</td>
<td rowspan="2"><p>SAN Storage</p>
<p>(PS500T-Cluster1)</p></td>
<td>Dell PS500T</td>
<td>1</td>
</tr>
<tr class="even">
<td>3.8TB NVME SSD</td>
<td>11</td>
</tr>
<tr class="odd">
<td>7</td>
<td><p>Backup Appliance</p>
<p>(prd-scs-backupstorage-01)</p></td>
<td>Dell DataDomain DD3300</td>
<td>1</td>
</tr>
<tr class="even">
<td>8</td>
<td>Tape Library</td>
<td>DELL ML3</td>
<td>1</td>
</tr>
<tr class="odd">
<td>9</td>
<td><p>Firewall</p>
<p>(PA-850-SCSPri)</p></td>
<td>Palo Alto PA 850</td>
<td>1</td>
</tr>
<tr class="even">
<td>10</td>
<td><p>Firewall</p>
<p>(PA-850-SCSSec)</p></td>
<td>Palo Alto PA 850</td>
<td>1</td>
</tr>
<tr class="odd">
<td>11</td>
<td><p>Switch</p>
<p>(???)</p></td>
<td>Cisco ???</td>
<td>1</td>
</tr>
<tr class="even">
<td>12</td>
<td><p>Switch</p>
<p>(???)</p></td>
<td>Cisco ???</td>
<td>1</td>
</tr>
<tr class="odd">
<td>13</td>
<td>KVM</td>
<td>CyberView</td>
<td>1</td>
</tr>
<tr class="even">
<td>13</td>
<td>UPS<br />
(???)</td>
<td>Vertiv? Liebert? GXT5 3000</td>
<td>1</td>
</tr>
<tr class="odd">
<td>14</td>
<td>UPS<br />
(???)</td>
<td>Vertiv? Liebert? GXT5 3000</td>
<td>1</td>
</tr>
</tbody>
</table>

Partition Configuration of Production Servers

| **Host Name**           | **Drive**       | **Capacity** | **Description**              |
|--------------------|-----------------|----------|--------------------------|
| prd-scs-admin-server-01 | local           | 2.4TB        | VMware?ESXi Operating system |
| prd-scs-admin-server-02 | local           | 2.4TB        | VMware?ESXi Operating system |
| PS500T-Cluster1         | VM_Volume01     | 20TB         | Shared pool of storage space |
| PS500T-Cluster1         | QuorumDisk-VM-1 | 2.5GB        | Shared pool of storage space |
| prd-scs-nas             | C:              | ???          | OS                           |
|                         | D:              | ???          | Data                         |

The Configuration of Physical Server in DR Site

|                           |                        |                             |                |                        |
|----------------------------|-------------------------|-----------------------------|----------------|------------------------|
| **Model**                 | **Host Name**          | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750Server | dr-scs-admin-server-01 | 192.168.20.17, 10.5.174.216 | G646RX3        | RAID-5                 |
| Dell PowerEdge R750Server | dr-scs-nas             | 192.168.20.35, 10.5.174.225 | ???            | ???                    |

The Configuration of SAN storage in DR Site

|             |                      |                |                       |                                                            |
|----------------|---------------|--------------|--------------|---------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CE    | N/A                   | 192.168.20.14                                              |
| SAN Storage | Dell PowerStore 500T | 3W1NBX3        | 11                    | 192.168.20.20, 192.168.20.21, 192.168.20.22, 192.168.20.23 |

The Configuration of Backup storage in Production

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|----------------|---------------|--------------|--------------|---------------|
| Backup Appliance | Dell DataDomain 3300 | J6XMBX3        | 15TB            | 192.168.20.25  |

The Configuration of Firewalls in DR Site

|               |                 |                 |                  |                |
|---------------|-------------|-------------|----------------|-----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSDR  | 192.168.20.12   | 10.5.174.215    | Palo Alto PA-850 | 011901063069   |

The Configuration of Switches in DR Site

|               |                 |              |                |
|---------------|-----------------|--------------|----------------|
| **Host Name** | **Internal IP** | **Model**    | **Serial No.** |
| ???           | 192.168.20.13   | Catalyst ??? | ???            |

The Configuration of UPS in DR Site

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A01000A | 192.168.20.11  |

Hardware Components of Disaster Recovery Servers

<table>
<colgroup>
<col style="width: 5%" />
<col style="width: 34%" />
<col style="width: 53%" />
<col style="width: 5%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Hardware Component</th>
<th>Configuration</th>
<th>Qty</th>
</tr>
<tr class="odd">
<th rowspan="5">1</th>
<th rowspan="5"><p>ESXi Hypervisor Server</p>
<p>(dr-scs-admin-server-01)</p></th>
<th>Dell PowerEdge R750</th>
<th>1</th>
</tr>
<tr class="header">
<th>Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz</th>
<th>1</th>
</tr>
<tr class="odd">
<th>32GB DDR4 Synchronous Registered (Buffered)</th>
<th>8</th>
</tr>
<tr class="header">
<th>1.2TB SAS HDD</th>
<th>3</th>
</tr>
<tr class="odd">
<th>ESXi 8.0.3</th>
<th>1</th>
</tr>
<tr class="header">
<th rowspan="5">2</th>
<th rowspan="5"><p>NAS</p>
<p>(dr-scs-nas)</p></th>
<th>Dell PowerEdge R750</th>
<th>1</th>
</tr>
<tr class="odd">
<th>CPU???</th>
<th>???</th>
</tr>
<tr class="header">
<th>RAM???</th>
<th>???</th>
</tr>
<tr class="odd">
<th>HDD???</th>
<th>???</th>
</tr>
<tr class="header">
<th>Windows Server 2022</th>
<th>???</th>
</tr>
<tr class="odd">
<th rowspan="2">3</th>
<th rowspan="2"><p>SAN Switch</p>
<p>(dr-scs-sw-01)</p></th>
<th>Dell DS6610B</th>
<th>1</th>
</tr>
<tr class="header">
<th>Ports</th>
<th>16</th>
</tr>
<tr class="odd">
<th rowspan="2">4</th>
<th><p>SAN Storage</p>
<p>(PS500T-Cluster2)</p></th>
<th>Dell PS500T</th>
<th>1</th>
</tr>
<tr class="header">
<th>DMZ Firewall 1 (CDPDZFW1)</th>
<th>3.8TB NVME SSD</th>
<th>11</th>
</tr>
<tr class="odd">
<th>5</th>
<th><p>Backup Appliance</p>
<p>(dr-scs-backupstorage-01)</p></th>
<th>Dell DataDomain DD3300</th>
<th>1</th>
</tr>
<tr class="header">
<th>6</th>
<th><p>Firewall</p>
<p>(PA-850-SCSPri)</p></th>
<th>Palo Alto PA 850</th>
<th>1</th>
</tr>
<tr class="odd">
<th>7</th>
<th><p>Switch</p>
<p>(???)</p></th>
<th>Cisco ???</th>
<th>1</th>
</tr>
<tr class="header">
<th>8</th>
<th>KVM</th>
<th>CyberView</th>
<th>1</th>
</tr>
<tr class="odd">
<th>9</th>
<th>UPS<br />
(???)</th>
<th>Vertiv? Liebert? GXT5 3000</th>
<th>1</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Partition Configuration of DR Servers

|                        |             |              |                              |
|--------------------|-----------------|----------|--------------------------|
| **Host Name**          | **Drive**   | **Capacity** | **Description