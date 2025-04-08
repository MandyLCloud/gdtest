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

# Introduction

The System Installation plan describes the procedure and schedule for
deploying the application in the production environment, including 3
parts of the system:

-   Database Server

-   Backend Server

-   Frontend and Web Portal Server

# Project Environment Description

## Network Diagram

Below is a logical network diagram in 1/F West Kowloon Government Office
for production and UAT site.

<img src="media/image2.png" style="width:6.62605in;height:5.91667in" alt="System Architecture Production Environment WKGO"/>

<img src="media/image3.png" style="width:6.62605in;height:5.81944in" alt="System Architecture Production and UAT Site"/>

The network will be separated into three zones: DMZ, trusted zone, and
storage network.

A two-tier firewall setup will be used to form the trusted zone and DMZ.
Incoming network traffic to the system must go through the DMZ before
entering the trusted zone.

To utilize hardware resources more effectively, servers listed in
section 2.2, except the backup server, will be set up in the form of virtual machines (VM) and consolidated into DMZ
VM host servers and trusted zone VM host servers for each physical site.
Two VM host servers will be built in each zone for the purpose of high
availability.

Similarly, storage needed by all servers will be consolidated and
provided by SAN storage. A dedicated network will be set up and
interconnected with the VM host servers. The backup server will also
exist in this storage-dedicated network to carry out backup tasks of VM
host servers in DMZ and trusted zone.

The diagram below illustrates the physical setup.

<img src="media/image6.png" style="width:6.62605in;height:5.30556in" alt="Rack Diagram"/>

## Hardware Specification

Production and UAT environment:

List of machines and virtual machines:

**Production Environment - WKGO**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                                | IP                                        |
|-----------------------------|----------------------------|----------------------------------------|-------------------------------------------|
| prd-scs-admin-server-01     | prd-scs-vcenter-01         | vCenter                                | 192.168.10.24 / 10.5.161.210              |
|                             | prd-scs-log-01             | Kiwi Log Server                        | 192.168.10.11 / 10.5.161.223              |
|                             | prd-scs-admin-api-01       | API Server                             | 192.168.12.11                             |
|                             | prd-scs-admin-frontend-01  | Frontend Server                        | 192.168.12.12                             |
|                             | prd-scs-admin-backend-01   | Backend Server                         | 192.168.12.13                             |
|                             | prd-scs-db-01              | Database Server                        | 192.168.12.14                             |
|                             | prd-scs-filer              | File Server                            | 192.168.12.20                             |
|                             | prd-scs-proxy              | Reverse Proxy Server                   | 192.168.12.15 / 10.5.161.226              |
| prd-scs-admin-server-02     | prd-scs-backup-01          | Veeam Backup Server                    | 192.168.10.25 / 10.5.161.211              |
|                             | prd-scs-esetnod32          | NOD32 Anti-Virus Server                | 192.168.10.34 / 10.5.161.215              |
|                             | prd-scs-admin-api-02       | API Server                             | 192.168.12.16                             |
|                             | prd-scs-admin-frontend-02  | Frontend Server                        | 192.168.12.17                             |
|                             | prd-scs-admin-backend-02   | Backend Server                         | 192.168.12.18                             |
|                             | prd-scs-db-02              | Database Server                        | 192.168.12.19                             |
| prd-scs-nas               | N/A                        | NAS                                    | 192.168.10.35, 10.5.161.218              |
| PA-850-SCSPri             | N/A                        | Firewall (Primary)                       | 192.168.10.12 / 10.5.161.205              |
| PA-850-SCSSec             | N/A                        | Firewall (Secondary)                     | 192.168.10.13 / 10.5.161.220              |
| Switch 1                    | N/A                        | Switch                                 | 192.168.10.14                             |
| Switch 2                    | N/A                        | Switch                                 | 192.168.10.15                             |
| PS500T-Cluster1             | N/A                        | SAN Storage                            | 192.168.10.26, 192.168.10.27, 192.168.10.28, 192.168.10.29 |
| prd-scs-backupstorage-01    | N/A                        | Backup Appliance                       | 192.168.10.20                             |
| Dell ML3                    | N/A                        | Tape Library                           | 192.168.10.20                             |
| Cyber View                  | N/A                        | KVM                                    | N/A                                       |
| Vertiv? Liebert? GXT5 3000  | N/A                        | UPS 1                                  | 192.168.11.20                             |
| Vertiv? Liebert? GXT5 3000  | N/A                        | UPS 2                                  | 192.168.11.21                             |

**UAT Environment - WKGO**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                                | IP                                        |
|-----------------------------|----------------------------|----------------------------------------|-------------------------------------------|
| prd-scs-admin-server-01     | uat-scs-admin-api-01       | API Server                             | 192.168.13.10                             |
|                             | uat-scs-admin-frontend-01  | Frontend Server                        | 192.168.13.11                             |
|                             | uat-scs-admin-backend-01   | Backend Server                         | 192.168.13.12                             |
|                             | uat-scs-db-01              | Database Server                        | 192.168.13.13                             |
|                             | uat-scs-filer              | File Server                            | 192.168.13.15                             |
|                             | uat-scs-proxy              | Reverse Proxy Server                   | 192.168.13.14 / 10.5.161.224              |
| GCIS P1                     | scsuwi                     | Reverse Proxy Server (Internet DMZ)    | 192.168.0.7 / 45.119.94.99                |
|                             | scsuwg                     | Reverse Proxy Server (GNET DMZ)        | 192.168.4.7 / 10.148.11.220               |
|                             | scsuad                     | Apps Server                            | 192.168.8.9                               |
|                             | scsudb                     | Database Server                        | 192.168.8.10                              |

