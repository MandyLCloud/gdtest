# System Installation Plan

This document consolidates information from multiple source files to provide a comprehensive System Installation Plan for the Licensing Self-Certification Portal (LSCP) of the Buildings Department.

## 1. Introduction

This System Installation Plan describes the procedure and schedule for deploying the application in the production environment. The system comprises three main parts:

*   Database Server
*   Backend Server
*   Frontend and Web Portal Server

## 2. Project Environment Description

### 2.1 Network Diagram

Below is a logical network diagram in 1/F West Kowloon Government Office for production and UAT site.

[DIAGRAM HERE]

The network will be separated into three zones: DMZ, trusted zone, and storage network.

A two-tier firewall setup will be used to form the trusted zone and DMZ. Incoming network traffic to the system must go through the DMZ before entering the trusted zone.

To utilize hardware resources more effectively, servers listed in section [1.3.3], except the backup server, will be set up in the form of virtual machines (VM) and consolidated into DMZ VM host servers and trusted zone VM host servers for each physical site. Two VM host servers will be built in each zone for the purpose of high availability.

Similarly, storage needed by all servers will be consolidated and provided by SAN storage. A dedicated network will be set up and interconnected with the VM host servers. The backup server will also exist in this storage-dedicated network to carry out backup tasks of VM host servers in DMZ and trusted zone.

The diagram below illustrates the physical setup.

### 2.2 Hardware Specification

**Production and UAT environment:**

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
| prd-scs-admin-server-01 | prd-scs-vcenter-01 | vCenter Server | 192.168.10.24/10.5.161.210 |

**DR environment:**

List of machines and virtual machines:

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
| dr-scs-admin-server-01 | dr-scs-vcenter-01 | vCenter Server | 192.168.20.18/10.5.174.225 |

#### Detailed Hardware Components

The Configuration of Physical Server in Production

|                            |                         |                             |                |                        |
|---------------------------|-------------------------|-----------------------------|----------------|------------------------|
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
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010008 | 192.168.11.20  |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A010004 | 192.168.11.21  |

Hardware Components of Production Servers

| **Item** | **Hardware Component** | **Configuration** | **Qty** |
|---|---|---|---|
| 1 | ESXi Hypervisor Server (prd-scs-admin-server-01) | Dell PowerEdge R750 | 1 |
|   |   | Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz | 1 |
|   |   | 32GB DDR4 Synchronous Registered (Buffered) | 8 |
|   |   | 1.2TB SAS HDD | 3 |
|   |   | ESXi 8.0.3 | 1 |
| 2 | ESXi Hypervisor Server (prd-scs-admin-server-02) | Dell PowerEdge R750 | 1 |
|   |   | Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz | 1 |
|   |   | 32GB DDR4 Synchronous Registered (Buffered) | 8 |
|   |   | 1.2TB SAS HDD | 3 |
|   |   | ESXi 8.0.3 | 1 |
| 3 | NAS (prd-scs-nas) | Dell PowerEdge R750 | 1 |
|   |   | CPU??? | ??? |
|   |   | RAM??? | ??? |
|   |   | HDD??? | ??? |
|   |   | Windows Server 2022 | ??? |
| 4 | SAN Switch (prd-scs-sw-01) | Dell DS6610B | 1 |
|   |   | Ports | 16 |
| 5 | SAN Switch (prd-scs-sw-02) | Dell DS6610B | 1 |
|   |   | Ports | 16 |
| 6 | SAN Storage (PS500T-Cluster1) | Dell PS500T | 1 |
|   |   | 3.8TB NVME SSD | 11 |
| 7 | Backup Appliance (prd-scs-backupstorage-01) | Dell DataDomain DD3300 | 1 |
| 8 | Tape Library | DELL ML3 | 1 |
| 9 | Firewall (PA-850-SCSPri) | Palo Alto PA 850 | 1 |
| 10 | Firewall (PA-850-SCSSec) | Palo Alto PA 850 | 1 |
| 11 | Switch (???) | Cisco ??? | 1 |
| 12 | Switch (???) | Cisco ??? | 1 |
| 13 | KVM | CyberView | 1 |
| 13 | UPS (???) | Vertiv? Liebert? GXT5 3000 | 1 |
| 14 | UPS (???) | Vertiv? Liebert? GXT5 3000 | 1 |

Partition Configuration of Production Servers

