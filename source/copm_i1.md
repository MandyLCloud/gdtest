<img src="media/image9.jpg" style="width:1.30903in;height:1.30903in"
alt="bd_logo" />

**COMPUTER OPERATION PROCEDURE MANUAL**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">COMBINED SYSTEM DEVELOPMENT SERVICES</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**<span class="smallcaps">  
OF</span>**

**<span class="smallcaps">BUILDINGS DEPARTMENT</span>**

**Version: 0.1**

**  
Jan 2025**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR.

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 80%" />
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
<p>Master Concept (Hong Kong) Limited (MC)</p>
</blockquote></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

| **Amendment History** |                      |                                      |                           |            |
|---------|---------------------|--------------------|------------|-----------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date       |
| 1                     | 1st draft            | All                                  | 0.1                       | 16/01/2025 |
|                       |                      |                                      |                           |            |
|                       |                      |                                      |                           |            |

**TABLE OF CONTENTS**

[1. Purpose 5](#purpose)

[2. Scope 6](#scope)

[3. Reference 7](#reference)

[4. Definitions and Conventions 8](#definitions-and-conventions)

> [4.1 Definitions 8](#definitions)
>
> [4.2 Conventions 9](#conventions)
>
> [4.3 System Information 12](#system-information)
>
> [4.4 Hardware Components Description
> 17](#hardware-components-description)
>
> [4.5 System Software Environment 20](#system-software-environment)
>
> [4.6 System Software Licensing 26](#system-software-licensing)
>
> [4.7 Communication Network Configuration
> 28](#communication-network-configuration)
>
> [4.7.1 IP Address for Internet Production Environment
> 28](#ip-address-for-internet-production-environment)

[5. Computer System Operating Procedure
29](#computer-system-operating-procedure)

> [5.1 Shutdown Procedure Including Network Devices (Production & UAT)
> 29](#shutdown-procedure-including-network-devices-production-uat)

[6. Health Check 33](#health-check)

[7. Operation Housekeeping Jobs 33](#operation-housekeeping-jobs)

> [7.1 Recover Database and Control File Backup from VM
> 34](#recover-database-and-control-file-backup-from-vm)

[8. Configurations 35](#configurations)

> [8.1 External Firewall 35](#external-firewall)

[9. Deployment Guides 48](#deployment-guides)

> [9.1 Deploying LSCP Web 48](#deploying-lscp-web)
>
> [9.2 Deploy Mobile App 49](#deploy-mobile-app)

#  

# 1. Purpose

The Computer Operating Procedures Manual (COPM) provides information and
operating instructions related to the operation of the computer system.
The intended users are the operating staff of the relevant section.

This manual is not intended to be a complete replacement of the formal
technical publication as issued by the manufacturer. However,
information and instructions documented in the manual would be specific
to the installation and should take precedence over the manufacturer’s
counterparts or details.

#  

# 2. Scope

This document is to be used as a guide for operating the system. It
addresses the tasks that need to be monitored by the administrator to
make sure that the system is functioned properly.

#  

# 3. Reference

-   System Installation Plan

-   Application Operation Manual

# 4. Definitions and Conventions 

## 4.1 Definitions

None.

##  

## 4.2 Conventions

## 

The following acronyms are used in the text of this document:

<table>
<colgroup>
<col style="width: 57%" />
<col style="width: 42%" />
</colgroup>
<thead>
<tr class="header">
<th><blockquote>
<p>Abbreviation</p>
</blockquote></th>
<th><blockquote>
<p>Description</p>
</blockquote></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>BD</p>
</blockquote></th>
<th>Buildings Department</th>
</tr>
<tr class="header">
<th><blockquote>
<p>WKGO</p>
</blockquote></th>
<th>West Kowloon Government Offices</th>
</tr>
<tr class="odd">
<th><blockquote>
<p>AIA</p>
</blockquote></th>
<th>Building Department office at AIA tower</th>
</tr>
<tr class="header">
<th><blockquote>
<p>ISCCA</p>
</blockquote></th>
<th>Intranet Server Certificate Certification Authority </th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Computer System Information

Hardware and Computer Hardware Configuration. The following diagram
illustrates the architecture of LSCP for production site and UAT site.

The following diagram illustrates the architecture of LSCP for
Production site and UAT site in another perspective.

\[TODO\]

The internet connection is provided by an ISP Router

\[TODO\]

The setup is similar to the production and UAT site, but with one VM
host server in the DMZ and trusted zone, and the role of SAN Storage is
taken over by the Backup Server.

The diagram below illustrates the physical setup.

A site-to-site connection network is available, which allows SAN storage
and backup server to transfer incremental data backup from production
site to DR site, and recover data in opposite direction upon restoration
from DR site.  

##  

## 4.3 System Information 

System Information of Production Servers

| Item | Role Description   | Item Description (e.g. Brand name, model no., etc.) | Hostname / ID / Tag | IP  |
|-----|----------------|----------------------|---------------|---------------|
| 1    | Web Server         |                                                     |                     |     |
| 2    | Web Server         |                                                     |                     |     |
| 3    | vCenter            |                                                     |                     |     |
| 4    | Log server         |                                                     |                     |     |
| 5    | Anti-Virus server  |                                                     |                     |     |
| 6    | Application Server |                                                     |                     |     |
| 7    | Application Server |                                                     |                     |     |
| 8    | Web Server         |                                                     |                     |     |
| 9    | Web Server         |                                                     |                     |     |
| 10   | Database Server    |                                                     |                     |     |
| 11   | Database Server    |                                                     |                     |     |

System Information of DR Servers

| Item | Role Description | Item Description (e.g. Brand name, model no., etc.) | Hostname / ID / Tag | IP  |
|------|----------------|----------------------|---------------|--------------|
|      |                  |                                                     |                     |     |
|      |                  |                                                     |                     |     |

System Information of UAT Servers

| Item | Role Description | Item Description (e.g. Brand name, model no., etc.) | Hostname / ID / Tag | IP  |
|-----|-----------------|-----------------------|---------------|--------------|
|      |                  |                                                     |                     |     |
|      |                  |                                                     |                     |     |
|      |                  |                                                     |                     |     |
|      |                  |                                                     |                     |     |

Partition Configuration of Production Servers

| Host Name | Drive | Capacity | Description |
|-----------|-------|----------|-------------|
|           |       |          |             |
|           |       |          |             |
|           |       |          |             |
|           |       |          |             |
|           |       |          |             |
|           |       |          |             |
|           |       |          |             |
|           |       |          |             |
|           |       |          |             |

Partition Configuration of Production VM Guests

| Name | Drive | Capacity | Usage |
|------|-------|----------|-------|
|      |       |          |       |
|      |       |          |       |
|      |       |          |       |
|      |       |          |       |
|      |       |          |       |

Partition Configuration of DR Servers

| Host Name | Drive | Capacity | Usage |
|-----------|-------|----------|-------|
|           |       |          |       |
|           |       |          |       |
|           |       |          |       |
|           |       |          |       |
|           |       |          |       |

Partition Configuration of DR VM Guests

| Server Name | Drive | Capacity | Usage |
|-------------|-------|----------|-------|
|             |       |          |       |
|             |       |          |       |
|             |       |          |       |
|             |       |          |       |
|             |       |          |       |

RAID Configuration of Production and UAT

| Volume name | Volume capacity | Raid Type | HOSTNAME | Used by |
|-------------|-----------------|-----------|----------|---------|
|             |                 |           |          |         |
|             |                 |           |          |         |
|             |                 |           |          |         |
|             |                 |           |          |         |
|             |                 |           |          |         |
|             |                 |           |          |         |
|             |                 |           |          |         |

##  

## 4.4 Hardware Components Description

Hardware Components of Production Servers

| Item | Hardware Component | Configuration | Qty |
|------|--------------------|---------------|-----|
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |

Hardware Components of Disaster Recovery Servers

| Item | Hardware Component | Configuration | Qty |
|------|--------------------|---------------|-----|
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |
|      |                    |               |     |

## 4.5 System Software Environment

System Software of Production

| Machine | Hostname | Software |
|---------|----------|----------|
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |
|         |          |          |

\*VMware vSphere is a suite of software components for virtualization.
These include ESXi, vCenter Server, and other software components such
as vCenter Single Sign-On, and vCenter Server plug-ins that fulfill
several different functions in the vSphere environment.

https://docs.VMware .com/en/VMware
-vSphere/8.0/vsphere-vcenter-esxi-management/GUID-B3A1A79B-EF9B-4C10-A053-D54D88254C52.html

Production

| Item | Software Component | Qty |
|------|--------------------|-----|
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |
|      |                    |     |

System Software of DR

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 15%" />
<col style="width: 60%" />
</colgroup>
<thead>
<tr class="header">
<th>Machine</th>
<th>Hostname</th>
<th>Software</th>
</tr>
<tr class="odd">
<th>Kiwi Log Servers</th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>Antivirus Server</th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th><p>DR Web Server</p>
<p>(Static Content) 1</p></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th><p>DR Web</p>
<p>Application Server 1</p></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>DR BD Web Server 1</th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th><p>DR Database</p>
<p>Server (SQL Server) 1</p></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>Backup Server</th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>vCenter Server</th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>VM Host</th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>VM Host</th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

\*VMware vSphere is a suite of software components for virtualization.
These include ESXi, vCenter Server, and other software components such
as vCenter Single Sign-On, and vCenter Server plug-ins that fulfill
several different functions in the vSphere environment.

https://docs.VMware .com/en/VMware
-vSphere/8.0/vsphere-vcenter-esxi-management/GUID-B3A1A79B-EF9B-4C10-A053-D54D88254C52.html

DR

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 54%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><blockquote>
<p>Item No.</p>
</blockquote></th>
<th><blockquote>
<p>Description</p>
</blockquote></th>
<th><blockquote>
<p>Quantity</p>
</blockquote></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>1</p>
</blockquote></th>
<th>Windows Server 2019 Standard</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>2</p>
</blockquote></th>
<th>Symantec Endpoint Protection</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>3</p>
</blockquote></th>
<th>SolarWinds Event Log Forwarder for Windows 1.2</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>4</p>
</blockquote></th>
<th>VMware Tools 12</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>5</p>
</blockquote></th>
<th>SQL Server 2022</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>6</p>
</blockquote></th>
<th>Kiwi Syslog Server 9.8.1</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>7</p>
</blockquote></th>
<th>SQL Server Compact 4</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>8</p>
</blockquote></th>
<th>Symantec Endpoint Protection Manager version 14</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>9</p>
</blockquote></th>
<th>vCenter 8.0.2</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>10</p>
</blockquote></th>
<th>SQL Server Management Studio</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>11</p>
</blockquote></th>
<th>Microsoft SQL Server 2017 (64-bit)</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>12</p>
</blockquote></th>
<th>Veeam Backup &amp; Replication Server 12</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>13</p>
</blockquote></th>
<th>Dell EMC OpenManage Systems Management Software (64-Bit) 10</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>14</p>
</blockquote></th>
<th>Git 2.41</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>15</p>
</blockquote></th>
<th>VMware vSphere 8</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>16</p>
</blockquote></th>
<th>IIS 10.0.17763.1</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>17</p>
</blockquote></th>
<th>IIS 6.0</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>18</p>
</blockquote></th>
<th>Microsoft ASP.NET Core 6.0.23 Shared Framework (x86)
6.0.23.23480</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>19</p>
</blockquote></th>
<th>Microsoft ASP.NET Core 6.0.21 Shared Framework (x64)
6.0.21.23364</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>20</p>
</blockquote></th>
<th>Microsoft ASP.NET Core Module V2 16.0.23196.0</th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

System Software of UAT

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 16%" />
<col style="width: 60%" />
</colgroup>
<thead>
<tr class="header">
<th>Machine</th>
<th>Hostname</th>
<th>Software</th>
</tr>
<tr class="odd">
<th><p>UAT Web Server</p>
<p>(Static Content)</p></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th><p>UAT Web</p>
<p>Application Server</p></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>UAT BD Web Server</th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>UAT Database Server (SQL Server)</th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 54%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><blockquote>
<p>Item No.</p>
</blockquote></th>
<th><blockquote>
<p>Description</p>
</blockquote></th>
<th><blockquote>
<p>Quantity</p>
</blockquote></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>1</p>
</blockquote></th>
<th>Windows Server 2019</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>2</p>
</blockquote></th>
<th>SQL Server 2022</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>3</p>
</blockquote></th>
<th>Symantec Endpoint Protection</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>4</p>
</blockquote></th>
<th>SolarWinds Event Log Forwarder for Windows 1.2</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>5</p>
</blockquote></th>
<th>VMware Tools 12</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>6</p>
</blockquote></th>
<th>SQL Server Management Studio</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>7</p>
</blockquote></th>
<th>Git 2.41</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>8</p>
</blockquote></th>
<th>Bonobo Git Server 6.5</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>9</p>
</blockquote></th>
<th>IIS 10.0.17763.1</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>10</p>
</blockquote></th>
<th>IIS 6.0</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>11</p>
</blockquote></th>
<th>Microsoft ASP.NET Core 6.0.23 Shared Framework (x86)
6.0.23.23480</th>
<th></th>
</tr>
<tr class="header">
<th><blockquote>
<p>12</p>
</blockquote></th>
<th>Microsoft ASP.NET Core 6.0.21 Shared Framework (x64)
6.0.21.23364</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>13</p>
</blockquote></th>
<th>Microsoft ASP.NET Core Module V2 16.0.23196.0</th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Framework using during development

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 54%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><blockquote>
<p>1</p>
</blockquote></th>
<th>Angular 14.1.1 (web frontend)</th>
<th></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>2</p>
</blockquote></th>
<th>Flutter (mobile apps)</th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 4.6 System Software Licensing

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 7%" />
<col style="width: 70%" />
</colgroup>
<thead>
<tr class="header">
<th>Product</th>
<th>Quantity</th>
<th>Description</th>
</tr>
<tr class="odd">
<th>Windows Server 2022 Standard</th>
<th></th>
<th><p>2 VM guests share 1 license, Physical machine requires 1
license.</p>
<p>DMZ VM Host 1 – prd-ext-web-01</p>
<p>DMZ VM Host 2 – prd-ext-web-02, uat-web-01</p>
<p>VM Host 1 - prd-webapp-01, prd-bdweb-01, prd-db-01, prd-log-01,
prd-av-01</p>
<p>VM host 2 – prd-webapp-02, prd-bdweb-02, prd-db-02, uat-webapp-01,
uat-bdweb-01, uat-db-01</p>
<p>DR DMZ VM Host – dr-ext-web-01</p>
<p>DR VM Host – dr-webapp-01, dr-bdweb-01, dr-db-01, dr-log-01,
dr-av-01</p>
<p>(total 20 windows VM Guests / 2) + 2 physical backup server -
CDPPNBK1, CDPDNBK1= 12</p></th>
</tr>
<tr class="header">
<th>SQL Server Standard 2022 - 2 core pack</th>
<th></th>
<th><p>4 vCPU in prd-db-01, 4 vCPU in prd-db-02, 4 vCPU in dr-db-01 = 12
cores</p>
<p>(Since uat-bd-01 located in same host with prd-db-02, so no licenses
requires)</p></th>
</tr>
<tr class="odd">
<th>Symantec Endpoint Protection (3-year)</th>
<th></th>
<th><p>All VM guest in Production, UAT, DR and 2 backup servers in
production and DR requires Symantec Endpoint Protection</p>
<p>prd-ext-web-01, prd-ext-web-02, prd-webapp-01, prd-webapp-02,
prd-bdweb-01,</p>
<p>prd-bdweb-02, prd-db-01, prd-db-02, prd-log-01, prd-av-01</p>
<p>uat-web-01, uat-webapp-01, uat-bdweb-01, uat-db-01</p>
<p>dr-ext-web-01, dr-webapp-01, dr-bdweb-01, dr-db-01, dr-log-01,
dr-av-01</p>
<p>CDPPNBK1, CDPDNBK1</p>
<p>(total 22 windows instances) + 2 Symantec Endpoint Protection manger
installed on prd-av-01, dr-av-01</p></th>
</tr>
<tr class="header">
<th>Kiwi syslog server (3-year maintenance)</th>
<th></th>
<th>Production and DR environment got a log server with Kiwi syslog
server installed respectively – prd-log-01, dr-log-01</th>
</tr>
<tr class="odd">
<th>VMware vSphere 8 Standard for 1 processor (3-year support)</th>
<th></th>
<th>Assigned to Production environment, 1 host requires 2 licenses, 4
hosts – CDPPZVM1, CPDDZVM2, CDPPNVM3, CDPPNVM4</th>
</tr>
<tr class="header">
<th>VMware vSphere 8 Essential Kit for 3 hosts (3-year support)</th>
<th></th>
<th>Assigned to DR environment vCenter - drvcsa01 and 2 hosts CDPDZVM1,
CDPDNVM2</th>
</tr>
<tr class="odd">
<th>VMware vCenter Server 8 Standard for vSphere 8 (Per instance)
(3-year support)</th>
<th></th>
<th>Assigned to Production environment vCenter - prdvcsa01</th>
</tr>
<tr class="header">
<th>Veeam Availability Suite Universal Perpetual (10 instance) (3-year
support)</th>
<th></th>
<th><p>It requires to backup all VM guest + 2 vCenter instance in
Production and DR environment</p>
<p>prd-ext-web-01, prd-ext-web-02, prd-webapp-01, prd-webapp-02,
prd-bdweb-01,</p>
<p>prd-bdweb-02, prd-db-01, prd-db-02, prd-log-01, prd-av-01</p>
<p>uat-web-01, uat-webapp-01, uat-bdweb-01, uat-db-01</p>
<p>dr-ext-web-01, dr-webapp-01, dr-bdweb-01, dr-db-01, dr-log-01,
dr-av-01</p>
<p>(total 20 VM guest + 2 vCenter = 22 instances to support, so 3
licenses required)</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 4.7 Communication Network Configuration

### 4.7.1 IP Address for Internet Production Environment

Public IP address: 202.130.119.91

Public Domain Name: LSCP.bd.gov.hk

SMTP server Public IP address / DNS:smtpx.cis.hksarg

| Gateway | Subnet | IP Range | Zone |
|---------|--------|----------|------|
|         |        |          |      |
|         |        |          |      |
|         |        |          |      |

The Configuration of Internal Firewalls

| Host Name | Internal IP | External IP | Model | Serial No. | Zone |
|-----------|-------------|-------------|-------|------------|------|
|           |             |             |       |            |      |
|           |             |             |       |            |      |

The Configuration of DMZ Firewalls

| Host Name | Internal IP | External IP | Model | Serial No. | Zone |
|-----------|-------------|-------------|-------|------------|------|
|           |             |             |       |            |      |
|           |             |             |       |            |      |

The Configuration of Internal switches

| Host Name | Internal IP | Model | Serial No. | Zone |
|-----------|-------------|-------|------------|------|
|           |             |       |            |      |

The Configuration of DMZ switches

| Host Name | Internal IP | Model | Serial No. | Zone |
|-----------|-------------|-------|------------|------|
|           |             |       |            |      |

The Configuration of KVM

| Internal IP | Model | Serial No. |
|-------------|-------|------------|
|             |       |            |

The Configuration of storage

| Storage Type | Model | Serial No. | No. of hard disks | IP Address |
|--------------|-------|------------|-------------------|------------|
|              |       |            |                   |            |

The Configuration of UPS in Production

| Model | Serial No. | IP Address |
|-------|------------|------------|
|       |            |            |
|       |            |            |

#  

# 5. Computer System Operating Procedure

## 5.1 Shutdown Procedure Including Network Devices (Production & UAT)

Shutdown all guest VM excluding vCenter

Prerequisite RDP and do the following step

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><ol type="1">
<li><p>[TODO]</p></li>
</ol></th>
</tr>
<tr class="odd">
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Shutdown all ESXi host

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><ol type="1">
<li><p>[TODO]</p></li>
</ol></th>
</tr>
<tr class="odd">
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Shutdown SAN storage

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><ol type="1">
<li><p>[TODO]</p></li>
</ol></th>
</tr>
<tr class="odd">
<th></th>
</tr>
<tr class="header">
<th></th>
</tr>
<tr class="odd">
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Save DMZ and internal switches configuration

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><ol type="1">
<li><p>TODO</p></li>
</ol></th>
</tr>
<tr class="odd">
<th></th>
</tr>
<tr class="header">
<th></th>
</tr>
<tr class="odd">
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Shutdown external firewall

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><ol type="1">
<li><p>TODO</p></li>
</ol></th>
</tr>
<tr class="odd">
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Shutdown internal firewall

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><ol type="1">
<li><p>TODO</p></li>
</ol></th>
</tr>
<tr class="odd">
<th></th>
</tr>
<tr class="header">
<th></th>
</tr>
<tr class="odd">
<th></th>
</tr>
<tr class="header">
<th></th>
</tr>
<tr class="odd">
<th></th>
</tr>
<tr class="header">
<th></th>
</tr>
<tr class="odd">
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Shutdown backup server

|     |
|-----|
|     |

Shutdown UPS remove power cables connect to it.

#  

# 6. Health Check

Abnormal case

Taking System Dumps

The LSCP database backup and control file backup is used for data backup
and recovery of the SQL Server database to the control file. Please
refer to Section 8.

Checking the Air-Conditioning System/Power Supply System

Whenever there is a check on the air-conditioning system or power
supplies system, LSCP support staff shall follow the procedures in
Section 6 to switch off the hardware and all the LSCP VM and physical
servers, and then power on and load the server systems up again.

Fault Reporting Procedures

Maintenance team shall submit a fault report to the BD office to report
the problem.

First Line System Crash/Communication Faults Diagnosis

First Line System Crash Diagnosis

Maintenance team is responsible for the first line system crash
diagnosis. Since most of the error messages in the LSCP application will
be logged down in the “System Log” or “Application Log” in the Microsoft
Event Viewer, LSCP support staff shall check all the error messages in
the “System Log” and “Application Log”. After LSCP Support staff has
identified the cause of the problem, he/she shall take proper action to
inform the corresponding technical support for attention to the problem
and resolve the problem.

System Prompts/Exception Handling

Whenever there is a system or application error messages pop up on the
console, LSCP support staff shall determine whether the problem is
critical or not. In case of critical system error encountered that would
seriously affect the production LSCP application service, LSCP support
staff shall take proper action to inform the corresponding technical
support for attention to the problem and resolve the problem.

Communication Faults Diagnosis

Maintenance team could check the status of the connection of each server
by using the standard “ping” command to ping the IP address (refer to
section 5.3.3) of each server. If LSCP support staff can remote the
server but haven’t got any response when pinging by another server, the
problem shall be on the network. LSCP support staff shall contact MC to
fix the problem as soon as possible. For Intranet LSCP, LSCP support
staff shall contact BD-network supporting staff to fix the problem as
soon as possible.

# 7. Operation Housekeeping Jobs

## 7.1 Recover Database and Control File Backup from VM

TODO

#  

# 8. Configurations

## 8.1 External Firewall

Please refer to BD LSCP - Prod Installation & Operation Manual (network)
v1.0 Section 1

Please reference BD - VM & Network Upgrade for LSCP Site Infra Config
Info - 20230427_v0.1 tab - Prod - FW port, Prod - FW VIP policy, DR - FW
port, DR - FW VIP policy

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>###run in
prd-db-02-----------------------------------------------</p>
<p>use master</p>
<p>create master key encryption by password = ' “your password” ',</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p>
<p>use master</p>
<p>create certificate prd_db_02_10yrs_cert</p>
<p>with subject = 'prd-db-02-10yrs cert for availability group'</p>
<p>expiry_date = '20331231';</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p>
<p>use master</p>
<p>create endpoint endpoint_availabilitygroup</p>
<p>state = started</p>
<p>as tcp</p>
<p>(</p>
<p>listener_port = 5022, listener_ip = all</p>
<p>)</p>
<p>for database_mirroring</p>
<p>(</p>
<p>authentication = certificate prd_db_02_10yrs_cert,</p>
<p>encryption = required algorithm aes,</p>
<p>role = all</p>
<p>);</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p>
<p>use master</p>
<p>backup certificate prd_db_02_10yrs_cert</p>
<p>to file = 'c:\source\prd_db_02_10yrs_cert.cer';</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p>
<p>use master</p>
<p>create login login_availabilitygroup</p>
<p>with password = ' “your password” ';</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p>
<p>use master</p>
<p>create user login_availabilitygroup</p>
<p>for login login_availabilitygroup</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  Copy the certificate 'c:\source\prd_db_02_10yrs_cert.cer' to
    prd-db-01 c:\source

2.  Open a new query on prd-db-02 and perform the following query one by
    one.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>use master</p>
<p>create certificate prd_db_01_10yrs_cert</p>
<p>authorisation login_availabilitygroup</p>
<p>from file = 'c:\source\prd_db_01_10yrs_cert.cer'</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p>
<p>use master</p>
<p>grant connect on endpoint::endpoint_availabilitygroup</p>
<p>to [login_availabilitygroup];</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  Open a new query on prd-db-01 and perform the following query one by
    one.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>use master</p>
<p>create certificate prd_db_02_10yers_cert</p>
<p>authorisation login_availabilitygroup</p>
<p>from file = 'c:\source\prd_db_02_10yrs_cert.cer'</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p>
<p>use master</p>
<p>grant connect on endpoint::endpoint_availabilitygroup</p>
<p>to [login_availabilitygroup];</p>
<p>go</p>
<p>—-----------------------------------------------------------------------</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

|     |
|-----|

1.  Launch Microsoft SQL Server Management Studio on prd-db-01 and
    connect to prd-db-01.

> <img src="media/image19.png" style="width:6.5in;height:3.54167in" />

1.  Create New Database by right clicking Databases -\> New Database.

> <img src="media/image7.png" style="width:2.87118in;height:3.58674in" />

1.  Input Database name and click OK.

> <img src="media/image18.png" style="width:4.05724in;height:3.84896in" />

1.  Backup the database by right clicking that database -\> Tasks -\>
    Back Up.

> <img src="media/image11.png" style="width:5.66007in;height:3.8913in" />

1.  Click OK.

> <img src="media/image1.png" style="width:5.04549in;height:3.71134in" />

1.  Create Always On High Availability by clicking Always On High
    Availability -\> New Availability Group Wizard.

> <img src="media/image14.png" style="width:4.86458in;height:3.89583in" />

1.  Click Next.

> <img src="media/image10.png" style="width:4.91007in;height:4.30418in" />

1.  Input the Availability group name -\> select Windows Server Failover
    Cluster -\> check Database Level Health Detection.

> <img src="media/image16.png" style="width:4.53507in;height:3.96136in" />

1.  Check the database and click Next.

> <img src="media/image12.png" style="width:3.90243in;height:3.40837in" />

1.  Click Add Replica.

> <img src="media/image4.png" style="width:5.9375in;height:5.40972in" />

1.  Select PRD-DB-02 as Servername and click Connect.

> <img src="media/image8.png" style="width:4.01424in;height:2.65943in" />

1.  Check both Automatic Failover (Up to 5) and click Listener.

> <img src="media/image3.png" style="width:5.28507in;height:4.63291in" />

1.  Input the Listener DNS Name, Port, IP address and click Next.

> <img src="media/image20.png" style="width:4.07674in;height:3.71in" />

1.  Select Automatic seeding and click Next.

> <img src="media/image13.png" style="width:4.09757in;height:3.73171in" />

1.  Click Next.

> <img src="media/image6.png" style="width:4.72257in;height:4.29623in" />

1.  Click “Script”.

> <img src="media/image5.png" style="width:6.5in;height:5.68056in" />

1.  Replace the all “NT Service\MSSQLSERVER” with
    “login_availabilitygroup”.

> <img src="media/image15.png" style="width:4.50382in;height:2.70662in" />
>
> <img src="media/image2.png" style="width:6.5in;height:4in" />

1.  Click “Execute” to finish the configuration.

> <img src="media/image17.png" style="width:6.5in;height:4.44444in" />

1.  Click “Cancel” to exit the installation.

> <img src="media/image5.png" style="width:6.5in;height:5.68056in" />

#  

# 9. Deployment Guides

## 9.1 Deploying LSCP Web

Deploy Web Frontend

1.  TODO

Deploy Web Backend

1.  TODO

## 9.2 Deploy Mobile App

1.  TODO

\<\<\< End of document \>\>\>
