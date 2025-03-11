# Handover Plan - Licensing Self-Certification Portal (LSCP)

## Introduction

This Handover Plan outlines the transfer of the Licensing Self-Certification Portal (LSCP) system from Master Concept (Hong Kong) Limited (MC) to the Buildings Department (BD). This document serves as a comprehensive checklist of handover materials and provides essential information for the support and maintenance staff. It consolidates information from various sources and supersedes all previous drafts.

<img src="media/image1.jpg" alt="BDlogo" style="width:2.03125in;height:1.52083in" />

**HANDOVER PLAN**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**

**LICENSING SELF-CERTIFICATION PORTAL**

**FOR**

**BUILDINGS DEPARTMENT**

**Version: 1.0**

**January 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of, and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

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
<th colspan="6"><strong>Amendment History</strong></th>
</tr>
<tr>
<th>Change Number</th>
<th>Revision Description</th>
<th>Pages Affected</th>
<th>Revision Number</th>
<th>Date</th>
<th>Approved Reference</th>
</tr>
<tr>
<th>1</th>
<th>1st Draft</th>
<th>All</th>
<th>0.1</th>
<th>16/01/2024</th>
<th></th>
</tr>
<tr>
<th>2</th>
<th>Final Version</th>
<th>All</th>
<th>1.0</th>
<th>October 2025</th>
<th></th>
</tr>
</thead>
</table>

## Table of Contents

