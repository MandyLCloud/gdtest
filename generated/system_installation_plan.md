# System Installation Plan

## 1. Introduction

This System Installation Plan (SIP) outlines the procedures and schedule for deploying the Licensing Self-Certification Portal (LSCP) application in the production environment. The system comprises three main parts:

*   Database Server
*   Backend Server
*   Frontend and Web Portal Server

This document is based on the User Requirements Specifications (URS) T223, System Manual and other relevant documentation.

## 2. Project Environment Description

### 2.1 Network Diagram

A logical network diagram for the production and UAT sites located in 1/F West Kowloon Government Office (WKGO) is provided below:

`[DIAGRAM HERE]`

The network is separated into three zones:

*   DMZ (Demilitarized Zone)
*   Trusted Zone
*   Storage Network

A two-tier firewall setup is implemented to establish the Trusted Zone and DMZ. All incoming network traffic must pass through the DMZ before entering the Trusted Zone.

To optimize hardware resource utilization, servers (excluding the backup server) are configured as virtual machines (VMs) and consolidated into DMZ VM host servers and Trusted Zone VM host servers for each physical site. Two VM host servers are deployed in each zone for high availability.

Storage requirements for all servers are consolidated and provided by SAN storage. A dedicated network interconnects the VM host servers. The backup server resides within this storage-dedicated network to perform backup tasks for VM host servers in both the DMZ and Trusted Zone.

The physical setup is illustrated below:

### 2.2 Hardware Specification

#### Production and UAT Environment:

The following table lists the machines and virtual machines in the Production and UAT environments:

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

#### DR Environment:

The following table lists the machines and virtual machines in the Disaster Recovery (DR) environment:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

### 2.3 Software Specification

The following table details the software specifications for the LSCP:

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

## 3. Application Deployment Procedure for Production

### 3.1 Database Server

To install the database server, follow these steps:

1.  Remote login to `PRD-DB-01 (10.5.113.218)`.

### 3.2 Backend Servers

1.  Remote login into `PRD-WEBAPP-01`.

### 3.3 Frontend Servers

1.  Remote login into `PRD-WEBAPP-01`.

#### 3.3.1 sFTP Server Setup

1.  Install OpenSSH server in Windows Server. Go to Apps & Features, click ?Optional Features?, click ?Add a feature?, check ?OpenSSH Server?.

## 4. System Installation Schedule and Result

### 4.1 System Installation Schedule

The following table summarizes the planned installation schedule:

| Pre-Requisite |  | Start Date | End Date | Start time | End Time |
|---|---|---|---|---|---|
| Database Server Installation (Production and DR) |  |  |  |  |  |
| Backend Server Installation (Production and DR) |  |  |  |  |  |
| Frontend Server Installation (Production and DR) |  |  |  |  |  |
| Functionality test (VM & Networking) |  |  |  |  |  |
| Database setup |  |  |  |  |  |
| Deployment for 1<sup>st</sup> version of frontend server |  |  |  |  |  |
| Deployment for 1<sup>st</sup> version of backend server |  |  |  |  |  |
| Application Health Check |  |  |  |  |  |
| 1 |  |  |  |  |  |
| Deployment for Latest Mobile Application |  |  |  |  |  |
| Final Check Production Web Server |  |  |  |  |  |
| Final Check Production Database Server |  |  |  |  |  |
| Final Check DR Web & Database server |  |  |  |  |  |
| Final Check IIS & Framework |  |  |  |  |  |

### 4.2 System Installation Result

The following table summarizes the actual system installation schedule and results:

| Pre-Requisite |  | Actual Start Date | Actual End Date | Actual Start time | Actual End Time | Status/Result |
|---|---|---|---|---|---|---|
| Database Server Installation (Production, UAT and DR) |  |  |  |  |  |  |
| Backend Server Installation (Production, UAT and DR) |  |  |  |  |  |  |
| Frontend Server Installation (Production, UAT and DR) |  |  |  |  |  |  |
| Functionality test (VM & Networking) |  |  |  |  |  |  |
| Database setup |  |  |  |  |  |  |
| Deployment for 1<sup>st</sup> version of frontend server |  |  |  |  |  |  |
| Deployment for 1<sup>st</sup> version of backend server |  |  |  |  |  |  |
| Application Health Check |  |  |  |  |  |  |
| 1 |  |  |  |  |  |  |
| Deployment for Latest Mobile Application |  |  |  |  |  |  |
| Final Check Production Web Server |  |  |  |  |  |  |
| Final Check Production Database Server |  |  |  |  |  |  |
| Final Check DR Web & DB server |  |  |  |  |  |  |
| Final Check IIS & Framework |  |  |  |  |  |  |

## Appendix: Hardware and Software Inventory

Refer to the System Manual for detailed hardware and software inventories for each environment (Production, UAT, DEV, DR).  Key components include:

*   Physical Servers (Model, Host Name, IP, Serial No., Disk Configuration)
*   SAN Storage (Type, Model, Serial No., No. of Hard Disks, IP Address)
*   Backup Storage (Type, Model, Serial No., Volume Size, IP Address)
*   Firewalls (Host Name, Internal IP, External IP, Model, Serial No.)
*   Switches (Host Name, Internal IP, Model, Serial No.)
*   Guest Servers (Role, Host Name, vCPU, RAM, Disk, IP Addresses, Data Center, Host Server/Zone)
*   Operating Systems and Software Versions

## Appendix: Security and Backup Strategy

Refer to the System Manual for detailed information on security and backup procedures. Key aspects include:

*   System Control
*   Backup Procedures (VM Image Backup, Database Backup)
*   Security Measures (Data Transmission Security, Data Storage and Auditing Security, System Security, Physical Security, Password and Group Control)
*   Change Control
*   Disaster Recovery
*   Database Backup Strategy (SQL Database Backup, Recovery, Backup Schedule)

## Appendix: Network Configuration

Refer to the System Manual for detailed network configurations, including:

*   SMTPX Configuration
*   WKGO Production Network Gateway
*   AIA DR Network Gateway
*   Rack Diagram
*   Firewall Configurations
*   Switch Configurations

## Appendix: Database Administration

Refer to the System Manual for detailed database administration procedures, including:

*   Cleaning Database Transaction Logs
*   Database Backup

## Appendix: System Constraints and Limitations

*   URL path length limit: 250
*   Special characters not allowed for files/folders: ~, #, %, &, \*, {, }, \\ :, \<, \>, ?, /, \|, ?

## Appendix: Log Management

1.  Following activities shall include in the log:

    *   Attempts for log-in
    *   Unauthorised update/access
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

<<End of Document>>