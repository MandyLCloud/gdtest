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
reproduced in whole or in part without the express permission of the Government of the HKSAR.

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
  <tbody></tbody>
</table>

**TABLE OF CONTENTS**

[1. Environment Description](#environment-description)
  * [1.1 Production and UAT Environment](#production-and-uat-environment)
  * [1.2 DR Environment](#dr-environment)
[2. Purpose](#purpose)
  * [2.1 Schedule](#schedule)
  * [2.2 Verification](#verification)
[3. Documentation](#documentation)
[4. Program Source Code](#program-source-code)
[5. Administration Accounts Checklist](#administration-accounts-checklist)
[6. Backup](#backup)
  * [6.1 VM Backup](#vm-backup)
  * [6.2 Database Backup](#database-backup)
[7. Outstanding Items/Issues](#outstanding-itemsissues)
[8. Licensed Software](#licensed-software)
[9. Database Administration](#database-administration)
  * [9.1 Clean Database Transaction Logs](#clean-database-transaction-logs)
  * [9.2 Database Backup](#database-backup-procedure)
[10. Log Management](#log-management)

# 1. Environment Description

This section describes the Production, UAT, and DR environments for the Licensing Self-Certification Portal (LSCP).

## 1.1 Production and UAT Environment

Production and UAT environments are hosted in two datacenters: On-premise (WKGO) and Government Cloud Infrastructure Services (GCIS).

**System Architecture Overview**

The system is designed with a multi-layered architecture for security and scalability.

<img src="media/image2.png" style="width:6.62605in;height:5.91667in" />

The architecture can also be visualized as follows:

<img src="media/image3.png" style="width:6.62605in;height:5.81944in" />

**WKGO (On-Premise)**:
The on-premise system at WKGO is behind an internal firewall with NAT, segmented into Production, UAT, and DEV subnets for internal users. A reverse proxy server with load balancing enhances security and distributes incoming requests to frontend web servers.

**GCIS (Government Cloud Infrastructure Services)**:
The GCIS environment is divided into Internet DMZ (iDMZ), Trusted Zone, and Gnet DMZ (gDMZ). Both iDMZ and gDMZ include reverse proxy servers and a Web Application Firewall (WAF) in front of the iDMZ for enhanced security.

**Key Components:**

*   **External Application Server**: Serves static web content (HTML, CSS, JavaScript) to the internet via IIS and proxies backend APIs to web application servers.
*   **External Web Server**: Hosts backend APIs (ExpressJS) for business logic and database operations, acting as an intermediary between the frontend and data storage.
*   **BD Web Servers**: Backend portal for internal BD users, utilizing the same technology stack as External Application Servers but deployed in different zones for security and internal access.
*   **Database Management Servers**: Microsoft SQL Server database engine for both internal and external LSCP applications.

**Web Browser Support**

<img src="media/image4.png" style="width:6.62605in;height:2.375in" />

**Integration with External Systems:**

*   **iAM Smart**: Provides secure login and user information retrieval.
*   **Departmental Portal**: BD web service for user identity pass-through within BD intranet.
*   **SMTPX**: CIS-provided SMTP service for OTP and email notifications.
*   **MWMS**: Provides AP/RSE/RGE/AS data snapshots via SFTP for batch processing.
*   **BCIS**: Provides address and BD case data, synced via SQL queries nightly and real-time for new BD cases.

**List of Machines and Virtual Machines (Production & UAT):**

**WKGO Production Environment:**

| **Hostname (Physical Machine)** | **Hostname (Virtual Machine)** | **Purpose**                     | **IP**                  |
|---------------------------------|--------------------------------|---------------------------------|-------------------------|
| prd-scs-admin-server-01         | prd-scs-vcenter-01             | vCenter Server                  | 192.168.10.24 / 10.5.161.210|
|                                 | prd-scs-log-01                 | Kiwi Log Server                 | 192.168.10.11 / 10.5.161.223|
|                                 | prd-scs-admin-api-01           | API Server                      | 192.168.12.11           |
|                                 | prd-scs-admin-frontend-01      | Frontend Server                 | 192.168.12.12           |
|                                 | prd-scs-admin-backend-01       | Backend Server                  | 192.168.12.13           |
|                                 | prd-scs-db-01                  | Database Server                 | 192.168.12.14           |
|                                 | prd-scs-filer                  | File Server                     | 192.168.12.20           |
|                                 | prd-scs-proxy                  | Reverse Proxy Server            | 192.168.12.15 / 10.5.161.226|
| prd-scs-admin-server-02         | prd-scs-backup-01              | Veeam Backup Server             | 192.168.10.25 / 10.5.161.211|
|                                 | prd-scs-esetnod32              | NOD32 Anti-Virus Server         | 192.168.10.34 / 10.5.161.215|
|                                 | prd-scs-admin-api-02           | API Server                      | 192.168.12.16           |
|                                 | prd-scs-admin-frontend-02      | Frontend Server                 | 192.168.12.17           |
|                                 | prd-scs-admin-backend-02       | Backend Server                  | 192.168.12.18           |
|                                 | prd-scs-db-02                  | Database Server                 | 192.168.12.19           |
| prd-scs-nas                     |                                | NAS                             | 192.168.10.35 / 10.5.161.218|

**GCIS Production Environment (P1):**

| **Hostname (Physical Machine)** | **Hostname (Virtual Machine)** | **Purpose**                     | **IP**                  |
|---------------------------------|--------------------------------|---------------------------------|-------------------------|
| GCIS Infrastructure             | scspwi                         | Reverse Proxy Server (Internet) | 192.168.0.6 / 45.119.92.84 |
|                                 | scspwg                         | Reverse Proxy Server (GNET)     | 192.168.4.6 / 10.160.11.211|
|                                 | scspad                         | Apps Server                     | 192.168.8.6             |
|                                 | scspdb                         | Database Server                 | 192.168.8.7             |
|                                 | scspbk2                        | Veeam Backup Server             | 192.168.8.9             |
|                                 | scsplog                        | Kiwi Log Server                 | 192.168.8.10            |

**WKGO UAT Environment:**

| **Hostname (Physical Machine)** | **Hostname (Virtual Machine)** | **Purpose**                     | **IP**                  |
|---------------------------------|--------------------------------|---------------------------------|-------------------------|
| prd-scs-admin-server-01         | uat-scs-admin-api-01           | API Server                      | 192.168.13.10           |
|                                 | uat-scs-admin-frontend-01      | Frontend Server                 | 192.168.13.11           |
|                                 | uat-scs-admin-backend-01       | Backend Server                  | 192.168.13.12           |
|                                 | uat-scs-db-01                  | Database Server                 | 192.168.13.13           |
|                                 | uat-scs-filer                  | File Server                     | 192.168.13.15           |
|                                 | uat-scs-proxy                  | Reverse Proxy Server            | 192.168.13.14 / 10.5.161.224|

**GCIS UAT Environment (T1):**

| **Hostname (Physical Machine)** | **Hostname (Virtual Machine)** | **Purpose**                     | **IP**                  |
|---------------------------------|--------------------------------|---------------------------------|-------------------------|
| GCIS Infrastructure             | scsuwi                         | Reverse Proxy Server (Internet) | 192.168.0.7 / 45.119.94.99 |
|                                 | scsuwg                         | Reverse Proxy Server (GNET)     | 192.168.4.7 / 10.148.11.220|
|                                 | scsuad                         | Apps Server                     | 192.168.8.9             |
|                                 | scsudb                         | Database Server                 | 192.168.8.10            |

## 1.2 DR Environment

The Disaster Recovery (DR) environment mirrors the Production environment to ensure business continuity in case of a disaster.

**System Architecture Overview (DR)**

The DR environment maintains a similar architecture to the production environment.

<img src="media/image5.png" style="width:6.62605in;height:6.44444in" />

**List of Machines and Virtual Machines (DR):**

**AIA DR Environment:**

| **Hostname (Physical Machine)** | **Hostname (Virtual Machine)** | **Purpose**                     | **IP**                  |
|---------------------------------|--------------------------------|---------------------------------|-------------------------|
| dr-scs-admin-server-01          | dr-scs-vcenter-01              | vCenter Server                  | 192.168.20.18 / 10.5.174.225|
|                                 | dr-scs-backup-01               | Veeam Backup Server             | 192.168.20.19 / 10.5.161.224|
|                                 | dr-scs-log-01                  | Kiwi Log Server                 | 192.168.20.10           |
|                                 | dr-scs-admin-api-01            | API Server                      | 192.168.22.11           |
|                                 | dr-scs-admin-frontend-01       | Frontend Server                 | 192.168.22.12           |
|                                 | dr-scs-admin-backend-01        | Backend Server                  | 192.168.22.13           |
|                                 | dr-scs-db-01                   | Database Server                 | 192.168.22.14           |
|                                 | dr-scs-filer                   | File Server                     | 192.168.22.16           |
|                                 | dr-scs-proxy                   | Reverse Proxy Server            | 192.168.22.15 / 10.5.174.228|
| dr-scs-nas                      |                                | NAS                             | 192.168.20.35 / 10.5.174.225|

**GCIS DR Environment (P2):**

| **Hostname (Physical Machine)** | **Hostname (Virtual Machine)** | **Purpose**                     | **IP**                  |
|---------------------------------|--------------------------------|---------------------------------|-------------------------|
| GCIS Infrastructure             | scspwi                         | Reverse Proxy Server (Internet) | 192.168.0.6 / 45.119.93.84 |
|                                 | scspwg                         | Reverse Proxy Server (GNET)     | 192.168.4.6 / 10.160.139.211|
|                                 | scspad                         | Apps Server                     | 192.168.8.6             |
|                                 | scspdb                         | Database Server                 | 192.168.8.7             |
|                                 | scspbk2                        | Veeam Backup Server             | 192.168.8.9             |
|                                 | scsplog                        | Kiwi Log Server                 | 192.168.8.10            |

# 2. Purpose

This document serves as a checklist for handover materials within the project scope. It also provides essential information for support and maintenance staff responsible for the ongoing maintenance of the Licensing Self-Certification Portal (LSCP). This handover ensures that all deliverables are properly transferred from the system implementation team of LSCP to the Buildings Department (BD) of the Government of the Hong Kong Special Administrative Region (HKSARG).

The hand-over items for this project are categorized as follows:

1.  Documentation
2.  Program Source code (Backend Application, Frontend Web App, Frontend Mobile App)
3.  Administration Accounts
4.  System backup
5.  Hardware (Covered in Environment Description)
6.  Software Packages and Licenses (Covered in Licensed Software)

## 2.1 Schedule

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |

## 2.2 Verification

The verification process ensures the proper functionality and accessibility of the system post-handover.

1.  **Application URL verification**
    > Verify access to each application by checking the access links (URLs).

2.  **Login accounts verification**
    > Verify login accounts for applications and servers by performing login actions.

# 3. Documentation

The following documents are to be handed over as part of the system delivery.

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

# 4. Program Source Code

Locations for program source code handover.

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |
|                      |         |           |

# 5. Administration Accounts Checklist

This section lists user accounts for system management across different areas.

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
  <tbody></tbody>
</table>

**Administration Accounts on LSCP**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |
|             |           |              |          |

# 6. Backup

<span class="mark">\[RY Note: Following content needs to check\]</span>

## 6.1 VM Backup

VM backup services are managed by dedicated backup servers.

*   **Daily VM Image Backup**: Performed daily and stored on backup servers.
*   **DR Copy**: Production VM images are copied to the DR site's backup server for redundancy.

## 6.2 Database Backup

*   **Database Full Export Backup**: Includes full database export of schemas, table structures, packages, stored procedures, and data.
*   **Daily Backup**: Full export backups are performed daily on DB servers and stored locally. These backups are further protected by VM backups.

**Backup Strategy Details (From System Manual)**

Production, UAT, and DEV environments at WKGO and DR at AIA are backed up by backup servers (prd-scs-backup-01 and dr-scs-backup-01).

*   **Backup Frequency**: Daily VM image backups, weekly backups to tape, and daily copies to AIA (for WKGO environments). GCIS environments are backed up by GCIS-provided services with offsite replication to DR GCIS P2.
*   **Scope**: All instances, including system files, database backups, and data files, are backed up as VM images managed by Veeam.
*   **Database Server Backup**: Database servers perform local database backups stored on local hard disks, which are then backed up by the VM backup server and copied to AIA.
*   **GCIS Backup**: Production environments on GCIS P1 are backed up by GCIS backup services with offsite copy and replication to DR GCIS P2. Production database servers on GCIS P1 also perform local backups, additionally backed up by Veeam backup server (scspbk2). UAT and DEV environments on GCIS are backed up by GCIS-provided services.

**Backup Schedule (From System Manual)**

|                                         | Schedule                                        |
|-----------------------------------------|-------------------------------------------------|
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

# 8. Licensed Software

<span class="mark">\[RY Note: Items are for reference only. They are incorrect\]</span>

| Item                                                                              | Amount | Expire At |
|-----------------------------------------------------------------------------------|--------|-----------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual                                            |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

# 9. Database Administration

This section provides procedures for database administration tasks.

## 9.1 Clean Database Transaction Logs

Procedure to clean up transaction logs to reclaim disk space:

1.  Login to the database server and launch SQL Server Management Studio (SSMS).
2.  Login to the database with an account having the `sysadmin` role.
3.  In SSMS, right-click the database "bd_scs" and select "Properties".
4.  Under "Options", change the "Recovery model" to "Simple".
5.  Click "OK" to apply the change.
6.  Right-click "bd_scs" again, navigate to "Tasks" -> "Shrink", and select "Files".
7.  Under "File type", select "Log".
8.  Under "Shrink action", select "Reorganize pages before releasing unused space", and click "OK".
9.  After shrinking, right-click "bd_scs", select "Properties", and under "Options", change the "Recovery model" back to "Full".

## 9.2 Database Backup

**Database Backup Procedure**

Steps to perform an additional database backup:

1.  In SSMS, right-click the database "bd_scs", and select "Tasks" -> "Back Up...".
2.  In the "Back Up Database - bd_scs" dialog, under "Destination", remove any existing backup destinations by clicking "Remove". Then, click "Add...".
3.  In the "Select Backup Destination" dialog, click the "..." button next to the "File name" input field. Choose the desired directory and enter a filename for the backup file, ensuring it ends with ".bak". Click "OK".
4.  Verify the backup destination is correctly selected, and then click "OK" in the "Back Up Database - bd_scs" dialog to start the backup process.
5.  Once the backup is complete, the ".bak" file will be located in the specified destination.

# 10. Log Management

**Log Management Policy**

1.  **Logged Activities**: The following activities are to be logged:
    *   Log-in attempts
    *   Unauthorized updates/access attempts
    *   Failed privilege elevation attempts
    *   Password change attempts
    *   Access attempts to critical files (e.g., configuration files, password files)
    *   Actions by privileged users
    *   Use of privileged rights (e.g., user account management)
    *   Security-related system failures and alerts
    *   Changes to user access rights
    *   Failed access attempts to critical systems and files
    *   Computer services usage (e.g., file copying, searching)
    *   Audit policy modifications
    *   Activation/de-activation of protection systems (e.g., anti-malware, IDS)

2.  **Log Retention and Management**:
    *   Logs are retained for **180 days**.
    *   Logs are centralized and managed by a Syslog server.
    *   Access to logs is restricted to authorized personnel.

3.  **Log Review**: Logs are reviewed regularly for security monitoring and audit purposes.

4.  **User Profiling Restriction**: Logs are not to be used for profiling individual user activity unless required for a necessary audit activity authorized by a Directorate rank officer.

\<\<\< End of document \>\>\>
```