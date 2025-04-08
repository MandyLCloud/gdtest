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

> [1.1 System Summary](#system-summary)
>
> [1.2 System Architecture](#system-architecture)
>
> [1.3 Equipment Configuration](#equipment-configuration)
>
> [1.4 Guest Servers Components](#guest-servers-components)
>
> [1.5 Gateway and SMTPX Configuration](#gateway-and-smtpx-configuration)
>
> [1.6 Detailed Server and Network Configurations](#detailed-server-and-network-configurations)

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
> [6.3 Database Backup Strategy](#database-backup-strategy)
> [6.4 Recovery](#recovery)
> [6.5 Backup Schedule](#backup-schedule)

[7. Outstanding Items/Issues](#outstanding-itemsissues)

[8. Licensed Software](#licensed-software)

[9. Database Administration](#database-administration)
    > [9.1 Clean Database Transaction Logs](#clean-database-transaction-logs)
    > [9.2 Database Backup Procedure](#database-backup-procedure)
    > [9.3 System Constraints and Limitations](#system-constraints-and-limitations)

[10. Log Management](#log-management)

# 1. Environment Description

## 1.1 System Summary

The Licensing Self-Certification Portal (LSCP) is designed to provide an electronic platform for Buildings Department (BD) officers and public users involved in site inspection and site monitoring. The system aims to streamline the process of providing, managing, and reviewing inspection and monitoring records.

## 1.2 System Architecture

The LSCP system is hosted across two datacenters: On-premise (WKGO) and Government Cloud Infrastructure Services (GCIS).

**WKGO (On-Premise) Environment:**

The on-premise system is located behind an internal firewall and is segmented into three subnets: Production, UAT, and DEV, primarily for internal users. A reverse proxy server with load balancing enhances security and distributes incoming requests to the frontend web servers.

**GCIS (Government Cloud Infrastructure Services) Environment:**

The GCIS environment is divided into three subnets: Internet DMZ (iDMZ), Trusted Zone, and Gnet DMZ (gDMZ). Both iDMZ and gDMZ include a reverse proxy server and a Web Application Firewall (WAF) in front of the iDMZ for enhanced security.

**User Access Flow:**

*   **External Users (Public):** Access the system via the internet through the LSCP Web Application, which communicates with the Application Server via a reverse proxy. The Application Server hosts static web interface files.  System logic is handled by External Application Servers which forward requests to Web Servers in the Trusted Zone. These web servers, built with reactjs and nodeJS, interact with Database Servers (Microsoft SQL Servers) and an in-built file storage to process data and return results.
*   **Internal Users (BD Officers):** Access the internal BDSCS application from the BD intranet, connecting to BD Web Servers in the Trusted Zone through the Departmental Portal (OSDP). These BD Web Servers perform similar functions to the External Web Servers and handle user authentication via the Departmental Portal.

**Supporting Servers in Trusted Zone:**

*   **Log Server:** Stores system and application logs from various servers.
*   **File Server:** Stores temporary and permanent files.
*   **Database Server:** Hosts Microsoft SQL Server for system and user data.
*   **vCenter Server:** Manages VM Hypervisors on physical servers.
*   **Backup Server:** Manages database snapshots.

**System Architecture Diagrams:**

**Production Environment:**

<img src="media/image2.png" style="width:6.62605in;height:5.91667in" />

**Production and UAT Site Architecture:**

<img src="media/image3.png" style="width:6.62605in;height:5.81944in" />

**Disaster Recovery Environment:**

<img src="media/image5.png" style="width:6.62605in;height:6.44444in" />

**Web Browser Support:**

<img src="media/image4.png" style="width:6.62605in;height:2.375in" />

## 1.3 Equipment Configuration

### Hardware Components

**Configuration of Physical Servers in Production (WKGO)**

|                            |                         |                             |                |                        |
|----------------------------|-------------------------|-----------------------------|----------------|------------------------|
| **Model**                  | **Host Name**           | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750 Server | prd-scs-admin-server-01 | 192.168.10.22, 10.5.161.206 | F646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-admin-server-02 | 192.168.10.23, 10.5.161.207 | D646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-nas             | 192.168.10.35, 10.5.161.218 | ???            | ???                    |

**Configuration of SAN Storage in Production (WKGO)**

|             |                      |                |                       |                                                            |
|-----------------|----------------------|----------------|-----------------------|----------------------------------------------------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CC    | N/A                   | 192.168.10.16                                              |
| SAN Switch  | Dell DS6610B         | FRC1924T0CD    | N/A                   | 192.168.10.17                                              |
| SAN Storage | Dell PowerStore 500T | HV1NBX3        | 11                    | 192.168.10.26, 192.168.10.27, 192.168.10.28, 192.168.10.29 |

**Configuration of Backup Storage in Production (WKGO)**

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|-----------------|----------------------|----------------|-----------------|----------------|
| Backup Appliance | Dell DataDomain 3300 | 17XMBX3        | 15TB            | 192.168.10.20  |

**Configuration of Tape Library in Production (WKGO)**

| **Type**     | **Model** | **Serial No.** | **No. of slots** | **IP Address** |
|--------------|-----------|----------------|------------------|----------------|
| Tape Library | Dell ML3  | 3555L3A7801YY0 | 35               | 192.168.10.20  |

**Configuration of Firewalls in Production (WKGO)**

|               |                 |                 |                  |                |
|---------------|-----------------|-----------------|------------------|-----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSPri | 192.168.10.12   | 10.5.161.205    | Palo Alto PA-850 | 11901063047    |
| PA-850-SCSSec | 192.168.10.13   | 10.5.161.220    | Palo Alto PA-850 | 11901063049    |

**Configuration of Switches in Production (WKGO)**

| **Host Name** | **Internal IP** | **Model** | **Serial No.** |
|---------------|-----------------|-----------|----------------|
|               | 192.168.10.14   | Catalyst  |                |
|               | 192.168.10.15   | Catalyst  |                |

**Configuration of KVM in Production (WKGO)**

|            |                |
|------------|----------------|
| **Model**  | **Serial No.** |
| Cyber View |                |

**Configuration of UPS in Production (WKGO)**

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010008 | 192.168.11.20  |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010004 | 192.168.11.21  |

**Hardware Components of Production Servers (WKGO)**

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
<td>Vertiv? Liebert? GXT5 3000</td>
<td>1</td>
</tr>
<tr class="odd">
<td>14</td>
<td>UPS<br />
(???)</td>
<td>Vertiv? Liebert? GXT5 3000</td>
<td>1</td>
</tr>
</tbody>
</table>

**Partition Configuration of Production Servers (WKGO)**

| **Host Name**           | **Drive**       | **Capacity** | **Description**              |
|-------------------------|-----------------|--------------|------------------------------|
| prd-scs-admin-server-01 | local           | 2.4TB        | VMware?ESXi Operating system |
| prd-scs-admin-server-02 | local           | 2.4TB        | VMware?ESXi Operating system |
| PS500T-Cluster1         | VM_Volume01     | 20TB         | Shared pool of storage space |
| PS500T-Cluster1         | QuorumDisk-VM-1 | 2.5GB        | Shared pool of storage space |
| prd-scs-nas             | C:              | ???          | OS                           |
|                         | D:              | ???          | Data                         |

**Configuration of Physical Servers in DR Site (AIA)**

|                           |                        |                             |                |                        |
|---------------------------|------------------------|-----------------------------|----------------|------------------------|
| **Model**                 | **Host Name**          | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750Server | dr-scs-admin-server-01 | 192.168.20.17, 10.5.174.216 | G646RX3        | RAID-5                 |
| Dell PowerEdge R750Server | dr-scs-nas             | 192.168.20.35, 10.5.174.225 | ???            | ???                    |

**Configuration of SAN Storage in DR Site (AIA)**

|             |                      |                |                       |                                                            |
|-----------------|----------------------|----------------|-----------------------|----------------------------------------------------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CE    | N/A                   | 192.168.20.14                                              |
| SAN Storage | Dell PowerStore 500T | 3W1NBX3        | 11                    | 192.168.20.20, 192.168.20.21, 192.168.20.22, 192.168.20.23 |

**Configuration of Backup Storage in DR Site (AIA)**

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|-----------------|----------------------|----------------|-----------------|----------------|
| Backup Appliance | Dell DataDomain 3300 | J6XMBX3        | 15TB            | 192.168.20.25  |

**Configuration of Firewalls in DR Site (AIA)**

|               |                 |                 |                  |                |
|---------------|-----------------|-----------------|------------------|-----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSDR  | 192.168.20.12   | 10.5.174.215    | Palo Alto PA-850 | 011901063069   |

**Configuration of Switches in DR Site (AIA)**

|               |                 |              |                |
|---------------|-----------------|--------------|----------------|
| **Host Name** | **Internal IP** | **Model**    | **Serial No.** |
| ???           | 192.168.20.13   | Catalyst ??? | ???            |

**Configuration of UPS in DR Site (AIA)**

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A01000A | 192.168.20.11  |

**Hardware Components of Disaster Recovery Servers (AIA)**

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
<th>Vertiv? Liebert? GXT5 3000</th>
<th>1</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

**Partition Configuration of DR Servers (AIA)**

|                        |             |              |                              |
|------------------------|-------------|--------------|------------------------------|
| **Host Name**          | **Drive**   | **Capacity** | **Description**              |
| dr-scs-admin-server-01 | local       | 2.4TB        | VMware?ESXi Operating system |
| PS500T-Cluster2        | VM Volume01 | 20TB         | Shared pool of storage space |
| dr-scs-nas             | C:          | ???          | OS                           |
|                        | D:          | ???          | Data                         |

## 1.4 Guest Servers Components

**Production Guest Servers (WKGO)**

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

**UAT Guest Servers (WKGO)**

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
<td>4