```markdown
<img src="media/image1.jpg" style="width:2.03125in;height:1.52083in"
alt="BDlogo" />

**SYSTEM INSTALLATION PLAN**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**OF**

**BUILDINGS DEPARTMENT**

**Version: 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR.

| **Distribution** |                                         |
|------------------|-----------------------------------------|
| Copy No.         | Holder                                  |
| 1                | Buildings Department (BD)               |
| 2                | Master Concept (Hong Kong) Limited (MC) |

| **Amendment History** |                      |                                      |                           |           |                    |
|----------|--------------------|--------------|---------|---------|-----------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date      | Approval Reference |
| 1                     | 1st draft            | All                                  | 0.1                       | 16/01/225 |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |

**TABLE OF CONTENTS**

[1. Introduction 5](#introduction)
[2. Project Environment Description 6](#project-environment-description)
    [2.1 Network Diagram 6](#network-diagram)
    [2.2 Hardware Specification 6](#hardware-specification)
    [2.3 Software Specification 8](#software-specification)
[3. Application Deployment Procedure for Production 10](#application-deployment-procedure-for-production)
    [3.1 Database Server 10](#database-server)
    [3.2 Backend Servers 10](#backend-servers)
    [3.3 Frontend Servers 10](#frontend-servers)
        [3.3.1 sFTP Server Setup 10](#sftp-server-setup)
[4. System Installation Schedule and Result 11](#system-installation-schedule-and-result)
    [4.1 System Installation Schedule 11](#system-installation-schedule)
    [4.2 System Installation Result 12](#system-installation-result)

# Introduction

The System Installation plan describes the procedure and schedule for
deploying the application in the production environment, including 3
parts of the system:

-   Database Server
-   Backend Server
-   Frontend and Web Portal Server

This document outlines the plan for installing the Licensing Self-Certification Portal (LSCP) system, developed under the Combined System Development Services project for the Buildings Department. It provides details on the project environment, hardware and software specifications, deployment procedures, and installation schedule. This document is intended for technical staff involved in the system deployment and maintenance.

# Project Environment Description

## Network Diagram

Below is a logical network diagram in 1/F West Kowloon Government Office
for production and UAT site.

<span class="mark">\[DIAGRAM HERE\]</span>

The network will be separated into three zones: DMZ, trusted zone, and
storage network.

A two-tier firewall setup will be used to form the trusted zone and DMZ.
Incoming network traffic to the system must go through the DMZ before
entering the trusted zone.

To utilize hardware resources more effectively, servers listed in
section 1.3.3, except the backup server, will
be set up in the form of virtual machines (VM) and consolidated into DMZ
VM host servers and trusted zone VM host servers for each physical site.
Two VM host servers will be built in each zone for the purpose of high
availability.

Similarly, storage needed by all servers will be consolidated and
provided by SAN storage. A dedicated network will be set up and
interconnected with the VM host servers. The backup server will also
exist in this storage-dedicated network to carry out backup tasks of VM
host servers in DMZ and trusted zone.

The diagram below illustrates the physical setup.

## Hardware Specification

Production and UAT environment:

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose                                  | IP             |
|-----------------------------|----------------------------|------------------------------------------|----------------|
|                             |                            |                                          |                |
|                             |                            |                                          |                |
|                             |                            |                                          |                |
|                             |                            |                                          |                |
|                             |                            |                                          |                |
|                             |                            |                                          |                |
|                             |                            |                                          |                |
|                             |                            |                                          |                |
|                             |                            |                                          |                |

DR environment:

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|-----------------------------|----------------------------|---------|----|
|                             |                            |         |    |
|                             |                            |         |    |
|                             |                            |         |    |
|                             |                            |         |    |
|                             |                            |         |    |

### Detailed Hardware Components

#### Production Environment - WKGO

**Physical Servers:**

|                            |                         |                             |                |                        |
|----------------------------|-------------------------|-----------------------------|----------------|------------------------|
| **Model**                  | **Host Name**           | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750 Server | prd-scs-admin-server-01 | 192.168.10.22, 10.5.161.206 | F646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-admin-server-02 | 192.168.10.23, 10.5.161.207 | D646RX3        | RAID-5                 |
| Dell PowerEdge R750 Server | prd-scs-nas             | 192.168.10.35, 10.5.161.218 | ???            | ???                    |

**SAN Storage:**

|             |                      |                |                       |                                                            |
|-------------|----------------------|----------------|-----------------------|------------------------------------------------------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CC    | N/A                   | 192.168.10.16                                              |
| SAN Switch  | Dell DS6610B         | FRC1924T0CD    | N/A                   | 192.168.10.17                                              |
| SAN Storage | Dell PowerStore 500T | HV1NBX3        | 11                    | 192.168.10.26, 192.168.10.27, 192.168.10.28, 192.168.10.29 |

**Backup Storage:**

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|------------------|----------------------|----------------|-----------------|----------------|
| Backup Appliance | Dell DataDomain 3300 | 17XMBX3        | 15TB            | 192.168.10.20  |

**Tape Library:**

| **Type**     | **Model** | **Serial No.** | **No. of slots** | **IP Address** |
|--------------|-----------|----------------|------------------|----------------|
| Tape Library | Dell ML3  | 3555L3A7801YY0 | 35               | 192.168.10.20  |

**Firewalls:**

|               |                 |                 |                  |                |
|---------------|-----------------|-----------------|------------------|----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSPri | 192.168.10.12   | 10.5.161.205    | Palo Alto PA-850 | 11901063047    |
| PA-850-SCSSec | 192.168.10.13   | 10.5.161.220    | Palo Alto PA-850 | 11901063049    |

**Switches:**

| **Host Name** | **Internal IP** | **Model** | **Serial No.** |
|---------------|-----------------|-----------|----------------|
|               | 192.168.10.14   | Catalyst  |                |
|               | 192.168.10.15   | Catalyst  |                |

**KVM:**

|            |                |
|------------|----------------|
| **Model**  | **Serial No.** |
| Cyber View |                |

**UPS:**

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010008 | 192.168.11.20  |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010004 | 192.168.11.21  |

**Hardware Components of Production Servers:**

| **Item** | **Hardware Component**                                 | **Configuration**                               | **Qty** |
|----------|--------------------------------------------------------|-----------------------------------------------|---------|
| 1        | ESXi Hypervisor Server (prd-scs-admin-server-01)       | Dell PowerEdge R750                           | 1       |
|          |                                                        | Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz      | 1       |
|          |                                                        | 32GB DDR4 Synchronous Registered (Buffered)   | 8       |
|          |                                                        | 1.2TB SAS HDD                                   | 3       |
|          |                                                        | ESXi 8.0.3                                      | 1       |
| 2        | ESXi Hypervisor Server (prd-scs-admin-server-02)       | Dell PowerEdge R750                           | 1       |
|          |                                                        | Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz      | 1       |
|          |                                                        | 32GB DDR4 Synchronous Registered (Buffered)   | 8       |
|          |                                                        | 1.2TB SAS HDD                                   | 3       |
|          |                                                        | ESXi 8.0.3                                      | 1       |
| 3        | NAS (prd-scs-nas)                                      | Dell PowerEdge R750                           | 1       |
|          |                                                        | CPU???                                          | ???     |
|          |                                                        | RAM???                                          | ???     |
|          |                                                        | HDD???                                          | ???     |
|          |                                                        | Windows Server 2022                             | ???     |
| 4        | SAN Switch (prd-scs-sw-01)                              | Dell DS6610B                                    | 1       |
|          |                                                        | Ports                                           | 16      |
| 5        | SAN Switch (prd-scs-sw-02)                              | Dell DS6610B                                    | 1       |
|          |                                                        | Ports                                           | 16      |
| 6        | SAN Storage (PS500T-Cluster1)                           | Dell PS500T                                     | 1       |
|          |                                                        | 3.8TB NVME SSD                                  | 11      |
| 7        | Backup Appliance (prd-scs-backupstorage-01)           | Dell DataDomain DD3300                          | 1       |
| 8        | Tape Library                                           | DELL ML3                                        | 1       |
| 9        | Firewall (PA-850-SCSPri)                               | Palo Alto PA 850                                | 1       |
| 10       | Firewall (PA-850-SCSSec)                               | Palo Alto PA 850                                | 1       |
| 11       | Switch (???)                                            | Cisco ???                                       | 1       |
| 12       | Switch (???)                                            | Cisco ???                                       | 1       |
| 13       | KVM                                                    | CyberView                                       | 1       |
| 13       | UPS (???)                                              | Vertiv? Liebert? GXT5 3000                      | 1       |
| 14       | UPS (???)                                              | Vertiv? Liebert? GXT5 3000                      | 1       |

**Partition Configuration of Production Servers:**

| **Host Name**           | **Drive**       | **Capacity** | **Description**              |
|-------------------------|-----------------|--------------|--------------------------|
| prd-scs-admin-server-01 | local           | 2.4TB        | VMware?ESXi Operating system |
| prd-scs-admin-server-02 | local           | 2.4TB        | VMware?ESXi Operating system |
| PS500T-Cluster1         | VM_Volume01     | 20TB         | Shared pool of storage space |
| PS500T-Cluster1         | QuorumDisk-VM-1 | 2.5GB        | Shared pool of storage space |
| prd-scs-nas             | C:              | ???          | OS                           |
|                         | D:              | ???          | Data                         |

#### Disaster Recovery Site - AIA

**Physical Servers:**

|                           |                        |                             |                |                        |
|---------------------------|------------------------|-----------------------------|----------------|------------------------|
| **Model**                 | **Host Name**          | **IP**                      | **Serial No.** | **Disk Configuration** |
| Dell PowerEdge R750Server | dr-scs-admin-server-01 | 192.168.20.17, 10.5.174.216 | G646RX3        | RAID-5                 |
| Dell PowerEdge R750Server | dr-scs-nas             | 192.168.20.35, 10.5.174.225 | ???            | ???                    |

**SAN Storage:**

|             |                      |                |                       |                                                            |
|-------------|----------------------|----------------|-----------------------|------------------------------------------------------------|
| **Type**    | **Model**            | **Serial No.** | **No. of hard disks** | **IP Address**                                             |
| SAN Switch  | Dell DS6610B         | FRC1924T0CE    | N/A                   | 192.168.20.14                                              |
| SAN Storage | Dell PowerStore 500T | 3W1NBX3        | 11                    | 192.168.20.20, 192.168.20.21, 192.168.20.22, 192.168.20.23 |

**Backup Storage:**

| **Type**         | **Model**            | **Serial No.** | **Volume Size** | **IP Address** |
|------------------|----------------------|----------------|-----------------|----------------|
| Backup Appliance | Dell DataDomain 3300 | J6XMBX3        | 15TB            | 192.168.20.25  |

**Firewalls:**

|               |                 |                 |                  |                |
|---------------|-----------------|-----------------|------------------|----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSDR  | 192.168.20.12   | 10.5.174.215    | Palo Alto PA-850 | 011901063069   |

**Switches:**

|               |                 |              |                |
|---------------|-----------------|--------------|----------------|
| **Host Name** | **Internal IP** | **Model**    | **Serial No.** |
| ???           | 192.168.20.13   | Catalyst ??? | ???            |

**UPS:**

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A01000A | 192.168.20.11  |

**Hardware Components of Disaster Recovery Servers:**

| **Item** | **Hardware Component**                                 | **Configuration**                               | **Qty** |
|----------|--------------------------------------------------------|-----------------------------------------------|---------|
| 1        | ESXi Hypervisor Server (dr-scs-admin-server-01)        | Dell PowerEdge R750                           | 1       |
|          |                                                        | Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz      | 1       |
|          |                                                        | 32GB DDR4 Synchronous Registered (Buffered)   | 8       |
|          |                                                        | 1.2TB SAS HDD                                   | 3       |
|          |                                                        | ESXi 8.0.3                                      | 1       |
| 2        | NAS (dr-scs-nas)                                       | Dell PowerEdge R750                           | 1       |
|          |                                                        | CPU???                                          | ???     |
|          |                                                        | RAM???                                          | ???     |
|          |                                                        | HDD???                                          | ???     |
|          |                                                        | Windows Server 2022                             | ???     |
| 3        | SAN Switch (dr-scs-sw-01)                               | Dell DS6610B                                    | 1       |
|          |                                                        | Ports                                           | 16      |
| 4        | SAN Storage (PS500T-Cluster2)                           | Dell PS500T                                     | 1       |
|          |                                                        | 3.8TB NVME SSD                                  | 11      |
| 5        | Backup Appliance (dr-scs-backupstorage-01)            | Dell DataDomain DD3300                          | 1       |
| 6        | Firewall (PA-850-SCSPri)                               | Palo Alto PA 850                                | 1       |
| 7        | Switch (???)                                            | Cisco ???                                       | 1       |
| 8        | KVM                                                    | CyberView                                       | 1       |
| 9        | UPS (???)                                              | Vertiv? Liebert? GXT5 3000                      | 1       |

**Partition Configuration of DR Servers:**

|                        |             |              |                              |
|------------------------|-------------|--------------|------------------------------|
| **Host Name**          | **Drive**   | **Capacity** | **Description**              |
| dr-scs-admin-server-01 | local       | 2.4TB        | VMware?ESXi Operating system |
| PS500T-Cluster2        | VM Volume01 | 20TB         | Shared pool of storage space |
| dr-scs-nas             | C:          | ???          | OS                           |
|                        | D:          | ???          | Data                         |

### Guest Servers Components

#### Production Guest Servers - WKGO & GCIS P1

| **Role**             | **Host Name**       | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses**                 | **Data Center** | **Host Server / Zone** |
|----------------------|---------------------|----------|--------------|---------------|------------------------------------|-----------------|------------------------|
| vCenter              | prd-scs-vcenter-01  | 16       | 39           | 1.33TB        | 192.168.10.24 / 10.5.161.210       | WKGO            | prd-scs-admin-server-01  |
| Veeam Backup Server  | prd-scs-backup-01   | 8        | 24           | 300 + 1TB     | 192.168.10.25 / 10.5.161.211       | WKGO            | prd-scs-admin-server-02  |
| Kiwi Log Server      | prd-scs-log-01      | 4        | 16           | 300 + 500     | 192.168.10.11 / 10.5.161.223       | WKGO            | prd-scs-admin-server-01  |
| NOD32 Anti-Virus Server| prd-scs-esetnod32   | 4        | 16           | 300           | 192.168.10.34 / 10.5.161.215       | WKGO            | prd-scs-admin-server-02  |
| API Server           | prd-scs-admin-api-01| 2        | 4            | 100           | 192.168.12.11                      | WKGO            | prd-scs-admin-server-01  |
| Frontend Server      | prd-scs-admin-frontend-01| 2    | 4            | 100           | 192.168.12.12                      | WKGO            | prd-scs-admin-server-01  |
| Backend Server       | prd-scs-admin-backend-01| 2     | 4            | 100           | 192.168.12.13                      | WKGO            | prd-scs-admin-server-01  |
| Database Server      | prd-scs-db-01       | 8        | 16           | 100 + 500     | 192.168.12.14                      | WKGO            | prd-scs-admin-server-01  |
| File Server          | prd-scs-filer       | 2        | 4            | 100 + 1TB     | 192.168.12.20                      | WKGO            | prd-scs-admin-server-01  |
| Reverse Proxy Server | prd-scs-proxy       | 2        | 4            | 100           | 192.168.12.15 / 10.5.161.226       | WKGO            | prd-scs-admin-server-01  |
| API Server           | prd-scs-admin-api-02| 2        | 4            | 100           | 192.168.12.16                      | WKGO            | prd-scs-admin-server-02  |
| Frontend Server      | prd-scs-admin-frontend-02| 2    | 4            | 100           | 192.168.12.17                      | WKGO            | prd-scs-admin-server-02  |
| Backend Server       | prd-scs-admin-backend-02| 2     | 4            | 100           | 192.168.12.18                      | WKGO            | prd-scs-admin-server-02  |
| Database Server      | prd-scs-db-02       | 8        | 16           | 100 + 500     | 192.168.12.19                      | WKGO            | prd-scs-admin-server-02  |
| Reverse Proxy Server | scspwi              | 2        | 8            | 100           | 192.168.0.6 / 45.119.92.84         | GCIS P1         | iDMZ                     |
| Reverse Proxy Server | scspwg              | 2        | 8            | 100           | 192.168.4.6 / 10.160.11.211        | GCIS P1         | gDMZ                     |
| Apps Server          | scspad              | 4        | 16           | 100 + 500     | 192.168.8.6                        | GCIS P1         | Trust Zone               |
| Database Server      | scspdb              | 4        | 16           | 100 + 200     | 192.168.8.7                        | GCIS P1         | Trust Zone               |
| Veeam Backup Server  | scspbk2             | 4        | 16           | 100 + 1TB     | 192.168.8.9                        | GCIS P1         | Trust Zone               |
| Kiwi Log Server      | scsplog             | 2        | 8            | 100 + 100     | 192.168.8.10                       | GCIS P1         | Trust Zone               |

#### UAT Guest Servers - WKGO & GCIS T1

| **Role**             | **Host Name**       | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses**                 | **Data Center** | **Host Server / Zone** |
|----------------------|---------------------|----------|--------------|---------------|------------------------------------|-----------------|------------------------|
| API Server           | uat-scs-admin-api-01| 2        | 4            | 100           | 192.168.13.10                      | WKGO            | prd-scs-admin-server-01  |
| Frontend Server      | uat-scs-admin-frontend-01| 2    | 4            | 100           | 192.168.13.11                      | WKGO            | prd-scs-admin-server-01  |
| Backend Server       | uat-scs-admin-backend-01| 2     | 4            | 100           | 192.168.13.12                      | WKGO            | prd-scs-admin-server-01  |
| Database Server      | uat-scs-db-01       | 2        | 4            | 100           | 192.168.13.13                      | WKGO            | prd-scs-admin-server-01  |
| File Server          | uat-scs-filer       | 2        | 4            | 100 + 200     | 192.168.13.15                      | WKGO            | prd-scs-admin-server-01  |
| Reverse Proxy Server | uat-scs-proxy       | 2        | 4            | 100           | 192.168.13.14 / 10.5.161.224       | WKGO            | prd-scs-admin-server-01  |
| Reverse Proxy Server | scsuwi              | 2        | 8            | 100           | 192.168.0.7 / 45.119.94.99         | GCIS T1         | iDMZ                     |
| Reverse Proxy Server | scsuwg              | 2        | 8            | 100           | 192.168.4.7 / 10.148.11.220        | GCIS T1         | gDMZ                     |
| Apps Server          | scsuad              | 4        | 16           | 100 + 200     | 192.168.8.9                        | GCIS T1         | Trust Zone               |
| Database Server      | scsudb              | 4        | 16           | 100 + 100     | 192.168.8.10                       | GCIS T1         | Trust Zone               |

#### DEV Guest Servers - WKGO & GCIS T1

| **Role**             | **Host Name**       | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses**                 | **Data Center** | **Host Server / Zone** |
|----------------------|---------------------|----------|--------------|---------------|------------------------------------|-----------------|------------------------|
| API Server           | dev-scs-admin-api-01| 2        | 4            | 100           | 192.168.14.10                      | WKGO            | prd-scs-admin-server-02  |
| Frontend Server      | dev-scs-admin-frontend-01| 2    | 4            | 100           | 192.168.14.11                      | WKGO            | prd-scs-admin-server-02  |
| Backend Server       | dev-scs-admin-backend-01| 2     | 4            | 100           | 192.168.14.12                      | WKGO            | prd-scs-admin-server-02  |
| Database Server      | dev-scs-db-01       | 2        | 4            | 100           | 192.168.14.13                      | WKGO            | prd-scs-admin-server-02  |
| File Server          | dev-scs-filer       | 2        | 4            | 100 + 200     | 192.168.14.15                      | WKGO            | prd-scs-admin-server-02  |
| Reverse Proxy Server | dev-scs-proxy       | 2        | 4            | 100           | 192.168.14.14 / 10.5.161.225       | WKGO            | prd-scs-admin-server-02  |
| Reverse Proxy Server | scsdwi              | 2        | 8            | 100           | 192.168.0.6 / 45.119.94.100        | GCIS T1         | iDMZ                     |
| Reverse Proxy Server | scsdwg              | 2        | 8            | 100           | 192.168.4.6 / 10.148.11.220        | GCIS T1         | gDMZ                     |
| Apps Server          | scsdad              | 4        | 16           | 100 + 200     | 192.168.8.7                        | GCIS T1         | Trust Zone               |
| Database Server      | scsddb              | 4        | 16           | 100 + 100     | 192.168.8.8                        | GCIS T1         | Trust Zone               |

#### Disaster Recovery Guest Servers - AIA & GCIS P2

| **Role**             | **Host Name**       | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses**                 | **Data Center** | **Host Server / Zone** |
|----------------------|---------------------|----------|--------------|---------------|------------------------------------|-----------------|------------------------|
| vCenter              | dr-scs-vcenter-01   | 16       | 39           | 1.33TB        | 192.168.20.18 / 10.5.174.225       | AIA             | dr-scs-admin-server-01   |
| Veeam Backup Server  | dr-scs-backup-01    | 8        | 24           | 300 + 1TB     | 192.168.20.19 / 10.5.161.224       | AIA             | dr-scs-admin-server-01   |
| Kiwi Log Server      | dr-scs-log-01       | 4        | 8            | 300 + 500     | 192.168.20.10                      | AIA             | dr-scs-admin-server-01   |
| API Server           | dr-scs-admin-api-01 | 2        | 8            | 90            | 192.168.22.11                      | AIA             | dr-scs-admin-server-01   |
| Frontend Server      | dr-scs-admin-frontend-01| 2    | 8            | 90            | 192.168.22.12                      | AIA             | dr-scs-admin-server-01   |
| Backend Server       | dr-scs-admin-backend-01| 2     | 8            | 90            | 192.168.22.13                      | AIA             | dr-scs-admin-server-01   |
| Database Server      | dr-scs-db-01        | 2        | 8            | 90 + 500      | 192.168.22.14                      | AIA             | dr-scs-admin-server-01   |
| File Server          | dr-scs-filer        | 2        | 8            | 90 + 1TB      | 192.168.22.16                      | AIA             | dr-scs-admin-server-01   |
| Reverse Proxy Server | dr-scs-proxy        | 2        | 4            | 90            | 192.168.22.15 / 10.5.174.228       | AIA             | dr-scs-admin-server-01   |
| Reverse Proxy Server | scspwi              | 2        | 8            | 100           | 192.168.0.6 / 45.119.93.84         | GCIS P2         | iDMZ                     |
| Reverse Proxy Server | scspwg              | 2        | 8            | 100           | 192.168.4.6 / 10.160.139.211       | GCIS P2         | gDMZ                     |
| Apps Server          | scspad              | 4        | 16           | 100 + 500     | 192.168.8.6                        | GCIS P2         | Trust Zone               |
| Database Server      | scspdb              | 4        | 16           | 100 + 200     | 192.168.8.7                        | GCIS P2         | Trust Zone               |
| Veeam Backup Server  | scspbk2             | 4        | 16           | 100 + 1TB     | 192.168.8.9                        | GCIS P2         | Trust Zone               |
| Kiwi Log Server      | scsplog             | 2        | 8            | 100 + 100     | 192.168.8.10                       | GCIS P2         | Trust Zone               |

## Software Specification

| Category             | Software                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        