# Application Operation Manual - Licensing Self-Certification Portal (LSCP)

**Version: 0.1**

**Date: Jan 2025**

## 1. Introduction

This Application Operation Manual (AOM) provides relevant information for the application operation staff of the Licensing Self-Certification Portal (LSCP) system. It details instructions for all work performed when running the application system, including job submission, report checking, and dispatching. This document consolidates information from the Computer Operation Procedures Manual, System Manual, and other related documents to provide a comprehensive guide.

## 2. Scope

This manual covers the software and hardware configurations for LSCP, system environment details, application configurations, server and workstation information, and backup services. It is intended for staff responsible for maintaining the application system.

## 3. References

*   System Analysis and Design Report
*   System Manual (T351)
*   Program Manual (T321)
*   Computer Operation Procedure Manual (T356)
*   Training Manual
*   Data Manual

## 4. Definitions and Conventions

### 4.1 Definitions

None specified in the provided documents.

### 4.2 Conventions

The following acronyms are used:

| Abbreviation | Description                                      |
| :----------- | :----------------------------------------------- |
| BD           | Buildings Department                             |
| LSCP         | Licensing Self-Certification Portal              |
| DMZ          | Demilitarized Zone                               |
| SAN          | Storage Area Network                             |
| VM           | Virtual Machine                                  |
| ITU          | Information Technology Unit                      |
| WKGO         | West Kowloon Government Offices                  |
| GCIS         | Government Cloud Infrastructure Services         |
| AP           | Authorized Person                                |
| RSE          | Registered Structural Engineer                   |
| RGE          | Registered Geotechnical Engineer                 |
| RC           | Registered Contractor                            |
| AP/RSE       | Authorized Person / Registered Structural Engineer |
| MWMS         | Minor Works Management System                    |
| CRM          | Customer Relationship Management                 |
| ESH          | E-Submission Hub                                 |
| ERKS         | Electronic Record Keeping System                 |
| BRAVO        | (System Name)                                    |
| EBD          | Education Bureau Department                      |
| SWD          | Social Welfare Department                        |
| MC           | Master Concept (Hong Kong) Limited              |
| EDB          | Education Bureau                                 |
| EBDC         | Education Bureau CCC                             |
| BCIS         | Building Control Information System              |
| HA           | High Availability                                |
| RTO          | Recovery Time Objective                          |
| LoR          | Letter of Requirement                            |
| BSR          | Building Safety Requirements                     |

## 5. System Overview

The LSCP system is composed of two subsystems: LSCP Web and LSCP Mobile. It serves two main user categories:

*   BD Officers
*   Public users involved in site inspection and monitoring

The primary objective is to provide an electronic platform for site inspection and site monitoring personnel to manage and review records.

### 5.1 System Architecture

The system is hosted on two datacenters: On-premise (WKGO) and Government Cloud Infrastructure Services (GCIS).

**On-Premise (WKGO):**

*   Behind an internal firewall with NAT, separated into Production, UAT, and DEV subnets.
*   Reverse proxy server with load balancing for security and request distribution.

**Government Cloud Infrastructure Services (GCIS):**

*   Divided into three subnets: Internet DMZ (iDMZ), Trusted Zone, and Gnet DMZ (gDMZ).
*   Reverse proxy server and Web Application Firewall (WAF) in front of iDMZ for enhanced security.

**External Users:**

*   Access the system via the internet using the LSCP Web Application.
*   Interact with the Application Server through the reverse proxy server.
*   Application Server hosts static web interface files.

**Internal Users:**

*   Access the system from the BD intranet through the Departmental Portal (OSDP).
*   Connect to the BD Web Servers in the Trusted Zone.
*   User authentication via Departmental Portal.

**Trusted Zone Servers:**

*   Log Server: Stores system and application logs.
*   File Server: Stores temporary and permanent files.
*   Database Server: Hosts Microsoft SQL Server for system and user information.
*   vCenter Server: Manages VM Hypervisors.
*   Backup Server: Keeps database snapshots.

