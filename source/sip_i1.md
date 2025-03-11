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

© The Government of the Hong Kong Special Administrative Region

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

[3. Application Deployment Procedure for Production
10](#application-deployment-procedure-for-production)

> [3.1 Database Server 10](#database-server)
>
> [3.2 Backend Servers 10](#backend-servers)
>
> [3.3 Frontend Servers 10](#frontend-servers)
>
> [3.3.1 sFTP Server Setup 10](#sftp-server-setup)

[4. System Installation Schedule and Result
11](#system-installation-schedule-and-result)

> [4.1 System Installation Schedule 11](#system-installation-schedule)
>
> [4.2 System Installation Result 12](#system-installation-result)

#  

# Introduction

The System Installation plan describes the procedure and schedule for
deploying the application in the production environment, including 3
parts of the system:

-   Database Server

-   Backend Server

-   Frontend and Web Portal Server

#  

# Project Environment Description

# 

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
section <span class="mark">1.3.3</span>, except the backup server, will
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

DR environment:

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
<tr class="odd">
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## Software Specification

|     |     |     |     |
|-----|-----|-----|-----|
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |
|     |     |     |     |

#  

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
    > Click “Optional Features”, click “Add a feature”, check “OpenSSH
    > Server”

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

##  

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