| **Host Name**           | **Drive**       | **Capacity** | **Description**              |
|--------------------|-----------------|----------|--------------------------|
| prd-scs-admin-server-01 | local           | 2.4TB        | VMware?ESXi Operating system |
| prd-scs-admin-server-02 | local           | 2.4TB        | VMware?ESXi Operating system |
| PS500T-Cluster1         | VM_Volume01     | 20TB         | Shared pool of storage space |
| PS500T-Cluster1         | QuorumDisk-VM-1 | 2.5GB        | Shared pool of storage space |
| prd-scs-nas             | C:              | ???          | OS                           |
|                         | D:              | ???          | Data                         |

The Configuration of Physical Server in DR Site

|                           |                        |                             |                |                        |
|---------------------------|-------------------------|-----------------------------|----------------|------------------------|
| **Model**                 | **Host Name**           | **IP**                      | **Serial No.** | **Disk Configuration** |
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
|---------------------------|-----------------|-----------------|----------------|-----------------|
| **Host Name** | **Internal IP** | **External IP** | **Model**        | **Serial No.** |
| PA-850-SCSDR  | 192.168.20.12   | 10.5.174.215    | Palo Alto PA-850 | 011901063069   |

The Configuration of Switches in DR Site

|               |                 |              |                |
|---------------------------|-----------------|--------------|----------------|
| **Host Name** | **Internal IP** | **Model**    | **Serial No.** |
| ???           | 192.168.20.13   | Catalyst ??? | ???            |

The Configuration of UPS in DR Site

|                            |                      |                |
|----------------------------|----------------------|----------------|
| **Model**                  | **Serial No.**       | **IP Address** |
| Vertiv? Liebert? GXT5 3000 | 2102311887222A01000A | 192.168.20.11  |

Hardware Components of Disaster Recovery Servers

| Item | Hardware Component | Configuration | Qty |
|---|---|---|---|
| 1 | ESXi Hypervisor Server (dr-scs-admin-server-01) | Dell PowerEdge R750 | 1 |
|   |   | Intel(R) Xeon(R) Gold 6326 CPU @ 2.90GHz | 1 |
|   |   | 32GB DDR4 Synchronous Registered (Buffered) | 8 |
|   |   | 1.2TB SAS HDD | 3 |
|   |   | ESXi 8.0.3 | 1 |
| 2 | NAS (dr-scs-nas) | Dell PowerEdge R750 | 1 |
|   |   | CPU??? | ??? |
|   |   | RAM??? | ??? |
|   |   | HDD??? | ??? |
|   |   | Windows Server 2022 | ??? |
| 3 | SAN Switch (dr-scs-sw-01) | Dell DS6610B | 1 |
|   |   | Ports | 16 |
| 4 | SAN Storage (PS500T-Cluster2) | Dell PS500T | 1 |
|   |   | 3.8TB NVME SSD | 11 |
| 5 | Backup Appliance (dr-scs-backupstorage-01) | Dell DataDomain DD3300 | 1 |
| 6 | Firewall (PA-850-SCSPri) | Palo Alto PA 850 | 1 |
| 7 | Switch (???) | Cisco ??? | 1 |
| 8 | KVM | CyberView | 1 |
| 9 | UPS (???) | Vertiv? Liebert? GXT5 3000 | 1 |

Partition Configuration of DR Servers

|                        |             |              |                              |
|------------------------|-------------|--------------|------------------------------|
| **Host Name**          | **Drive**   | **Capacity** | **Description**              |
| dr-scs-admin-server-01 | local       | 2.4TB        | VMware?ESXi Operating system |
| PS500T-Cluster2        | VM Volume01 | 20TB         | Shared pool of storage space |
| dr-scs-nas             | C:          | ???          | OS                           |
|                        | D:          | ???          | Data                         |

### 2.3 Software Specification

| Machine | Hostname | Software Requirement |
|---|---|---|
| vCenter Server | prd-scs-vcenter-01 | vCenter 8.0.3 Build 24322831 |

**Development Frameworks:**

| Framework | Version |
|---|---|
| React (frontend) | 18.2.0 |

#### Guest Servers Components

**Production guest servers**

| **Role** | **Host Name** | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses** | **Data Center** | **Host Server / Zone** |
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

**UAT guest servers**

| **Role** | **Host Name** | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses** | **Data Center** | **Host Server / Zone** |
|---|---|---|---|---|---|---|---|
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

**DEV guest servers**

| **Role** | **Host Name** | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses** | **Data Center** | **Host Server / Zone** |
|---|---|---|---|---|---|---|---|
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

