<img src="media/image1.jpg" style="width:1.30903in;height:1.30903in" />

**SYSTEM MANUAL**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">COMBINED SYSTEM DEVELOPMENT SERVICES</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**<span class="smallcaps">OF THE</span>**

**<span class="smallcaps">BUILDINGS DEPARTMENT</span>**

**Version: 0.1**

**Nov 2024**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR

<table>
<colgroup>
<col style="width: 17%" />
<col style="width: 82%" />
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

|                   |                      |                                      |                           |            |
|----------|------------------------------|-------------|----------|------------|
| Amendment History |                      |                                      |                           |            |
| Change Number     | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date       |
| 1                 | 1st draft            | All                                  | 0.1                       | 7/11/2024  |
| 2                 | 2<sup>nd</sup> draft | All                                  | 0.2                       | 19/11/2024 |
|                   |                      |                                      |                           |            |

TABLE OF CONTENTS

[1. Purpose 5](#_heading=h.3j2qqm3)

[2. Scope 5](#_heading=h.3znysh7)

[3. Reference 5](#_heading=h.tyjcwt)

[4. Definitions and Convention 6](#_heading=h.206ipza)

> [4.1 Definitions 6](#definitions)
>
> [4.2 Conventions 6](#conventions)

[5. System Summary 7](#_heading=h.2dlolyb)

> [5.1 Objective 7](#objective)
>
> [5.2 System Architecture 8](#system-architecture)
>
> [5.3 System Functions 15](#system-functions)

[6. Equipment Configuration 26](#_heading=h.35nkun2)

> [6.1 Computer Hardware 26](#computer-hardware)
>
> [6.1.1 Hardware Components 26](#hardware-components)
>
> [6.1.2 Guest Servers Components 34](#guest-servers-components)
>
> [6.1.3 Gateway and SMTPX Configuration
> 36](#gateway-and-smtpx-configuration)
>
> [6.1.4 Database Configuration 39](#_heading=h.34g0dwd)
>
> [6.1.5 Detailed Server and Network Configurations
> 40](#_heading=h.1jlao46)

[7. Software Inventories 45](#_heading=h.2iq8gzs)

> [7.1 Inventory of Application Programs
> 45](#inventory-of-application-programs)
>
> [7.2 Inventory of System Software and Software Package
> 45](#inventory-of-system-software-and-software-package)

[8. Security and Backup 51](#_heading=h.2w5ecyt)

> [8.1 System Control 51](#_heading=h.1baon6m)
>
> [8.2 Backup 51](#_heading=h.3vac5uf)
>
> [8.3 Security 52](#_heading=h.2afmg28)
>
> [8.3.1 Data Transmission Security 52](#data-transmission-security)
>
> [8.3.2 Data Storage and Auditing Security
> 52](#data-storage-and-auditing-security)
>
> [8.3.3 System Security 52](#system-security)
>
> [8.3.4 Physical Security 53](#physical-security)
>
> [8.3.5 Password and Group Control 53](#password-and-group-control)
>
> [8.3.6 Control Procedure of Application User Account and Production
> Support Account
> 53](#control-procedure-of-application-user-account-and-production-support-account)
>
> [8.4 Change Control 54](#_heading=h.3mzq4wv)
>
> [8.5 Disaster Recovery 54](#_heading=h.2250f4o)
>
> [8.6 Database Backup Strategy 54](#_heading=h.haapch)
>
> [8.6.1 SQL Database Backup 54](#sql-database-backup)
>
> [8.6.2 Recovery 54](#recovery)
>
> [8.6.3 Backup Schedule 55](#backup-schedule)

[9. Database Administration 57](#database-administration)

> [9.1 Clean Database Transaction Logs 57](#_heading=h.upglbi)
>
> [9.2 Database Backup 60](#_heading=h.3ep43zb)
>
> [9.3 System Constraints and Limitations 62](#bookmark=id.1hmsyys)

1.  <span id="_heading=h.3j2qqm3" class="anchor"></span>**Purpose**

The objective of this document is to provide an overview of the system
by listing out in brief the programs, data files, equipment, clerical
procedure, computer operation procedure, etc. Reader interested in
specific area may refer to the corresponding manuals (Data Manual,
Program Manual, etc.).

The major readers of System Manual are the staff responsible for
maintaining the application system.

<span id="_heading=h.3znysh7" class="anchor"></span>

1.  **Scope**

The System Manual provides a general overview of the software and
hardware configurations for LSCP, and shows the system environment
details such as applications configurations, server and workstation
information and backup services.

In addition, some major system parameters, system configuration files
and the system inventory are enclosed in the Appendices.

The major readers of this document are the staff responsible for
maintaining the application system. Readers interested in specific area
may refer to the corresponding manuals (Data Manual, Program Manual,
etc.).

1.  <span id="_heading=h.tyjcwt" class="anchor"></span>**Reference  
    **

-   Training Manual;

-   Data Manual;

-   Program Manual;

-   Application Operation Manual;

-   Computer Operation Procedure Manual.

1.  <span id="_heading=h.206ipza" class="anchor"></span>**Definitions
    and Convention**

## 4.1 Definitions

None.

## 4.2 Conventions

The following acronyms are used in the text of this document: -

<table>
<colgroup>
<col style="width: 26%" />
<col style="width: 73%" />
</colgroup>
<thead>
<tr class="header">
<th><blockquote>
<p><strong><u>Abbreviation</u></strong></p>
</blockquote></th>
<th><blockquote>
<p><strong><u>Description</u></strong></p>
</blockquote></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>BD</p>
</blockquote></th>
<th><blockquote>
<p>Buildings Department</p>
</blockquote></th>
</tr>
<tr class="header">
<th><blockquote>
<p>LSCP</p>
</blockquote></th>
<th><blockquote>
<p>Licensing Self-Certification Portal</p>
</blockquote></th>
</tr>
<tr class="odd">
<th><blockquote>
<p>DMZ</p>
</blockquote></th>
<th>Demilitarized Zone</th>
</tr>
<tr class="header">
<th><blockquote>
<p>SAN</p>
</blockquote></th>
<th>Storage Area Network</th>
</tr>
<tr class="odd">
<th><blockquote>
<p>VM</p>
</blockquote></th>
<th><blockquote>
<p>Virtual Machine</p>
</blockquote></th>
</tr>
<tr class="header">
<th><blockquote>
<p>ITU</p>
</blockquote></th>
<th>Information Technology Unit</th>
</tr>
<tr class="odd">
<th><blockquote>
<p>WKGO</p>
</blockquote></th>
<th>West Kowloon Government Offices</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span id="_heading=h.2dlolyb" class="anchor"></span>**System
    Summary**

## 5.1 Objective

The users of the LSCP can be classified into two categories:

-   BD Officers

-   Public users involved in site inspection and site monitoring

The primary objective of LSCP is to provide an electronic platform for
site inspection and site monitoring personnel to provide, manage, and
review the inspection and monitoring records.

## 5.2 System Architecture

This is an overview of the system structure of LSCP in the Production
Environment.

<img src="media/image2.png" style="width:6.62605in;height:5.91667in" />

The following diagram illustrates the architecture of the LSCP for
Production site and UAT site in another perspective.

<img src="media/image3.png" style="width:6.62605in;height:5.81944in" />

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
    > servers

-   File Server to store the temporary and permanent files

-   Database Server that hosts Microsoft SQL server to store all the
    > system and user information

-   vCenter Server to manage the VM Hypervisors on each of the physical
    > servers

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

<u>Web Browser Support</u>

<img src="media/image4.png" style="width:6.62605in;height:2.375in" />

<u>iAM Smart</u>

The iAM Smart system implemented by the Government of Hong Kong focuses
primarily on providing a secure and convenient login mechanism and
retrieving basic user information. Pilot CDPSS has integrated with iAM
Smart authentication module. Users can utilize iAM Smart to log in to
Pilot CDPSS services and retrieve basic information associated with
their digital identity.

<u>Departmental Portal</u>

The Departmental Portal is a web service of BD to pass BD user’s
identity to other wb services including the LSCP. When BD users access
LSCP website through the Departmental Portal, the user ID will be
provided to the LSCP to complete the login process without further input
from the user. This login method only available inside BD’s network.

<u>SMTPX</u>

The notification module in BDSCS would send login one-time password
(OTP) and email notification by initiating an SMTPX service provided by
CIS.

<u>MWMS</u>

MWMS would provide data of AP/RSE/RGE/AS acknowledged by BD. Snapshots
of the MWMS data will be interfaced to BDSCS through SFTP and then
internal and external BDSCS applications would intake this data by
processing the batch file auto-generated and delivered from MWMS daily.

<u>BCIS</u>

BCIS would provide address data and BD case data acknowledged by BD. The
latest copy of the BCIS database would be synced to BDSCS through SQL
queries at midnight. The data would then be used in both external and
internal portals for address selection, folio management, and case
logic. Meanwhile, the new BD cases would be synced to BCIS in real time
through a SQL stored procedure.

This is an overview of the system structure of Pilot CDPSS in Disaster
Recovery Environment, similar with the production environment

<img src="media/image5.png" style="width:6.62605in;height:6.44444in" />

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

1.  <span id="_heading=h.35nkun2" class="anchor"></span>**Equipment
    Configuration**

##  Computer Hardware 

### Hardware Components

The Configuration of Physical Server in Production

|                            |                         |                             |                |                        |
|---------------|-------------|--------------|------------|------------------|
| **Model**                  | **Host Name**           | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750 Server | prd-scs-admin-server-01 | 192.168.10.22, 10.5.161.206 | F646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-admin-server-02 | 192.168.10.23, 10.5.161.207 | D646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-nas             | 192.168.10.35, 10.5.161.218 | ???            | ???                    |

The Configuration of SAN storage in Production

|             |                      |                |                       |                                                            |
|----------------|---------------|--------------|--------------|---------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CC    | N/A                   | 192.168.10.16                                              |
| SAN Switch  | Dell DS6610B         | FRC1924T0CD    | N/A                   | 192.168.10.17                                              |
| SAN Storage | Dell PowerStore 500T | HV1NBX3        | 11                    | 192.168.10.26, 192.168.10.27, 192.168.10.28, 192.168.10.29 |

The Configuration of Backup storage in Production

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|----------------|---------------|--------------|--------------|---------------|
| Backup Appliance | Dell DataDomain 3300 | 17XMBX3        | 15TB            | 192.168.10.20  |

The Configuration of Tape Library in Production

| **Type**     | **Model** | **Serial No.** | **No. of slots** | **IP Address** |
|--------------|-----------|----------------|------------------|----------------|
| Tape Library | Dell ML3  | 3555L3A7801YY0 | 35               | 192.168.10.20  |

The Configuration of Firewalls in Production

|               |                 |                 |                  |                |
|--------------|-------------|-------------|---------------|-----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSPri | 192.168.10.12   | 10.5.161.205    | Palo Alto PA-850 | 11901063047    |
| PA-850-SCSSec | 192.168.10.13   | 10.5.161.220    | Palo Alto PA-850 | 11901063049    |

The Configuration of switches in Production

| **Host Name** | **Internal IP** | **Model** | **Serial No.** |
|---------------|-----------------|-----------|----------------|
|               | 192.168.10.14   | Catalyst  |                |
|               | 192.168.10.15   | Catalyst  |                |

The Configuration of KVM in Production

|            |                |
|------------|----------------|
| **Model**  | **Serial No.** |
| Cyber View |                |

The Configuration of UPS in Production

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv™ Liebert® GXT5 3000 | 2102311887222A010008 | 192.168.11.20  |
| Vertiv™ Liebert® GXT5 3000 | 2102311887222A010004 | 192.168.11.21  |

Hardware Components of Production Servers

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
<td>CyberView</td>
<td>1</td>
</tr>
<tr class="even">
<td>13</td>
<td>UPS<br />
(???)</td>
<td>Vertiv™ Liebert® GXT5 3000</td>
<td>1</td>
</tr>
<tr class="odd">
<td>14</td>
<td>UPS<br />
(???)</td>
<td>Vertiv™ Liebert® GXT5 3000</td>
<td>1</td>
</tr>
</tbody>
</table>

Partition Configuration of Production Servers

| **Host Name**           | **Drive**       | **Capacity** | **Description**              |
|--------------------|-----------------|----------|--------------------------|
| prd-scs-admin-server-01 | local           | 2.4TB        | VMware ESXi Operating system |
| prd-scs-admin-server-02 | local           | 2.4TB        | VMware ESXi Operating system |
| PS500T-Cluster1         | VM_Volume01     | 20TB         | Shared pool of storage space |
| PS500T-Cluster1         | QuorumDisk-VM-1 | 2.5GB        | Shared pool of storage space |
| prd-scs-nas             | C:              | ???          | OS                           |
|                         | D:              | ???          | Data                         |

The Configuration of Physical Server in DR Site

|                           |                        |                             |                |                        |
|---------------|-------------|----------------|---------------|--------------|
| **Model**                 | **Host Name**          | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750Server | dr-scs-admin-server-01 | 192.168.20.17, 10.5.174.216 | G646RX3        | RAID-5                 |
| Dell PowerEdge R750Server | dr-scs-nas             | 192.168.20.35, 10.5.174.225 | ???            | ???                    |

The Configuration of SAN storage in DR Site

|             |                      |                |                       |                                                            |
|----------------|---------------|--------------|--------------|---------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CE    | N/A                   | 192.168.20.14                                              |
| SAN Storage | Dell PowerStore 500T | 3W1NBX3        | 11                    | 192.168.20.20, 192.168.20.21, 192.168.20.22, 192.168.20.23 |

The Configuration of Backup storage in Production

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|----------------|---------------|--------------|--------------|---------------|
| Backup Appliance | Dell DataDomain 3300 | J6XMBX3        | 15TB            | 192.168.20.25  |

The Configuration of Firewalls in DR Site

|               |                 |                 |                  |                |
|---------------|-------------|-------------|----------------|-----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSDR  | 192.168.20.12   | 10.5.174.215    | Palo Alto PA-850 | 011901063069   |

The Configuration of Switches in DR Site

|               |                 |              |                |
|---------------|-----------------|--------------|----------------|
| **Host Name** | **Internal IP** | **Model**    | **Serial No.** |
| ???           | 192.168.20.13   | Catalyst ??? | ???            |

The Configuration of UPS in DR Site

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv™ Liebert® GXT5 3000 | 2102311887222A01000A | 192.168.20.11  |

Hardware Components of Disaster Recovery Servers

<table>
<colgroup>
<col style="width: 5%" />
<col style="width: 34%" />
<col style="width: 53%" />
<col style="width: 5%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Hardware Component</th>
<th>Configuration</th>
<th>Qty</th>
</tr>
<tr class="odd">
<th rowspan="5">1</th>
<th rowspan="5"><p>ESXi Hypervisor Server</p>
<p>(dr-scs-admin-server-01)</p></th>
<th>Dell PowerEdge R750</th>
<th>1</th>
</tr>
<tr class="header">
<th>Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz</th>
<th>1</th>
</tr>
<tr class="odd">
<th>32GB DDR4 Synchronous Registered (Buffered)</th>
<th>8</th>
</tr>
<tr class="header">
<th>1.2TB SAS HDD</th>
<th>3</th>
</tr>
<tr class="odd">
<th>ESXi 8.0.3</th>
<th>1</th>
</tr>
<tr class="header">
<th rowspan="5">2</th>
<th rowspan="5"><p>NAS</p>
<p>(dr-scs-nas)</p></th>
<th>Dell PowerEdge R750</th>
<th>1</th>
</tr>
<tr class="odd">
<th>CPU???</th>
<th>???</th>
</tr>
<tr class="header">
<th>RAM???</th>
<th>???</th>
</tr>
<tr class="odd">
<th>HDD???</th>
<th>???</th>
</tr>
<tr class="header">
<th>Windows Server 2022</th>
<th>???</th>
</tr>
<tr class="odd">
<th rowspan="2">3</th>
<th rowspan="2"><p>SAN Switch</p>
<p>(dr-scs-sw-01)</p></th>
<th>Dell DS6610B</th>
<th>1</th>
</tr>
<tr class="header">
<th>Ports</th>
<th>16</th>
</tr>
<tr class="odd">
<th rowspan="2">4</th>
<th><p>SAN Storage</p>
<p>(PS500T-Cluster2)</p></th>
<th>Dell PS500T</th>
<th>1</th>
</tr>
<tr class="header">
<th>DMZ Firewall 1 (CDPDZFW1)</th>
<th>3.8TB NVME SSD</th>
<th>11</th>
</tr>
<tr class="odd">
<th>5</th>
<th><p>Backup Appliance</p>
<p>(dr-scs-backupstorage-01)</p></th>
<th>Dell DataDomain DD3300</th>
<th>1</th>
</tr>
<tr class="header">
<th>6</th>
<th><p>Firewall</p>
<p>(PA-850-SCSPri)</p></th>
<th>Palo Alto PA 850</th>
<th>1</th>
</tr>
<tr class="odd">
<th>7</th>
<th><p>Switch</p>
<p>(???)</p></th>
<th>Cisco ???</th>
<th>1</th>
</tr>
<tr class="header">
<th>8</th>
<th>KVM</th>
<th>CyberView</th>
<th>1</th>
</tr>
<tr class="odd">
<th>9</th>
<th>UPS<br />
(???)</th>
<th>Vertiv™ Liebert® GXT5 3000</th>
<th>1</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Partition Configuration of DR Servers

|                        |             |              |                              |
|--------------------|-----------------|----------|--------------------------|
| **Host Name**          | **Drive**   | **Capacity** | **Description**              |
| dr-scs-admin-server-01 | local       | 2.4TB        | VMware ESXi Operating system |
| PS500T-Cluster2        | VM Volume01 | 20TB         | Shared pool of storage space |
| dr-scs-nas             | C:          | ???          | OS                           |
|                        | D:          | ???          | Data                         |

### Guest Servers Components

Production guest servers

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 20%" />
<col style="width: 10%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Role</strong></th>
<th><strong>Host Name</strong></th>
<th><strong>vCPU</strong></th>
<th><strong>RAM<br />
(GB)</strong></th>
<th><strong>Disk<br />
(GB)</strong></th>
<th><strong>IP Addresses</strong></th>
<th><strong>Data Center</strong></th>
<th><strong>Host Server / Zone</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vCenter</td>
<td>prd-scs-<br />
vcenter-01</td>
<td>16</td>
<td>39</td>
<td>1.33TB</td>
<td><p>192.168.10.24 /</p>
<p>10.5.161.210</p></td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>Veeam Backup Server</td>
<td>prd-scs-<br />
backup-01</td>
<td>8</td>
<td>24</td>
<td><p>300 +</p>
<p>1TB</p></td>
<td><p>192.168.10.25 /</p>
<p>10.5.161.211</p></td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="odd">
<td>Kiwi Log<br />
Server</td>
<td>prd-scs-<br />
log-01</td>
<td>4</td>
<td>16</td>
<td><p>300 +</p>
<p>500</p></td>
<td><p>192.168.10.11 /</p>
<p>10.5.161.223</p></td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>NOD32<br />
Anti-Virus<br />
Server</td>
<td>prd-scs-<br />
esetnod32</td>
<td>4</td>
<td>16</td>
<td>300</td>
<td><p>192.168.10.34 /</p>
<p>10.5.161.215</p></td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="odd">
<td>API<br />
Server</td>
<td>prd-scs-<br />
admin-<br />
api-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.12.11</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>Frontend<br />
Server</td>
<td>prd-scs-<br />
admin-<br />
frontend-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.12.12</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="odd">
<td>Backend<br />
Server</td>
<td>prd-scs-<br />
admin-<br />
backend-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.12.13</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>Database<br />
Server</td>
<td>prd-scs-<br />
db-01</td>
<td>8</td>
<td>16</td>
<td><p>100 +</p>
<p>500</p></td>
<td>192.168.12.14</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="odd">
<td>File<br />
Server</td>
<td>prd-scs-<br />
filer</td>
<td>2</td>
<td>4</td>
<td><p>100 +</p>
<p>1TB</p></td>
<td>192.168.12.20</td>
<td>WKGO</td>
<td>prd-scs-admin-server-01</td>
</tr>
<tr class="even">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>prd-scs-<br />
proxy</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td><p>192.168.12.15 /</p>
<p>10.5.161.226</p></td>
<td>WKGO</td>
<td>prd-scs-admin-server-01</td>
</tr>
<tr class="odd">
<td>API<br />
Server</td>
<td>prd-scs-<br />
admin-<br />
api-02</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.12.16</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="even">
<td>Frontend<br />
Server</td>
<td>prd-scs-<br />
admin-<br />
frontend-02</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.12.17</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="odd">
<td>Backend<br />
Server</td>
<td>prd-scs-<br />
admin-<br />
backend-02</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.12.18</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="even">
<td>Database<br />
Server</td>
<td>prd-scs-<br />
db-02</td>
<td>8</td>
<td>16</td>
<td><p>100 +</p>
<p>500</p></td>
<td>192.168.12.19</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="odd">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>scspwi</td>
<td>2</td>
<td>8</td>
<td>100</td>
<td><p>192.168.0.6 /</p>
<p>45.119.92.84</p></td>
<td><p>GCIS</p>
<p>P1</p></td>
<td>iDMZ</td>
</tr>
<tr class="even">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>scspwg</td>
<td>2</td>
<td>8</td>
<td>100</td>
<td><p>192.168.4.6 /</p>
<p>10.160.11.211</p></td>
<td><p>GCIS</p>
<p>P1</p></td>
<td>gDMZ</td>
</tr>
<tr class="odd">
<td>Apps<br />
Server</td>
<td>scspad</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>500</p></td>
<td>192.168.8.6</td>
<td><p>GCIS</p>
<p>P1</p></td>
<td>Trust Zone</td>
</tr>
<tr class="even">
<td>Database<br />
Server</td>
<td>scspdb</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>200</p></td>
<td>192.168.8.7</td>
<td><p>GCIS</p>
<p>P1</p></td>
<td>Trust Zone</td>
</tr>
<tr class="odd">
<td>Veeam<br />
Backup<br />
Server</td>
<td>scspbk2</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>1TB</p></td>
<td>192.168.8.9</td>
<td><p>GCIS</p>
<p>P1</p></td>
<td>Trust Zone</td>
</tr>
<tr class="even">
<td>Kiwi Log<br />
Server</td>
<td>scsplog</td>
<td>2</td>
<td>8</td>
<td><p>100 +</p>
<p>100</p></td>
<td>192.168.8.10</td>
<td><p>GCIS</p>
<p>P1</p></td>
<td>Trust Zone</td>
</tr>
</tbody>
</table>

UAT guest servers

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 20%" />
<col style="width: 10%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Role</strong></th>
<th><strong>Host Name</strong></th>
<th><strong>vCPU</strong></th>
<th><strong>RAM<br />
(GB)</strong></th>
<th><strong>Disk<br />
(GB)</strong></th>
<th><strong>IP Addresses</strong></th>
<th><strong>Data Center</strong></th>
<th><strong>Host Server / Zone</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>API<br />
Server</td>
<td>uat-scs-<br />
admin-<br />
api-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.13.10</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>Frontend<br />
Server</td>
<td>uat-scs-<br />
admin-<br />
frontend-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.13.11</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="odd">
<td>Backend<br />
Server</td>
<td>uat-scs-<br />
admin-<br />
backend-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.13.12</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>Database<br />
Server</td>
<td>uat-scs-<br />
db-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.13.13</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-01</td>
</tr>
<tr class="odd">
<td>File<br />
Server</td>
<td>uat-scs-<br />
filer</td>
<td>2</td>
<td>4</td>
<td><p>100 +</p>
<p>200</p></td>
<td>192.168.13.15</td>
<td>WKGO</td>
<td>prd-scs-admin-server-01</td>
</tr>
<tr class="even">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>uat-scs-<br />
proxy</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td><p>192.168.13.14 /</p>
<p>10.5.161.224</p></td>
<td>WKGO</td>
<td>prd-scs-admin-server-01</td>
</tr>
<tr class="odd">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>scsuwi</td>
<td>2</td>
<td>8</td>
<td>100</td>
<td><p>192.168.0.7 /</p>
<p>45.119.94.99</p></td>
<td><p>GCIS</p>
<p>T1</p></td>
<td>iDMZ</td>
</tr>
<tr class="even">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>scsuwg</td>
<td>2</td>
<td>8</td>
<td>100</td>
<td><p>192.168.4.7 /</p>
<p>10.148.11.220</p></td>
<td><p>GCIS</p>
<p>T1</p></td>
<td>gDMZ</td>
</tr>
<tr class="odd">
<td>Apps<br />
Server</td>
<td>scsuad</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>200</p></td>
<td>192.168.8.9</td>
<td><p>GCIS</p>
<p>T1</p></td>
<td>Trust Zone</td>
</tr>
<tr class="even">
<td>Database<br />
Server</td>
<td>scsudb</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>100</p></td>
<td>192.168.8.10</td>
<td><p>GCIS</p>
<p>T1</p></td>
<td>Trust Zone</td>
</tr>
</tbody>
</table>

DEV guest servers

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 20%" />
<col style="width: 10%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Role</strong></th>
<th><strong>Host Name</strong></th>
<th><strong>vCPU</strong></th>
<th><strong>RAM<br />
(GB)</strong></th>
<th><strong>Disk<br />
(GB)</strong></th>
<th><strong>IP Addresses</strong></th>
<th><strong>Data Center</strong></th>
<th><strong>Host Server / Zone</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>API<br />
Server</td>
<td>dev-scs-<br />
admin-<br />
api-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.14.10</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="even">
<td>Frontend<br />
Server</td>
<td>dev-scs-<br />
admin-<br />
frontend-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.14.11</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="odd">
<td>Backend<br />
Server</td>
<td>dev-scs-<br />
admin-<br />
backend-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.14.12</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="even">
<td>Database<br />
Server</td>
<td>dev-scs-<br />
db-01</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td>192.168.14.13</td>
<td>WKGO</td>
<td>prd-scs-admin-<br />
server-02</td>
</tr>
<tr class="odd">
<td>File<br />
Server</td>
<td>dev-scs-<br />
filer</td>
<td>2</td>
<td>4</td>
<td><p>100 +</p>
<p>200</p></td>
<td>192.168.14.15</td>
<td>WKGO</td>
<td>prd-scs-admin-server-02</td>
</tr>
<tr class="even">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>dev-scs-<br />
proxy</td>
<td>2</td>
<td>4</td>
<td>100</td>
<td><p>192.168.14.14 /</p>
<p>10.5.161.225</p></td>
<td>WKGO</td>
<td>prd-scs-admin-server-02</td>
</tr>
<tr class="odd">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>scsdwi</td>
<td>2</td>
<td>8</td>
<td>100</td>
<td><p>192.168.0.6 /</p>
<p>45.119.94.100</p></td>
<td><p>GCIS</p>
<p>T1</p></td>
<td>iDMZ</td>
</tr>
<tr class="even">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>scsdwg</td>
<td>2</td>
<td>8</td>
<td>100</td>
<td><p>192.168.4.6 /</p>
<p>10.148.11.220</p></td>
<td><p>GCIS</p>
<p>T1</p></td>
<td>gDMZ</td>
</tr>
<tr class="odd">
<td>Apps<br />
Server</td>
<td>scsdad</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>200</p></td>
<td>192.168.8.7</td>
<td><p>GCIS</p>
<p>T1</p></td>
<td>Trust Zone</td>
</tr>
<tr class="even">
<td>Database<br />
Server</td>
<td>scsddb</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>100</p></td>
<td>192.168.8.8</td>
<td><p>GCIS</p>
<p>T1</p></td>
<td>Trust Zone</td>
</tr>
</tbody>
</table>

Disaster Recovery guest servers

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 20%" />
<col style="width: 10%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Role</strong></th>
<th><strong>Host Name</strong></th>
<th><strong>vCPU</strong></th>
<th><strong>RAM<br />
(GB)</strong></th>
<th><strong>Disk<br />
(GB)</strong></th>
<th><strong>IP Addresses</strong></th>
<th><strong>Data Center</strong></th>
<th><strong>Host Server / Zone</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vCenter</td>
<td>dr-scs-<br />
vcenter-01</td>
<td>16</td>
<td>39</td>
<td>1.33TB</td>
<td><p>192.168.20.18 /</p>
<p>10.5.174.225</p></td>
<td>AIA</td>
<td>dr-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>Veeam Backup Server</td>
<td>dr-scs-<br />
backup-01</td>
<td>8</td>
<td>24</td>
<td><p>300 +</p>
<p>1TB</p></td>
<td><p>192.168.20.19 /</p>
<p>10.5.161.224</p></td>
<td>AIA</td>
<td>dr-scs-admin-<br />
server-01</td>
</tr>
<tr class="odd">
<td>Kiwi Log<br />
Server</td>
<td>dr-scs-<br />
log-01</td>
<td>4</td>
<td>8</td>
<td><p>300 +</p>
<p>500</p></td>
<td>192.168.20.10</td>
<td>AIA</td>
<td>dr-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>API<br />
Server</td>
<td>dr-scs-<br />
admin-<br />
api-01</td>
<td>2</td>
<td>8</td>
<td>90</td>
<td>192.168.22.11</td>
<td>AIA</td>
<td>dr-scs-admin-<br />
server-01</td>
</tr>
<tr class="odd">
<td>Frontend<br />
Server</td>
<td>dr-scs-<br />
admin-<br />
frontend-01</td>
<td>2</td>
<td>8</td>
<td>90</td>
<td>192.168.22.12</td>
<td>AIA</td>
<td>dr-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>Backend<br />
Server</td>
<td>dr-scs-<br />
admin-<br />
backend-01</td>
<td>2</td>
<td>8</td>
<td>90</td>
<td>192.168.22.13</td>
<td>AIA</td>
<td>dr-scs-admin-<br />
server-01</td>
</tr>
<tr class="odd">
<td>Database<br />
Server</td>
<td>dr-scs-<br />
db-01</td>
<td>2</td>
<td>8</td>
<td><p>90 +</p>
<p>500</p></td>
<td>192.168.22.14</td>
<td>AIA</td>
<td>dr-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>File<br />
Server</td>
<td>dr-scs-<br />
filer</td>
<td>2</td>
<td>8</td>
<td><p>90 +</p>
<p>1TB</p></td>
<td>192.168.22.16</td>
<td>AIA</td>
<td>dr-scs-admin-<br />
server-01</td>
</tr>
<tr class="odd">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>dr-scs-<br />
proxy</td>
<td>2</td>
<td>4</td>
<td>90</td>
<td><p>192.168.22.15 /</p>
<p>10.5.174.228</p></td>
<td>AIA</td>
<td>dr-scs-admin-<br />
server-01</td>
</tr>
<tr class="even">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>scspwi</td>
<td>2</td>
<td>8</td>
<td>100</td>
<td><p>192.168.0.6 /</p>
<p>45.119.93.84</p></td>
<td><p>GCIS</p>
<p>P2</p></td>
<td>iDMZ</td>
</tr>
<tr class="odd">
<td>Reverse<br />
Proxy<br />
Server</td>
<td>scspwg</td>
<td>2</td>
<td>8</td>
<td>100</td>
<td><p>192.168.4.6 /</p>
<p>10.160.139.211</p></td>
<td><p>GCIS</p>
<p>P2</p></td>
<td>gDMZ</td>
</tr>
<tr class="even">
<td>Apps<br />
Server</td>
<td>scspad</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>500</p></td>
<td>192.168.8.6</td>
<td><p>GCIS</p>
<p>P2</p></td>
<td>Trust Zone</td>
</tr>
<tr class="odd">
<td>Database<br />
Server</td>
<td>scspdb</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>200</p></td>
<td>192.168.8.7</td>
<td><p>GCIS</p>
<p>P2</p></td>
<td>Trust Zone</td>
</tr>
<tr class="even">
<td>Veeam<br />
Backup<br />
Server</td>
<td>scspbk2</td>
<td>4</td>
<td>16</td>
<td><p>100 +</p>
<p>1TB</p></td>
<td>192.168.8.9</td>
<td><p>GCIS</p>
<p>P2</p></td>
<td>Trust Zone</td>
</tr>
<tr class="odd">
<td>Kiwi Log<br />
Server</td>
<td>scsplog</td>
<td>2</td>
<td>8</td>
<td><p>100 +</p>
<p>100</p></td>
<td>192.168.8.10</td>
<td><p>GCIS</p>
<p>P2</p></td>
<td>Trust Zone</td>
</tr>
</tbody>
</table>

### Gateway and SMTPX Configuration

SMTPX

<table>
<colgroup>
<col style="width: 30%" />
<col style="width: 69%" />
</colgroup>
<tbody>
<tr class="odd">
<td>SMTPX service hostname</td>
<td>smtpx.cis.hksarg (resolvable by CCGO DNS)</td>
</tr>
<tr class="even">
<td>SMTPX service IP address</td>
<td><p>10.106.5.103</p>
<p>10.106.5.104</p>
<p>10.106.105.103</p>
<p>10.106.105.104</p>
<p>(IP addresses are provided for ACL settings. To enjoy the automatic
failover feature,</p>
<p>mail servers should access SMTPX service through hostname.)</p></td>
</tr>
<tr class="odd">
<td>SMTP port number</td>
<td>587</td>
</tr>
<tr class="even">
<td>Sender IP address</td>
<td>(B/Ds' IP address within GNET)</td>
</tr>
<tr class="odd">
<td>Login and password</td>
<td>Not required</td>
</tr>
<tr class="even">
<td>Authentication</td>
<td>By e-Certificate issued from Hong Kong Post or the Government
ISCCA</td>
</tr>
<tr class="odd">
<td>Sender address in e-mail</td>
<td>Valid e-mail address registered in IMX service</td>
</tr>
<tr class="even">
<td>Connection encryption</td>
<td>STARTTLS (Mandatory)</td>
</tr>
<tr class="odd">
<td>Compatible Protocols</td>
<td>SPF and DKIM</td>
</tr>
</tbody>
</table>

SMTPX configured in the IIS 6.0 of the following servers

scspwg, scsuwg,scsdwg

WKGO Production Network Gateway

|              |               |                  |                      |
|--------------|---------------|------------------|----------------------|
| **Gateway**  | **Subnet**    | **IP Range**     | **vlan / Zone**      |
| 192.168.10.1 | 255.255.255.0 | 192.168.10.1-254 | Management           |
| 192.168.11.1 | 255.255.255.0 | 192.168.11.1-254 | Replication / Backup |
| 192.168.12.1 | 255.255.255.0 | 192.168.12.1-254 | Production           |
| 192.168.13.1 | 255.255.255.0 | 192.168.13.1-254 | UAT                  |
| 192.168.14.1 | 255.255.255.0 | 192.168.14.1-254 | DEV                  |
| 10.5.161.1   | 255.255.255.0 | 10.5.161.205-235 | BD Network           |

AIA DR Network Gateway

|              |               |                  |                      |
|--------------|---------------|------------------|----------------------|
| **Gateway**  | **Subnet**    | **IP Range**     | **vlan / Zone**      |
| 192.168.20.1 | 255.255.255.0 | 192.168.20.1-254 | Management           |
| 192.168.21.1 | 255.255.255.0 | 192.168.21.1-254 | Replication / Backup |
| 192.168.22.1 | 255.255.255.0 | 192.168.22.1-254 | Production           |
| 10.5.174.1   | 255.255.255.0 | 10.5.174.215-234 | BD Network           |

1.  <span id="_heading=h.34g0dwd" class="anchor"></span>Database
    Configuration

WKGO Production:

> Windows Cluster: prd-scs-db-cl-01 192.168.12.21
>
> Database Availability Group: prd-scs-db-agl 192.168.12.22  
> Replicas:

-   prd-scs-db-01 192.168.12.14 (Primary)

-   prd-scs-db-02 192.168.12.19 (Secondary)

WKGO UAT:

> Database: uat-scs-db-01 192.168.13.13

WKGO DEV:

> Database: dev-scs-db-01 192.168.14.13

AIA DR:

> Database: dr-scs-db-01 192.168.22.14

GCIS P1:

> Database: scspdb 192.168.8.7

GCIS UAT:

> Database: scsudb 192.168.8.10

GCIS DEV:

> Database: scsddb 192.168.8.8

GCIS P2 DR:

> Database: scspdb 192.168.8.7

1.  <span id="_heading=h.1jlao46" class="anchor"></span>Detailed Server
    and Network Configurations

Rack diagram

<img src="media/image6.png" style="width:6.62605in;height:5.30556in" />

1.  External firewall

Please reference BD CDPSS - Prod Installation & Operation Manual
(network) v1.0 Section 1

Please reference BD - VM & Network Upgrade for CDPSS Site Infra
Configuration Information - 20230427_v0.1 tab - Prod - FW port, Prod -
FW VIP policy, DR - FW port, DR - FW VIP policy

(both documents attached below)

1.  Internal firewall

Please reference BD CDPSS - Prod Installation & Operation Manual
(network) v1.0 Section 2

Please reference BD - VM & Network Upgrade for CDPSS Site Infra
Configuration Information - 20230427_v0.1 tab - Prod - FW port, Prod -
FW VIP policy, DR - FW port, DR - FW VIP policy

1.  Windows NLB

Please reference BD CDPSS - Prod Installation & Operation Manual
(network) v1.0 Section 3

![](media/image7.emf)![](media/image8.emf)

1.  Switches - Prod DMZ Port

<img src="media/image9.png" style="width:6.62569in;height:5.86111in" />

1.  Switches - Prod INT SW Port

<img src="media/image10.png" style="width:6.62569in;height:5.75in" />

1.  Switches – DR DMZ SW Port

<img src="media/image11.png" style="width:6.62569in;height:3.43056in" />

1.  Switches – DR INT SW Port

<img src="media/image12.png" style="width:6.62569in;height:3.66667in" />

1.  <span id="_heading=h.2iq8gzs" class="anchor"></span>**Software
    Inventories**

### 7.1 Inventory of Application Programs

For details of Application Programs for LSCP, please refer to Program
Manual (T352).

### 7.2 Inventory of System Software and Software Package

Summary of software required is given in the following table:

<u>Production Environment – WKGO</u>

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

\*VMware vSphere is a suite of software components for virtualization.
These include ESXi, vCenter Server, and other software components such
as vCenter Single Sign-On, and vCenter Server plug-ins that fulfill
several different functions in the vSphere environment.

*https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-vcenter-esxi-management/GUID-B3A1A79B-EF9B-4C10-A053-D54D88254C52.html*

<u>UAT Environment – WKGO</u>

<table>
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
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>Microsoft SQL Server 2022 16.0.1000.6</p>
<p>Microsoft Management Studio 19.1</p></td>
</tr>
<tr class="even">
<td>File Server</td>
<td>uat-scs-filer</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p></td>
</tr>
<tr class="odd">
<td>Reverse Proxy Server</td>
<td>uat-scs-proxy</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>Nginx 1.26.2</p></td>
</tr>
</tbody>
</table>

<u>DEV Environment – WKGO</u>

<table>
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
<td>dev-scs-admin-api-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p></td>
</tr>
<tr class="odd">
<td>Frontend Server</td>
<td>dev-scs-admin-frontend-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>IIS 10.0.20348.1</p></td>
</tr>
<tr class="even">
<td>Backupend Server</td>
<td>dev-scs-admin-backend-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p></td>
</tr>
<tr class="odd">
<td>Database Server</td>
<td>dev-scs-db-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>Microsoft SQL Server 2022 16.0.1000.6</p>
<p>Microsoft Management Studio 19.1</p></td>
</tr>
<tr class="even">
<td>File Server</td>
<td>dev-scs-filer</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p></td>
</tr>
<tr class="odd">
<td>Reverse Proxy Server</td>
<td>dev-scs-proxy</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>Nginx 1.26.2</p></td>
</tr>
</tbody>
</table>

<u>Production Environment – GCIS P1</u>

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
<td><p>Veeam Backup</p>
<p>Server</p></td>
<td>scspbk2</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Veeam Backup &amp; Replication 12.1.2.172</p></td>
</tr>
<tr class="odd">
<td>Kiwi Log Server</td>
<td>scsplog</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Kiwi Syslog Server 9.8.3 (Service Edition)</p></td>
</tr>
<tr class="even">
<td>Reverse Proxy Server</td>
<td><p>scspwi</p>
<p>scspwg</p></td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Nginx 1.26.2</p></td>
</tr>
<tr class="odd">
<td>Application Server</td>
<td>scspad</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>IIS 10.0.17763.1</p></td>
</tr>
<tr class="even">
<td>Database Server</td>
<td>scspdb</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Microsoft SQL Server 2022 16.0.1000.6</p>
<p>Microsoft Management Studio 19.1</p></td>
</tr>
</tbody>
</table>

<u>UAT Environment – GCIS T1</u>

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
<td>Reverse Proxy Server</td>
<td><p>scsuwi</p>
<p>scsuwg</p></td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Nginx 1.26.2</p></td>
</tr>
<tr class="odd">
<td>Application Server</td>
<td>scsuad</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>IIS 10.0.17763.1</p></td>
</tr>
<tr class="even">
<td>Database Server</td>
<td>scsudb</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Microsoft SQL Server 2022 16.0.1000.6</p>
<p>Microsoft Management Studio 19.1</p></td>
</tr>
</tbody>
</table>

<u>DEV Environment – GCIS T1</u>

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
<td>Reverse Proxy Server</td>
<td><p>scsdwi</p>
<p>scsdwg</p></td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Nginx 1.26.2</p></td>
</tr>
<tr class="odd">
<td>Application Server</td>
<td>scsdad</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>IIS 10.0.17763.1</p></td>
</tr>
<tr class="even">
<td>Database Server</td>
<td>scsddb</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Microsoft SQL Server 2022 16.0.1000.6</p>
<p>Microsoft Management Studio 19.1</p></td>
</tr>
</tbody>
</table>

<u>DR Environment – AIA</u>

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
<td>dr-scs-backup-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>Veeam Backup &amp; Replication 12.1.2.172</p></td>
</tr>
<tr class="even">
<td>Kiwi Log Server</td>
<td>dr-scs-log-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>Kiwi Syslog Server NG 1.2.1.4</p></td>
</tr>
<tr class="odd">
<td>API Server</td>
<td>dr-scs-admin-api-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p></td>
</tr>
<tr class="even">
<td>Frontend Server</td>
<td>drd-scs-admin-frontend-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>IIS 10.0.20348.1</p></td>
</tr>
<tr class="odd">
<td>Backupend Server</td>
<td>dr-scs-admin-backend-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p></td>
</tr>
<tr class="even">
<td>Database Server</td>
<td>dr-scs-db-01</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>Microsoft SQL Server 2022 16.0.1000.6</p>
<p>Microsoft Management Studio 19.1</p></td>
</tr>
<tr class="odd">
<td>File Server</td>
<td>dr-scs-filer</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p></td>
</tr>
<tr class="even">
<td>Reverse Proxy Server</td>
<td>dr-scs-proxy</td>
<td><p>Windows Server 2022 21H2</p>
<p>VMware Tools 12.4.0.23259341</p>
<p>ESET Server Security 10.0.12012.0</p>
<p>ESET Management Agent 10.1.1292.0</p>
<p>Nginx 1.26.2</p></td>
</tr>
<tr class="odd">
<td>vCenter</td>
<td>dr-scs-vcenter-01</td>
<td>vCenter 8.0.3 Build 24322831</td>
</tr>
<tr class="even">
<td>VM Host</td>
<td>dr-scs-admin-server-01</td>
<td>VMWare vSphere 8.0.3 Build 24022510</td>
</tr>
</tbody>
</table>

\*VMware vSphere is a suite of software components for virtualization.
These include ESXi, vCenter Server, and other software components such
as vCenter Single Sign-On, and vCenter Server plug-ins that fulfill
several different functions in the vSphere environment.

*https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-vcenter-esxi-management/GUID-B3A1A79B-EF9B-4C10-A053-D54D88254C52.html*

<u>Production Environment (Replicate from P1)– GCIS P2</u>

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
<td><p>Veeam Backup</p>
<p>Server</p></td>
<td>scspbk2</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Veeam Backup &amp; Replication 12.1.2.172</p></td>
</tr>
<tr class="odd">
<td>Kiwi Log Server</td>
<td>scsplog</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Kiwi Syslog Server 9.8.3 (Service Edition)</p></td>
</tr>
<tr class="even">
<td>Reverse Proxy Server</td>
<td><p>scspwi</p>
<p>scspwg</p></td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Nginx 1.26.2</p></td>
</tr>
<tr class="odd">
<td>Application Server</td>
<td>scspad</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>IIS 10.0.17763.1</p></td>
</tr>
<tr class="even">
<td>Database Server</td>
<td>scspdb</td>
<td><p>Windows Server 2019 1809</p>
<p>VMware Tools 12.1.0.20219665</p>
<p>Bitdefender Endpoint Security Tools 7.9.17.458</p>
<p>Microsoft SQL Server 2022 16.0.1000.6</p>
<p>Microsoft Management Studio 19.1</p></td>
</tr>
</tbody>
</table>

Framework using during development

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 54%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><blockquote>
<p>1</p>
</blockquote></td>
<td>React (frontend)</td>
<td><blockquote>
<p>18.2.0</p>
</blockquote></td>
</tr>
<tr class="even">
<td><blockquote>
<p>2</p>
</blockquote></td>
<td>ExpressJS (backend)</td>
<td><blockquote>
<p>4.19.2</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><blockquote>
<p>3</p>
</blockquote></td>
<td>NodeJS (runtime)</td>
<td><blockquote>
<p>20.11.1</p>
</blockquote></td>
</tr>
</tbody>
</table>

1.  <span id="_heading=h.2w5ecyt" class="anchor"></span>**Security and
    Backup**

    1.  <span id="_heading=h.1baon6m" class="anchor"></span> System
        > Control

There will be no change in the existing authentication mechanisms. BD
staff would still be authenticated by the OSDP before they can access
the LSCP. If OSDP is unavailable in some situations such as maintenance,
the LSCP would itself authenticate the users by the username and
password + one-time password.

As for external users, they will still be required to be authenticated
by OTP sent via email.

Password complexity and policy will be updated to follow the latest IT
Security Guidelines \[G3\].

The LSCP grants functions access rights to users based on their post,
and only “Responsible Officers” are allowed to maintain their own
records.

1.  <span id="_heading=h.3vac5uf" class="anchor"></span>Backup

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

1.  <span id="_heading=h.2afmg28" class="anchor"></span>Security

The system conforms to security policy, guideline and regulation set out
by the Buildings Department and DPO.

### 8.3.1 Data Transmission Security

Data of the LSCP is classified to the “Restricted” level. Data
transmission over the network will be encrypted by HTTPS over TLS. In
order to enable TLS on the web servers of the LSCP, certificates will be
applied, OGCIO’s Intranet Server Certificate Certification Authority
(ISCCA) certificate will be apply for securing servers, applications,
and communications within BD internal network (intranet)., Public SSL
certificates, from HK post are used on public-facing servers and
websites, intended to be trusted by the general public over Internet.
Self-generated cert is used to secure the availability group which
contains 2 production databases. And iAM Smart cert are configured in
LSCP backend application in order to work with iAM Smart Mobile App.

### 8.3.2 Data Storage and Auditing Security

Data of the LSCP in production environment is stored in SAN storage. On
the other hand, data storage in DR environment is stored in local server
storage, Access and audit controls to this folder or drive are strictly
controlled. Both environments facilitated with RAID (Redundant Array of
Inexpensive Disks or Redundant Array of Independent Disks) mirroring
data storage technology and all data are encrypted, OS secured by RAID 1
while data secured by ADAPT and Raid 6. In terms of fault tolerance,
ADAPT (Autonomic Distributed Allocation Protection Technology) and Raid
6 withstands the failure of 2 hard disks. Moreover, all data facilitated
with audit trail, records add/ change/ delete actions reposted in
database for tracking who/ when/ what data being amended.

### 8.3.3 System Security

Regular service pack and patch updates are performed on operating system
and software installed in servers and user workstations in order to fix
the known security issues.

All servers in both the production and DR environment will be installed
with Antivirus clients and managed by a virtualised Antivirus Management
server installed at Trust zone. The server will download the latest
virus signatures from the antivirus software provider (Symantec) and
update all client servers during non-peak hours. Protection policy, such
as scanning schedule, will be enforced by the BD’s antivirus management
server too.

The external users will be responsible for the security protection on
their computers. Their computers will have personal firewall enabled,
the latest security patches applied, and anti-virus protection and
malicious code detection installed.

### 8.3.4 Physical Security

Servers and equipment of the development/testing, production and DR
environments are located in the server rooms, which the server rooms
setup compliant with the section 8 of IT Security Guidelines \[G3\] and
section 5.8 of Data Centre Site Preparation Guidelines \[G36\] where
applicable.

### 8.3.5 Password and Group Control

The LSCP is protected by password control, BD user is able to login via
DP of the Buildings Department and Internet, if login via Internet, it
requires to submit password plus a one- time password by Authenticator,
otherwise only one password requires. Public user can login via Internet
and iAM Smart app, login via Internet requires password plus a one-time
password by email, login via iAM Smart app requires no password.

User are limited to access specific function, field, case and
administrative authority by assignment of user group to user account.

### 8.3.6 Control Procedure of Application User Account and Production Support Account

If user is new to the LSCP, user is required to register. For certain
role, such as head of stream, user is required to provide their
Registered Professionals or Contractors registration number. And all
public user is required to provide HKID and check versus our database.

For external users, the LSCP implemented One-Time-Password token as
secure login approach so that they can access the LSCP from their
working locations for submission and retrieval of assignment details,
and inspection results.

All information submitted by low level TCP staff will be vetted by Head
of stream staff before saving as finalized records on the system.

To deliver on-going production support or change request, Application
Maintenance Team may require to access the production servers for cause
investigation, system/ application log collection or change request
deployment. The Application Maintenance Team should seek the System
Maintenance Committee’s approval by email. With the proof of
authorization, ITU can help to login the servers, after that the
Application Maintenance Team operates on the servers under the ITU’s
monitoring. In case, the information/ operation can only be accessed/
executed under particular system account, the Application Maintenance
Team should ask system account holder or designated person (Business
Coordination Team member) to logon for his action.

1.  <span id="_heading=h.3mzq4wv" class="anchor"></span>Change Control

During the SI&I stage, program source of the LSCP is maintained by the
Application Maintenance Team with aid of GIT repository with version
control, any updating on the program source is recorded for tracking of
program changes. GIT will be continue using in the change control
solution for the SM&S stage. For detail procedure, please refer to COPM.

1.  Disaster Recovery

**GCIS**

<u>Automatic Failover</u>:

If GCIS Prod 1 goes down, the GCIS Prod 2 disaster recovery (DR)
environment will be automatically activated by the VM Site Recovery
Manager. After a brief delay, users will be directed to the temporary
domain (www2) to continue their usage seamlessly

<u>Virtual Machine Backups:</u>

The virtual machines of GCIS Prod 1 will undergo daily overnight
backups, with each backup retained for 30 days.

<u>Daily Database Backup:</u>

A cron job is scheduled to export the GCIS Prod 1 database backup to the
backup server every day at 22:00.

**BDSCS External (On-Prem):**

<u>Load Balancing with NGINX:</u>

A NGINX Reverse Proxy/Load Balancer (running on ESXi) distributes
traffic across two servers. In case one server becomes unavailable,
traffic will automatically be redirected to the other server.

<u>Scheduled Database Backup:</u>

A cron job runs daily at 18:30 to export the database.

<u>Backup Transfer:</u>

At 19:00, the VM service will send the exported database backup to the
production backup server.

<u>VM Replication to DR Environment:</u>

All production virtual machines will be replicated to the disaster
recovery (DR) environment using the VEEAM architecture, ensuring
continuity in the event of a failure

1.  <span id="_heading=h.haapch" class="anchor"></span>Database Backup
    Strategy

### 8.6.1 SQL Database Backup

Beside DB server VM backup which is mentioned by section 8.2 and section
8.3, database full export backup will be carried out as well. This type
of backup contains full database export database objects including
schemas, table structures, packages, stored procedures and data at 18:45
daily.

The daily full export backup is done on DB servers (uat-db-01,
prd-db-01, prd-db-02, dr-db-01), data stored on the DB servers’
directory: D:\backup\\

### 8.6.2 Recovery

The table below shows the impact, system recovery and the expected
duration before the BDSCS is resumed to normal operation when various
system failures occur.

<table>
<colgroup>
<col style="width: 5%" />
<col style="width: 31%" />
<col style="width: 26%" />
<col style="width: 20%" />
<col style="width: 15%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#</td>
<td>Failure Scenario</td>
<td>Impact</td>
<td>System Recovery</td>
<td>Total down time</td>
</tr>
<tr class="even">
<td>1</td>
<td>System (hardware) failure of the primary database server</td>
<td><p>Production BDSCS services not available;</p>
<p>All BDSCS users cannot use BDSCS</p></td>
<td>Pilot BDSCS needs to be setup using standby DB</td>
<td>~1 hour</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Electricity shortage on primary site</td>
<td><p>Production BDSCS services not available;</p>
<p>All BDSCS users cannot use BDSCS</p></td>
<td>BDSCSneeds to be setup using DR site</td>
<td>~half day</td>
</tr>
<tr class="even">
<td>3</td>
<td>System failure of either one of the App servers on primary site</td>
<td>According to the number of concurrent user, the performance may be
degraded.</td>
<td>No effect on system availability</td>
<td>N/A</td>
</tr>
<tr class="odd">
<td>4</td>
<td>System failure of ALL App servers on primary site</td>
<td><p>Production BDSCS Web services not available;</p>
<p>ALL BDSCS Web users cannot use BDSCS</p></td>
<td>BDSCS needs to be restored using App servers VM image backup</td>
<td>~half day</td>
</tr>
<tr class="even">
<td>5</td>
<td>Database connection failure since SQL database instance down</td>
<td><p>BDSCS services not available;</p>
<p>ALL BDSCS users cannot use BDSCS</p></td>
<td>Restart SQL database instance</td>
<td>~1 hour</td>
</tr>
<tr class="odd">
<td>6</td>
<td>Primary database crushed</td>
<td>No impact as it will failover to the secondary database</td>
<td>BDSCS needs to be setup using secondary DB</td>
<td>~1 hour</td>
</tr>
<tr class="even">
<td>7</td>
<td>System failure (hardware failure) on one of the VM servers</td>
<td>No impact as all VM Server is formed in cluster. If one have failure
hardware failover will proceed automatically.</td>
<td>N/A</td>
<td>N/A</td>
</tr>
</tbody>
</table>

### 8.6.3 Backup Schedule 

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

# 9. Database Administration

1.  <span id="_heading=h.upglbi" class="anchor"></span>Clean Database
    Transaction Logs

To clean up transaction log to reclaim space:

1.  Login to the database server, launch the SQL Server Management
    > Studio (SSMS) software

2.  In SSMS, login the database with account having sysadmin role

3.  On the left pane, find and right click the database “bd_scs”, then
    > select “Properties”

<img src="media/image13.png" style="width:4.63859in;height:5.67074in" />

1.  Under “Options”, change “Recovery model” to “Simple”

<img src="media/image14.png" style="width:6.27585in;height:2.17739in" />

1.  Click “Ok” to apply the change

2.  Right click “bd_scs” again, under “Tasks” → “Shrink”, select “Files”

<img src="media/image15.png" style="width:6.62605in;height:2.09722in" />

1.  Under “File type”, select “Log”

<img src="media/image16.png" style="width:6.62605in;height:2.51389in" />

1.  Under “Shrink action” select “Reorganize pages before releasing
    > unused space”, then press “OK”.

<img src="media/image17.png" style="width:6.62605in;height:3.06944in" />

1.  After shrinking, right click the database “bd_scs”, then select
    > “Properties”, under “Options”, change “Recovery model” back to
    > “Full”

<img src="media/image18.png" style="width:6.62605in;height:2.16667in" />

1.  <span id="_heading=h.3ep43zb" class="anchor"></span>Database Backup

While there is scheduled database full backup daily, additional backup
can be done by following step:

1.  In SSMS, right click database “bd_scs”, select “Tasks” → “Back Up…”

<img src="media/image19.png" style="width:6.62605in;height:2.56944in" />

1.  Under “Destination”, click “Remove” to remove existing backup
    > destination, then click “Add…”.

<img src="media/image20.png" style="width:6.62605in;height:1.90278in" />

1.  Click the three dots button next to “File name” input field, then
    > pick the directory and input the file name of the backup, the file
    > name should end with “.bak”, then press “OK”.

> <img src="media/image21.png" style="width:4.60417in;height:4.03125in" />

1.  The backup destination is selected, now click “OK” to start the
    > backup.

<img src="media/image22.png" style="width:6.62605in;height:3.41667in" />

1.  The backup is completed with the “.bak” file picked in step 3 as the
    > result.

<!-- -->

1.  <span id="bookmark=id.1hmsyys" class="anchor"></span>System
    Constraints and Limitations

-   URL path length limit 250

-   ~, #, %, & , \*, {, }, \\ :, \<, \>, ?, /, \|, “ special character
    is not allowed for files/folder

Reference:
[<u>https://docs.microsoft.com/en-us/sharepoint/install/software-boundaries-and-limits-0</u>](https://docs.microsoft.com/en-us/sharepoint/install/software-boundaries-and-limits-0)

# 10. Log Management

1\. Following activities shall include in the log:

> − Attempts for log-in
>
> − Unauthorised update/access
>
> − Failed attempts for privileges elevation
>
> − Attempts for password changes
>
> − Access attempts to critical files (e.g., software configuration
> files, password and key files, etc.)
>
> − Actions taken by privileged users
>
> − Use of privileged rights such as addition and deletion of user
> accounts
>
> − Security related system failures and alerts
>
> − Changes to user access rights
>
> − Failed access attempts to systems and files identified as critical
> to the system
>
> − Computer services such as file copying or searching
>
> − Modification to audit policy
>
> − Activation and de-activation of protection systems, such as
> anti-malware systems and intrusion detection systems

2\. Logs shall be retained for **180 days** and centralised and managed
by Syslog server. Unauthorised access is restricted.

3\. Logs will be reviewed regularly.

4\. Logs shall not be used to profile the activity of a particular user
unless it relates to a necessary audit activity supported by a
Directorate rank officer.

> \<\<\< End of document \>\>\>
