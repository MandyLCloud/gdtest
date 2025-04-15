# Computer Operation Procedures Manual

## Purpose

This Computer Operation Procedures Manual (COPM) provides information and operating instructions related to the operation of the Licensing Self-Certification Portal (LSCP) computer system. It is intended for use by the operating staff of the relevant section. This manual is not intended to replace formal technical publications but provides specific details for this installation.

## Scope

This document serves as a guide for operating the system, outlining tasks monitored by the administrator to ensure proper system function. It addresses the operation of the system, including software and hardware configurations.

## Reference

*   System Installation Plan
*   Application Operation Manual

## Definitions and Conventions

### 4.1 Definitions

None specified.

### 4.2 Conventions

The following acronyms are used:

*   BD: Buildings Department
*   LSCP: Licensing Self-Certification Portal
*   DMZ: Demilitarized Zone
*   SAN: Storage Area Network
*   VM: Virtual Machine
*   ITU: Information Technology Unit
*   WKGO: West Kowloon Government Offices
*   AIA: Building Department office at AIA tower
*   ISCCA: Intranet Server Certificate Certification Authority

## 5. System Summary

### 5.1 Objective

The LSCP aims to provide an electronic platform for site inspection and monitoring personnel to manage and review records efficiently. It also allows applicants, Authorized Persons (AP), Registered Structure Engineers (RSE), and users in the Social Welfare Department (SWD) and Education Bureau (EDB) to submit application forms and documents electronically.

### 5.2 System Architecture

The system architecture comprises both on-premise (WKGO) and cloud-based (GCIS) components. The on-premise system is behind an internal firewall using NAT for subnet separation. A reverse proxy server with load balancing enhances security and distributes incoming requests to frontend web servers.

The GCIS system is divided into Internet DMZ (iDMZ), Trusted Zone, and Gnet DMZ (gDMZ), each with reverse proxy servers and a Web Application Firewall (WAF).

*   **External Application Server:** Serves static web content and proxies backend APIs.
*   **External Web Server:** Hosts the backend API, handling business logic and database operations.
*   **BD Web Servers:** Provide access to the internal BDSCS application for BD users via the Departmental Portal (OSDP).
*   **Database Management Servers:** Utilize Microsoft SQL Server for data storage.

### 5.3 System Functions

The system provides the following functions:

*   UF-WEB-001-1: Public User Authentication with Password
*   UF-WEB-001-2: Logout system to clear user session
*   UF-WEB-001-3: Single User Session
*   UF-WEB-001-4: GEO and BD User Authentication
*   UF-WEB-001-5: Public User Authentication with iAM Smart
*   UF-WEB-001-6: Forgot Password
*   UF-WEB-001-7: Change Password
*   UF-WEB-001-8: Public Users create/register an account
*   UF-WEB-001-9: User Account Confirmation
*   UF-WEB-001-10: Resend User Account Confirmation Email
*   UF-WEB-001-11: User Account Detail Management
*   UF-WEB-001-12: User Email Address Update Confirmation
*   UF-WEB-001-13: Public User Accounts Management
*   UF-WEB-001-14: BD User Accounts Management
*   UF-WEB-001-15: Public User Account Password Policy
*   UF-WEB-002-1: Assign TCPs
*   UF-WEB-002-2: Request TCP acceptance
*   UF-WEB-002-3: Notification for TCP assignment
*   UF-WEB-002-4: Unassign TCPs
*   UF-WEB-002-5: Temporary replacement of Head of Stream
*   UF-WEB-002-6: Temporary replacement of TCP
*   UF-WEB-002-7: Resignation of Head of Stream by BD officer
*   UF-WEB-002-8: Notification of Head of Stream resignation
*   UF-WEB-003-1: Listing out responsible Inspection Form
*   UF-WEB-003-2: Listing out responsible Site-Monitoring Schemes
*   UF-WEB-004-1: Form record submission and amendment
*   UF-WEB-004-2: Search responsible Site Project
*   UF-WEB-004-3: Create Site Project from the submitted Supervision plan
*   UF-WEB-004-4: Edit and update Site Project Detail
*   UF-WEB-004-5: List out Site Project
*   UF-WEB-004-6: View Site Project Detail
*   UF-WEB-004-7: Supervision Plan Detail View
*   UF-WEB-004-8: Supervision Plan Detail Management
*   UF-WEB-004-9: Import SMIS Excel into CDPSS

## 6. Equipment Configuration