### 5.2 System Functions

| Function ID   | Function Name                                                                  |
| :------------ | :----------------------------------------------------------------------------- |
| UF-WEB-001-1  | Public User Authentication with Password                                       |
| UF-WEB-001-2  | Logout system to clear user session                                            |
| UF-WEB-001-3  | Single User Session                                                            |
| UF-WEB-001-4  | GEO and BD User Authentication                                                 |
| UF-WEB-001-5  | Public User Authentication with iAM Smart                                      |
| UF-WEB-001-6  | Forgot Password                                                                |
| UF-WEB-001-7  | Change Password                                                                |
| UF-WEB-001-8  | Public Users create/register an account                                        |
| UF-WEB-001-9  | User Account Confirmation                                                      |
| UF-WEB-001-10 | Resend User Account Confirmation Email                                         |
| UF-WEB-001-11 | User Account Detail Management                                                 |
| UF-WEB-001-12 | User Email Address Update Confirmation                                         |
| UF-WEB-001-13 | Public User Accounts Management                                                |
| UF-WEB-001-14 | BD User Accounts Management                                                    |
| UF-WEB-001-15 | Public User Account Password Policy                                            |
| UF-WEB-002-1  | Assign TCPs                                                                    |
| UF-WEB-002-2  | Request TCP acceptance                                                         |
| UF-WEB-002-3  | Notification for TCP assignment                                                |
| UF-WEB-002-4  | Unassign TCPs                                                                  |
| UF-WEB-002-5  | Temporary replacement of Head of Stream                                        |
| UF-WEB-002-6  | Temporary replacement of TCP                                                   |
| UF-WEB-002-7  | Resignation of Head of Stream by BD officer                                  |
| UF-WEB-002-8  | Notification of Head of Stream resignation                                     |
| UF-WEB-003-1  | Listing out responsible Inspection Form                                        |
| UF-WEB-003-2  | Listing out responsible Site-Monitoring Schemes                                |
| UF-WEB-004-1  | Form record submission and amendment                                           |
| UF-WEB-004-2  | Search responsible Site Project                                                |
| UF-WEB-004-3  | Create Site Project from the submitted Supervision plan                         |
| UF-WEB-004-4  | Edit and update Site Project Detail                                            |
| UF-WEB-004-5  | List out Site Project                                                          |
| UF-WEB-004-6  | View Site Project Detail                                                       |
| UF-WEB-004-7  | Supervision Plan Detail View                                                   |
| UF-WEB-004-8  | Supervision Plan Detail Management                                             |
| UF-WEB-004-9  | Import SMIS Excel into CDPSS                                                   |

## 6. Equipment Configuration

### 6.1 Computer Hardware

#### 6.1.1 Hardware Components

**Production Servers (WKGO):**

| Item | Hardware Component | Configuration                                  | Qty |
| :--- | :----------------- | :--------------------------------------------- | :-: |
| 1    | ESXi Hypervisor Server (prd-scs-admin-server-01) | Dell PowerEdge R750, Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz, 32GB DDR4 (8), 1.2TB SAS HDD (3), ESXi 8.0.3 | 1   |
| 2    | ESXi Hypervisor Server (prd-scs-admin-server-02) | Dell PowerEdge R750, Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz, 32GB DDR4 (8), 1.2TB SAS HDD (3), ESXi 8.0.3 | 1   |
| 3    | NAS (prd-scs-nas) | Dell PowerEdge R750, CPU???, RAM???, HDD???, Windows Server 2022 | 1   |
| 4    | SAN Switch (prd-scs-sw-01) | Dell DS6610B, Ports: 16 | 1   |
| 5    | SAN Switch (prd-scs-sw-02) | Dell DS6610B, Ports: 16 | 1   |
| 6    | SAN Storage (PS500T-Cluster1) | Dell PS500T, 3.8TB NVME SSD (11) | 1   |
| 7    | Backup Appliance (prd-scs-backupstorage-01) | Dell DataDomain DD3300, 15TB | 1   |
| 8    | Tape Library | DELL ML3, 35 slots | 1   |
| 9    | Firewall (PA-850-SCSPri) | Palo Alto PA 850 | 1   |
| 10   | Firewall (PA-850-SCSSec) | Palo Alto PA 850 | 1   |
| 11   | Switch (???) | Cisco ??? | 1   |
| 12   | Switch (???) | Cisco ??? | 1   |
| 13   | KVM | CyberView | 1   |
| 14   | UPS (???) | Vertiv? Liebert? GXT5 3000 | 1   |
| 15   | UPS (???) | Vertiv? Liebert? GXT5 3000 | 1   |

