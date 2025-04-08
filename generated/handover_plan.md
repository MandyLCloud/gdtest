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

[1. Environment Description 4](#environment-description)

[2. Purpose 6](#purpose)

> [2.1 Schedule 6](#schedule)
>
> [2.2 Verification 6](#verification)

[3. Documentation 7](#documentation)

[4. Program Source Code 9](#program-source-code)

[5. Administration Accounts Checklist
10](#administration-accounts-checklist)

[6. Backup 11](#backup)

> [6.1 VM Backup 11](#vm-backup)
>
> [6.2 Database Backup 11](#database-backup)

[7. Outstanding Items/Issues 12](#outstanding-itemsissues)

[8. Licensed Software 13](#licensed-software)

[9. Log Management 14](#log-management)

# 1. Environment Description

Production and UAT environment:

\[an image here]

The system is holding on two datacenters: On-premise (WKGO) and
Government Cloud Infrastructure Services (GCIS).

The On-premise system is behind an internal firewall that uses NAT to
separate into 3 subnets. There are Production, UAT and DEV for internal
users only.

A reverse proxy server with load balancing function is used for
increased security and share the incoming requests to the frontend web
servers.

The system on GCIS is divided into 3 subnets: Internet DMZ (iDMZ),
Trusted Zone and Gnet DMZ (gDMZ).

Both iDMZ and gDMZ contain a reverse proxy server and a Web Application
Firewall (WAF) also deployed in front of the iDMZ for increased security
access.

External users (i.e. public users) access the system from the internet
through the internet using LSCP Web Application, which interacts with
the Application Server through the reverse proxy server. The Application
Server hosts the static web interface files.

To perform system logic, the External Application Servers will pass
requests to the Web Servers in the Trusted Zone. The web application,
written in reactjs, will interact with the external web server that is
written in nodeJS that in turns perform CRUD on the Database Servers,
which host Microsoft SQL Servers, and the in-built file storage to
perform logic computing, and return result to the External Web Servers
then to the internet.

In addition to external users, internal users who would access the
internal BDSCS application from BD intranet, would connect to the BD Web
Servers in the Trusted Zone, through the Departmental Portal (OSDP). The
BD Web Servers perform the same function as the External Web Servers and
perform user authentication functions when interfaced with the
Departmental Portal.

Finally, there are some more servers in the Trusted Zone to support
internal BDSCS application, which includes:

-   Log Server to store the system and application log from other
    servers
-   File Server to store the temporary and permanent files
-   Database Server that hosts Microsoft SQL server to store all the
    system and user information
-   vCenter Server to manage the VM Hypervisors on each of the physical
    servers
-   Backup Server to keep snapshots of the database

Below are further details of each of the system components in the BDSCS:

<u>External Application Server</u>

The external application servers serve the static web contents in form
of HTML, CSS, and JavaScript to the internet, through Microsoft's
Internet Information Services (IIS), and also proxy the backend APIs
(GraphQL format) to the web application servers as being in the DMZ.

The website hosted on the external web servers is written in JavaScript
under the React framework. After compiling the JavaScript project, the
result files are stored in the external web servers and served by IIS,
with rewrite rules to proxy the backend APIs.

<u>External Web Server</u>

The external web server, in this context, refers to a server that hosts
and runs the backend API responsible for processing business logic and
performing database operations. In the case of IIS (Internet Information
Services) and expressJS, IIS serves as the web server software, while
ExpressJS represents the framework used for developing the backend
APIs.

The backend API, developed using ExpressJS, encompasses the code that
handles various tasks, including interacting with databases, executing
business logic, and processing requests from clients. It acts as the
intermediary between the frontend (such as a mobile or web application)
and the underlying data storage.

When a client application makes a request to the backend API, IIS
receives the request and passes it to the appropriate ExpressJS code for
processing. The backend API then performs the necessary operations,
which may involve querying the database, executing business rules, or
performing calculations. Once the processing is complete, the backend
API generates a response that is sent back to the client application
(External Application Server in this case) through IIS.

<u>BD Web Servers</u>

The BDSCS backend portal was developed for internal BD users and BD ITU.
It is using the same technology stack as Extra Application Server but
just deployed to different zones to ensure security and connectivity for
internal BD users only

<u>Database Management Servers</u>

Both the internal and external BDSCS applications are built on the
Microsoft SQL Server database engine.

**System Architecture Diagrams:**

**Production Environment:**

<img src="media/image2.png" style="width:6.62605in;height:5.91667in" />

<img src="media/image3.png" style="width:6.62605in;height:5.81944in" />

**Disaster Recovery Environment:**

<img src="media/image5.png" style="width:6.62605in;height:6.44444in" />

**List of machines and virtual machines:**

**Production Environment (WKGO):**

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
</thead>
<tbody>
<tr class="odd">
<th rowspan="2">prd-scs-admin-server-01</th>
<td>prd-scs-vcenter-01</td>
<td>vCenter</td>
<td>192.168.10.24 / 10.5.161.210</td>
</tr>
<tr class="header">
<td>prd-scs-log-01</td>
<td>Kiwi Log Server</td>
<td>192.168.10.11 / 10.5.161.223</td>
</tr>
<tr class="odd">
<th rowspan="3">prd-scs-admin-server-02</th>
<td>prd-scs-backup-01</td>
<td>Veeam Backup Server</td>
<td>192.168.10.25 / 10.5.161.211</td>
</tr>
<tr class="header">
<td>prd-scs-esetnod32</td>
<td>NOD32 Anti-Virus Server</td>
<td>192.168.10.34 / 10.5.161.215</td>
</tr>
<tr class="odd">
<td>dev-scs-proxy</td>
<td>Reverse Proxy Server (DEV)</td>
<td>192.168.14.14 / 10.5.161.225</td>
</tr>
<tr class="header">
<th rowspan="7">prd-scs-admin-server-01 &<br> prd-scs-admin-server-02</th>
<td>prd-scs-admin-api-01, prd-scs-admin-api-02</td>
<td>API Server (PRD)</td>
<td>192.168.12.11, 192.168.12.16</td>
</tr>
<tr class="odd">
<td>prd-scs-admin-frontend-01, prd-scs-admin-frontend-02</td>
<td>Frontend Server (PRD)</td>
<td>192.168.12.12, 192.168.12.17</td>
</tr>
<tr class="header">
<td>prd-scs-admin-backend-01, prd-scs-admin-backend-02</td>
<td>Backend Server (PRD)</td>
<td>192.168.12.13, 192.168.12.18</td>
</tr>
<tr class="odd">
<td>prd-scs-db-01, prd-scs-db-02</td>
<td>Database Server (PRD)</td>
<td>192.168.12.14, 192.168.12.19</td>
</tr>
<tr class="header">
<td>prd-scs-filer</td>
<td>File Server (PRD)</td>
<td>192.168.12.20</td>
</tr>
<tr class="odd">
<td>prd-scs-proxy</td>
<td>Reverse Proxy Server (PRD)</td>
<td>192.168.12.15 / 10.5.161.226</td>
</tr>
<tr class="header">
<td>uat-scs-proxy</td>
<td>Reverse Proxy Server (UAT)</td>
<td>192.168.13.14 / 10.5.161.224</td>
</tr>
</tbody>
</table>

**Production Environment (GCIS P1):**

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
</thead>
<tbody>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scspwi</td>
<td>Reverse Proxy Server (Internet DMZ)</td>
<td>192.168.0.6 / 45.119.92.84</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scspwg</td>
<td>Reverse Proxy Server (GNET DMZ)</td>
<td>192.168.4.6 / 10.160.11.211</td>
</tr>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scspad</td>
<td>Apps Server (Trust Zone)</td>
<td>192.168.8.6</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scspdb</td>
<td>Database Server (Trust Zone)</td>
<td>192.168.8.7</td>
</tr>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scspbk2</td>
<td>Veeam Backup Server (Trust Zone)</td>
<td>192.168.8.9</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scsplog</td>
<td>Kiwi Log Server (Trust Zone)</td>
<td>192.168.8.10</td>
</tr>
</tbody>
</table>

**UAT Environment (WKGO):**

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
</thead>
<tbody>
<tr class="odd">
<th>prd-scs-admin-server-01</th>
<td>uat-scs-admin-api-01</td>
<td>API Server (UAT)</td>
<td>192.168.13.10</td>
</tr>
<tr class="header">
<th>prd-scs-admin-server-01</th>
<td>uat-scs-admin-frontend-01</td>
<td>Frontend Server (UAT)</td>
<td>192.168.13.11</td>
</tr>
<tr class="odd">
<th>prd-scs-admin-server-01</th>
<td>uat-scs-admin-backend-01</td>
<td>Backend Server (UAT)</td>
<td>192.168.13.12</td>
</tr>
<tr class="header">
<th>prd-scs-admin-server-01</th>
<td>uat-scs-db-01</td>
<td>Database Server (UAT)</td>
<td>192.168.13.13</td>
</tr>
<tr class="odd">
<th>prd-scs-admin-server-01</th>
<td>uat-scs-filer</td>
<td>File Server (UAT)</td>
<td>192.168.13.15</td>
</tr>
<tr class="header">
<th>prd-scs-admin-server-01</th>
<td>uat-scs-proxy</td>
<td>Reverse Proxy Server (UAT)</td>
<td>192.168.13.14 / 10.5.161.224</td>
</tr>
</tbody>
</table>

**UAT Environment (GCIS T1):**

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
</thead>
<tbody>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scsuwi</td>
<td>Reverse Proxy Server (Internet DMZ)</td>
<td>192.168.0.7 / 45.119.94.99</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scsuwg</td>
<td>Reverse Proxy Server (GNET DMZ)</td>
<td>192.168.4.7 / 10.148.11.220</td>
</tr>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scsuad</td>
<td>Apps Server (Trust Zone)</td>
<td>192.168.8.9</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scsudb</td>
<td>Database Server (Trust Zone)</td>
<td>192.168.8.10</td>
</tr>
</tbody>
</table>

**DEV Environment (WKGO):**

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
</thead>
<tbody>
<tr class="odd">
<th>prd-scs-admin-server-02</th>
<td>dev-scs-admin-api-01</td>
<td>API Server (DEV)</td>
<td>192.168.14.10</td>
</tr>
<tr class="header">
<th>prd-scs-admin-server-02</th>
<td>dev-scs-admin-frontend-01</td>
<td>Frontend Server (DEV)</td>
<td>192.168.14.11</td>
</tr>
<tr class="odd">
<th>prd-scs-admin-server-02</th>
<td>dev-scs-admin-backend-01</td>
<td>Backend Server (DEV)</td>
<td>192.168.14.12</td>
</tr>
<tr class="header">
<th>prd-scs-admin-server-02</th>
<td>dev-scs-db-01</td>
<td>Database Server (DEV)</td>
<td>192.168.14.13</td>
</tr>
<tr class="odd">
<th>prd-scs-admin-server-02</th>
<td>dev-scs-filer</td>
<td>File Server (DEV)</td>
<td>192.168.14.15</td>
</tr>
<tr class="header">
<th>prd-scs-admin-server-02</th>
<td>dev-scs-proxy</td>
<td>Reverse Proxy Server (DEV)</td>
<td>192.168.14.14 / 10.5.161.225</td>
</tr>
</tbody>
</table>

**DEV Environment (GCIS T1):**

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
</thead>
<tbody>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scsdwi</td>
<td>Reverse Proxy Server (Internet DMZ)</td>
<td>192.168.0.6 / 45.119.94.100</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scsdwg</td>
<td>Reverse Proxy Server (GNET DMZ)</td>
<td>192.168.4.6 / 10.148.11.220</td>
</tr>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scsdad</td>
<td>Apps Server (Trust Zone)</td>
<td>192.168.8.7</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scsddb</td>
<td>Database Server (Trust Zone)</td>
<td>192.168.8.8</td>
</tr>
</tbody>
</table>

**DR Environment (AIA):**

\[image here]

**List of machines and virtual machines:**

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
</thead>
<tbody>
<tr class="odd">
<th rowspan="2">dr-scs-admin-server-01</th>
<td>dr-scs-vcenter-01</td>
<td>vCenter (DR)</td>
<td>192.168.20.18 / 10.5.174.225</td>
</tr>
<tr class="header">
<td>dr-scs-log-01</td>
<td>Kiwi Log Server (DR)</td>
<td>192.168.20.10</td>
</tr>
<tr class="odd">
<th rowspan="7">dr-scs-admin-server-01</th>
<td>dr-scs-backup-01</td>
<td>Veeam Backup Server (DR)</td>
<td>192.168.20.19 / 10.5.161.224</td>
</tr>
<tr class="header">
<td>dr-scs-admin-api-01</td>
<td>API Server (DR)</td>
<td>192.168.22.11</td>
</tr>
<tr class="odd">
<td>dr-scs-admin-frontend-01</td>
<td>Frontend Server (DR)</td>
<td>192.168.22.12</td>
</tr>
<tr class="header">
<td>dr-scs-admin-backend-01</td>
<td>Backend Server (DR)</td>
<td>192.168.22.13</td>
</tr>
<tr class="odd">
<td>dr-scs-db-01</td>
<td>Database Server (DR)</td>
<td>192.168.22.14</td>
</tr>
<tr class="header">
<td>dr-scs-filer</td>
<td>File Server (DR)</td>
<td>192.168.22.16</td>
</tr>
<tr class="odd">
<td>dr-scs-proxy</td>
<td>Reverse Proxy Server (DR)</td>
<td>192.168.22.15 / 10.5.174.228</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scspwi</td>
<td>Reverse Proxy Server (Internet DMZ - DR)</td>
<td>192.168.0.6 / 45.119.93.84</td>
</tr>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scspwg</td>
<td>Reverse Proxy Server (GNET DMZ - DR)</td>
<td>192.168.4.6 / 10.160.139.211</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scspad</td>
<td>Apps Server (Trust Zone - DR)</td>
<td>192.168.8.6</td>
</tr>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scspdb</td>
<td>Database Server (Trust Zone - DR)</td>
<td>192.168.8.7</td>
</tr>
<tr class="header">
<th>GCIS Infrastructure</th>
<td>scspbk2</td>
<td>Veeam Backup Server (Trust Zone - DR)</td>
<td>192.168.8.9</td>
</tr>
<tr class="odd">
<th>GCIS Infrastructure</th>
<td>scsplog</td>
<td>Kiwi Log Server (Trust Zone - DR)</td>
<td>192.168.8.10</td>
</tr>
</tbody>
</table>

# 2. Purpose

This document is a checklist of handover materials within project scope;
and it also provides relevant information to the support maintenance
staffs who will be maintaining this system in the future. All these
deliverables should be received from system implementation team of the
Licensing Self-Certification Portal (LSCP); to the Buildings Department
(BD) of the Government of the Hong Kong Special Administrative Region
(HKSARG or the Government).

The hand-over items of this project can be summarized into the following
6 items:

> 1\. Documentation
>
> 2\. Program Source code (Backend Application, Frontend Web App,
> Fronted Mobile App)
>
> 3\. Administration Accounts
>
> 4\. System backup
>
> 5\. Hardware
>
> 6\. Software Packages and Licenses

## 2.1 Schedule

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     |      | MC/BD          |
| Verification |      | BD             |

## 2.2 Verification

1.  The application URL verification

> The access link (URL) of each application should be verified by
> performing an access checking.

2.  Login accounts verification

> The login accounts of the applications and servers should be verified
> by processing login action.

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

In this section, it will list the user account for management in the
different areas.

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

**Administration Accounts on LSCP**

| Environment | User Type | User account | Password |
|-------------|-----------|--------------|----------|
| UAT         | BD Admin  |              |          |
| PRD / DR    | BD Admin  |              |          |
|             |           |              |          |

# 6. Backup

<span class="mark">\[RY Note: Following content needs to check]</span>

## 6.1 VM Backup

Backup service is carried out by backup server.

Daily VM image backup is carried out and store in the backup servers. A
further copy of production VM images is copied to DR?s backuper server.

**Backup Strategy Details:**

Production, UAT and DEV environments on WKGO and DR on AIA will be
backuped by the backup servers (prd-scs-backup-01 and dr-scs-backup-01).

Daily VM image backup is carried out and stored in the backup storage,
Weekly to tape and Daily Copy to AIA.

Production and DR site included 8 backups, PROD VM Backup Job 3 Daily,
PROD VM Backup to Tape Job 3 Weekly, PROD UAT VM Backup Job 1 Daily,
PROD UAT VM Backup to Tape Job 1 Weekly, PROD DEV VM Backup Job 2 Daily,
PROD DEV VM Backup to Tape Job 2 Weekly, DR VM Backup Job 4 Daily and
PROD All jobs to DR Backup Copy Job 1 to AIA.

All instances including system files, database backup and data file will
be backuped by backup jobs as VM Image managed by Veeam.

Database servers (in both PROD and DR) will perform a local database
backup and store in local harddisk. It will be backed up by the backup
server and copied to AIA.

Production environments on GCIS P1 will be backuped by backup services
that are provided by GCIS with offsite copy and replicated to DR GCIS
P2.

Production database server on GCIS P1 will perform a local database
backup and store in local harddisk. It will be backed up by the Veeam
backup server (scspbk2) for additional copy.

UAT and DEV environments on GCIS will be backup by backup services that
are provided by GCIS.

## 6.2 Database Backup

Database full export backup: this type of backup contains full database
exported database objects including schemas, table structures, packages,
stored procedures and data.

Daily full export backup is done on DB servers, data stored on the DB
servers and further backed up by VM Backup.

**SQL Database Backup:**

Beside DB server VM backup, database full export backup will be carried out as well. This type
of backup contains full database export database objects including
schemas, table structures, packages, stored procedures and data at 18:45
daily.

The daily full export backup is done on DB servers (uat-db-01,
prd-db-01, prd-db-02, dr-db-01), data stored on the DB servers?
directory: D:\backup\\

**Backup Schedule:**

|                                         |                                                 |
|-------------------------------------|-----------------------------------|
| Name                                    | Schedule                                        |
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

<span class="mark">\[RY Note: Items are for reference only. They are
incorrect]</span>

| Item                                                                              | Amount | Expire At |
|------------------------|------------------------|------------------------|
| Windows 2022 Standard (16-Core) - Perpetual                                       |        |           |
| SQL 2019 Standard (2-Core) - Perpetual                                            |        |           |
| Veeam Availability Suite Universal License (10-Instance) with 3 year prod support |        |           |
| Symantec SEP License (3 years)                                                    |        |           |
| Kiwi Log Servers (with 3 year support & subscription)                             |        |           |
| vSphere Standard (basic Support with 3years SNS)                                  |        |           |
| vCenter Standard (basic Support with 3years SNS)                                  |        |           |

# 9. Log Management

1\. Following activities shall include in the log:

> ? Attempts for log-in
>
> ? Unauthorised update/access
>
> ? Failed attempts for privileges elevation
>
> ? Attempts for password changes
>
> ? Access attempts to critical files (e.g., software configuration
> files, password and key files, etc.)
>
> ? Actions taken by privileged users
>
> ? Use of privileged rights such as addition and deletion of user
> accounts
>
> ? Security related system failures and alerts
>
> ? Changes to user access rights
>
> ? Failed access attempts to systems and files identified as critical
> to the system
>
> ? Computer services such as file copying or searching
>
> ? Modification to audit policy
>
> ? Activation and de-activation of protection systems, such as
> anti-malware systems and intrusion detection systems

2\. Logs shall be retained for **180 days** and centralised and managed
by Syslog server. Unauthorised access is restricted.

3\. Logs will be reviewed regularly.

4\. Logs shall not be used to profile the activity of a particular user
unless it relates to a necessary audit activity supported by a
Directorate rank officer.

\<\<\< End of document \>\>\>
```