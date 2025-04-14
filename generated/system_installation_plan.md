# System Installation Plan

This document outlines the plan for installing the Licensing Self-Certification Portal (LSCP) system for the Buildings Department (BD).  It covers the introduction, project environment, deployment procedures, and installation schedule.  This plan is based on version 0.1, dated January 2025.

**? The Government of the Hong Kong Special Administrative Region**

The contents of this document remain the property of and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

## Distribution

| Copy No. | Holder                                  |
|----------|-----------------------------------------|
| 1        | Buildings Department (BD)               |
| 2        | Master Concept (Hong Kong) Limited (MC) |

## Amendment History

| Change Number | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date       | Approval Reference |
|---------------|----------------------|---------------------------------------|---------------------------|------------|--------------------|
| 1             | 1st draft            | All                                   | 0.1                       | 16/01/225  |                    |
|               |                      |                                       |                           |            |                    |
|               |                      |                                       |                           |            |                    |
|               |                      |                                       |                           |            |                    |
|               |                      |                                       |                           |            |                    |
|               |                      |                                       |                           |            |                    |

## Table of Contents

1.  [Introduction](#introduction)
2.  [Project Environment Description](#project-environment-description)
    *   [Network Diagram](#network-diagram)
    *   [Hardware Specification](#hardware-specification)
    *   [Software Specification](#software-specification)
3.  [Application Deployment Procedure for Production](#application-deployment-procedure-for-production)
    *   [Database Server](#database-server)
    *   [Backend Servers](#backend-servers)
    *   [Frontend Servers](#frontend-servers)
        *   [sFTP Server Setup](#sftp-server-setup)
4.  [System Installation Schedule and Result](#system-installation-schedule-and-result)
    *   [System Installation Schedule](#system-installation-schedule)
    *   [System Installation Result](#system-installation-result)

## 1. Introduction

The System Installation plan describes the procedure and schedule for deploying the application in the production environment. The system comprises three main parts:

*   Database Server
*   Backend Server
*   Frontend and Web Portal Server

## 2. Project Environment Description

### 2.1 Network Diagram

Below is a logical network diagram in 1/F West Kowloon Government Office for production and UAT site.

`[DIAGRAM HERE]`

The network is separated into three zones: DMZ, trusted zone, and storage network.

A two-tier firewall setup is used to form the trusted zone and DMZ. Incoming network traffic to the system must go through the DMZ before entering the trusted zone.

To utilize hardware resources more effectively, servers, except the backup server, are set up as virtual machines (VM) and consolidated into DMZ VM host servers and trusted zone VM host servers for each physical site. Two VM host servers are built in each zone for high availability.

Storage needed by all servers is consolidated and provided by SAN storage. A dedicated network interconnects with the VM host servers. The backup server also exists in this storage-dedicated network to carry out backup tasks of VM host servers in DMZ and trusted zone.

The diagram below illustrates the physical setup.

### 2.2 Hardware Specification

**Production and UAT environment:**

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|-----------------------------|-----------------------------|---------|----|
|                             |                             |         |    |
|                             |                             |         |    |
|                             |                             |         |    |
|                             |                             |         |    |
|                             |                             |         |    |
|                             |                             |         |    |
|                             |                             |         |    |
|                             |                             |         |    |

**DR environment:**

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|-----------------------------|-----------------------------|---------|----|
|                             |                             |         |    |
|                             |                             |         |    |
|                             |                             |         |    |
|                             |                             |         |    |
|                             |                             |         |    |

### 2.3 Software Specification

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

## 3. Application Deployment Procedure for Production

### 3.1 Database Server

To install the database server, follow these steps:

1.  Remote login to PRD-DB-01(10.5.113.218).

### 3.2 Backend Servers

1.  Remote login into PRD-WEBAPP-01.

### 3.3 Frontend Servers

1.  Remote login into PRD-WEBAPP-01.

#### 3.3.1 sFTP Server Setup

1.  Install OpenSSH server in Windows Server. Go to Apps & Features,
    > Click ?Optional Features?, click ?Add a feature?, check ?OpenSSH
    > Server?

## 4. System Installation Schedule and Result

### 4.1 System Installation Schedule

The following table summarizes the testing schedule:

| Pre-Requisite                                            |     | Start Date | End Date | Start time | End Time |
|----------------------------------------------------------|-----|------------|----------|------------|----------|
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

### 4.2 System Installation Result

The following table summarizes the actual system installation schedule:

| Pre-Requisite                                            |     | Actual Start Date | Actual End Date | Actual Start time | Actual End Time | Status/Result |
|----------------------------------------------------------|-----|-------------------|-----------------|-------------------|-----------------|---------------|
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

<<End of Document>>
