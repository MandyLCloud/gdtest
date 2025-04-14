![BDlogo](media/image1.jpg)

# SYSTEM INSTALLATION PLAN

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**

**LICENSING SELF-CERTIFICATION PORTAL**

**OF**

**BUILDINGS DEPARTMENT**

**Version: 0.1**

**Jan 2025**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

| Distribution |                                     |
|-------------|-------------------------------------|
| Copy No.    | Holder                              |
| 1           | Buildings Department (BD)           |
| 2           | Master Concept (Hong Kong) Limited (MC) |

| Amendment History |                       |                |            |           |           |
|------------------|------------------------|----------------|------------|-----------|-----------|
| Change Number    | Revision Description   | Pages Affected | Revision / | Date      | Approval  |
|                  |                       | on Respective  | Version    |           | Reference |
|                  |                       | Version        | Number     |           |           |
| 1                | 1st draft             | All            | 0.1        | 16/01/225 |           |

# TABLE OF CONTENTS

[1. Introduction](#introduction)

[2. Project Environment Description](#project-environment-description)
- [2.1 Network Diagram](#network-diagram)
- [2.2 Hardware Specification](#hardware-specification)
- [2.3 Software Specification](#software-specification)

[3. Application Deployment Procedure for Production](#application-deployment-procedure-for-production)
- [3.1 Database Server](#database-server)
- [3.2 Backend Servers](#backend-servers)
- [3.3 Frontend Servers](#frontend-servers)
  - [3.3.1 sFTP Server Setup](#sftp-server-setup)

[4. System Installation Schedule and Result](#system-installation-schedule-and-result)
- [4.1 System Installation Schedule](#system-installation-schedule)
- [4.2 System Installation Result](#system-installation-result)

# Introduction

The System Installation plan describes the procedure and schedule for deploying the application in the production environment, including 3 parts of the system:

- Database Server
- Backend Server
- Frontend and Web Portal Server

# Project Environment Description

## Network Diagram

Below is a logical network diagram in 1/F West Kowloon Government Office for production and UAT site.

[DIAGRAM HERE]

The network will be separated into three zones: DMZ, trusted zone, and storage network.

A two-tier firewall setup will be used to form the trusted zone and DMZ. Incoming network traffic to the system must go through the DMZ before entering the trusted zone.

To utilize hardware resources more effectively, servers listed in section [1.3.3], except the backup server, will be set up in the form of virtual machines (VM) and consolidated into DMZ VM host servers and trusted zone VM host servers for each physical site. Two VM host servers will be built in each zone for the purpose of high availability.

Similarly, storage needed by all servers will be consolidated and provided by SAN storage. A dedicated network will be set up and interconnected with the VM host servers. The backup server will also exist in this storage-dedicated network to carry out backup tasks of VM host servers in DMZ and trusted zone.

The diagram below illustrates the physical setup.

## Hardware Specification

Production and UAT environment:

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---------------------------|---------------------------|---------|-----|
| prd-scs-admin-server-01 | prd-scs-vcenter-01 | vCenter Server | 192.168.10.24/10.5.161.210 |


DR environment:

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---------------------------|---------------------------|---------|-----|
| dr-scs-admin-server-01 | dr-scs-vcenter-01 | vCenter Server | 192.168.20.18/10.5.174.225 |


## Software Specification

| Machine | Hostname | Software Requirement |
|---------|----------|---------------------|
| vCenter Server | prd-scs-vcenter-01 | vCenter 8.0.3 Build 24322831 |


Development Frameworks:

| Framework | Version |
|-----------|---------|
| React (frontend) | 18.2.0 |


# Application Deployment Procedure for Production

## Database Server

To install database server, follow these steps:

1. Remote login to PRD-DB-01
2. Install Microsoft SQL Server 2022 (16.0.1000.6)
3. Install Microsoft SQL Server Management Studio 19.1
4. Configure SQL Server with:
   - Authentication mode: Windows Authentication and SQL Server Authentication
   - Enable TCP/IP protocol
   - Configure firewall to allow SQL Server port (default 1433)
5. Create database LSCP_DB with:
   - Initial size: 100GB
   - Autogrowth: 1GB
   - Maximum size: Unlimited
6. Configure database backup schedule:
   - Daily incremental backup at 00:00
   - Weekly full backup on Sunday at 00:00
7. Configure database maintenance plan:
   - Weekly index rebuild
   - Daily statistics update
8. Configure database monitoring and alerts:
   - Space usage alerts at 85% and 95%
   - Performance alerts for long-running queries
   - Failed job alerts

## Backend Servers

1. Remote login into PRD-WEBAPP-01 and PRD-WEBAPP-02
2. Install prerequisites:
   - Windows Server 2022 updates
   - .NET 6.0 Runtime
   - NodeJS 20.11.1
3. Install backend application:
   - Deploy API application files to C:\inetpub\wwwroot\lscp-api
   - Configure application pool with:
     - .NET CLR Version: .NET CLR v4.0
     - Managed Pipeline Mode: Integrated
     - Identity: Custom service account
4. Configure application settings:
   - Update appsettings.json with production values
   - Configure connection strings
   - Set up logging paths
5. Configure Windows services:
   - Install and configure background job services
   - Set up Windows service recovery options
6. Configure SSL certificates:
   - Install SSL certificate
   - Bind certificate to HTTPS port
7. Configure IIS:
   - Create website and application pool
   - Configure URL bindings
   - Set up compression and caching rules

## Frontend Servers

1. Remote login into PRD-WEBAPP-01 and PRD-WEBAPP-02
2. Install prerequisites:
   - IIS 10.0.20348.1
   - URL Rewrite module
   - Application Request Routing
3. Install frontend application:
   - Deploy React application files to C:\inetpub\wwwroot\lscp-web
   - Configure static file caching
   - Set up compression for static files
4. Configure IIS:
   - Create website with appropriate bindings
   - Configure SSL certificates
   - Set up URL rewrite rules for SPA
   - Configure CORS if needed
5. Configure monitoring:
   - Set up IIS logging
   - Configure health check endpoints
   - Set up performance monitoring

### sFTP Server Setup

1. Install OpenSSH server in Windows Server:
   - Go to Apps & Features
   - Click "Optional Features"
   - Click "Add a feature"
   - Check "OpenSSH Server"
2. Configure OpenSSH server:
   - Create dedicated service account
   - Configure authentication methods
   - Set up SFTP chroot directory
3. Configure firewall:
   - Allow inbound port 22 (SSH)
   - Restrict access to specific IP ranges
4. Set up user accounts:
   - Create SFTP users
   - Configure user permissions
   - Set up public key authentication
5. Configure logging and monitoring:
   - Enable detailed logging
   - Set up log rotation
   - Configure alerts for failed login attempts

# System Installation Schedule and Result

## System Installation Schedule

The following table summarises the testing schedule:

| Pre-Requisite | Start Date | End Date | Start time | End Time |
|---------------|------------|----------|------------|----------|
| Database Server Installation (Production and DR) |  |  |  |  |
| Backend Server Installation (Production and DR) |  |  |  |  |
| Frontend Server Installation (Production and DR) |  |  |  |  |
| Functionality test (VM & Networking) |  |  |  |  |
| Database setup |  |  |  |  |
| Deployment for 1st version of frontend server |  |  |  |  |
| Deployment for 1st version of backend server |  |  |  |  |
| Application Health Check |  |  |  |  |
| Deployment for Latest Mobile Application |  |  |  |  |
| Final Check Production Web Server |  |  |  |  |
| Final Check Production Database Server |  |  |  |  |
| Final Check DR Web & Database server |  |  |  |  |
| Final Check IIS & Framework |  |  |  |  |

## System Installation Result

The following table summarises the actual system installation schedule:

| Pre-Requisite | Actual Start Date | Actual End Date | Actual Start time | Actual End Time | Status/Result |
|---------------|-------------------|-----------------|-------------------|-----------------|---------------|
| Database Server Installation (Production, UAT and DR) |  |  |  |  |  |
| Backend Server Installation (Production, UAT and DR) |  |  |  |  |  |
| Frontend Server Installation (Production, UAT and DR) |  |  |  |  |  |
| Functionality test (VM & Networking) |  |  |  |  |  |
| Database setup |  |  |  |  |  |
| Deployment for 1st version of frontend server |  |  |  |  |  |
| Deployment for 1st version of backend server |  |  |  |  |  |
| Application Health Check |  |  |  |  |  |
| Deployment for Latest Mobile Application |  |  |  |  |  |
| Final Check Production Web Server |  |  |  |  |  |
| Final Check Production Database Server |  |  |  |  |  |
| Final Check DR Web & DB server |  |  |  |  |  |
| Final Check IIS & Framework |  |  |  |  |  |

<<End of Document>>
