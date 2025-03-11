# Handover Plan

## Introduction

This Handover Plan outlines the transfer of the Licensing Self-Certification Portal (LSCP) system from Master Concept (Hong Kong) Limited (MC) to the Buildings Department (BD) of the Government of the Hong Kong Special Administrative Region (HKSARG). This document serves as a comprehensive checklist of handover materials and provides essential information for the support and maintenance staff.  All deliverables listed herein should be received by BD from the LSCP implementation team.

## 1. System Overview

The LSCP aims to provide an electronic platform for site inspection and site monitoring personnel to submit, manage, and review inspection and monitoring records.  Users include BD officers and public users involved in these activities.

### 1.1 System Architecture

The LSCP is deployed across two data centers: On-premise (WKGO) and Government Cloud Infrastructure Services (GCIS).

**On-Premise (WKGO):** Located behind an internal firewall with NAT separating three subnets (Production, UAT, and DEV) for internal access only. A reverse proxy server with load balancing enhances security and distributes incoming requests.

**GCIS:** Divided into three subnets: Internet DMZ (iDMZ), Trusted Zone, and Gnet DMZ (gDMZ). Both iDMZ and gDMZ utilize a reverse proxy server, and a Web Application Firewall (WAF) further secures iDMZ access.

External users access the system via the internet through the LSCP Web Application, interacting with Application Servers via the reverse proxy. Internal users access the BDSCS application from the BD intranet, connecting to BD Web Servers in the Trusted Zone through the Departmental Portal (OSDP).  Database Servers, Log Servers, File Servers, a vCenter Server, and Backup Servers reside in the Trusted Zone.

**Disaster Recovery Environment:** Mirrors the production environment architecture and is located at AIA.

**(Detailed diagrams and explanations from the System Manual are included in Appendix A.)**

### 1.2 System Functions

A detailed list of system functions and their corresponding IDs is provided in **Appendix B**.

## 2. Environment Description

### 2.1 Production and UAT Environment

**(Image from hp_i1.md)**

**List of machines and virtual machines:** (To be populated by MC)

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
| ... | ... | ... | ... |

### 2.2 DR Environment

**(Image from hp_i1.md)**

**List of machines and virtual machines:** (To be populated by MC)

| Hostname (Physical Machine) | Hostname (Virtual Machine) | Purpose | IP |
|---|---|---|---|
| ... | ... | ... | ... |


## 3. Handover Schedule and Verification

### 3.1 Schedule

| Action | Date | Action Parties |
|---|---|---|
| Handover | (To be determined) | MC/BD |
| Verification | (To be determined) | BD |

### 3.2 Verification

* **Application URL Verification:** Access links (URLs) will be verified through access checks.
* **Login Accounts Verification:** Login accounts for applications and servers will be verified through login attempts.

## 4. Deliverables

### 4.1 Documentation

**(Table from hp_i1.md with populated file names and versions)**

### 4.2 Program Source Code

| Component | Machine | Directory |
|---|---|---|
| Frontend Application | (To be determined) | (To be determined) |
| Backend Application | (To be determined) | (To be determined) |


### 4.3 Administration Accounts Checklist

**(Table from hp_i1.md with populated account details)**

**Administration Accounts on LSCP:** (Table from hp_i1.md with populated account details)

### 4.4 Backup

* **VM Backup:** Daily VM image backups are performed and stored on backup servers. Production VM images are copied to the DR backup server.
* **Database Backup:** Daily full database backups are performed.

**(Detailed backup procedures and schedules are included in Appendix C.)**

### 4.5 Hardware

**(Detailed hardware specifications and configurations are included in Appendix D.)**

### 4.6 Licensed Software

**(Table from hp_i1.md with corrected and populated license details)**

## 5. Outstanding Items/Issues

None.

## Appendix A: System Architecture Diagrams and Explanations

**(Content from System Manual section 5.2)**

## Appendix B: System Functions

**(Content from System Manual section 5.3)**

## Appendix C: Backup and Recovery Procedures

**(Content from System Manual sections 8.2, 8.5, 8.6, and 9.2)**

## Appendix D: Hardware and Software Inventory

**(Content from System Manual sections 6 and 7)**

## Appendix E: Log Management

**(Content from System Manual section 10)**


---

**Document History**

**(Combined and updated Amendment History table from both input files)**

**Distribution:**

**(Combined Distribution table from both input files)**

? The Government of the Hong Kong Special Administrative Region. The contents of this document remain the property of, and may not be reproduced in whole or in part without the express permission of, the Government of the HKSAR.
