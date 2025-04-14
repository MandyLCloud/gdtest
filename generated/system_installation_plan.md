# System Installation Plan

## 1. Introduction

This System Installation Plan (SIP) outlines the procedures and schedule for deploying the Licensing Self-Certification Portal (LSCP) application in the production environment. The system comprises three main parts:

*   Database Server
*   Backend Server
*   Frontend and Web Portal Server

This document is based on the User Requirements Specifications (URS) T223, System Manual (SM) and is intended for distribution to Buildings Department (BD) and Master Concept (Hong Kong) Limited (MC).

## 2. Project Environment Description

### 2.1 Network Diagram

A logical network diagram for the production and UAT sites at 1/F West Kowloon Government Office (WKGO) is shown below.

**[DIAGRAM HERE]**

The network is separated into three zones:

*   DMZ
*   Trusted Zone
*   Storage Network

A two-tier firewall setup forms the Trusted Zone and DMZ. Incoming network traffic must pass through the DMZ before entering the Trusted Zone.

Virtual machines (VMs) are used to utilize hardware resources effectively. Servers (except the backup server) are set up as VMs and consolidated into DMZ VM host servers and Trusted Zone VM host servers for each physical site. Two VM host servers are built in each zone for high availability.

Storage is consolidated and provided by SAN storage. A dedicated network interconnects with the VM host servers. The backup server resides in this storage-dedicated network to perform backup tasks of VM host servers in DMZ and Trusted Zone.

### 2.2 Hardware Specification

#### Production and UAT Environment:

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

#### DR Environment:

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

### 2.3 Software Specification

|  |  |  |  |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## 3. Application Deployment Procedure for Production

### 3.1 Database Server

To install the database server:

1.  Remote login to PRD-DB-01 (10.5.113.218).

### 3.2 Backend Servers

1.  Remote login into PRD-WEBAPP-01.

### 3.3 Frontend Servers

1.  Remote login into PRD-WEBAPP-01.

#### 3.3.1 sFTP Server Setup

1.  Install OpenSSH server in Windows Server. Go to Apps & Features, click ?Optional Features?, click ?Add a feature?, check ?OpenSSH Server?.

## 4. System Installation Schedule and Result

### 4.1 System Installation Schedule

The following table summarizes the planned testing schedule:

| Pre-Requisite |  | Start Date | End Date | Start Time | End Time |
|---|---|---|---|---|---|
| Database Server Installation (Production and DR) |  |  |  |  |  |
| Backend Server Installation (Production and DR) |  |  |  |  |  |
| Frontend Server Installation (Production and DR) |  |  |  |  |  |
| Functionality test (VM & Networking) |  |  |  |  |  |
| Database setup |  |  |  |  |  |
| Deployment for 1st version of frontend server |  |  |  |  |  |
| Deployment for 1st version of backend server |  |  |  |  |  |
| Application Health Check |  |  |  |  |  |
| 1 |  |  |  |  |  |
| Deployment for Latest Mobile Application |  |  |  |  |  |
| Final Check Production Web Server |  |  |  |  |  |
| Final Check Production Database Server |  |  |  |  |  |
| Final Check DR Web & Database server |  |  |  |  |  |
| Final Check IIS & Framework |  |  |  |  |  |

### 4.2 System Installation Result

The following table summarizes the actual system installation schedule:

| Pre-Requisite |  | Actual Start Date | Actual End Date | Actual Start Time | Actual End Time | Status/Result |
|---|---|---|---|---|---|---|
| Database Server Installation (Production, UAT and DR) |  |  |  |  |  |  |
| Backend Server Installation (Production, UAT and DR) |  |  |  |  |  |  |
| Frontend Server Installation (Production, UAT and DR) |  |  |  |  |  |  |
| Functionality test (VM & Networking) |  |  |  |  |  |  |
| Database setup |  |  |  |  |  |  |
| Deployment for 1st version of frontend server |  |  |  |  |  |  |
| Deployment for 1st version of backend server |  |  |  |  |  |  |
| Application Health Check |  |  |  |  |  |  |
| 1 |  |  |  |  |  |  |
| Deployment for Latest Mobile Application |  |  |  |  |  |  |
| Final Check Production Web Server |  |  |  |  |  |  |
| Final Check Production Database Server |  |  |  |  |  |  |
| Final Check DR Web & DB server |  |  |  |  |  |  |
| Final Check IIS & Framework |  |  |  |  |  |  |

<<End of Document>>