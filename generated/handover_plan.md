# Handover Plan

## Introduction

This Handover Plan outlines the transfer of the Licensing Self-Certification Portal (LSCP) system from Master Concept (Hong Kong) Limited (MC) to the Buildings Department (BD) of the Government of the Hong Kong Special Administrative Region (HKSARG).  This document serves as a comprehensive checklist of handover materials and provides essential information for the support and maintenance staff.  All deliverables listed herein should be received by BD from the LSCP implementation team.

## 1. System Overview

The LSCP aims to provide an electronic platform for site inspection and site monitoring personnel to submit, manage, and review inspection and monitoring records.  Users include BD officers and public users involved in these activities.

### 1.1 System Architecture

The LSCP is deployed across two data centers: On-premise (WKGO) and Government Cloud Infrastructure Services (GCIS).  The on-premise system resides behind a firewall with NAT, segmented into Production, UAT, and DEV subnets for internal access. A reverse proxy with load balancing enhances security and distributes requests to frontend web servers.

The GCIS deployment is divided into Internet DMZ (iDMZ), Trusted Zone, and Gnet DMZ (gDMZ). Both iDMZ and gDMZ utilize a reverse proxy and Web Application Firewall (WAF) for enhanced security.

External users access the system via the internet through the LSCP Web Application, which interacts with Application Servers through the reverse proxy.  Internal users access the BDSCS application via the Departmental Portal (OSDP), connecting to BD Web Servers in the Trusted Zone.  The system also includes Log Servers, File Servers, Database Servers, a vCenter Server, and Backup Servers.

Detailed diagrams of the system architecture in both Production and Disaster Recovery environments are provided in the System Manual (attached).

### 1.2 System Functions

A detailed list of system functions, including user authentication, TCP management, form submission, and site project management, is provided in the System Manual (attached).

## 2. Environment Description

### 2.1 Production and UAT Environment

[Image of Production and UAT environment]

A detailed list of physical and virtual machines, their purpose, and IP addresses for the Production and UAT environment is included in the System Manual (attached).

### 2.2 Disaster Recovery Environment

[Image of DR environment]

A detailed list of physical and virtual machines, their purpose, and IP addresses for the DR environment is included in the System Manual (attached).

## 3. Handover Schedule and Verification

### 3.1 Schedule

| Action       | Date | Action Parties |
|--------------|------|----------------|
| Handover     | TBD  | MC/BD          |
| Verification | TBD  | BD             |

### 3.2 Verification

* **Application URL Verification:** Access to each application URL will be verified.
* **Login Accounts Verification:** Login accounts for applications and servers will be verified.

## 4. Documentation

A complete list of documents to be handed over, including file names and versions, is provided in the attached Handover Plan document. This includes documents such as the SA&D Report, PID, system test plans and results, user manuals, DR plan, and security procedures.

## 5. Program Source Code

| Component            | Machine | Directory |
|----------------------|---------|-----------|
| Frontend Application | TBD     | TBD       |
| Backend Application  | TBD     | TBD       |


## 6. Administration Accounts Checklist

Detailed administration account information, including user type, hostname, IP addresses, access methods, usernames, and passwords, for various systems (Blade Servers, Hypervisors, Windows Servers, etc.) and the LSCP application (UAT and PRD/DR environments) is provided in the attached Handover Plan document.

## 7. Backup and Recovery

### 7.1 Backup

VM backups are performed daily by the backup server and stored on backup servers. Production VM images are also copied to the DR backup server. Database full export backups are performed daily on DB servers.  Detailed backup procedures and schedules are outlined in the System Manual (attached).

### 7.2 Recovery

The System Manual (attached) details the recovery procedures for various failure scenarios, including database server failure, electricity shortage, and application server failure. It also outlines the expected downtime for each scenario.

## 8. Licensed Software

A detailed list of licensed software, including the item, amount, and expiry date, is provided in the attached Handover Plan document.

## 9. Outstanding Items/Issues

None.

## 10. System Manual

The attached System Manual provides a comprehensive overview of the LSCP system, including:

* Equipment Configuration (hardware and software)
* Security and Backup Procedures
* Database Administration
* Log Management

## Appendices

All relevant appendices, including rack diagrams, network configurations, and software inventories, are included in the System Manual (attached).


## Contact Information

For any questions or concerns regarding this handover plan, please contact the designated representatives from MC and BD.


---

**Note:**  Placeholders like "TBD" and "[Image]" should be replaced with actual data before finalizing the document.  Ensure all attached documents are included with the handover package.  The logo image references should be updated to point to the correct location of the image files.  The date in the Handover Plan (Jan 2025) should be updated to reflect the actual handover date.  The amendment history tables should be updated to reflect the final version of the document.
