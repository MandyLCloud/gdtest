<img src="media/image3.jpg" style="width:1.30903in;height:1.30903in" />

**Disaster Recovery Plan** **(T373)**

**of**

**FOR PILOT SYSTEM OF**

**SELF-CERTIFICATION SYSTEM (SCS)**

**FOR THE**

**BUILDINGS DEPARTMENT**

Version: 0.1

**Nov 2024**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 86%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Distribution</strong></th>
</tr>
<tr class="odd">
<th>Copy No.</th>
<th>Holder</th>
</tr>
<tr class="header">
<th>1</th>
<th><blockquote>
<p>Buildings Department (BD)</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>2</th>
<th><blockquote>
<p>Master Concept (Hong Kong) Limited</p>
</blockquote></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

| **Amendment History** |                      |                                      |                           |         |                    |
|----------|-------------------------|---------|---------|---------|-----------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date    | Approval Reference |
| 1                     | First draft          | N/A                                  | 0.1                       | 6/11/24 |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |
|                       |                      |                                      |                           |         |                    |

**Table of Contents**

[**1. INTRODUCTION 1**](#introduction)

[**2. BACKUP STRATEGY 1**](#backup-strategy)

[**3. DISASTER RECOVERY PROCEDURES 2**](#disaster-recovery-procedures)

> [3.1. PREPARATION OF DR SITE 2](#preparation-of-dr-site)
>
> [3.1.1. Contact Point for Disaster Recovery
> 2](#contact-point-for-disaster-recovery)
>
> [3.1.2. Disaster Recovery Site Location
> 4](#disaster-recovery-site-location)
>
> [3.1.3. Disaster Recovery Equipment 4](#_heading=h.35nkun2)
>
> [3.2. DISASTER RECOVERY 6](#disaster-recovery)
>
> [3.2.1. Backup the VM from Production VM (Initial/One Time)
> 6](#backup-the-vm-from-production-vm-initialone-time)
>
> [3.2.2. Restore CDPSS Web Application
> 7](#restore-lscp-web-application)
>
> [3.2.3. Recovery Data & Data Files 8](#recovery-data-data-files)
>
> [3.2.4. Config DR backup Server static route and IP address
> 9](#config-dr-backup-server-static-route-and-ip-address)

[**4. PLANNING FOR DISASTER RECOVERY DRILL
9**](#planning-for-disaster-recovery-drill)

> [4.1. STAGE 0 – SITE READINESS 9](#stage-0-site-readiness)
>
> [4.1.1. Network Connection 9](#network-connection)
>
> [4.1.2. Server Status Check 10](#server-status-check)
>
> [4.2. STAGE 1 – SYSTEM ENVIRONMENT SET UP TEST
> 10](#stage-1-system-environment-set-up-test)
>
> [4.2.1. Procedure to start-up the DR DB Server
> 10](#procedure-to-start-up-the-dr-db-server)
>
> [4.2.2. Procedure to start-up the DR Web Server
> 10](#procedure-to-start-up-the-dr-web-server)
>
> [4.2.3. Procedure to start-up the DR Backend Server
> 10](#procedure-to-start-up-the-dr-backend-server)
>
> [4.2.4. Procedure to start-up the DR API Server
> 10](#procedure-to-start-up-the-dr-api-server)
>
> [4.3. STAGE 2 – APPLICATION SYSTEM TEST
> 11](#stage-2-application-system-test)
>
> [4.3.1. Procedure to test API service 11](#_heading=h.4k668n3)
>
> [4.3.2. Procedure to test Web Server 11](#_heading=h.1egqt2p)
>
> [4.3.3. Procedure to test Backend Server
> 11](#procedure-to-test-backend-portal)

[**5. CURRENT AND MINIMUM HARDWARE CAPACITY
11**](#current-and-minimum-hardware-capacity)

#  INTRODUCTION

> The Disaster Recovery Plan (DRP) defines the disaster recovery
> procedures in case the system of pilot project of self-certification
> system (SCS) for Buildings Department (BD) is being interrupted. It
> contains the information needed to post-interruption decision-making
> and the response to any disruptive or extended interruption of the
> system’s normal operations and services.
>
> This document should be updated whenever there is any change in the
> hardware, software, operation procedure, and responsible party of the
> system. Moreover, regular drill should be conducted to ensure the
> procedures are correct and workable and this document should be
> reviewed after every Disaster Recovery (DR) drill.

# BACKUP STRATEGY

> Offsite backup is the process of transferring data from primary site
> to a separate storage device, i.e. de-duplicated backup disk at DR
> site. If the original data is lost or damaged, the data restoration
> from the backup disk could help the system switch the operation to DR
> site to sustain the service at an acceptable degraded level.
>
> The backup includes following:

-   Data; and

-   Data File (e.g. supporting document of Form A, Form B or Quality
    > Supervision Form, Generated report)

> Application backup is not necessary, because the application
> installation or update will be installed on both Production and DR
> sites every single time.

1.   <span class="smallcaps">DATA BACKUP</span>

> At least two types of data should be backed up. They are:

-   Database

-   Data File

> The data stored in the MSSQL will be stored in local storage and copy
> through Veeam to DR site by scheduler and script setup on Production
> server

1.    
    <span class="smallcaps">SYSTEM BACKUP</span>

> As the system should not have many changes regularly, it is
> recommended to perform a full system image backup after any system
> patching.
>
> Backup will be run by Veeam and backup to SAN storage. Veeam
> Replication will be run from SAN storage to Dell Data Domain to store
> the SAN data. There is also a weekly backup job to backup data to
> tape.
>
> The following system image of servers will be backup:
>
> prd-scs-log-01
>
> prd-scs-esetnod32
>
> prd-scs-proxy
>
> prd-scs-filer
>
> prd-scs-admin-api-01
>
> prd-scs-admin-frontend-01
>
> prd-scs-admin-backend-01
>
> prd-scs-db-01
>
> prd-scs-admin-api-02
>
> prd-scs-admin-frontend-01
>
> prd-scs-admin-backend-02
>
> prd-scs-db-02
>
> scspad
>
> scspdb
>
> scsplog
>
> scspwg
>
> scspwi

# DISASTER RECOVERY PROCEDURES

##  PREPARATION OF DR SITE

###  Contact Point for Disaster Recovery

> The following is the list of contact point for disaster recovery of
> SCS:

| **Role**              | **Department** | **Contact Point** | **Contact No. at office hours** | **Contact No. after office hour** |
|-----------------|------------|---------------|-------------|-----------------|
| Chief DR Commander    | BD             |                   |                                 |                                   |
| Business DR Commander | BD             |                   |                                 |                                   |
| End-user Coordinator  | BD             |                   |                                 |                                   |
| Project Team          | MCI            | Harry             | +852 9092 7057                  | +852 9092 7057                    |
| Project Team          | MCI            | Harry             | +852 9092 7057                  | +852 9092 7057                    |

<img src="media/image5.png" style="width:6.62605in;height:6.44444in" />

### Disaster Recovery Site Location

BD Headquarters (BDHQ), North Tower, West Kowloon Government Offices
(WKGO), 11 Hoi Ting Road, Yau Ma Tei, Kowloon

AIA DR Site

**Disaster Recovery Equipment**

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 20%" />
<col style="width: 10%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Role</strong></th>
<th><strong>Host Name</strong></th>
<th><strong>vCPU</strong></th>
<th><strong>RAM<br />
(GB)</strong></th>
<th><strong>Disk<br />
(GB)</strong></th>
<th><strong>IP Addresses</strong></th>
<th><strong>Data Center</strong></th>
<th><strong>Host Server / Zone</strong></th>
</tr>
<tr class="odd">
<th>vCenter</th>
<th>dr-scs-<br />
vcenter-01</th>
<th>16</th>
<th>39</th>
<th>1.33TB</th>
<th><p>192.168.20.18 /</p>
<p>10.5.174.225</p></th>
<th>AIA</th>
<th>dr-scs-admin-<br />
server-01</th>
</tr>
<tr class="header">
<th>Veeam Backup Server</th>
<th>dr-scs-<br />
backup-01</th>
<th>8</th>
<th>24</th>
<th><p>300 +</p>
<p>1TB</p></th>
<th><p>192.168.20.19 /</p>
<p>10.5.161.224</p></th>
<th>AIA</th>
<th>dr-scs-admin-<br />
server-01</th>
</tr>
<tr class="odd">
<th>Kiwi Log<br />
Server</th>
<th>dr-scs-<br />
log-01</th>
<th>4</th>
<th>8</th>
<th><p>300 +</p>
<p>500</p></th>
<th>192.168.20.10</th>
<th>AIA</th>
<th>dr-scs-admin-<br />
server-01</th>
</tr>
<tr class="header">
<th>API<br />
Server</th>
<th>dr-scs-<br />
admin-<br />
api-01</th>
<th>2</th>
<th>8</th>
<th>90</th>
<th>192.168.22.11</th>
<th>AIA</th>
<th>dr-scs-admin-<br />
server-01</th>
</tr>
<tr class="odd">
<th>Frontend<br />
Server</th>
<th>dr-scs-<br />
admin-<br />
frontend-01</th>
<th>2</th>
<th>8</th>
<th>90</th>
<th>192.168.22.12</th>
<th>AIA</th>
<th>dr-scs-admin-<br />
server-01</th>
</tr>
<tr class="header">
<th>Backend<br />
Server</th>
<th>dr-scs-<br />
admin-<br />
backend-01</th>
<th>2</th>
<th>8</th>
<th>90</th>
<th>192.168.22.13</th>
<th>AIA</th>
<th>dr-scs-admin-<br />
server-01</th>
</tr>
<tr class="odd">
<th>Database<br />
Server</th>
<th>dr-scs-<br />
db-01</th>
<th>2</th>
<th>8</th>
<th><p>90 +</p>
<p>500</p></th>
<th>192.168.22.14</th>
<th>AIA</th>
<th>dr-scs-admin-<br />
server-01</th>
</tr>
<tr class="header">
<th>File<br />
Server</th>
<th>dr-scs-<br />
filer</th>
<th>2</th>
<th>8</th>
<th><p>90 +</p>
<p>1TB</p></th>
<th>192.168.22.16</th>
<th>AIA</th>
<th>dr-scs-admin-<br />
server-01</th>
</tr>
<tr class="odd">
<th>Reverse<br />
Proxy<br />
Server</th>
<th>dr-scs-<br />
proxy</th>
<th>2</th>
<th>4</th>
<th>90</th>
<th><p>192.168.22.15 /</p>
<p>10.5.174.228</p></th>
<th>AIA</th>
<th>dr-scs-admin-<br />
server-01</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

<u>GCIS environment</u>

Because of the DR nature of GCIS (P1/P2 architecture), no physical
hardware is used for DR.

##  DISASTER RECOVERY

### Backup the VM from Production VM (Initial/One Time)

The DR’s VMs will be installed and configured via restore related VM
snapshot of Production on LSCP Backup Server via Veeam.

> <img src="media/image1.png" style="width:4.65625in;height:2.27083in" />  
>   
> Backup list:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><blockquote>
<p>Production VM</p>
</blockquote></th>
<th>DR VM</th>
</tr>
<tr class="odd">
<th>vCenter</th>
<th>prd-scs-vcenter-01</th>
<th>dr-scs-vcenter-01</th>
</tr>
<tr class="header">
<th>Proxy</th>
<th>prd-scs-proxy</th>
<th>dr-scs-proxy</th>
</tr>
<tr class="odd">
<th>Kiwi Log Servers</th>
<th>prd-scs-log-01</th>
<th>dr-scs-log-01</th>
</tr>
<tr class="header">
<th>File Server</th>
<th>prd-scs-filer</th>
<th>dr-scs-filer</th>
</tr>
<tr class="odd">
<th>Application Server</th>
<th><p>prd-scs-admin-frontend-01</p>
<p>prd-scs-admin-frontend-02</p></th>
<th><p>dr-scs-admin-frontend-01</p>
<p>dr-scs-admin-frontend-02</p></th>
</tr>
<tr class="header">
<th>API Server</th>
<th><p>prd-scs-admin-api-01</p>
<p>prd-scs-admin-api-02</p></th>
<th><p>dr-scs-admin-api-01</p>
<p>dr-scs-admin-api-01</p></th>
</tr>
<tr class="odd">
<th>Backend Server</th>
<th><p>prd-scs-admin-backend-01</p>
<p>prd-scs-admin-backend-02</p></th>
<th><p>dr-scs-admin-backend-01</p>
<p>dr-scs-admin-backend-02</p></th>
</tr>
<tr class="header">
<th><p>Database</p>
<p>Server (SQL Server) 1</p></th>
<th><p>prd-scs-db-01</p>
<p>prd-scs-db-02</p></th>
<th><p>dr-scs-db-01</p>
<p>dr-scs-db-02</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> <u>GCIS</u>
>
> The servers in Production VM and DR VM are the same but in P1 and P2
> respectively. Please refer to **<u>System Manual</u>**.

### Restore LSCP Web Application

> <u>As DR VM servers will be keep to available on DR site in parallel
> with Production, every new application updates will be deployed to
> production VM and DR VM in same time</u>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Frontend Website Application for public users</th>
<th><blockquote>
<p>scspad (GCIS P1)</p>
</blockquote></th>
<th>scspad (GCIS P2)</th>
</tr>
<tr class="odd">
<th>Backend Application</th>
<th><blockquote>
<p>prd-scs-admin-frontend-01<br />
prd-scs-admin-frontend-02</p>
</blockquote></th>
<th>dr-scs-admin-frontend-01<br />
dr-scs-admin-frontend-02</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

<u>GCIS</u>

<span class="mark">GCIS DR will perform by GCIS and we just need check
the url and data after DR or Drill. The link will be
[<u>www1.scs.bd.gov.hk</u>](http://www1.scs.bd.gov.hk)</span>

###  Recovery Data & Data Files

The Database BAK file will be daily backup and copied from production to
DR site by Scheduler and programming script.

The Data File (e.g. supporting documents and submission forms) files
will be daily batch backup from production to DR site by Scheduler and
programming script.

The backup database and data files will be stored on PRD ( D:\backup)

via Veeam copy to DR VM & Path (D:\backup), it will be manual restored
if need to setup DR

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 22%" />
<col style="width: 16%" />
<col style="width: 21%" />
<col style="width: 18%" />
</colgroup>
<thead>
<tr class="header">
<th><blockquote>
<p>Server</p>
</blockquote></th>
<th><blockquote>
<p>Production VM</p>
</blockquote></th>
<th>Copy to</th>
<th>Restore to DR VM</th>
<th>Files</th>
</tr>
<tr class="odd">
<th>File Server</th>
<th>prd-scs-filer</th>
<th>D:\backup</th>
<th>D:\backend\upload (dr-scs-filer)</th>
<th>Data File (e.g. supporting documents and submission forms)</th>
</tr>
<tr class="header">
<th>Database Server (SQL Server)</th>
<th><p>prd-scs-db-01</p>
<p>prd-scs-db-02</p></th>
<th>D:\backup</th>
<th>dr-scs-db-01</th>
<th>SQL Server Database BAK</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Restore sql server database from .bak file Using SQL-Server Management
Studio

1.  Connect to your SQL Server, right-click on the “Databases”
    > directory, and choose “Restore Database”

> <img src="media/image4.png" style="width:6.05292in;height:2.7124in" />

1.  Click the button beneath the “Source” section next to “Device”

2.  In the “Select backup device” press “Add”

3.  Select the backup file or files (.bak) you are going to restore,
    > then click “OK”

4.  In the “Restore Database” window specify the database’s name you
    > will restore and click “OK” to start

> <img src="media/image2.png" style="width:4.47257in;height:2.64834in"
> alt="ssms restore options" />

### Config DR backup Server static route and IP address

The DR’s VMs will be installed and configured and parallel run with
below URL and IP.

DR URL
[<u>www1.<span class="mark">scs.bd.ccgo.hksarg</span></u>](http://www1.scs.bd.ccgo.hksarg)

IP 10.5.174.245

No DNS required for additional configuration for DR restore, just notice
users to use DR URL to visit DR web application.

<u>GCIS</u>

The DR’s VMs will be installed and configured and parallel run with
below URL and IP.

DR URL
[<span class="mark">www1.scs.bd.gov.hk</span>](http://www1.scs.bd.gov.hk)

IP 172.21.131.38

No DNS required for additional configuration for DR restore, just notice
users to use DR URL to visit DR web application.

# PLANNING FOR DISASTER RECOVERY DRILL

##  STAGE 0 – SITE READINESS

### Network Connection

1.  Make sure all switches are powered on.

2.  Make sure all network cables are connected properly.

3.  Try reset the switch by unplug and reconnect power if the above
    > procedure didn’t help.

### Server Status Check

1.  Login to the DR servers by sharepoint administrator account.

2.  Open “Event Viewer” inside “Programs 🡪 Administration Tools”.

3.  Check all the “Warning” and “Error” logs.

> 4\. Report to SM&S contractor for any warnings and errors found to see
> if they have adverse impacts to CDPSS.

##  STAGE 1 – SYSTEM ENVIRONMENT SET UP TEST

###  Procedure to start-up the DR DB Server 

1.  After Power on the server, make sure the below service is in a
    > “Running” state

> “SQL Server (MSSQLSERVER)”

### Procedure to start-up the DR Web Server

1.  After Power on the server, make sure the below service is in a
    > “Running” state

> “Office Online”

1.  If the service is not in a “Running” state, start the service
    > manually.

### Procedure to start-up the DR Backend Server

1.  After Power on the server, make sure the below service is in a
    > “Running” state

> “Office Online”

1.  If the service is not in a “Running” state, start the service
    > manually.

### Procedure to start-up the DR API Server

1.  After Power on the server, make sure the below service is in a
    > “Running” state

> “Office Online”

1.  If the service is not in a “Running” state, start the service
    > manually.

##  STAGE 2 – APPLICATION SYSTEM TEST

###  Procedure to test Frontend (GCIS)

1.  Before the DR test date, create a record in the frontend

2.  On DR day, check both
    > [<u>https://www2.scs.bd.gov.hk/</u>](https://cdpssdr.bd.gov.hk/)
    > and
    > [<u>https://www2.scs.bd.gov.hk/api</u>](https://www2.scs.bd.gov.hk/api)
    > are accessible

3.  Check if the record from 1. exists in those environments

### Procedure to test Backend Portal

On DR day, make sure the LSCP backend can be accessed by: {backend
domain} or {OSDP}

# CURRENT AND MINIMUM HARDWARE CAPACITY

> Please refer to the following document:

-   Site Specification; and

-   System Manual