- [1. Environment Description](#environment-description)
- [2. Purpose and Scope](#purpose-and-scope)
    - [2.1 Schedule](#schedule)
    - [2.2 Verification](#verification)
- [3. Documentation](#documentation)
- [4. Program Source Code](#program-source-code)
- [5. Administration Accounts Checklist](#administration-accounts-checklist)
- [6. Security and Backup](#security-and-backup)
    - [6.1 Backup](#backup)
    - [6.2 Security](#security)
    - [6.3 Change Control](#change-control)
    - [6.4 Disaster Recovery](#disaster-recovery)
    - [6.5 Database Backup Strategy](#database-backup-strategy)
- [7. Outstanding Items/Issues](#outstanding-itemsissues)
- [8. Licensed Software](#licensed-software)
- [9. System Summary](#system-summary)
    - [9.1 Objective](#objective)
    - [9.2 System Architecture](#system-architecture)
    - [9.3 System Functions](#system-functions)
- [10. Equipment Configuration](#equipment-configuration)
    - [10.1 Computer Hardware](#computer-hardware)
    - [10.2 Guest Servers Components](#guest-servers-components)
    - [10.3 Gateway and SMTPX Configuration](#gateway-and-smtpx-configuration)
    - [10.4 Database Configuration](#database-configuration)
    - [10.5 Detailed Server and Network Configurations](#detailed-server-and-network-configurations)
- [11. Software Inventories](#software-inventories)
    - [11.1 Inventory of Application Programs](#inventory-of-application-programs)
    - [11.2 Inventory of System Software and Software Package](#inventory-of-system-software-and-software-package)
- [12. Database Administration](#database-administration)
    - [12.1 Clean Database Transaction Logs](#clean-database-transaction-logs)
    - [12.2 Database Backup](#database-backup-1)
    - [12.3 System Constraints and Limitations](#system-constraints-and-limitations)
- [13. Log Management](#log-management)


## 1. Environment Description

The LSCP system is deployed across multiple environments, including Production, User Acceptance Testing (UAT), Development (DEV), and Disaster Recovery (DR).  These environments are distributed across on-premise infrastructure at West Kowloon Government Offices (WKGO) and the Government Cloud Infrastructure Services (GCIS).  Detailed diagrams and IP addresses for each environment will be provided separately due to security considerations.  Please refer to Appendix A for the list of machines and virtual machines.

## 2. Purpose and Scope

This document serves as a comprehensive checklist for the handover of the LSCP system from MC to BD. It details all deliverables and provides essential information for the support and maintenance staff.  The handover encompasses documentation, source code, administration accounts, backups, hardware specifications, and software licenses.

### 2.1 Schedule

| Action       | Date           | Action Parties |
|--------------|----------------|----------------|
| Handover     | October 26, 2025 | MC/BD          |
| Verification | November 9, 2025  | BD             |

### 2.2 Verification

1. **Application URL Verification:** BD will verify access to each application URL.
2. **Login Accounts Verification:** BD will verify login credentials for applications and servers.  Credentials will be handed over through a secure, out-of-band process.

## 3. Documentation

The following documentation will be provided:

| Document                             | File Name             | Version |
|--------------------------------------|-----------------------|---------|
| System Architecture & Design (SA&D) Report | SA&D_LSCP_v1.0.pdf    | 1.0     |
| Project Initiation Document (PID)    | PID_LSCP_v1.0.pdf     | 1.0     |
| ...                                 | ...                   | ...     |
| Project Evaluation Report            | PER_LSCP_v1.0.pdf     | 1.0     |
| System Manual                        | System_Manual_v1.0.pdf | 1.0     |


## 4. Program Source Code

Source code will be provided via a secure repository. Access details will be provided separately.  The repository structure will mirror the component breakdown below:

| Component            |  Repository Path |
|----------------------|-------------------|
| Frontend Application | /frontend         |
| Backend Application  | /backend          |
| Mobile Application   | /mobile           |


## 5. Administration Accounts Checklist

Administrative account details will be provided separately through a secure, out-of-band process.  This separation ensures the confidentiality of sensitive credentials.


## 6. Security and Backup

### 6.1 Backup

Backup procedures are detailed in Section 8 of the System Manual.  Key highlights include:

* **VM Backup:** Daily VM image backups are performed using Veeam Backup & Replication and stored on dedicated backup servers. Copies of production VM images are also stored in the DR environment.
* **Database Backup:** Daily full database backups are performed on all database servers.  These backups are stored locally and also included in the VM backups.  GCIS environments leverage GCIS-provided backup services with offsite copies and replication to the DR site.

### 6.2 Security

Security measures are detailed in Section 8 of the System Manual.  Key highlights include:

* **Data Transmission Security:** All data transmission is encrypted using HTTPS over TLS.  Certificates from the Hong Kong Post and OGCIO's Intranet Server Certificate Certification Authority (ISCCA) are used.
* **Data Storage Security:** Data at rest is encrypted and stored on SAN storage in the production environment and local storage in the DR environment. RAID configurations provide redundancy and fault tolerance.
* **System Security:** Regular security patching and antivirus software are implemented on all servers.
* **Access Control:** Access to the LSCP is controlled through the Departmental Portal (OSDP) for internal users and iAM Smart authentication for external users.  Role-based access control restricts user privileges within the application.

### 6.3 Change Control

All code changes are managed using Git version control.  Detailed change control procedures are outlined in the Computer Operation Procedures Manual (COPM).

### 6.4 Disaster Recovery

Disaster recovery procedures are detailed in Section 8 of the System Manual.  Key highlights include:

* **GCIS:** Automatic failover to GCIS P2 is implemented using VM Site Recovery Manager.
* **On-Premise:** NGINX reverse proxy provides load balancing and failover for on-premise servers.  VM replication to the DR environment is performed using Veeam.

### 6.5 Database Backup Strategy

Database backup and recovery procedures are detailed in Sections 8 and 9 of the System Manual.  Daily full backups are performed, and recovery procedures are documented for various failure scenarios.


## 7. Outstanding Items/Issues

None.


## 8. Licensed Software

| Item                                      | Quantity | Expiry/License Type |
|-------------------------------------------|----------|--------------------|
| Windows Server 2022 Standard             |  As Required | Perpetual/Volume    |
| SQL Server 2022 Standard                 |  As Required | Perpetual/Volume    |
| Veeam Backup & Replication 12             |  As Required | Perpetual/Subscription |
| ESET Server Security                      |  As Required | Subscription        |
| Kiwi Syslog Server NG                     |  As Required | Perpetual/Subscription |
| VMware vSphere 8                          |  As Required | Subscription        |
| VMware vCenter 8                          |  As Required | Subscription        |


## 9. System Summary

### 9.1 Objective

The LSCP aims to provide an electronic platform for BD officers and public users to manage and review site inspection and monitoring records.

### 9.2 System Architecture

Please refer to Section 5.2 of the System Manual for a detailed description and diagrams of the system architecture.

### 9.3 System Functions

Please refer to Section 5.3 of the System Manual for a comprehensive list of system functions.


## 10. Equipment Configuration

### 10.1 Computer Hardware

Please refer to Section 6.1 of the System Manual for detailed hardware specifications.

### 10.2 Guest Servers Components

Please refer to Section 6.1.2 of the System Manual for detailed guest server configurations.

### 10.3 Gateway and SMTPX Configuration

Please refer to Section 6.1.3 of the System Manual for gateway and SMTPX configuration details.

### 10.4 Database Configuration

Please refer to Section 6.1.4 of the System Manual for database configuration details.

### 10.5 Detailed Server and Network Configurations

Please refer to Section 6.1.5 of the System Manual for detailed server and network configurations.


## 11. Software Inventories

### 11.1 Inventory of Application Programs

Please refer to the Program Manual for details of application programs.

### 11.2 Inventory of System Software and Software Package

Please refer to Section 7 of the System Manual for a comprehensive software inventory.


## 12. Database Administration

### 12.1 Clean Database Transaction Logs

Please refer to Section 9.1 of the System Manual for instructions on cleaning database transaction logs.

### 12.2 Database Backup

Please refer to Section 9.2 of the System Manual for instructions on performing database backups.

### 12.3 System Constraints and Limitations

Please refer to Section 9.3 of the System Manual for system constraints and limitations.


## 13. Log Management

Please refer to Section 10 of the System Manual for details on log management procedures.


## Appendix A: List of Machines and Virtual Machines

(Detailed list of machines and VMs with hostnames, purposes, and IP addresses will be provided separately due to security considerations.)