**DR environment:**

List of machines and virtual machines:

**DR Environment - AIA**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                                | IP                                        |
|-----------------------------|----------------------------|----------------------------------------|-------------------------------------------|
| dr-scs-admin-server-01      | dr-scs-vcenter-01          | vCenter                                | 192.168.20.18 / 10.5.174.225              |
|                             | dr-scs-backup-01           | Veeam Backup Server                    | 192.168.20.19 / 10.5.161.224              |
|                             | dr-scs-log-01              | Kiwi Log Server                        | 192.168.20.10                             |
|                             | dr-scs-admin-api-01        | API Server                             | 192.168.22.11                             |
|                             | dr-scs-admin-frontend-01   | Frontend Server                        | 192.168.22.12                             |
|                             | dr-scs-admin-backend-01    | Backend Server                         | 192.168.22.13                             |
|                             | dr-scs-db-01               | Database Server                        | 192.168.22.14                             |
|                             | dr-scs-filer               | File Server                            | 192.168.22.16                             |
|                             | dr-scs-proxy               | Reverse Proxy Server                   | 192.168.22.15 / 10.5.174.228              |
| dr-scs-nas                | N/A                        | NAS                                    | 192.168.20.35, 10.5.174.225              |
| PA-850-SCSDR              | N/A                        | Firewall                               | 192.168.20.12 / 10.5.174.215              |
| Switch DR                   | N/A                        | Switch                                 | 192.168.20.13                             |
| PS500T-Cluster2             | N/A                        | SAN Storage                            | 192.168.20.20, 192.168.20.21, 192.168.20.22, 192.168.20.23 |
| dr-scs-backupstorage-01     | N/A                        | Backup Appliance                       | 192.168.20.25                             |
| Vertiv? Liebert? GXT5 3000  | N/A                        | UPS                                    | 192.168.20.11                             |
| GCIS P2                     | scspwi                     | Reverse Proxy Server (Internet DMZ)    | 192.168.0.6 / 45.119.93.84                |
|                             | scspwg                     | Reverse Proxy Server (GNET DMZ)        | 192.168.4.6 / 10.160.139.211              |
|                             | scspad                     | Apps Server                            | 192.168.8.6                               |
|                             | scspdb                     | Database Server                        | 192.168.8.7                               |

**DEV Environment - WKGO**

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                                | IP                                        |
|-----------------------------|----------------------------|----------------------------------------|-------------------------------------------|
| prd-scs-admin-server-02     | dev-scs-admin-api-01       | API Server                             | 192.168.14.10                             |
|                             | dev-scs-admin-frontend-01  | Frontend Server                        | 192.168.14.11                             |
|                             | dev-scs-admin-backend-01   | Backend Server                         | 192.168.14.12                             |
|                             | dev-scs-db-01              | Database Server                        | 192.168.14.13                             |
|                             | dev-scs-filer              | File Server                            | 192.168.14.15                             |
|                             | dev-scs-proxy              | Reverse Proxy Server                   | 192.168.14.14 / 10.5.161.225              |
| GCIS T1                     | scsdwi                     | Reverse Proxy Server (Internet DMZ)    | 192.168.0.6 / 45.119.94.100               |
|                             | scsdwg                     | Reverse Proxy Server (GNET DMZ)        | 192.168.4.6 / 10.148.11.220               |
|                             | scsdad                     | Apps Server                            | 192.168.8.7                               |
|                             | scsddb                     | Database Server                        | 192.168.8.8                               |

## Software Specification

