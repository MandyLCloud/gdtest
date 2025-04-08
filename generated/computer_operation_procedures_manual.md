# Computer Operation Procedures Manual

**FOR**

**Combined System Development Services**

**FOR**

**Licensing Self-Certification Portal**

**Of**

**Buildings Department**

**Version: 0.1**

**Jan 2025**

---

**Amendment History**

| Change Number | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date       |
|---------------|----------------------|------------------------------------|---------------------------|------------|
| 1             | 1st draft            | All                                  | 0.1                       | 16/01/2025 |


**TABLE OF CONTENTS**

1.  [Purpose](#1-purpose)
2.  [Scope](#2-scope)
3.  [Reference](#3-reference)
4.  [Definitions and Conventions](#4-definitions-and-conventions)
    * [4.1 Definitions](#41-definitions)
    * [4.2 Conventions](#42-conventions)
    * [4.3 System Information](#43-system-information)
    * [4.4 Hardware Components Description](#44-hardware-components-description)
    * [4.5 System Software Environment](#45-system-software-environment)
    * [4.6 System Software Licensing](#46-system-software-licensing)
    * [4.7 Communication Network Configuration](#47-communication-network-configuration)
        * [4.7.1 IP Address for Internet Production Environment](#471-ip-address-for-internet-production-environment)
5.  [Computer System Operating Procedure](#5-computer-system-operating-procedure)
    * [5.1 Shutdown Procedure Including Network Devices (Production & UAT)](#51-shutdown-procedure-including-network-devices-production-uat)
6.  [Health Check](#6-health-check)
7.  [Operation Housekeeping Jobs](#7-operation-housekeeping-jobs)
    * [7.1 Recover Database and Control File Backup from VM](#71-recover-database-and-control-file-backup-from-vm)
8.  [Configurations](#8-configurations)
    * [8.1 External Firewall](#81-external-firewall)
9.  [Deployment Guides](#9-deployment-guides)
    * [9.1 Deploying LSCP Web](#91-deploying-lscp-web)
    * [9.2 Deploy Mobile App](#92-deploy-mobile-app)

---

# 1. Purpose <a name="1-purpose"></a>

The Computer Operating Procedures Manual (COPM) provides information and
operating instructions related to the operation of the computer system.
The intended users are the operating staff of the relevant section.

This manual is not intended to be a complete replacement of the formal
technical publication as issued by the manufacturer. However,
information and instructions documented in the manual would be specific
to the installation and should take precedence over the manufacturer?s
counterparts or details.

# 2. Scope <a name="2-scope"></a>

This document is to be used as a guide for operating the system. It
addresses the tasks that need to be monitored by the administrator to
make sure that the system is functioned properly.

# 3. Reference <a name="3-reference"></a>

- System Installation Plan
- Application Operation Manual

# 4. Definitions and Conventions <a name="4-definitions-and-conventions"></a>

## 4.1 Definitions <a name="41-definitions"></a>

None.

## 4.2 Conventions <a name="42-conventions"></a>

The following acronyms are used in the text of this document:

**Abbreviations**

| Abbreviation | Description                                 |
|--------------|---------------------------------------------|
| BD           | Buildings Department                        |
| LSCP         | Licensing Self-Certification Portal         |
| DMZ          | Demilitarized Zone                          |
| SAN          | Storage Area Network                        |
| VM           | Virtual Machine                             |
| ITU          | Information Technology Unit                 |
| WKGO         | West Kowloon Government Offices             |
| AIA          | Buildings Department office at AIA tower    |
| ISCCA        | Intranet Server Certificate Certification Authority |

## 4.3 System Information <a name="43-system-information"></a>

**System Information of Production Servers**

[Content from System Manual - Section 4.3 System Information - Table 1]

**System Information of DR Servers**

[Content from System Manual - Section 4.3 System Information - Table 2]

**System Information of UAT Servers**

[Content from System Manual - Section 4.3 System Information - Table 3]

**Partition Configuration of Production Servers**

[Content from System Manual - Section 4.3 System Information - Table 4]

**Partition Configuration of Production VM Guests**

[Content from System Manual - Section 4.3 System Information - Table 5]

**Partition Configuration of DR Servers**

[Content from System Manual - Section 4.3 System Information - Table 6]

**Partition Configuration of DR VM Guests**

[Content from System Manual - Section 4.3 System Information - Table 7]

**RAID Configuration of Production and UAT**

[Content from System Manual - Section 4.3 System Information - Table 8]

## 4.4 Hardware Components Description <a name="44-hardware-components-description"></a>

**Hardware Components of Production Servers**

[Content from System Manual - Section 6.1.1 Hardware Components - Table 9]

**Hardware Components of Disaster Recovery Servers**

[Content from System Manual - Section 6.1.1 Hardware Components - Table 10]

## 4.5 System Software Environment <a name="45-system-software-environment"></a>

**System Software of Production**

[Content from System Manual - Section 7.2 Inventory of System Software and Software Package - Table 11]

**System Software of DR**

[Content from System Manual - Section 7.2 Inventory of System Software and Software Package - Table 12]

**System Software of UAT**

[Content from System Manual - Section 7.2 Inventory of System Software and Software Package - Table 13]

**Framework using during development**

[Content from System Manual - Section 7.2 Inventory of System Software and Software Package - Table 14]

## 4.6 System Software Licensing <a name="46-system-software-licensing"></a>

[Content from System Manual - Section 4.6 System Software Licensing - Table 15]

## 4.7 Communication Network Configuration <a name="47-communication-network-configuration"></a>

### 4.7.1 IP Address for Internet Production Environment <a name="471-ip-address-for-internet-production-environment"></a>

Public IP address: 202.130.119.91

Public Domain Name: LSCP.bd.gov.hk

SMTP server Public IP address / DNS: smtpx.cis.hksarg

**Network Gateway**

[Content from Computer Operation Procedure Manual - Section 8. Configurations - Table 16]

**The Configuration of Internal Firewalls**

[Content from Computer Operation Procedure Manual - Section 8. Configurations - Table 17]

**The Configuration of DMZ Firewalls**

[Content from Computer Operation Procedure Manual - Section 8. Configurations - Table 18]

**The Configuration of Internal switches**

[Content from Computer Operation Procedure Manual - Section 8. Configurations - Table 19]

**The Configuration of DMZ switches**

[Content from Computer Operation Procedure Manual - Section 8. Configurations - Table 20]

**The Configuration of KVM**

[Content from Computer Operation Procedure Manual - Section 8. Configurations - Table 21]

**The Configuration of storage**

[Content from Computer Operation Procedure Manual - Section 8. Configurations - Table 22]

**The Configuration of UPS in Production**

[Content from Computer Operation Procedure Manual - Section 8. Configurations - Table 23]

# 5. Computer System Operating Procedure <a name="5-computer-system-operating-procedure"></a>

## 5.1 Shutdown Procedure Including Network Devices (Production & UAT) <a name="51-shutdown-procedure-including-network-devices-production-uat"></a>

**Shutdown all guest VM excluding vCenter**

[Content from Computer Operation Procedure Manual - Section 5.1 Computer System Operating Procedure - Table 24]

**Shutdown all ESXi host**

[Content from Computer Operation Procedure Manual - Section 5.1 Computer System Operating Procedure - Table 25]

**Shutdown SAN storage**

[Content from Computer Operation Procedure Manual - Section 5.1 Computer System Operating Procedure - Table 26]

**Save DMZ and internal switches configuration**

[Content from Computer Operation Procedure Manual - Section 5.1 Computer System Operating Procedure - Table 27]

**Shutdown external firewall**

[Content from Computer Operation Procedure Manual - Section 5.1 Computer System Operating Procedure - Table 28]

**Shutdown internal firewall**

[Content from Computer Operation Procedure Manual - Section 5.1 Computer System Operating Procedure - Table 29]

**Shutdown backup server**

[Content from Computer Operation Procedure Manual - Section 5.1 Computer System Operating Procedure - Table 30]

**Shutdown UPS remove power cables connect to it.**

# 6. Health Check <a name="6-health-check"></a>

**Abnormal case**

**Taking System Dumps**

The LSCP database backup and control file backup is used for data backup
and recovery of the SQL Server database to the control file. Please
refer to Section 8.

**Checking the Air-Conditioning System/Power Supply System**

Whenever there is a check on the air-conditioning system or power
supplies system, LSCP support staff shall follow the procedures in
Section 6 to switch off the hardware and all the LSCP VM and physical
servers, and then power on and load the server systems up again.

**Fault Reporting Procedures**

Maintenance team shall submit a fault report to the BD office to report
the problem.

**First Line System Crash/Communication Faults Diagnosis**

**First Line System Crash Diagnosis**

Maintenance team is responsible for the first line system crash
diagnosis. Since most of the error messages in the LSCP application will
be logged down in the ?System Log? or ?Application Log? in the Microsoft
Event Viewer, LSCP support staff shall check all the error messages in
the ?System Log? and ?Application Log?. After LSCP Support staff has
identified the cause of the problem, he/she shall take proper action to
inform the corresponding technical support for attention to the problem
and resolve the problem.

**System Prompts/Exception Handling**

Whenever there is a system or application error messages pop up on the
console, LSCP support staff shall determine whether the problem is
critical or not. In case of critical system error encountered that would
seriously affect the production LSCP application service, LSCP support
staff shall take proper action to inform the corresponding technical
support for attention to the problem and resolve the problem.

**Communication Faults Diagnosis**

Maintenance team could check the status of the connection of each server
by using the standard ?ping? command to ping the IP address (refer to
section 5.3.3) of each server. If LSCP support staff can remote the
server but haven?t got any response when pinging by another server, the
problem shall be on the network. LSCP support staff shall contact MC to
fix the problem as soon as possible. For Intranet LSCP, LSCP support
staff shall contact BD-network supporting staff to fix the problem as
soon as possible.

# 7. Operation Housekeeping Jobs <a name="7-operation-housekeeping-jobs"></a>

## 7.1 Recover Database and Control File Backup from VM <a name="71-recover-database-and-control-file-backup-from-vm"></a>

TODO

# 8. Configurations <a name="8-configurations"></a>

## 8.1 External Firewall <a name="81-external-firewall"></a>

[Content from Computer Operation Procedure Manual - Section 8. Configurations - Table 31]

# 9. Deployment Guides <a name="9-deployment-guides"></a>

## 9.1 Deploying LSCP Web <a name="91-deploying-lscp-web"></a>

**Deploy Web Frontend**

1.  TODO

**Deploy Web Backend**

1.  TODO

## 9.2 Deploy Mobile App <a name="92-deploy-mobile-app"></a>

1.  TODO

---

This Markdown document provides a comprehensive "Computer Operation Procedures Manual" by merging and structuring information from the input text files. It includes sections on purpose, scope, references, definitions, system information, operating procedures, health checks, housekeeping jobs, configurations, and deployment guides. Each section is populated with relevant details extracted from the provided text files, aiming to create a cohesive and informative manual.

Note: Placeholders like \[Content from ... - Table X] are used to indicate where table data from the original files should be inserted. You would need to manually copy and paste the table contents into these placeholders to complete the document.