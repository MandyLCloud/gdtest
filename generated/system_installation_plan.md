![BDlogo](media/image1.jpg)

# SYSTEM INSTALLATION PLAN

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**

**LICENSING SELF-CERTIFICATION PORTAL**

**OF**

**BUILDINGS DEPARTMENT**

**Version: 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

| Distribution |                                     |
|-------------|-------------------------------------|
| Copy No.    | Holder                              |
| 1           | Buildings Department (BD)           |
| 2           | Master Concept (Hong Kong) Limited (MC) |

| Amendment History |                       |                |            |           |           |
|------------------|------------------------|----------------|------------|-----------|-----------|
| Change Number    | Revision Description   | Pages Affected | Revision / | Date      | Approval  |
|                  |                       | on Respective  | Version    |           | Reference |
|                  |                       | Version        | Number     |           |           |
| 1                | 1st draft             | All            | 0.1        | 16/01/225 |           |

# TABLE OF CONTENTS

[1. Introduction](#introduction)

[2. Project Environment Description](#project-environment-description)
- [2.1 Network Diagram](#network-diagram)
- [2.2 Hardware Specification](#hardware-specification)
- [2.3 Software Specification](#software-specification)

[3. Application Deployment Procedure for Production](#application-deployment-procedure-for-production)
- [3.1 Database Server](#database-server)
- [3.2 Backend Servers](#backend-servers)
- [3.3 Frontend Servers](#frontend-servers)
  - [3.3.1 sFTP Server Setup](#sftp-server-setup)

[4. System Installation Schedule and Result](#system-installation-schedule-and-result)
- [4.1 System Installation Schedule](#system-installation-schedule)
- [4.2 System Installation Result](#system-installation-result)

# Introduction

The System Installation plan describes the procedure and schedule for deploying the application in the production environment, including 3 parts of the system:

- Database Server
- Backend Server
- Frontend and Web Portal Server

# Project Environment Description

## Network Diagram

Below is a logical network diagram in 1/F West Kowloon Government Office for production and UAT site.

[DIAGRAM HERE]

The network will be separated into three zones: DMZ, trusted zone, and storage network.

A two-tier firewall setup will be used to form the trusted zone and DMZ. Incoming network traffic to the system must go through the DMZ before entering the trusted zone.

To utilize hardware resources more effectively, servers listed in section [1.3.3], except the backup server, will be set up in the form of virtual machines (VM) and consolidated into DMZ VM host servers and trusted zone VM host servers for each physical site. Two VM host servers will be built in each zone for the purpose of high availability.

Similarly, storage needed by all servers will be consolidated and provided by SAN storage. A dedicated network will be set up and interconnected with the VM host servers. The backup server will also exist in this storage-dedicated network to carry out backup tasks of VM host servers in DMZ and trusted zone.

The diagram below illustrates the physical setup.

## Hardware Specification

Production and UAT environment:

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---------------------------|---------------------------|---------|-----|
| prd-scs-admin-server-01 | prd-scs-vcenter-01 | vCenter Server | 192.168.10.24/10.5.161.210 |


DR environment:

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---------------------------|---------------------------|---------|-----|
| dr-scs-admin-server-01 | dr-scs-vcenter-01 | vCenter Server | 192.168.20.18/10.5.174.225 |


**Detailed Hardware Configurations (Production)**

|                            |                         |                             |                |                        |
|---------------|-------------|--------------|------------|------------------|
| **Model**                  | **Host Name**           | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750 Server | prd-scs-admin-server-01 | 192.168.10.22, 10.5.161.206 | F646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-admin-server-02 | 192.168.10.23, 10.5.161.207 | D646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-nas             | 192.168.10.35, 10.5.161.218 | ???            | ???                    |

**SAN Storage (Production)**

|             |                      |                |                       |                                                            |
|----------------|---------------|--------------|--------------|---------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CC    | N/A                   | 192.168.10.16                                              |
| SAN Switch  | Dell DS6610B         | FRC1924T0CD    | N/A                   | 192.168.10.17                                              |
| SAN Storage | Dell PowerStore 500T | HV1NBX3        | 11                    | 192.168.10.26, 192.168.10.27, 192.168.10.28, 192.168.10.29 |

**Backup Storage (Production)**

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|----------------|---------------|--------------|--------------|---------------|
| Backup Appliance | Dell DataDomain 3300 | 17XMBX3        | 15TB            | 192.168.10.20  |

**Tape Library (Production)**

| **Type**     | **Model** | **Serial No.** | **No. of slots** | **IP Address** |
|--------------|-----------|----------------|------------------|----------------|
| Tape Library | Dell ML3  | 3555L3A7801YY0 | 35               | 192.168.10.20  |

**Firewalls (Production)**

|               |                 |                 |                  |                |
|--------------|-------------|-------------|---------------|-----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSPri | 192.168.10.12   | 10.5.161.205    | Palo Alto PA-850 | 11901063047    |
| PA-850-SCSSec | 192.168.10.13   | 10.5.161.220    | Palo Alto PA-850 | 11901063049    |

**Switches (Production)**

| **Host Name** | **Internal IP** | **Model** | **Serial No.** |
|---------------|-----------------|-----------|----------------|
|               | 192.168.10.14   | Catalyst  |                |
|               | 192.168.10.15   | Catalyst  |                |

**UPS (Production)**

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010008 | 192.168.11.20  |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010004 | 192.168.11.21  |

**Hardware Components of Production Servers**

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

**Partition Configuration of Production Servers**

| **Host Name**           | **Drive**       | **Capacity** | **Description**              |
|--------------------|-----------------|----------|--------------------------|
| prd-scs-admin-server-01 | local           | 2.4TB        | VMware?ESXi Operating system |
| prd-scs-admin-server-02 | local           | 2.4TB        | VMware?ESXi Operating system |
| PS500T-Cluster1         | VM_Volume01     | 20TB         | Shared pool of storage space |
| PS500T-Cluster1         | QuorumDisk-VM-1 | 2.5GB        | Shared pool of storage space |
| prd-scs-nas             | C:              | ???          | OS                           |
|                         | D:              | ???          | Data                         |

**DR Site Hardware Configurations**

|                           |                        |                             |                |                        |
|---------------|-------------|----------------|---------------|--------------|
| **Model**                 | **Host Name**          | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750Server | dr-scs-admin-server-01 | 192.168.20.17, 10.5.174.216 | G646RX3        | RAID-5                 |
| Dell PowerEdge R750Server | dr-scs-nas             | 192.168.20.35, 10.5.174.225 | ???            | ???                    |

**SAN Storage (DR Site)**

|             |                      |                |                       |                                                            |
|----------------|---------------|--------------|--------------|---------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CE    | N/A                   | 192.168.20.14                                              |
| SAN Storage | Dell PowerStore 500T | 3W1NBX3        | 11                    | 192.168.20.20, 192.168.20.21, 192.168.20.22, 192.168.20.23 |

**Backup Storage (DR Site)**

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|----------------|---------------|--------------|--------------|---------------|
| Backup Appliance | Dell DataDomain 3300 | J6XMBX3        | 15TB            | 192.168.20.25  |

**Firewalls (DR Site)**

|               |                 |                 |                  |                |
|---------------|-------------|-------------|----------------|-----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSDR  | 192.168.20.12   | 10.5.174.215    | Palo Alto PA-850 | 011901063069   |

**Switches (DR Site)**

|               |                 |              |                |
|---------------|-----------------|--------------|----------------|
| **Host Name** | **Internal IP** | **Model**    | **Serial No.** |
| ???           | 192.168.20.13   | Catalyst ??? | ???            |

**UPS (DR Site)**

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A01000A | 192.168.20.11  |

**Hardware Components of Disaster Recovery Servers**

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

**Partition Configuration of DR Servers**

|                        |             |              |                              |
|--------------------|-----------------|----------|--------------------------|
| **Host Name**          | **Drive**   | **Capacity** | **Description**              |
| dr-scs-admin-server-01 | local       | 2.4TB        | VMware?ESXi Operating system |
| PS500T-Cluster2        | VM Volume01 | 20TB         | Shared pool of storage space |
| dr-scs-nas             | C:          | ???          | OS                           |
|                        | D:          | ???          | Data                         |

## Software Specification

| Machine | Hostname | Software Requirement |
|---------|----------|---------------------|
| vCenter Server | prd-scs-vcenter-01 | vCenter 8.0.3 Build 24322831 |


Development Frameworks:

| Framework | Version |
|-----------|---------|
| React (frontend) | 18.2.0 |

**Guest Servers (Production)**

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

**Guest Servers (UAT)**

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
<td>uat-