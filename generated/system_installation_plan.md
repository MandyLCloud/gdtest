<img src="media/image1.jpg" style="width:2.03125in;height:1.52083in"
alt="BDlogo" />

**SYSTEM INSTALLATION PLAN**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**OF**

**BUILDINGS DEPARTMENT**

**Version: 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR.

| **Distribution** |                                         |
|------------------|-----------------------------------------|
| Copy No.         | Holder                                  |
| 1                | Buildings Department (BD)               |
| 2                | Master Concept (Hong Kong) Limited (MC) |

| **Amendment History** |                      |                                      |                           |           |                    |
|----------|--------------------|--------------|---------|---------|-----------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date      | Approval Reference |
| 1                     | 1st draft            | All                                  | 0.1                       | 16/01/225 |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |

**TABLE OF CONTENTS**

[1. Introduction 5](#introduction)

[2. Project Environment Description 6](#project-environment-description)

> [2.1 Network Diagram 6](#network-diagram)
>
> [2.2 Hardware Specification 6](#hardware-specification)
>
> [2.3 Software Specification 8](#software-specification)

[3. Application Deployment Procedure for Production 10](#application-deployment-procedure-for-production)

> [3.1 Database Server 10](#database-server)
>
> [3.2 Backend Servers 10](#backend-servers)
>
> [3.3 Frontend Servers 10](#frontend-servers)
>
> [3.3.1 sFTP Server Setup 10](#sftp-server-setup)

[4. System Installation Schedule and Result 11](#system-installation-schedule-and-result)

> [4.1 System Installation Schedule 11](#system-installation-schedule)
>
> [4.2 System Installation Result 12](#system-installation-result)

# Introduction

The System Installation plan describes the procedure and schedule for
deploying the application in the production environment. The Licensing Self-Certification Portal (LSCP) allows Buildings Department (BD) users to receive, process and manage the application for certificates and notice required under Education Ordinance (Cap.279) and Child Care Services Ordinance (Cap. 243) for the registration of non-purpose built Educational Premises (EP) and Child Care Centre (CCC) and to provide building safety comment to Education Bureau upon applications for conducting courses of non-local higher and professional education under NLHPE(R) Rules (Cap.493B).

The system comprises 3 parts:

-   Database Server
-   Backend Server
-   Frontend and Web Portal Server

# Project Environment Description

## Network Diagram

Below is a logical network diagram in 1/F West Kowloon Government Office
for production and UAT site.

<span class="mark">\[DIAGRAM HERE\]</span>

The network will be separated into three zones: DMZ, trusted zone, and
storage network.

A two-tier firewall setup will be used to form the trusted zone and DMZ.
Incoming network traffic to the system must go through the DMZ before
entering the trusted zone.

To utilize hardware resources more effectively, servers listed in
section 1.3.3, except the backup server, will
be set up in the form of virtual machines (VM) and consolidated into DMZ
VM host servers and trusted zone VM host servers for each physical site.
Two VM host servers will be built in each zone for the purpose of high
availability.

Similarly, storage needed by all servers will be consolidated and
provided by SAN storage. A dedicated network will be set up and
interconnected with the VM host servers. The backup server will also
exist in this storage-dedicated network to carry out backup tasks of VM
host servers in DMZ and trusted zone.

The diagram below illustrates the physical setup.

## Hardware Specification

Production and UAT environment:

List of machines and virtual machines:

<table>
<thead>
<tr class="header">
<th>Hostname<br> (Physical Machine)</th>
<th>Hostname<br> (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr>
<td></td>
<td>prd-scs-vcenter-01</td>
<td>vCenter</td>
<td>192.168.10.24 / 10.5.161.210</td>
</tr>
<tr>
<td></td>
<td>prd-scs-backup-01</td>
<td>Veeam Backup Server</td>
<td>192.168.10.25 / 10.5.161.211</td>
</tr>
<tr>
<td></td>
<td>prd-scs-log-01</td>
<td>Kiwi Log Server</td>
<td>192.168.10.11 / 10.5.161.223</td>
</tr>
<tr>
<td></td>
<td>prd-scs-esetnod32</td>
<td>NOD32 Anti-Virus Server</td>
<td>192.168.10.34 / 10.5.161.215</td>
</tr>
<tr>
<td></td>
<td>prd-scs-admin-api-01</td>
<td>API Server</td>
<td>192.168.12.11</td>
</tr>
<tr>
<td></td>
<td>prd-scs-admin-frontend-01</td>
<td>Frontend Server</td>
<td>192.168.12.12</td>
</tr>
<tr>
<td></td>
<td>prd-scs-admin-backend-01</td>
<td>Backend Server</td>
<td>192.168.12.13</td>
</tr>
<tr>
<td></td>
<td>prd-scs-db-01</td>
<td>Database Server</td>
<td>192.168.12.14</td>
</tr>
<tr>
<td></td>
<td>prd-scs-filer</td>
<td>File Server</td>
<td>192.168.12.20</td>
</tr>
<tr>
<td></td>
<td>prd-scs-proxy</td>
<td>Reverse Proxy Server</td>
<td>192.168.12.15 / 10.5.161.226</td>
</tr>
<tr>
<td></td>
<td>prd-scs-admin-api-02</td>
<td>API Server</td>
<td>192.168.12.16</td>
</tr>
<tr>
<td></td>
<td>prd-scs-admin-frontend-02</td>
<td>Frontend Server</td>
<td>192.168.12.17</td>
</tr>
<tr>
<td></td>
<td>prd-scs-admin-backend-02</td>
<td>Backend Server</td>
<td>192.168.12.18</td>
</tr>
<tr>
<td></td>
<td>prd-scs-db-02</td>
<td>Database Server</td>
<td>192.168.12.19</td>
</tr>
<tr>
<td></td>
<td>uat-scs-admin-api-01</td>
<td>API Server (UAT)</td>
<td>192.168.13.10</td>
</tr>
<tr>
<td></td>
<td>uat-scs-admin-frontend-01</td>
<td>Frontend Server (UAT)</td>
<td>192.168.13.11</td>
</tr>
<tr>
<td></td>
<td>uat-scs-admin-backend-01</td>
<td>Backend Server (UAT)</td>
<td>192.168.13.12</td>
</tr>
<tr>
<td></td>
<td>uat-scs-db-01</td>
<td>Database Server (UAT)</td>
<td>192.168.13.13</td>
</tr>
<tr>
<td></td>
<td>uat-scs-filer</td>
<td>File Server (UAT)</td>
<td>192.168.13.15</td>
</tr>
<tr>
<td></td>
<td>uat-scs-proxy</td>
<td>Reverse Proxy Server (UAT)</td>
<td>192.168.13.14 / 10.5.161.224</td>
</tr>
<tr>
<td>prd-scs-admin-server-01</td>
<td></td>
<td>VM Host Server</td>
<td>192.168.10.22, 10.5.161.206</td>
</tr>
<tr>
<td>prd-scs-admin-server-02</td>
<td></td>
<td>VM Host Server</td>
<td>192.168.10.23, 10.5.161.207</td>
</tr>
<tr>
<td>prd-scs-nas</td>
<td></td>
<td>NAS</td>
<td>192.168.10.35, 10.5.161.218</td>
</tr>
</tbody>
</table>

DR environment:

List of machines and virtual machines:

<table>
<thead>
<tr class="header">
<th>Hostname<br> (Physical Machine)</th>
<th>Hostname<br> (Virtual Machine)</th>
<th>Purpose</th>
<th>IP</th>
</tr>
</thead>
<tbody>
<tr>
<td></td>
<td>dr-scs-vcenter-01</td>
<td>vCenter (DR)</td>
<td>192.168.20.18 / 10.5.174.225</td>
</tr>
<tr>
<td></td>
<td>dr-scs-backup-01</td>
<td>Veeam Backup Server (DR)</td>
<td>192.168.20.19 / 10.5.161.224</td>
</tr>
<tr>
<td></td>
<td>dr-scs-log-01</td>
<td>Kiwi Log Server (DR)</td>
<td>192.168.20.10</td>
</tr>
<tr>
<td></td>
<td>dr-scs-admin-api-01</td>
<td>API Server (DR)</td>
<td>192.168.22.11</td>
</tr>
<tr>
<td></td>
<td>dr-scs-admin-frontend-01</td>
<td>Frontend Server (DR)</td>
<td>192.168.22.12</td>
</tr>
<tr>
<td></td>
<td>dr-scs-admin-backend-01</td>
<td>Backend Server (DR)</td>
<td>192.168.22.13</td>
</tr>
<tr>
<td></td>
<td>dr-scs-db-01</td>
<td>Database Server (DR)</td>
<td>192.168.22.14</td>
</tr>
<tr>
<td></td>
<td>dr-scs-filer</td>
<td>File Server (DR)</td>
<td>192.168.22.16</td>
</tr>
<tr>
<td></td>
<td>dr-scs-proxy</td>
<td>Reverse Proxy Server (DR)</td>
<td>192.168.22.15 / 10.5.174.228</td>
</tr>
<tr>
<td>dr-scs-admin-server-01</td>
<td></td>
<td>VM Host Server (DR)</td>
<td>192.168.20.17, 10.5.174.216</td>
</tr>
<tr>
<td>dr-scs-nas</td>
<td></td>
<td>NAS (DR)</td>
<td>192.168.20.35, 10.5.174.225</td>
</tr>
</tbody>
</table>

## Software Specification

| Category | Software | Version |
|---|---|---|
| **Operating System** | Windows Server 2022 21H2 |  |
|  | Windows Server 2019 1809 (GCIS) |  |
|  | VMware ESXi | 8.0.3 |
| **Database** | Microsoft SQL Server 2022 | 16.0.1000.6 |
| **Web Server** | IIS | 10.0 |
|  | Nginx | 1.26.2 |
| **Virtualization** | VMware vSphere | 8.0.3 |
|  | VMware Tools | 12.4.0.23259341 (WKGO), 12.1.0.20219665 (GCIS) |
| **Backup** | Veeam Backup & Replication | 12.1.2.172 |
| **Log Management** | Kiwi Syslog Server NG | 1.2.1.4 (WKGO), 9.8.3 (GCIS) |
| **Anti-Virus** | ESET Server Security | 10.0.12012.0 (WKGO) |
|  | ESET Management Agent | 10.1.1292.0 (WKGO) |
|  | ESET PROTECT Server | 11.0.199.0 (WKGO) |
|  | Bitdefender Endpoint Security Tools | 7.9.17.458 (GCIS) |
| **Management Studio** | Microsoft Management Studio | 19.1 |
| **Framework (Frontend)** | React | 18.2.0 |
| **Framework (Backend)** | ExpressJS | 4.19.2 |
| **Runtime** | NodeJS | 20.11.1 |

# Application Deployment Procedure for Production

## Database Server

To install database server, follow these steps:

1.  Remote login to PRD-DB-01(10.5.113.218).

## Backend Servers

1.  Remote login into PRD-WEBAPP-01.

## Frontend Servers

1.  Remote login into PRD-WEBAPP-01.

### sFTP Server Setup

1.  Install OpenSSH server in Windows Server. Go to Apps & Features,
    > Click ?Optional Features?, click ?Add a feature?, check ?OpenSSH
    > Server?

# System Installation Schedule and Result

## System Installation Schedule

The following table summarises the testing schedule:

| Pre-Requisite                                            |     | Start Date | End Date | Start time | End Time |
|-----------------------------------|----|---------|---------|--------|--------|
| Database Server Installation (Production and DR)         |     |            |          |            |          |
| Backend Server Installation (Production and DR)          |     |            |          |            |          |
| Frontend Server Installation (Production and DR)         |     |            |          |            |          |
| Functionality test (VM & Networking)                     |     |            |          |            |          |
| Database setup                                           |     |            |          |            |          |
| Deployment for 1<sup>st</sup> version of frontend server |     |            |          |            |          |
| Deployment for 1<sup>st</sup> version of backend server  |     |            |          |            |          |
| Application Health Check                                 |     |            |          |            |          |
| 1                                                        |     |            |          |            |          |
| Deployment for Latest Mobile Application                 |     |            |          |            |          |
| Final Check Production Web Server                        |     |            |          |            |          |
| Final Check Production Database Server                   |     |            |          |            |          |
| Final Check DR Web & Database server                     |     |            |          |            |          |
| Final Check IIS & Framework                              |     |            |          |            |          |

## System Installation Result

The following table summarises the actual system installation schedule:

| Pre-Requisite                                            |     | Actual Start Date | Actual End Date | Actual Start time | Actual End Time | Status/Result |
|----------------------|----|-----------|-------------|--------|--------|---------|
| Database Server Installation (Production, UAT and DR)    |     |                   |                 |                   |                 |               |
| Backend Server Installation (Production, UAT and DR)     |     |                   |                 |                   |                 |               |
| Frontend Server Installation (Production, UAT and DR)    |     |                   |                 |                   |                 |               |
| Functionality test (VM & Networking)                     |     |                   |                 |                   |                 |               |
| Database setup                                           |     |                   |                 |                   |                 |               |
| Deployment for 1<sup>st</sup> version of frontend server |     |                   |                 |                   |                 |               |
| Deployment for 1<sup>st</sup> version of backend server  |     |                   |                 |                   |                 |               |
| Application Health Check                                 |     |                   |                 |                   |                 |               |
| 1                                                        |     |                   |                 |                   |                 |               |
| Deployment for Latest Mobile Application                 |     |                   |                 |                   |                 |               |
| Final Check Production Web Server                        |     |                   |                 |                   |                 |               |
| Final Check Production Database Server                   |     |                   |                 |                   |                 |               |
| Final Check DR Web & DB server                           |     |                   |                 |                   |                 |               |
| Final Check IIS & Framework                              |     |                   |                 |                   |                 |               |

\<\<End of Document\>\>