### 6.1 Computer Hardware

#### 6.1.1 Hardware Components

**Hardware Components of Production Servers**

| Item | Hardware Component | Configuration | Qty |
|---|---|---|---|
|  | ESXi Hypervisor Server (prd-scs-admin-server-01) | Dell PowerEdge R750, Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz, 32GB DDR4, 1.2TB SAS HDD | 1 |
|  | ESXi Hypervisor Server (prd-scs-admin-server-02) | Dell PowerEdge R750, Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz, 32GB DDR4, 1.2TB SAS HDD | 1 |
|  | NAS (prd-scs-nas) | Dell PowerEdge R750, CPU???, RAM???, HDD???, Windows Server 2022 | 1 |
|  | SAN Switch (prd-scs-sw-01) | Dell DS6610B, Ports: 16 | 1 |
|  | SAN Switch (prd-scs-sw-02) | Dell DS6610B, Ports: 16 | 1 |
|  | SAN Storage (PS500T-Cluster1) | Dell PS500T, 3.8TB NVME SSD: 11 | 1 |
|  | Backup Appliance (prd-scs-backupstorage-01) | Dell DataDomain DD3300, 15TB | 1 |
|  | Tape Library | DELL ML3, 35 slots | 1 |
|  | Firewall (PA-850-SCSPri) | Palo Alto PA 850 | 1 |
|  | Firewall (PA-850-SCSSec) | Palo Alto PA 850 | 1 |
|  | Switch (???) | Cisco ??? | 1 |
|  | Switch (???) | Cisco ??? | 1 |
|  | KVM | CyberView | 1 |
|  | UPS (???) | Vertiv? Liebert? GXT5 3000 | 1 |
|  | UPS (???) | Vertiv? Liebert? GXT5 3000 | 1 |

#### 6.1.2 Guest Servers Components

**Production guest servers**

| Role | Host Name | vCPU | RAM (GB) | Disk (GB) | IP Addresses | Data Center | Host Server / Zone |
|---|---|---|---|---|---|---|---|
| vCenter | prd-scs-vcenter-01 | 16 | 39 | 1.33TB | 192.168.10.24 / 10.5.161.210 | WKGO | prd-scs-admin-server-01 |
| Veeam Backup Server | prd-scs-backup-01 | 8 | 24 | 300 + 1TB | 192.168.10.25 / 10.5.161.211 | WKGO | prd-scs-admin-server-02 |
| Kiwi Log Server | prd-scs-log-01 | 4 | 16 | 300 + 500 | 192.168.10.11 / 10.5.161.223 | WKGO | prd-scs-admin-server-01 |
| NOD32 Anti-Virus Server | prd-scs-esetnod32 | 4 | 16 | 300 | 192.168.10.34 / 10.5.161.215 | WKGO | prd-scs-admin-server-02 |
| API Server | prd-scs-admin-api-01 | 2 | 4 | 100 | 192.168.12.11 | WKGO | prd-scs-admin-server-01 |
| Frontend Server | prd-scs-admin-frontend-01 | 2 | 4 | 100 | 192.168.12.12 | WKGO | prd-scs-admin-server-01 |
| Backend Server | prd-scs-admin-backend-01 | 2 | 4 | 100 | 192.168.12.13 | WKGO | prd-scs-admin-server-01 |
| Database Server | prd-scs-db-01 | 8 | 16 | 100 + 500 | 192.168.12.14 | WKGO | prd-scs-admin-server-01 |
| File Server | prd-scs-filer | 2 | 4 | 100 + 1TB | 192.168.12.20 | WKGO | prd-scs-admin-server-01 |
| Reverse Proxy Server | prd-scs-proxy | 2 | 4 | 100 | 192.168.12.15 / 10.5.161.226 | WKGO | prd-scs-admin-server-01 |
| API Server | prd-scs-admin-api-02 | 2 | 4 | 100 | 192.168.12.16 | WKGO | prd-scs-admin-server-02 |
| Frontend Server | prd-scs-admin-frontend-02 | 2 | 4 | 100 | 192.168.12.17 | WKGO | prd-scs-admin-server-02 |
| Backend Server | prd-scs-admin-backend-02 | 2 | 4 | 100 | 192.168.12.18 | WKGO | prd-scs-admin-server-02 |
| Database Server | prd-scs-db-02 | 8 | 16 | 100 + 500 | 192.168.12.19 | WKGO | prd-scs-admin-server-02 |
| Reverse Proxy Server | scspwi | 2 | 8 | 100 | 192.168.0.6 / 45.119.92.84 | GCIS P1 | iDMZ |
| Reverse Proxy Server | scspwg | 2 | 8 | 100 | 192.168.4.6 / 10.160.11.211 | GCIS P1 | gDMZ |
| Apps Server | scspad | 4 | 16 | 100 + 500 | 192.168.8.6 | GCIS P1 | Trust Zone |
| Database Server | scspdb | 4 | 16 | 100 + 200 | 192.168.8.7 | GCIS P1 | Trust Zone |
| Veeam Backup Server | scspbk2 | 4 | 16 | 100 + 1TB | 192.168.8.9 | GCIS P1 | Trust Zone |
| Kiwi Log Server | scsplog | 2 | 8 | 100 + 100 | 192.168.8.10 | GCIS P1 | Trust Zone |