**Partition Configuration (WKGO):**

| Host Name           | Drive | Capacity | Description                      |
| :------------------ | :---- | :------- | :------------------------------- |
| prd-scs-admin-server-01 | local | 2.4TB    | VMware ESXi Operating system     |
| prd-scs-admin-server-02 | local | 2.4TB    | VMware ESXi Operating system     |
| PS500T-Cluster1        | VM_Volume01 | 20TB     | Shared pool of storage space |
| PS500T-Cluster1        | QuorumDisk-VM-1 | 2.5GB    | Shared pool of storage space |
| prd-scs-nas           | C:    | ???      | OS                               |
|                       | D:    | ???      | Data                             |

**Disaster Recovery Servers (AIA):**

| Item | Hardware Component | Configuration                                  | Qty |
| :--- | :----------------- | :--------------------------------------------- | :-: |
| 1    | ESXi Hypervisor Server (dr-scs-admin-server-01) | Dell PowerEdge R750, Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz, 32GB DDR4 (8), 1.2TB SAS HDD (3), ESXi 8.0.3 | 1   |
| 2    | NAS (dr-scs-nas) | Dell PowerEdge R750, CPU???, RAM???, HDD???, Windows Server 2022 | 1   |
| 3    | SAN Switch (dr-scs-sw-01) | Dell DS6610B, Ports: 16 | 1   |
| 4    | SAN Storage (PS500T-Cluster2) | Dell PS500T, 3.8TB NVME SSD (11) | 1   |
| 5    | Backup Appliance (dr-scs-backupstorage-01) | Dell DataDomain DD3300, 15TB | 1   |
| 6    | Firewall (PA-850-SCSPri) | Palo Alto PA 850 | 1   |
| 7    | Switch (???) | Cisco ??? | 1   |
| 8    | KVM | CyberView | 1   |
| 9    | UPS (???) | Vertiv? Liebert? GXT5 3000 | 1   |

**Partition Configuration (DR):**

| Host Name           | Drive | Capacity | Description                      |
| :------------------ | :---- | :------- | :------------------------------- |
| dr-scs-admin-server-01 | local | 2.4TB    | VMware ESXi Operating system     |
| PS500T-Cluster2        | VM Volume01 | 20TB     | Shared pool of storage space |
| dr-scs-nas           | C:    | ???      | OS                               |
|                       | D:    | ???      | Data                             |

#### 6.1.2 Guest Servers Components

**Production Guest Servers:**

| Role | Host Name | vCPU | RAM (GB) | Disk (GB) | IP Addresses | Data Center | Host Server / Zone |
| :------------------ | :------------------ | :----: | :-------: | :--------: | :---------------------------------- | :---------- | :------------------------------- |
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

**UAT Guest Servers:**