**Disaster Recovery guest servers**

| **Role** | **Host Name** | **vCPU** | **RAM (GB)** | **Disk (GB)** | **IP Addresses** | **Data Center** | **Host Server / Zone** |
|---|---|---|---|---|---|---|---|
| vCenter | dr-scs-vcenter-01 | 16 | 39 | 1.33TB | 192.168.20.18 / 10.5.174.225 | AIA | dr-scs-admin-server-01 |
| Veeam Backup Server | dr-scs-backup-01 | 8 | 24 | 300 + 1TB | 192.168.20.19 / 10.5.161.224 | AIA | dr-scs-admin-server-01 |
| Kiwi Log Server | dr-scs-log-01 | 4 | 8 | 300 + 500 | 192.168.20.10 | AIA | dr-scs-admin-server-01 |
| API Server | dr-scs-admin-api-01 | 2 | 8 | 90 | 192.168.22.11 | AIA | dr-scs-admin-server-01 |
| Frontend Server | dr-scs-admin-frontend-01 | 2 | 8 | 90 | 192.168.22.12 | AIA | dr-scs-admin-server-01 |
| Backend Server | dr-scs-admin-backend-01 | 2 | 8 | 90 | 192.168.22.13 | AIA | dr-scs-admin-server-01 |
| Database Server | dr-scs-db-01 | 2 | 8 | 90 + 500 | 192.168.22.14 | AIA | dr-scs-admin-server-01 |
| File Server | dr-scs-filer | 2 | 8 | 90 + 1TB | 192.168.22.16 | AIA | dr-scs-admin-server-01 |
| Reverse Proxy Server | dr-scs-proxy | 2 | 4 | 90 | 192.168.22.15 / 10.5.174.228 | AIA | dr-scs-admin-server-01 |
| Reverse Proxy Server | scspwi | 2 | 8 | 100 | 192.168.0.6 / 45.119.93.84 | GCIS P2 | iDMZ |
| Reverse Proxy Server | scspwg | 2 | 8 | 100 | 192.168.4.6 / 10.160.139.211 | GCIS P2 | gDMZ |
| Apps Server | scspad | 4 | 16 | 100 + 500 | 192.168.8.6 | GCIS P2 | Trust Zone |
| Database Server | scspdb | 4 | 16 | 100 + 200 | 192.168.8.7 | GCIS P2 | Trust Zone |
| Veeam Backup Server | scspbk2 | 4 | 16 | 100 + 1TB | 192.168.8.9 | GCIS P2 | Trust Zone |
| Kiwi Log Server | scsplog | 2 | 8 | 100 + 100 | 192.168.8.10 | GCIS P2 | Trust Zone |

#### Gateway and SMTPX Configuration

**SMTPX**

|  |  |
|---|---|
| SMTPX service hostname | smtpx.cis.hksarg (resolvable by CCGO DNS) |
| SMTPX service IP address | 10.106.5.103, 10.106.5.104, 10.106.105.103, 10.106.105.104 (IP addresses are provided for ACL settings. To enjoy the automatic failover feature, mail servers should access SMTPX service through hostname.) |
| SMTP port number | 587 |
| Sender IP address | (B/Ds' IP address within GNET) |
| Login and password | Not required |
| Authentication | By e-Certificate issued from Hong Kong Post or the Government ISCCA |
| Sender address in e-mail | Valid e-mail address registered in IMX service |
| Connection encryption | STARTTLS (Mandatory) |
| Compatible Protocols | SPF and DKIM |

SMTPX configured in the IIS 6.0 of the following servers: scspwg, scsuwg, scsdwg

**WKGO Production Network Gateway**

|  |  |  |  |
|---|---|---|---|
| **Gateway** | **Subnet** | **IP Range** | **vlan / Zone** |
| 192.168.10.1 | 255.255.255.0 | 192.168.10.1-254 | Management |
| 192.168.11.1 | 255.255.255.0 | 192.168.11.1-254 | Replication / Backup |
| 192.168.12.1 | 255.255.255.0 | 192.168.12.1-254 | Production |
| 192.168.13.1 | 255.255.255.0 | 192.168.13.1-254 | UAT |
| 192.168.14.1 | 255.255.255.0 | 192.168.14.1-254 | DEV |
| 10.5.161.1 | 255.255.255.0 | 10.5.161.205-235 | BD Network |

**AIA DR Network Gateway**

|  |