#### 6.1.3 Gateway and SMTPX Configuration

**SMTPX**

| Item | Description |
|---|---|
| SMTPX service hostname | smtpx.cis.hksarg (resolvable by CCGO DNS) |
| SMTPX service IP address | 10.106.5.103, 10.106.5.104, 10.106.105.103, 10.106.105.104 |
| SMTP port number | 587 |
| Sender IP address | (B/Ds' IP address within GNET) |
| Login and password | Not required |
| Authentication | By e-Certificate issued from Hong Kong Post or the Government ISCCA |
| Sender address in e-mail | Valid e-mail address registered in IMX service |
| Connection encryption | STARTTLS (Mandatory) |
| Compatible Protocols | SPF and DKIM |

SMTPX configured in the IIS 6.0 of the following servers: scspwg, scsuwg, scsdwg

**WKGO Production Network Gateway**

| Gateway | Subnet | IP Range | vlan / Zone |
|---|---|---|---|
| 192.168.10.1 | 255.255.255.0 | 192.168.10.1-254 | Management |
| 192.168.11.1 | 255.255.255.0 | 192.168.11.1-254 | Replication / Backup |
| 192.168.12.1 | 255.255.255.0 | 192.168.12.1-254 | Production |
| 192.168.13.1 | 255.255.255.0 | 192.168.13.1-254 | UAT |
| 192.168.14.1 | 255.255.255.0 | 192.168.14.1-254 | DEV |
| 10.5.161.1 | 255.255.255.0 | 10.5.161.205-235 | BD Network |

#### 6.1.4 Database Configuration

**WKGO Production:**

*   Windows Cluster: prd-scs-db-cl-01 192.168.12.21
*   Database Availability Group: prd-scs-db-agl 192.168.12.22
*   Replicas:
    *   prd-scs-db-01 192.168.12.14 (Primary)
    *   prd-scs-db-02 192.168.12.19 (Secondary)

**WKGO UAT:**

*   Database: uat-scs-db-01 192.168.13.13

**WKGO DEV:**

*   Database: dev-scs-db-01 192.168.14.13

**AIA DR:**

*   Database: dr-scs-db-01 192.168.22.14

**GCIS P1:**

*   Database: scspdb 192.168.8.7

**GCIS UAT:**

*   Database: scsudb 192.168.8.10

**GCIS DEV:**

*   Database: scsddb 192.168.8.8

**GCIS P2 DR:**

*   Database: scspdb 192.168.8.7

#### 6.1.5 Detailed Server and Network Configurations

*   Rack diagram (See original document)
*   External firewall (See original document)
*   Internal firewall (See original document)
*   Windows NLB (See original document)
*   Switches - Prod DMZ Port (See original document)
*   Switches - Prod INT SW Port (See original document)
*   Switches ? DR DMZ SW Port (See original document)
*   Switches ? DR INT SW Port (See original document)

## 7. Software Inventories

### 7.1 Inventory of Application Programs

For details of Application Programs for LSCP, please refer to Program Manual (T352).

### 7.2 Inventory of System Software and Software Package

**System Software of Production**

| Machine | Hostname | Software |
|---|---|---|
| NAS | prd-scs-nas | ??? |
| Veeam Backup Server | prd-scs-backup-01 | Windows Server 2022 21H2, VMware Tools 12.4.0.23259341, ESET Server Security 10.0.12012.0, ESET Management Agent 10.1.1292.0, Veeam Backup & Replication 12.1.2.172 |
| Kiwi Log Server | prd-scs-log-01 | Windows Server 2022 21H2, VMware Tools 12.4.0.23259341, ESET Server Security 10.0.12012.0, ESET Management Agent 10.1.1292.0, Kiwi Syslog Server NG 1.2.1.4 |
| NOD32 Anti-Virus Server | prd-scs-esetnod32 | Windows Server 2022 21H2, VMware Tools 12.4.0.23259341, ESET Server Security 10.0.12012.0, ESET Management Agent 10.1.1292.0, ESET PROTECT Server 11.0.199.0 |
| API Server | prd-scs-admin-api-01, prd-scs-admin-api-02 | Windows Server 2022 21H2, VMware Tools 12.4.0.23259341, ESET Server Security 10.0.12012.0, ESET Management Agent 10.1.1292.0 |
| Frontend Server | prd-scs-admin-frontend-01, prd-scs-admin-frontend-02 | Windows Server 2022 21H2, VMware Tools 12.4.0.23259341, ESET Server Security 10.0.12012.0, ESET Management Agent 10.1.1292.0, IIS 10.0.20348.1 |
| Backend Server | prd-scs-admin-backend-01, prd-scs-admin-backend-02 | Windows Server 2022 21H2, VMware Tools 12.4.0.23259341, ESET Server Security 10.0.12012.0, ESET Management Agent 10.1.1292.0 |
| Database Server | prd-scs-db-01, prd-scs-db-02 | Windows Server 2022 21H2, VMware Tools 12.4.0.23259341, ESET Server Security 10.0.12012.0, ESET Management Agent 10.1.1292.0, Microsoft SQL Server 2022 16.0.1000.6, Microsoft Management Studio 19.1 |
| File Server | prd-scs-filer | Windows Server 2022 21H2, VMware Tools 12.4.0.23259341, ESET Server Security 10.0.12012.0, ESET Management Agent 10.1.1292.0 |
| Reverse Proxy Server | prd-scs-proxy | Windows Server 2022 21H2, VMware Tools 12.4.0.23259341, ESET Server Security 10.0.12012.0, ESET Management Agent 10.1.1292.0, Nginx 1.26.2 |
| vCenter | prd-scs-vcenter-01 | vCenter 8.0.3 Build 24322831 |
| VM Host | prd-scs-admin-server-01, prd-scs-admin-server-02 | VMWare vSphere 8.0.3 Build 24022510 |

**System Software of DR**

| Machine | Hostname | Software |
|---|---|---|
| Kiwi Log Servers |  |  |
| Antivirus Server |  |  |
| DR Web Server (Static Content) 1 |  |  |
| DR Web Application Server 1 |  |  |
| DR BD Web Server 1 |  |  |
| DR Database Server (SQL Server) 1 |  |  |
| Backup Server |  |  |
| vCenter Server |  |  |
| VM Host |  |  |
| VM Host |  |  |

**System Software of UAT**

| Machine | Hostname | Software |
|---|---|---|
| UAT Web Server (Static Content) |  |  |
| UAT Web Application Server |  |  |
| UAT BD Web Server |  |  |
| UAT Database Server (SQL Server) |  |  |

## 8. Security and Backup

### 8.1 System Control

The system uses password control, OSDP for BD users, and OTP via email for external users. User access is limited based on assigned roles.

### 8.2 Backup

*   Daily VM image backup to backup storage.
*   Weekly backup to tape and daily copy to AIA.
*   Database servers perform local database backups and copy to AIA.
*   GCIS environments utilize backup services provided by GCIS with offsite copy and replication to DR GCIS P2.

### 8.3 Security

*   Data transmission is encrypted using HTTPS over TLS.
*   Data is stored in SAN storage with RAID mirroring and encryption.
*   Regular service pack and patch updates are performed.
*   Antivirus clients are installed and managed by a virtualized Antivirus Management server.
*   Access and audit controls to data are strictly controlled.

#### 8.3.1 Data Transmission Security

Data transmission over the network will be encrypted by HTTPS over TLS. Certificates will be applied to enable TLS on web servers.

#### 8.3.2 Data Storage and Auditing Security

Data is stored in SAN storage with RAID mirroring and encryption. Access and audit controls are strictly controlled.

#### 8.3.3 System Security

Regular service pack and patch updates are performed on operating systems and software. Antivirus clients are installed and managed by a virtualized Antivirus Management server.

#### 8.3.4 Physical Security

Servers and equipment are located in server rooms compliant with IT security guidelines.

#### 8.3.5 Password and Group Control

The LSCP is protected by password control, BD user is able to login via DP of the Buildings Department and Internet, if login via Internet, it requires to submit password plus a one- time password by Authenticator, otherwise only one password requires. Public user can login via Internet and iAM Smart app, login via Internet requires password plus a one-time password by email, login via iAM Smart app requires no password.

User are limited to access specific function, field, case and administrative authority by assignment of user group to user account.

#### 8.3.6 Control Procedure of Application User Account and Production Support Account

If user is new to the LSCP, user is required to register. For certain role, such as head of stream, user is required to provide their Registered Professionals or Contractors registration number. And all public user is required to provide HKID and check versus our database.

For external users, the LSCP implemented One-Time-Password token as secure login approach so that they can access the LSCP from their working locations for submission and retrieval of assignment details, and inspection results.

All information submitted by low level TCP staff will be vetted by Head of stream staff before saving as finalized records on the system.

To deliver on-going production support or change request, Application Maintenance Team may require to access the production servers for cause investigation, system/ application log collection or change request deployment. The Application Maintenance Team should seek the System Maintenance Committee?s approval by email. With the proof of authorization, ITU can help to login the servers, after that the Application Maintenance Team operates on the servers under the ITU?s monitoring. In case, the information/ operation can only be accessed/ executed under particular system account, the Application Maintenance Team should ask system account holder or designated person (Business Coordination Team member) to logon for his action.

### 8.4 Change Control

Program source code is maintained using GIT with version control.

### 8.5 Disaster Recovery

**GCIS**

*   **Automatic Failover:** If GCIS Prod 1 goes down, the GCIS Prod 2 disaster recovery (DR) environment will be automatically activated by the VM Site Recovery Manager.
*   **Virtual Machine Backups:** The virtual machines of GCIS Prod 1 will undergo daily overnight backups, with each backup retained for 30 days.
*   **Daily Database Backup:** A cron job is scheduled to export the GCIS Prod 1 database backup to the backup server every day at 22:00.

**BDSCS External (On-Prem):**

*   **Load Balancing with NGINX:** A NGINX Reverse Proxy/Load Balancer (running on ESXi) distributes traffic across two servers. In case one server becomes unavailable, traffic will automatically be redirected to the other server.
*   **Scheduled Database Backup:** A cron job runs daily at 18:30 to export the database.
*   **Backup Transfer:** At 19:00, the VM service will send the exported database backup to the production backup server.
*   **VM Replication to DR Environment:** All production virtual machines will be replicated to the disaster recovery (DR) environment using the VEEAM architecture, ensuring continuity in the event of a failure.

### 8.6 Database Backup Strategy

#### 8.6.1 SQL Database Backup

Database full export backup will be carried out as well. This type of backup contains full database export database objects including schemas, table structures, packages, stored procedures and data at 18:45 daily.

The daily full export backup is done on DB servers (uat-db-01, prd-db-01, prd-db-02, dr-db-01), data stored on the DB servers? directory: D:\backup\

#### 8.6.2 Recovery

The table below shows the impact, system recovery and the expected duration before the BDSCS is resumed to normal operation when various system failures occur.

| # | Failure Scenario | Impact | System Recovery | Total down time |
|---|---|---|---|---|
| 1 | System (hardware) failure of the primary database server | Production BDSCS services not available; All BDSCS users cannot use BDSCS | Pilot BDSCS needs to be setup using standby DB | ~1 hour |
| 2 | Electricity shortage on primary site | Production BDSCS services not available; All BDSCS users cannot use BDSCS | BDSCS needs to be setup using DR site | ~half day |
| 3 | System failure of either one of the App servers on primary site | According to the number of concurrent user, the performance may be degraded. | No effect on system availability | N/A |
| 4 | System failure of ALL App servers on primary site | Production BDSCS Web services not available; ALL BDSCS Web users cannot use BDSCS | BDSCS needs to be restored using App servers VM image backup | ~half day |
| 5 | Database connection failure since SQL database instance down | BDSCS services not available; ALL BDSCS users cannot use BDSCS | Restart SQL database instance | ~1 hour |
| 6 | Primary database crushed | No impact as it will failover to the secondary database | BDSCS needs to be setup using secondary DB | ~1 hour |
| 7 | System failure (hardware failure) on one of the VM servers | No impact as all VM Server is formed in cluster. If one have failure hardware failover will proceed automatically. | N/A | N/A |

#### 8.6.3 Backup Schedule

| Name | Schedule |
|---|---|
| PROD VM Backup Job 3 Daily | Daily 12:01 AM (Full) |
| PROD VM Backup to Tape Job 3 Weekly | Every Sunday 09:00 AM (Full) |
| PROD UAT VM Backup Job 1 Daily | Daily 08:00 PM (Full) |
| PROD UAT VM Backup to Tape Job 1 Weekly | Every Sunday 06:00 AM (Full) |
| PROD DEV VM Backup Job 2 Daily | Daily 10:00 PM (Full) |
| PROD DEV VM Backup to Tape Job 2 Weekly | Every Sunday 03:00 AM (Full) |
| PROD All jobs to DR Backup Copy Job 1 | After every PROD VM Backup Job 1, 2 and 3 Daily |
| DR VM Backup Job 4 Daily | Daily 08:00 PM (Full) |

## 9. Database Administration

### 9.1 Clean Database Transaction Logs

To clean up transaction log to reclaim space:

1.  Login to the database server, launch the SQL Server Management Studio (SSMS) software
2.  In SSMS, login the database with account having sysadmin role
3.  On the left pane, find and right click the database ?bd\_scs?, then select ?Properties?
4.  Under ?Options?, change ?Recovery model? to ?Simple?
5.  Click ?Ok? to apply the change
6.  Right click ?bd\_scs? again, under ?Tasks? ? ?Shrink?, select ?Files?
7.  Under ?File type?, select ?Log?
8.  Under ?Shrink action? select ?Reorganize pages before releasing unused space?, then press ?OK?.
9.  After shrinking, right click the database ?bd\_scs?, then select ?Properties?, under ?Options?, change ?Recovery model? back to ?Full?

### 9.2 Database Backup

While there is scheduled database full backup daily, additional backup can be done by following step:

1.  In SSMS, right click database ?bd\_scs?, select ?Tasks? ? ?Back Up??
2.  Under ?Destination?, click ?Remove? to remove existing backup destination, then click ?Add??.
3.  In the "Select backup destination" window, click "Disk" and then "Add..."
4.  Select the backup file or files (.bak) you are going to restore, then click ?OK?
5.  In the ?Restore Database? window specify the database?s name you will restore and click ?OK? to start
6.  The backup destination is selected, now click ?OK? to start the backup.
7.  The backup is completed with the ?.bak? file picked in step 3 as the result.

### 9.3 System Constraints and Limitations

*   URL path length limit 250
*   ~, #, %, & , \*, {, }, \\ :, \<, \>, ?, /, \|, ? special character is not allowed for files/folder

# 10. Log Management

1.  Following activities shall include in the log:

    *   Attempts for log-in
    *   Unauthorized update/access
    *   Failed attempts for privileges elevation
    *   Attempts for password changes
    *   Access attempts to critical files (e.g., software configuration files, password and key files, etc.)
    *   Actions taken by privileged users
    *   Use of privileged rights such as addition and deletion of user accounts
    *   Security related system failures and alerts
    *   Changes to user access rights
    *   Failed access attempts to systems and files identified as critical to the system
    *   Computer services such as file copying or searching
    *   Modification to audit policy
    *   Activation and de-activation of protection systems, such as anti-malware systems and intrusion detection systems
2.  Logs shall be retained for **180 days** and centralised and managed by Syslog server. Unauthorised access is restricted.
3.  Logs will be reviewed regularly.
4.  Logs shall not be used to profile the activity of a particular user unless it relates to a necessary audit activity supported by a Directorate rank officer.

```
--- t352_i1.md ---
<img src="media/image1.jpg" style="width:1.30903in;height:1.30903in" />

**PROGRAM MANUAL**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">COMBINED SYSTEM DEVELOPMENT SERVICES</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**<span class="smallcaps">OF THE</span>**

**<span class="smallcaps">BUILDINGS DEPARTMENT</span>**

**Version: 0.1**

**Nov 2024**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 80%" />
</colgroup>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Distribution</strong></td>
</tr>
<tr class="even">
<td>Copy No.</td>
<td>Holder</td>
</tr>
<tr class="odd">
<td>1</td>
<td><blockquote>
<p>Buildings Department (BD)</p>
</blockquote></td>
</tr>
<tr class="even">
<td>2</td>
<td><blockquote>
<p>Master Concept (Hong Kong) Limited</p>
</blockquote></td>
</tr>
</tbody>
</table>

|                   |                      |                                      |                           |            |                    |
|----------|-------------------------|---------|---------|---------|-----------|