| Role | Host Name | vCPU | RAM (GB) | Disk (GB) | IP Addresses | Data Center | Host Server / Zone |
| :------------------ | :------------------ | :----: | :-------: | :--------: | :---------------------------------- | :---------- | :------------------------------- |
| API Server | uat-scs-admin-api-01 | 2 | 4 | 100 | 192.168.13.10 | WKGO | prd-scs-admin-server-01 |
| Frontend Server | uat-scs-admin-frontend-01 | 2 | 4 | 100 | 192.168.13.11 | WKGO | prd-scs-admin-server-01 |
| Backend Server | uat-scs-admin-backend-01 | 2 | 4 | 100 | 192.168.13.12 | WKGO | prd-scs-admin-server-01 |
| Database Server | uat-scs-db-01 | 2 | 4 | 100 | 192.168.13.13 | WKGO | prd-scs-admin-server-01 |
| File Server | uat-scs-filer | 2 | 4 | 100 + 200 | 192.168.13.15 | WKGO | prd-scs-admin-server-01 |
| Reverse Proxy Server | uat-scs-proxy | 2 | 4 | 100 | 192.168.13.14 / 10.5.161.224 | WKGO | prd-scs-admin-server-01 |
| Reverse Proxy Server | scsuwi | 2 | 8 | 100 | 192.168.0.7 / 45.119.94.99 | GCIS T1 | iDMZ |
| Reverse Proxy Server | scsuwg | 2 | 8 | 100 | 192.168.4.7 / 10.148.11.220 | GCIS T1 | gDMZ |
| Apps Server | scsuad | 4 | 16 | 100 + 200 | 192.168.8.9 | GCIS T1 | Trust Zone |
| Database Server | scsudb | 4 | 16 | 100 + 100 | 192.168.8.10 | GCIS T1 | Trust Zone |

**DEV Guest Servers:**

| Role | Host Name | vCPU | RAM (GB) | Disk (GB) | IP Addresses | Data Center | Host Server / Zone |
| :------------------ | :------------------ | :----: | :-------: | :--------: | :---------------------------------- | :---------- | :------------------------------- |
| API Server | dev-scs-admin-api-01 | 2 | 4 | 100 | 192.168.14.10 | WKGO | prd-scs-admin-server-02 |
| Frontend Server | dev-scs-admin-frontend-01 | 2 | 4 | 100 | 192.168.14.11 | WKGO | prd-scs-admin-server-02 |
| Backend Server | dev-scs-admin-backend-01 | 2 | 4 | 100 | 192.168.14.12 | WKGO | prd-scs-admin-server-02 |
| Database Server | dev-scs-db-01 | 2 | 4 | 100 | 192.168.14.13 | WKGO | prd-scs-admin-server-02 |
| File Server | dev-scs-filer | 2 | 4 | 100 + 200 | 192.168.14.15 | WKGO | prd-scs-admin-server-02 |
| Reverse Proxy Server | dev-scs-proxy | 2 | 4 | 100 | 192.168.14.14 / 10.5.161.225 | WKGO | prd-scs-admin-server-02 |
| Reverse Proxy Server | scsdwi | 2 | 8 | 100 | 192.168.0.6 / 45.119.94.100 | GCIS T1 | iDMZ |
| Reverse Proxy Server | scsdwg | 2 | 8 | 100 | 192.168.4.6 / 10.148.11.220 | GCIS T1 | gDMZ |
| Apps Server | scsdad | 4 | 16 | 100 + 200 | 192.168.8.7 | GCIS T1 | Trust Zone |
| Database Server | scsddb | 4 | 16 | 100 + 100 | 192.168.8.8 | GCIS T1 | Trust Zone |

**Disaster Recovery Guest Servers:**

