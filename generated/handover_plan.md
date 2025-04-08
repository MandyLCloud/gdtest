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
[2. Purpose](#purpose)
    [2.1 Schedule](#schedule)
    [2.2 Verification](#verification)
[3. Documentation](#documentation)
[4. Program Source Code](#program-source-code)
[5. Administration Accounts Checklist](#administration-accounts-checklist)
[6. Backup](#backup)
    [6.1 VM Backup](#vm-backup)
    [6.2 Database Backup](#database-backup)
    [6.3 Backup Schedule](#backup-schedule)
[7. Outstanding Items/Issues](#outstanding-itemsissues)
[8. Licensed Software](#licensed-software)
[9. System Overview](#system-overview)
    [9.1 Objective](#objective)
    [9.2 System Architecture](#system-architecture)
    [9.3 System Functions](#system-functions)
[10. Equipment Configuration](#equipment-configuration)
    [10.1 Computer Hardware](#computer-hardware)
        [10.1.1 Hardware Components](#hardware-components)
        [10.1.2 Guest Servers Components](#guest-servers-components)
        [10.1.3 Gateway and SMTPX Configuration](#gateway-and-smtpx-configuration)
        [10.1.4 Database Configuration](#database-configuration)
        [10.1.5 Detailed Server and Network Configurations](#detailed-server-and-network-configurations)
[11. Software Inventories](#software-inventories)
    [11.1 Inventory of Application Programs](#inventory-of-application-programs)
    [11.2 Inventory of System Software and Software Package](#inventory-of-system-software-and-software-package)
[12. Security](#security)
    [12.1 System Control](#system-control)
    [12.2 Data Transmission Security](#data-transmission-security)
    [12.3 Data Storage and Auditing Security](#data-storage-and-auditing-security)
    [12.4 System Security](#system-security)
    [12.5 Physical Security](#physical-security)
    [12.6 Password and Group Control](#password-and-group-control)
    [12.7 Control Procedure of Application User Account and Production Support Account](#control-procedure-of-application-user-account-and-production-support-account)
[13. Change Control](#change-control)
[14. Disaster Recovery](#disaster-recovery)
[15. Database Administration](#database-administration)
    [15.1 Clean Database Transaction Logs](#clean-database-transaction-logs)
    [15.2 Database Backup](#database-backup-admin)
    [15.3 System Constraints and Limitations](#system-constraints-and-limitations)
[16. Log Management](#log-management)

# 1. Environment Description

This section describes the Production, UAT (User Acceptance Testing), and DR (Disaster Recovery) environments for the Licensing Self-Certification Portal (LSCP).

**Production and UAT environment:**

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

**DR environment:**

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

This document serves as a checklist for all handover materials within the project scope of the Licensing Self-Certification Portal (LSCP). It also provides essential information for the Buildings Department (BD) support and maintenance staff who will be responsible for the system's upkeep in the future. The deliverables listed herein are to be provided by the system implementation team of the LSCP, Master Concept (MC), to the Buildings Department (BD) of the Government of the Hong Kong Special Administrative Region (HKSARG or the Government).

The key handover items for this project are categorized as follows:

1. Documentation
2. Program Source code (Backend Application, Frontend Web App, Frontend Mobile App)
3. Administration Accounts
4. System backup
5. Hardware (Detailed in Equipment Configuration Section)
6. Software Packages and Licenses (Detailed in Licensed Software and Software Inventory Sections)

## 2.1 Schedule

The following table outlines the planned schedule for the handover process:

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |

**Note:** Specific dates for Handover and Verification will be determined and updated in subsequent versions of this document.

## 2.2 Verification

To ensure a successful handover, the following verification steps will be performed by the Buildings Department (BD):

1.  **Application URL Verification**
    > The accessibility of each application will be verified by accessing its designated URL. This confirms that the applications are deployed and reachable on the network.

2.  **Login Accounts Verification**
    > The provided login accounts for applications and servers will be verified by successfully logging in. This ensures that the administrative accounts are functional and access credentials are valid.

# 3. Documentation

This section lists the documents to be handed over to the Buildings Department (BD). These documents are crucial for understanding, operating, and maintaining the LSCP system.

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

**Note:** File Names and Versions for each document will be provided in subsequent versions of this document as they are finalized.

# 4. Program Source Code

This section outlines the program source code components that will be handed over. Access to the source code is essential for future system modifications, enhancements, and maintenance.

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |
|                      |         |           |

**Note:** Specific Machine names and Directory paths for each component will be provided in subsequent versions of this document. This information will detail where the source code repositories are located.

# 5. Administration Accounts Checklist

This section provides a checklist for the administration accounts required for managing the LSCP system infrastructure and application. It is crucial to ensure that all necessary accounts are handed over and properly documented.

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

**Administration Accounts on LSCP Application**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |
|             |           |              |          |

**Note:** User accounts and Passwords for each system component and application environment will be provided securely and documented separately during the handover process. This section serves as a checklist to ensure all necessary accounts are handed over.

# 6. Backup

<span class="mark">[RY Note: Following content needs to check]</span>

This section describes the backup procedures and strategy for the LSCP system, ensuring data integrity and availability in case of system failures or disasters.

## 6.1 VM Backup

VM (Virtual Machine) backup services are managed by dedicated backup servers.

Daily VM image backups are performed and stored on backup servers. Additionally, a copy of production VM images is transferred to the Disaster Recovery (DR) site's backup server for redundancy.

## 6.2 Database Backup

Database backups are performed to ensure data recoverability. Two types of database backups are implemented:

**Database Full Export Backup:** This comprehensive backup method exports all database objects, including schemas, table structures, packages, stored procedures, and data.

Daily full export backups are conducted on the database servers. The backup data is initially stored on the DB servers and is further backed up through VM Backup processes.

## 6.3 Backup Schedule

The following table summarizes the backup schedule for the LSCP system:

| Name                                    | Schedule                                        |
|-------------------------------------|-----------------------------------|
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

**Note:** This section will be updated if any outstanding items or issues are identified during the handover process.

# 8. Licensed Software

<span class="mark">[RY Note: Items are for reference only. They are
incorrect]</span>

This section lists the licensed software utilized in the LSCP system. Ensuring the validity and transfer of these licenses is crucial for continued system operation.

| Item                                                                              | Amount | Expire At |
|------------------------|------------------------|------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual                                            |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

**Note:** Specific amounts and expiry dates for each licensed software will be verified and updated in subsequent versions of this document. Refer to the Software Inventory section for a detailed list of software installed.

# 9. System Overview

This section provides a summary of the Licensing Self-Certification Portal (LSCP) system, including its objectives, architecture, and key functions. This overview is intended to provide a high-level understanding of the system for support and maintenance staff.

## 9.1 Objective

The LSCP system caters to two primary user categories:

-   **Buildings Department (BD) Officers:** Internal users responsible for managing and reviewing inspection and monitoring records.
-   **Public Users:** External users involved in site inspections and site monitoring, who utilize the portal to provide and manage inspection and monitoring records.

The primary objective of the LSCP is to provide a digital platform for site inspection and monitoring personnel to efficiently manage, submit, and review inspection and monitoring records electronically. This aims to streamline processes, improve data management, and enhance overall efficiency in building licensing self-certification.

## 9.2 System Architecture

The LSCP system is deployed across two data centers:

-   **On-Premise (WKGO):** Located at West Kowloon Government Offices (WKGO).
-   **Government Cloud Infrastructure Services (GCIS):** Utilizing government cloud services.

**Production Environment Architecture:**

\[System Architecture Diagram - Production Environment - Image from sm_i1.md - media/image2.png]

**Production and UAT Site Architecture:**

\[System Architecture Diagram - Production and UAT Site - Image from sm_i1.md - media/image3.png]

**Disaster Recovery Environment Architecture:**

\[System Architecture Diagram - Disaster Recovery Environment - Image from sm_i1.md - media/image5.png]

**Key Architectural Components:**

*   **Firewalls:** Palo Alto PA-850 firewalls are used in both Production and DR sites to secure the network perimeter.
*   **Reverse Proxy Servers:** Nginx reverse proxy servers are deployed for load balancing and enhanced security, managing incoming requests to web servers.
*   **Web Application Firewall (WAF):**  Deployed in front of the internet DMZ (iDMZ) in GCIS for increased security access.
*   **External Application Servers:** Host static web content (HTML, CSS, JavaScript) and proxy backend API requests. Built using React framework and served by IIS.
*   **External Web Servers:** Host backend APIs responsible for business logic and database operations. Developed using ExpressJS and run on IIS.
*   **BD Web Servers:** Internal portal for BD users, using the same technology stack as External Application Servers but deployed in internal zones.
*   **Database Management Servers:** Microsoft SQL Server database engine is used for both internal and external LSCP applications.
*   **Log Servers:** Kiwi Syslog Servers are used to centralize and store system and application logs.
*   **File Servers:** Store temporary and permanent files for the system.
*   **vCenter Server:** Manages VM Hypervisors on physical servers in WKGO and DR sites.
*   **Backup Servers:** Veeam Backup servers for VM image backups and database backups.
*   **SAN Storage:** Dell PowerStore SAN storage in Production and DR WKGO sites for data storage.
*   **GCIS Cloud Infrastructure:** Utilizes GCIS for cloud-based components in Production, UAT and DR.

**Web Browser Support:**

\[Web Browser Support Table - Image from sm_i1.md - media/image4.png]

**Integration with External Systems:**

*   **iAM Smart:** Government authentication system for secure login and user information retrieval.
*   **Departmental Portal (OSDP):** BD's internal portal for user authentication within the BD intranet.
*   **SMTPX:** CIS provided SMTPX service for sending login OTPs and email notifications.
*   **MWMS:**  Provides data of AP/RSE/RGE/AS acknowledged by BD, interfaced via SFTP.
*   **BCIS:** Provides address data and BD case data, synced via SQL queries.

## 9.3 System Functions

The LSCP system provides a range of functions for both public users and BD officers. Key functions are listed below:

|               |                                                         |
|---------------|---------------------------------------------------------|
| Function ID   | Function Name                                           |
| UF-WEB-001-1  | Public User Authentication with Password                |
| UF-WEB-001-2  | Logout system to clear user session                     |
| UF-WEB-001-3  | Single User Session                                     |
| UF-WEB-001-4  | GEO and BD User Authentication                          |
| UF-WEB-001-5  | Public User Authentication with iAM Smart               |
| UF-WEB-001-6  | Forgot Password                                         |
| UF-WEB-001-7  | Change Password                                         |
| UF-WEB-001-8  | Public Users create/register an account                 |
| UF-WEB-001-9  | User Account Confirmation                               |
| UF-WEB-001-10 | Resend User Account Confirmation Email                  |
| UF-WEB-001-11 | User Account Detail Management                          |
| UF-WEB-001-12 | User Email Address Update Confirmation                  |
| UF-WEB-001-13 | Public User Accounts Management                         |
| UF-WEB-001-14 | BD User Accounts Management                             |
| UF-WEB-001-15 | Public User Account Password Policy                     |
| UF-WEB-002-1  | Assign TCPs                                             |
| UF-WEB-002-2  | Request TCP acceptance                                  |
| UF-WEB-002-3  | Notification for TCP assignment                         |
| UF-WEB-002-4  | Unassign TCPs                                           |
| UF-WEB-002-5  | Temporary replacement of Head of Stream                 |
| UF-WEB-002-6  | Temporary replacement of TCP                            |
| UF-WEB-002-7  | Resignation of Head of Stream by BD officer             |
| UF-WEB-002-8  | Notification of Head of Stream resignation              |
| UF-WEB-003-1  | Listing out responsible Inspection Form                 |
| UF-WEB-003-2  | Listing out responsible Site-Monitoring Schemes         |
| UF-WEB-004-1  | Form record submission and amendment                    |
| UF-WEB-004-2  | Search responsible Site Project                         |
| UF-WEB-004-3  | Create Site Project from the submitted Supervision plan |
| UF-WEB-004-4  | Edit and update Site Project Detail                     |
| UF-WEB-004-5  | List out Site Project                                   |
| UF-WEB-004-6  | View Site Project Detail                                |
| UF-WEB-004-7  | Supervision Plan Detail View                            |
| UF-WEB-004-8  | Supervision Plan Detail Management                      |
| UF-WEB-004-9  | Import SMIS Excel into CDPSS                            |

# 10. Equipment Configuration

This section details the equipment configuration for the LSCP system, providing a comprehensive inventory of hardware components in both Production and Disaster Recovery (DR) sites.

## 10.1 Computer Hardware

### 10.1.1 Hardware Components

**Production Site (WKGO) Physical Server Configuration:**

|                            |                         |                             |                |                        |
|----------------------------|-------------------------|-----------------------------|----------------|------------------------|
| **Model**                  | **Host Name**           | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750 Server | prd-scs-admin-server-01 | 192.168.10.22, 10.5.161.206 | F646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-admin-server-02 | 192.168.10.23, 10.5.161.207 | D646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-nas             | 192.168.10.35, 10.5.161.218 | ???            | ???                    |

**Production Site (WKGO) SAN Storage Configuration:**

|             |                      |                |                       |                                                            |
|----------------|---------------|--------------|--------------|---------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CC    | N/A                   | 192.168.10.16                                              |
| SAN Switch  | Dell DS6610B         | FRC1924T0CD    | N/A                   | 192.168.10.17                                              |
| SAN Storage | Dell PowerStore 500T | HV1NBX3        | 11                    | 192.168.10.26, 192.168.10.27, 192.168.10.28, 192.168.10.29 |

**Production Site (WKGO) Backup Storage Configuration:**

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|----------------|---------------|--------------|--------------|---------------|
| Backup Appliance | Dell DataDomain 3300 | 17XMBX3        | 15TB            | 192.168.10.20  |

**Production Site (WKGO) Tape Library Configuration:**

| **Type**     | **Model** | **Serial No.** | **No. of slots** | **IP Address** |
|--------------|-----------|----------------|------------------|----------------|
| Tape Library | Dell ML3  | 3555L3A7801YY0 | 35               | 192.168.10.20  |

**Production Site (WKGO) Firewall Configuration:**

|               |                 |                 |                  |                |
|-----------------|-----------------|-----------------|------------------|-----------------|
| **Host Name**   | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSPri | 192.168.10.12   | 10.5.161.205    | Palo Alto PA-850 | 11901063047    |
| PA-850-SCSSec | 192.168.10.13   | 10.5.161.220    | Palo Alto PA-850 | 11901063049    |

**Production Site (WKGO) Switch Configuration:**

| **Host Name** | **Internal IP** | **Model** | **Serial No.** |
|-----------------|-----------------|-----------|----------------|
|               | 192.168.10.14   | Catalyst  |                |
|               | 192.168.10.15   | Catalyst  |                |

**Production Site (WKGO) KVM Configuration:**

|            |                |
|------------|----------------|
| **Model**  | **Serial No.** |
| Cyber View |                |

**Production Site (WKGO) UPS Configuration:**

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010008 | 192.168.11.20  |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010004 | 192.168.11.21  |

**Hardware Components of Production Servers (WKGO):**

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