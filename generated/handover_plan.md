```markdown
![BDlogo](media/image1.jpg)

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

[System Summary](#system-summary)

[1. Environment Description](#environment-description)

[2. Purpose](#purpose)

> [2.1 Schedule](#schedule)
>
> [2.2 Verification](#verification)

[3. Documentation](#documentation)

[4. Program Source Code](#program-source-code)

[5. Administration Accounts Checklist](#administration-accounts-checklist)

[6. Backup](#backup)

> [6.1 VM Backup](#vm-backup)
>
> [6.2 Database Backup](#database-backup)

[7. Outstanding Items/Issues](#outstanding-itemsissues)

[8. Licensed Software](#licensed-software)

[9. Software Inventories](#software-inventories)

[10. Security and Backup](#security-and-backup-details)

[11. Database Administration](#database-administration-details)

[12. Log Management](#log-management-details)

# System Summary

## 5.1 Objective

The users of the LSCP can be classified into two categories:

-   BD Officers
-   Public users involved in site inspection and site monitoring

The primary objective of LSCP is to provide an electronic platform for site inspection and site monitoring personnel to provide, manage, and review the inspection and monitoring records.

## 5.2 System Architecture

This is an overview of the system structure of LSCP in the Production Environment.

![Production Architecture](media/image2.png)

The following diagram illustrates the architecture of the LSCP for Production site and UAT site in another perspective.

![Production and UAT Architecture](media/image3.png)

The system is hosted in two datacenters: On-premise (WKGO) and Government Cloud Infrastructure Services (GCIS).

The On-premise system is behind an internal firewall that uses NAT to separate into 3 subnets: Production, UAT and DEV for internal users only.

A reverse proxy server with load balancing function is used for increased security and share the incoming requests to the frontend web servers.

The system on GCIS is divided into 3 subnets: Internet DMZ (iDMZ), Trusted Zone and Gnet DMZ (gDMZ).

Both iDMZ and gDMZ contain a reverse proxy server and a Web Application Firewall (WAF) also deployed in front of the iDMZ for increased security access.

External users (i.e. public users) access the system from the internet through the internet using LSCP Web Application, which interacts with the Application Server through the reverse proxy server. The Application Server hosts the static web interface files.

To perform system logic, the External Application Servers will pass requests to the Web Servers in the Trusted Zone. The web application, written in reactjs, will interact with the external web server that is written in nodeJS that in turns perform CRUD on the Database Servers, which host Microsoft SQL Servers, and the in-built file storage to perform logic computing, and return result to the External Web Servers then to the internet.

In addition to external users, internal users who would access the internal BDSCS application from BD intranet, would connect to the BD Web Servers in the Trusted Zone, through the Departmental Portal (OSDP). The BD Web Servers perform the same function as the External Web Servers and perform user authentication functions when interfaced with the Departmental Portal.

Finally, there are some more servers in the Trusted Zone to support internal BDSCS application, which includes:

-   Log Server to store the system and application log from other servers
-   File Server to store the temporary and permanent files
-   Database Server that hosts Microsoft SQL server to store all the system and user information
-   vCenter Server to manage the VM Hypervisors on each of the physical servers
-   Backup Server to keep snapshots of the database

Below are further details of each of the system components in the BDSCS:

<u>External Application Server</u>

The external application servers serve the static web contents in form of HTML, CSS, and JavaScript to the internet, through Microsoft's Internet Information Services (IIS), and also proxy the backend APIs (GraphQL format) to the web application servers as being in the DMZ.

The website hosted on the external web servers is written in JavaScript under the React framework. After compiling the JavaScript project, the result files are stored in the external web servers and served by IIS, with rewrite rules to proxy the backend APIs.

<u>External Web Server</u>

The external web server, in this context, refers to a server that hosts and runs the backend API responsible for processing business logic and performing database operations. In the case of IIS (Internet Information Services) and expressJS, IIS serves as the web server software, while ExpressJS represents the framework used for developing the backend APIs.

The backend API, developed using ExpressJS, encompasses the code that handles various tasks, including interacting with databases, executing business logic, and processing requests from clients. It acts as the intermediary between the frontend (such as a mobile or web application) and the underlying data storage.

When a client application makes a request to the backend API, IIS receives the request and passes it to the appropriate ExpressJS code for processing. The backend API then performs the necessary operations, which may involve querying the database, executing business rules, or performing calculations. Once the processing is complete, the backend API generates a response that is sent back to the client application (External Application Server in this case) through IIS.

<u>BD Web Servers</u>

The BDSCS backend portal was developed for internal BD users and BD ITU. It is using the same technology stack as Extra Application Server but just deployed to different zones to ensure security and connectivity for internal BD users only

<u>Database Management Servers</u>

Both the internal and external BDSCS applications are built on the Microsoft SQL Server database engine.

<u>Web Browser Support</u>

![Browser Support](media/image4.png)

<u>iAM Smart</u>

The iAM Smart system implemented by the Government of Hong Kong focuses primarily on providing a secure and convenient login mechanism and retrieving basic user information. Pilot CDPSS has integrated with iAM Smart authentication module. Users can utilize iAM Smart to log in to Pilot CDPSS services and retrieve basic information associated with their digital identity.

<u>Departmental Portal</u>

The Departmental Portal is a web service of BD to pass BD user?s identity to other wb services including the LSCP. When BD users access LSCP website through the Departmental Portal, the user ID will be provided to the LSCP to complete the login process without further input from the user. This login method only available inside BD?s network.

<u>SMTPX</u>

The notification module in BDSCS would send login one-time password (OTP) and email notification by initiating an SMTPX service provided by CIS.

<u>MWMS</u>

MWMS would provide data of AP/RSE/RGE/AS acknowledged by BD. Snapshots of the MWMS data will be interfaced to BDSCS through SFTP and then internal and external BDSCS applications would intake this data by processing the batch file auto-generated and delivered from MWMS daily.

<u>BCIS</u>

BCIS would provide address data and BD case data acknowledged by BD. The latest copy of the BCIS database would be synced to BDSCS through SQL queries at midnight. The data would then be used in both external and internal portals for address selection, folio management, and case logic. Meanwhile, the new BD cases would be synced to BCIS in real time through a SQL stored procedure.

This is an overview of the system structure of Pilot CDPSS in Disaster Recovery Environment, similar with the production environment

![DR Architecture](media/image5.png)

## 5.3 System Functions

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

# 1. Environment Description

Production and UAT environment:

![Production and UAT Environment Diagram](media/image3.png)

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
      <th rowspan="2">prd-scs-admin-server-01</th>
      <th>prd-scs-vcenter-01</th>
      <th>vCenter Server</th>
      <th>192.168.10.24 / 10.5.161.210</th>
    </tr>
    <tr class="header">
      <th>prd-scs-log-01</th>
      <th>Kiwi Log Server</th>
      <th>192.168.10.11 / 10.5.161.223</th>
    </tr>
    <tr class="odd">
      <th rowspan="3">prd-scs-admin-server-02</th>
      <th>prd-scs-backup-01</th>
      <th>Veeam Backup Server</th>
      <th>192.168.10.25 / 10.5.161.211</th>
    </tr>
    <tr class="header">
      <th>prd-scs-esetnod32</th>
      <th>NOD32 Anti-Virus Server</th>
      <th>192.168.10.34 / 10.5.161.215</th>
    </tr>
    <tr class="odd">
      <th>dev-scs-admin-api-01</th>
      <th>DEV API Server 1</th>
      <th>192.168.14.10</th>
    </tr>
    <tr class="header">
      <th rowspan="7"></th>
      <th>prd-scs-admin-api-01</th>
      <th>PRD API Server 1</th>
      <th>192.168.12.11</th>
    </tr>
    <tr class="odd">
      <th>prd-scs-admin-frontend-01</th>
      <th>PRD Frontend Server 1</th>
      <th>192.168.12.12</th>
    </tr>
    <tr class="header">
      <th>prd-scs-admin-backend-01</th>
      <th>PRD Backend Server 1</th>
      <th>192.168.12.13</th>
    </tr>
    <tr class="odd">
      <th>prd-scs-db-01</th>
      <th>PRD Database Server 1</th>
      <th>192.168.12.14</th>
    </tr>
    <tr class="header">
      <th>prd-scs-filer</th>
      <th>PRD File Server</th>
      <th>192.168.12.20</th>
    </tr>
    <tr class="odd">
      <th>prd-scs-proxy</th>
      <th>PRD Reverse Proxy Server</th>
      <th>192.168.12.15 / 10.5.161.226</th>
    </tr>
    <tr class="header">
      <th>uat-scs-admin-api-01</th>
      <th>UAT API Server 1</th>
      <th>192.168.13.10</th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

DR environment:

![DR Environment Diagram](media/image5.png)

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
      <th rowspan="2">dr-scs-admin-server-01</th>
      <th>dr-scs-vcenter-01</th>
      <th>DR vCenter Server</th>
      <th>192.168.20.18 / 10.5.174.225</th>
    </tr>
    <tr class="header">
      <th>dr-scs-log-01</th>
      <th>DR Kiwi Log Server</th>
      <th>192.168.20.10</th>
    </tr>
    <tr class="odd">
      <th rowspan="7">dr-scs-admin-server-01</th>
      <th>dr-scs-backup-01</th>
      <th>DR Veeam Backup Server</th>
      <th>192.168.20.19 / 10.5.161.224</th>
    </tr>
    <tr class="header">
      <th>dr-scs-admin-api-01</th>
      <th>DR API Server 1</th>
      <th>192.168.22.11</th>
    </tr>
    <tr class="odd">
      <th>dr-scs-admin-frontend-01</th>
      <th>DR Frontend Server 1</th>
      <th>192.168.22.12</th>
    </tr>
    <tr class="header">
      <th>dr-scs-admin-backend-01</th>
      <th>DR Backend Server 1</th>
      <th>192.168.22.13</th>
    </tr>
    <tr class="odd">
      <th>dr-scs-db-01</th>
      <th>DR Database Server 1</th>
      <th>192.168.22.14</th>
    </tr>
    <tr class="header">
      <th>dr-scs-filer</th>
      <th>DR File Server</th>
      <th>192.168.22.16</th>
    </tr>
    <tr class="odd">
      <th>dr-scs-proxy</th>
      <th>DR Reverse Proxy Server</th>
      <th>192.168.22.15 / 10.5.174.228</th>
    </tr>
    <tr class="header">
      <th>dr-scs-nas</th>
      <th>DR NAS</th>
      <th>NAS for DR Environment</th>
      <th>192.168.20.35, 10.5.174.225</th>
    </tr>
    <tr class="odd">
      <th>prd-scs-nas</th>
      <th>PRD NAS</th>
      <th>NAS for Production Environment</th>
      <th>192.168.10.35, 10.5.161.218</th>
    </tr>
    <tr class="header">
      <th>scspwi</th>
      <th>GCIS PRD Reverse Proxy Server (Internet)</th>
      <th>Reverse Proxy for GCIS PRD Internet Access</th>
      <th>192.168.0.6 / 45.119.92.84</th>
    </tr>
    <tr class="odd">
      <th>scspwg</th>
      <th>GCIS PRD Reverse Proxy Server (GNET)</th>
      <th>Reverse Proxy for GCIS PRD GNET Access</th>
      <th>192.168.4.6 / 10.160.11.211</th>
    </tr>
    <tr class="header">
      <th>scspad</th>
      <th>GCIS PRD Application Server</th>
      <th>Application Server for GCIS PRD</th>
      <th>192.168.8.6</th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

# 2. Purpose

This document is a checklist of handover materials within project scope; and it also provides relevant information to the support maintenance staffs who will be maintaining this system in the future. All these deliverables should be received from system implementation team of the Licensing Self-Certification Portal (LSCP); to the Buildings Department (BD) of the Government of the Hong Kong Special Administrative Region (HKSARG or the Government).

The hand-over items of this project can be summarized into the following 6 items:

> 1.  Documentation
> 2.  Program Source code (Backend Application, Frontend Web App, Fronted Mobile App)
> 3.  Administration Accounts
> 4.  System backup
> 5.  Hardware
> 6.  Software Packages and Licenses

## 2.1 Schedule

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |

## 2.2 Verification

1.  The application URL verification

> The access link (URL) of each application should be verified by performing an access checking.

2.  Login accounts verification

> The login accounts of the applications and servers should be verified by processing login action.

# 3. Documentation

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

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application |         |           |
| Backend Application  |         |           |
|                      |         |           |

# 5. Administration Accounts Checklist

In this section, it will list the user account for management in the different areas.

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

Administration Accounts on LSCP

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |
|             |           |              |          |

# 6. Backup

<span class="mark">\[RY Note: Following content needs to check\]</span>

## 6.1 VM Backup

Backup service is carried out by backup server.

Daily VM image backup is carried out and store in the backup servers. A further copy of production VM images is copied to DR?s backuper server.

## 6.2 Database Backup

Database full export backup: this type of backup contains full database exported database objects including schemas, table structures, packages, stored procedures and data.

Daily full export backup is done on DB servers, data stored on the DB servers and further backed up by VM Backup.

# 7. Outstanding Items/Issues

Nil.

# 8. Licensed Software

<span class="mark">\[RY Note: Items are for reference only. They are incorrect\]</span>

| Item                                                                              | Amount | Expire At |
|------------------------|------------------------|------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual                                            |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

# 9. Software Inventories

## 7.2 Inventory of System Software and Software Package

Summary of software required is given in the following table:

<u>Production Environment ? WKGO</u>

<table style="width:100%;">
  <colgroup>
    <col style="width: 19%" />
    <col style="width: 27%" />
    <col style="width: 52%" />
  </colgroup>
  <tbody>
    <tr class="odd">
      <td>Machine</td>
      <td>Hostname</td>
      <td>Software</td>
    </tr>
    <tr class="even">
      <td>NAS</td>
      <td>prd-scs-nas</td>
      <td>???</td>
    </tr>
    <tr class="odd">
      <td><p>Veeam Backup</p>
      <p>Server</p></td>
      <td>prd-scs-backup-01</td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p>
      <p>Veeam Backup &amp; Replication 12.1.2.172</p></td>
    </tr>
    <tr class="even">
      <td>Kiwi Log Server</td>
      <td>prd-scs-log-01</td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p>
      <p>Kiwi Syslog Server NG 1.2.1.4</p></td>
    </tr>
    <tr class="odd">
      <td>NOD32 Anti-Virus Server</td>
      <td>prd-scs-esetnod32</td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p>
      <p>ESET PROTECT Server 11.0.199.0</p></td>
    </tr>
    <tr class="even">
      <td>API Server</td>
      <td><p>prd-scs-admin-api-01</p>
      <p>prd-scs-admin-api-02</p></td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p></td>
    </tr>
    <tr class="odd">
      <td>Frontend Server</td>
      <td><p>prd-scs-admin-frontend-01</p>
      <p>prd-scs-admin-frontend-02</p></td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p>
      <p>IIS 10.0.20348.1</p></td>
    </tr>
    <tr class="even">
      <td>Backupend Server</td>
      <td><p>prd-scs-admin-backend-01</p>
      <p>prd-scs-admin-backend-02</p></td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p></td>
    </tr>
    <tr class="odd">
      <td>Database Server</td>
      <td><p>prd-scs-db-01</p>
      <p>prd-scs-db-02</p></td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p>
      <p>Microsoft SQL Server 2022 16.0.1000.6</p>
      <p>Microsoft Management Studio 19.1</p></td>
    </tr>
    <tr class="even">
      <td>File Server</td>
      <td>prd-scs-filer</td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p></td>
    </tr>
    <tr class="odd">
      <td>Reverse Proxy Server</td>
      <td>prd-scs-proxy</td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p>
      <p>Nginx 1.26.2</p></td>
    </tr>
    <tr class="even">
      <td>vCenter</td>
      <td>prd-scs-vcenter-01</td>
      <td>vCenter 8.0.3 Build 24322831</td>
    </tr>
    <tr class="odd">
      <td>VM Host</td>
      <td><p>prd-scs-admin-server-01</p>
      <p>prd-scs-admin-server-02</p></td>
      <td>VMWare vSphere 8.0.3 Build 24022510</td>
    </tr>
  </tbody>
</table>

\*VMware vSphere is a suite of software components for virtualization. These include ESXi, vCenter Server, and other software components such as vCenter Single Sign-On, and vCenter Server plug-ins that fulfill several different functions in the vSphere environment.

*https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-vcenter-esxi-management/GUID-B3A1A79B-EF9B-4C10-A053-D54D88254C52.html*

<u>UAT Environment ? WKGO</u>

<table style="width:100%;">
  <colgroup>
    <col style="width: 19%" />
    <col style="width: 28%" />
    <col style="width: 52%" />
  </colgroup>
  <tbody>
    <tr class="odd">
      <td>Machine</td>
      <td>Hostname</td>
      <td>Software</td>
    </tr>
    <tr class="even">
      <td>API Server</td>
      <td>uat-scs-admin-api-01</td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p></td>
    </tr>
    <tr class="odd">
      <td>Frontend Server</td>
      <td>uat-scs-admin-frontend-01</td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p>
      <p>IIS 10.0.20348.1</p></td>
    </tr>
    <tr class="even">
      <td>Backupend Server</td>
      <td>uat-scs-admin-backend-01</td>
      <td><p>Windows Server 2022 21H2</p>
      <p>VMware Tools 12.4.0.23259341</p>
      <p>ESET Server Security 10.0.12012.0</p>
      <p>ESET Management Agent 10.1.1292.0</p></td>
    </tr>
    <tr class="odd">
      <td>Database Server</td>
      <td>uat-scs-db-01</td>
      <td><p>Windows Server 2022 21H