| Role | Host Name | vCPU | RAM (GB) | Disk (GB) | IP Addresses | Data Center | Host Server / Zone |
| :------------------ | :------------------ | :----: | :-------: | :--------: | :---------------------------------- | :---------- | :------------------------------- |
| vCenter | dr-scs-vcenter-01 | 16 | 39 | 1.33TB | 192.168.20.18 / 10.5.174.225 | AIA | dr-scs-admin-server-01 |
| Veeam Backup Server | dr-scs-backup-01 | 8 | 24 | 300 + 1TB | 192.168.20.19 / 10.5.161.224 | AIA | dr-scs-admin-server-01 |
| Kiwi Log Server | dr-scs-log-01 | 4 | 8 | 300 + 500 | 192.168.20.10 | AIA | dr-scs-admin-server-01 |
| API Server | dr-scs-admin-api-01 | 2 | 8 | 90 | 192.168.22.11 | AIA | dr-scs-admin-server-01 |
| Frontend Server | dr-scs-admin-frontend-01 | 2 | 8 | 90 | 192.168.22.12 | AIA | dr-scs-admin-server-01 |
| Backend Server | dr-scs-admin-backend-01 | 2 | 8 | 90 | 192.168.22.13 | AIA | dr-scs-admin-server-01 |
| Database Server | dr-scs-db-01 | 2 | 8 | 90 + 500 | 192.168.22.14 | AIA | dr-scs-admin-server-01 |
| File Server | dr-scs-filer | 2 | 8 | 90 + 1TB | 192.168.22.16 | AIA | dr-scs-admin-server-01 |
| Reverse Proxy Server | dr-scs-proxy | 2 | 4 | 90 | 192.168.22.15 / 10.5.174.228 | AIA | dr-scs-admin-server-01 |

### 6.1.3 Gateway and SMTPX Configuration

**SMTPX:**

| Item                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SMTPX service hostname | smtpx.cis.hksarg (resolvable by CCGO DNS)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SMTPX service IP address | 10.106.5.103, 10.106.5.104, 10.106.105.103, 10.106.105.104 (IP addresses are provided for ACL settings. To enjoy the automatic failover feature, mail servers should access SMTPX service through hostname.) |
| SMTP port number      | 587                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Sender IP address     | (B/Ds' IP address within GNET)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Login and password    | Not required                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Authentication        | By e-Certificate issued from Hong Kong Post or the Government ISCCA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Sender address in e-mail | Valid e-mail address registered in IMX service                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Connection encryption | STARTTLS (Mandatory)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Compatible Protocols  | SPF and DKIM                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

SMTPX configured in the IIS 6.0 of the following servers: scspwi, scsuwg, scsdwg

**WKGO Production Network Gateway:**

| Gateway      | Subnet        | IP Range           | vlan / Zone          |
| :----------- | :------------ | :----------------- | :------------------- |
| 192.168.10.1 | 255.255.255.0 | 192.168.10.1-254 | Management           |
| 192.168.11.1 | 255.255.255.0 | 192.168.11.1-254 | Replication / Backup |
| 192.168.12.1 | 255.255.255.0 | 192.168.12.1-254 | Production           |
| 192.168.13.1 | 255.255.255.0 | 192.168.13.1-254 | UAT                  |
| 192.168.14.1 | 255.255.255.0 | 192.168.14.1-254 | DEV                  |
| 10.5.161.1   | 255.255.255.0 | 10.5.161.205-235 | BD Network           |

**AIA DR Network Gateway:**

| Gateway      | Subnet        | IP Range           | vlan / Zone          |
| :----------- | :------------ | :----------------- | :------------------- |
| 192.168.20.1 | 255.255.255.0 | 192.168.20.1-254 | Management           |
| 192.168.21.1 | 255.255.255.0 | 192.168.21.1-254 | Replication / Backup |
| 192.168.22.1 | 255.255.255.0 | 192.168.22.1-254 | Production           |
| 10.5.174.1   | 255.255.255.0 | 10.5.174.215-234 | BD Network           |

## 7. Software Inventories

### 7.1 Inventory of Application Programs

Refer to the Program Manual (T321) for details of Application Programs for LSCP.

### 7.2 Inventory of System Software and Software Package

**Production Environment ? WKGO**

| Machine | Hostname | Software                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     