| Category          | Software                                      | Version                  | Purpose                                                                 |
|-------------------|-----------------------------------------------|--------------------------|-------------------------------------------------------------------------|
| Operating System  | Windows Server 2022 21H2                      |                          | For most servers in WKGO and DR                                         |
|                   | Windows Server 2019 1809                      |                          | For servers in GCIS                                                       |
|                   | VMware ESXi                                   | 8.0.3                    | Hypervisor for Virtual Machines                                         |
| Virtualization    | VMware vCenter Server                         | 8.0.3                    | Management of VMware environment                                        |
| Web Server        | IIS                                           | 10.0                     | Hosting Frontend and Backend Applications                               |
|                   | Nginx                                         | 1.26.2                   | Reverse Proxy Server                                                      |
| Database          | Microsoft SQL Server 2022                     | 16.0.1000.6              | Database Management System                                              |
| Backup            | Veeam Backup & Replication                    | 12.1.2.172               | Virtual Machine Backup and Replication                                  |
| Log Management    | Kiwi Syslog Server NG                         | 1.2.1.4                  | Centralized Log Management (WKGO & DR)                                  |
|                   | Kiwi Syslog Server 9.8.3 (Service Edition)    |                          | Centralized Log Management (GCIS)                                       |
| Anti-Virus        | ESET Server Security                          | 10.0.12012.0             | Anti-virus protection (WKGO & DR)                                       |
|                   | ESET Management Agent                         | 10.1.1292.0              | Management agent for ESET Anti-virus (WKGO & DR)                          |
|                   | ESET PROTECT Server                           | 11.0.199.0               | Centralized management of ESET Anti-virus (WKGO & DR)                   |
|                   | Bitdefender Endpoint Security Tools           | 7.9.17.458               | Anti-virus protection (GCIS)                                            |
| Management Tools  | Microsoft SQL Server Management Studio (SSMS) | 19.1                     | Database administration and management                                    |
| Framework         | React                                         | 18.2.0                   | Frontend JavaScript framework                                           |
|                   | ExpressJS                                     | 4.19.2                   | Backend Node.js framework                                                |
|                   | NodeJS                                        | 20.11.1                  | Runtime environment for backend application                               |
| Other             | VMware Tools                                  | 12.4.0.23259341 (WKGO/DR) | VMware Tools for Virtual Machines                                       |
|                   |                                               | 12.1.0.20219665 (GCIS)   |                                                                         |

# Application Deployment Procedure for Production

## Database Server

To install database server, follow these steps:

1.  Remote login to PRD-DB-01(192.168.12.14).
2.  Install Microsoft SQL Server 2022.
3.  Configure database instance and create necessary databases and users according to application requirements.
4.  Setup database mirroring/availability group as per design.
5.  Perform initial database backup.

## Backend Servers

1.  Remote login into PRD-WEBAPP-01 (192.168.12.13).
2.  Install NodeJS runtime environment.
3.  Deploy backend application code to the server.
4.  Configure application settings, including database connection strings and API endpoints.
5.  Start backend application service.
6.  Repeat steps for PRD-WEBAPP-02 (192.168.12.18).
7.  Configure Network Load Balancer (NLB) for backend servers.

## Frontend Servers

1.  Remote login into PRD-WEBAPP-01 (192.168.12.12).
2.  Install IIS role and necessary features.
3.  Deploy frontend application code to the IIS website directory.
4.  Configure IIS website settings, including binding and SSL certificates.
5.  Configure reverse proxy settings to forward API requests to backend servers.
6.  Start IIS website.
7.  Repeat steps for PRD-WEBAPP-02 (192.168.12.17).
8.  Configure Windows Network Load Balancing (NLB) for frontend servers.

### sFTP Server Setup

1.  Install OpenSSH server in Windows Server on File Server (prd-scs-filer, 192.168.12.20). Go to Apps & Features,
    > Click ?Optional Features?, click ?Add a feature?, check ?OpenSSH
    > Server?
2.  Configure SSH service to start automatically.
3.  Create user accounts for sFTP access with appropriate permissions.
4.  Configure firewall rules to allow SSH traffic (port 22) to the sFTP server.
5.  Test sFTP access using a client like FileZilla or WinSCP.

# System Installation Schedule and Result

## System Installation Schedule

The following table summarises the testing schedule:

| Pre-Requisite                                            |     | Start Date | End Date   | Start time | End Time |
|----------------------------------------------------------|-----|------------|------------|------------|----------|
| Database Server Installation (Production and DR)         |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Backend Server Installation (Production and DR)          |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Frontend Server Installation (Production and DR)         |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Functionality test (VM & Networking)                     |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Database setup                                           |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Deployment for 1<sup>st</sup> version of frontend server |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Deployment for 1<sup>st</sup> version of backend server  |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Application Health Check                                 |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Integration Test                                         |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Deployment for Latest Mobile Application                 |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Final Check Production Web Server                        |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Final Check Production Database Server                   |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Final Check DR Web & Database server                     |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |
| Final Check IIS & Framework                              |     | YYYY-MM-DD | YYYY-MM-DD | HH:MM      | HH:MM    |

## System Installation Result

The following table summarises the actual system installation schedule:

| Pre-Requisite                                            |     | Actual Start Date | Actual End Date | Actual Start time | Actual End Time | Status/Result |
|----------------------------------------------------------|-----|-------------------|-----------------|-------------------|-----------------|---------------|
| Database Server Installation (Production, UAT and DR)    |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Backend Server Installation (Production, UAT and DR)     |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Frontend Server Installation (Production, UAT and DR)    |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Functionality test (VM & Networking)                     |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Database setup                                           |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Deployment for 1<sup>st</sup> version of frontend server |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Deployment for 1<sup>st</sup> version of backend server  |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Application Health Check                                 |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Integration Test                                         |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Deployment for Latest Mobile Application                 |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Final Check Production Web Server                        |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Final Check Production Database Server                   |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Final Check DR Web & DB server                           |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |
| Final Check IIS & Framework                              |     | YYYY-MM-DD        | YYYY-MM-DD      | HH:MM             | HH:MM           |               |

\<\<End of Document\>\>