# Program Specification Document

This document outlines the program specifications for the SCS system, including functional and technical requirements, security considerations, interface details, and constraints.

## 1. Introduction

This document details the requirements for the SCS system, covering functional, security, interface, and technical aspects. It also identifies constraints and includes appendices with supporting information.

## 2. Accessibility Conformance

The SCS system will be tested to conform to W3C WCAG 2.1 Level AA standards, utilizing tools like screen readers, screen magnifiers, and voice controls.

## 3. Security Requirements

### 3.1 REQ-SR-01 SRAA

*   **Priority:** High
*   **Functional Requirement:** A Security Risk Assessment Audit (SRAA) will be conducted to identify and address security vulnerabilities.  All findings and recommendations from the security auditors will be implemented.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc
*   **Reference:** Appendix 4 ? Information Security Requirement

### 3.2 REQ-SR-02 PIA and PCA

*   **Priority:** High
*   **Functional Requirement:** Privacy Impact Assessment (PIA) and Privacy Compliance Audit (PCA) will be conducted to address privacy issues. All findings and recommendations from the auditors will be implemented.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

### 3.3 REQ-SR-03 Encryption and Decryption of Classified Data

*   **Priority:** High
*   **Functional Requirement:** All classified data, such as HKID, will be encrypted during transmission and storage (file system or database). Strong symmetric encryption algorithms like AES 256bit or Hash functions like SHA-256 will be used.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

### 3.4 REQ-SR-04 System Audit

*   **Priority:** High
*   **Functional Requirement:** Important events (e.g., create case, login) will be logged and stored in the database for auditing purposes.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

### 3.5 REQ-SR-05 System Control

*   **Priority:** High
*   **Functional Requirement:** Security controls (e.g., Firewall, network control, physical access control) will be implemented to protect access to the system.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

## 4. Interface Requirements

### 4.1 REQ-IR-01 Interface with BCIS

*   **Priority:** High
*   **Functional Requirement:** The system shall provide interfaces with BCIS to complete certain tasks, including:
    1.  Receiving lists of addresses, file references, or other master data from BCIS for case creation.
    2.  Sending application data to BCIS to create cases using BCIS stored procedures in batch (To be confirmed).
    3.  Updating application data to BCIS using BCIS stored procedures.
    4.  Providing a reference link between SCS and BCIS.
    5.  Transferring data from SCS to BCIS for statistical reports.
    6.  Selecting blocks for new address creation in BCIS via to-do-list and email.
    7.  Handling all input and edit of 12 and 13 file Licensing cases in SCS instead of BCIS.
    8.  Mapping with BCIS users (User name, Post, File reference, DP login id, case officer).
    9.  Including Licensing nature Enquire.
    10. Linking to DV tables of BCIS.
    11. Conducting a detailed study for easy retrieval of records from SCS by comparing data storage against a reference link from SCS and BCIS, and determine a solution most suited to user requirements.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

### 4.2 REQ-IR-02 Interface with BD Website

*   **Priority:** High
*   **Functional Requirement:** The system shall display a list of Pre-accepted Proprietary Temporary structure data on the BD website.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

### 4.3 REQ-IR-03 Interface with Minor Works

*   **Priority:** High
*   **Functional Requirement:** The system shall provide an sFTP upload account to MWMS 2.0 to collect AP/RSE data (User Name, Registration Number, HKID, Expiry Date, etc.) daily. SCS will set up an sFTP server to receive AP/RSE data and update the database accordingly. The SCS system can use a Departmental Portal link to redirect to the CRM of MWMS to view detailed AP/RSE information, similar to ESH.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

### 4.4 REQ-IR-04 Interface with ESH

*   **Priority:** High
*   **Functional Requirement:** Cases of information and hyperlinks of SCS will be provided to ESH to view relating case information and redirect to SCS respectively.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

### 4.5 REQ-IR-05 Interface with ERKS

*   **Priority:** High
*   **Functional Requirement:** e-Certificates, e-notices, reply letters, and other documents are required to be imported into the ERKS system for record keeping. The detailed interface specification and implementation will be done in the SM&S stage.
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

### 4.6 REQ-IR-06 Interface with BRAVO

*   **Priority:** High
*   **Functional Requirement:** The SCS system can use `<https://dp2.bd.hksarg/bravo/intranetSignOn>` to redirect to BRAVO.  The SCS system could also be redirected to BRAVO through a URL call with specified parameters.

    **URL Syntax:**

    `<Departmental Portal URL>/bravo/BuildingSearchRedirection?`

    **Parameters:**

    *   **With Case number and Year:** `CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`
    *   **With Block ID:** `BLOCK_ID=<BLOCK_ID>`
    *   **With full File Reference No:** `SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=<SUBJECT_CODE>&CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>&SPECIAL_CAT=<SPECIAL_CAT>`
*   **Non-functional Requirement:** Nil
*   **Frequency of Use:** Ad-hoc

## 5. Technical Requirements

| Req. ID   | Requirement Name                           | Target Users | Priority |
| :-------- | :----------------------------------------- | :----------- | :------- |
| REQ-TR-01 | 24x7 Internet and Intranet                 | System Admin | H        |
| REQ-TR-02 | Integrated Cloud GCIS and On Premises      | System Admin | H        |
| REQ-TR-03 | Input Validation                           | System Admin | H        |
| REQ-TR-04 | Record Relocation from GCIS to On Premises | System Admin | H        |
| REQ-TR-05 | High Availability                          | System Admin | H        |
| REQ-TR-06 | Monitoring and Alert Generation            | System Admin | H        |
| REQ-TR-07 | DR Drill                                   | System Admin | H        |
| REQ-TR-08 | UTF-8, Unicode or HKSCS                     | System Admin | H        |
| REQ-TR-09 | System Logging                             | System Admin | H        |
| REQ-TR-10 | High Configurable                          | System Admin | H        |
| REQ-TR-11 | Backup and Recovery                          | System Admin | H        |
| REQ-TR-12 | Operation System and Browser Compatibility | System Admin | H        |
| REQ-TR-13 | Review and Update privilege                | System Admin | H        |
| REQ-TR-14 | Health Check                               | System Admin | H        |
| REQ-TR-15 | Encryption on All Communications           | System Admin | H        |
| REQ-TR-16 | Version Control for application            | System Admin | NA       |
| REQ-TR-17 | Monthly Usage Statistics and Ad-hoc Statistics | System Admin | H        |
| REQ-TR-18 | Check-in and Check-out                     | System Admin | NA       |
| REQ-TR-19 | Language support (EN/TC/SC)                | System Admin | H        |
| REQ-TR-20 | System Performance                         | System Admin | H        |
| REQ-TR-21 | Reports and statistics for monitor system performance | System Admin | H        |
| REQ-TR-22 | Ad-hoc and periodic updates on the contents | System Admin | H        |
| REQ-TR-23 | Provide refined Login & Authentication / FULL Audit features | System Admin | H        |
| REQ-TR-24 | Login user account login by user ID and password | BD/SWD/EBD/MC | H        |
| REQ-TR-25 | Version control of source code             | System Admin | H        |
| REQ-TR-26 | System log tracking                          | System Admin | H        |
| REQ-TR-27 | Scalable system frame design                | System Admin | H        |
| REQ-TR-28 | Data exchange with other system securely    | System Admin | H        |
| REQ-TR-29 | Security measurement                         | System Admin | H        |
| REQ-TR-30 | Help check email notification                | System Admin | H        |
| REQ-TR-31 | Email notification for all batch jobs        | System Admin | H        |
| REQ-TR-32 | Conform to the Interoperability Framework    | System Admin | H        |
| REQ-TR-33 | Manage System Parameters                     | System Admin | H        |
| REQ-TR-34 | Allow System Access by EBD and SWD           | System Admin | H        |
| REQ-TR-35 | Independent System (Not depended on other BD system) | System Admin | H        |
| REQ-TR-36 | Logout automatically for inactive for 30 minutes | System Admin | H        |
| REQ-TR-37 | Centralized log Management                   | System Admin | H        |
| REQ-TR-38 | Handle around 300 user accounts of EDB and SWD for Single Sign On | System Admin | H        |
| REQ-TR-39 | Paper Less                                   | System Admin | H        |
| REQ-TR-40 | PDF template and mapping field for letter generation | System Admin | H        |

### 5.1 Detailed Technical Requirements

*   **REQ-TR-01 24x7 Internet and Intranet:** The system shall provide 24x7 website access for AP/RSE through the Internet and for BD users through Intranet/GNET, maintaining high availability except during maintenance or exceptional handling.
*   **REQ-TR-02 Integrated Cloud GCIS and On Premises:** The system shall integrate GCIS in the Cloud and On Premises in BD, with front-end functions for AP/RSE in GCIS and back-end functions for BD users on premises.
*   **REQ-TR-03 Input Validation:** The system shall validate all data input to prevent security attacks like SQL Injection. CAPTCHA will be implemented for form submission to prevent DDOS attacks.
*   **REQ-TR-04 Record Relocation from GCIS to On Premises:** The system shall provide a function to relocate records from GCIS to on-premises.
*   **REQ-TR-05 High Availability:** The system shall maintain high availability with active-active application servers and DR capability.
*   **REQ-TR-06 Monitoring and Alert Generation:** A log server shall monitor server health and alert administrators by email in critical situations. Security audit logs shall be kept for 12 months. System, Application, equipment will be monitoring and alert email will be triggered if any warning and failure.
*   **REQ-TR-07 DR Drill:** DR Drill tests will be conducted to test disaster recovery procedures.  Recovery Time Objective (RTO) is 1 day.
*   **REQ-TR-08 UTF-8, Unicode or HKSCS:** The system shall support UTF-8, Unicode, or ISO10646 Standard and Hong Kong Supplementary Character Set (HKSCS) coded in ISO10646.
*   **REQ-TR-09 System Logging:** The system shall record and track all functions, tasks, processes, and user actions. The system log, user activity log, and transaction log of SCS should be produced and kept for at least 12 months and achieve all logs.
*   **REQ-TR-10 High Configurable:** The system shall be highly configurable in coding and avoid hard coding as far as possible.
*   **REQ-TR-11 Backup and Recovery:** The system shall execute periodic backups to external storage: daily incremental backups and weekly full backups. Full backups shall be kept for 6 months. Archive outdated information, when required but no more than twice per year.
*   **REQ-TR-12 Operation System and Browser Compatibility:** The system shall support the following OS/Browser combinations:

    | Operating System / Browser | Microsoft Windows 8.1 | Microsoft Windows 10 and 11 | Mac OS X | Linux | iOS | Android |
    | :------------------------- | :-------------------- | :-------------------------- | :------- | :---- | :-- | :------ |
    | Microsoft Edge             | Not applicable        | Yes                         | Not applicable | Not applicable | Not applicable | Not applicable |
    | Safari                     | Not applicable        | Not applicable              | Yes      | Not applicable | Yes | Not applicable |
    | Mozilla Firefox            | Yes                   | Yes                         | Yes      | Yes   | Yes | Yes |
    | Google Chrome              | Yes                   | Yes                         | Yes      | Yes   | Yes | Yes |
*   **REQ-TR-13 Review and Update Privilege:** The system shall provide a function to review and update user privileges.
*   **REQ-TR-14 Health Check:** The system shall provide a function to perform health checks. A health check hyperlink will be provided to System Administration to check the system on a regular basis.
*   **REQ-TR-15 Encryption on All Communications:** Communication and data transfer between client and server or server to server will be encrypted using HTTPS.
*   **REQ-TR-16 Version Control for application:** Programming versioning shall be maintained.
*   **REQ-TR-17 Monthly Usage Statistics and Ad-hoc Statistics:**
    1.  Allow data administrator to run ?Select? SQL statement through the application website. Results shall be exportable as CSV excel file. (e.g. No contain HKID )
    2.  Appendix 4 - Utilisation Survey
    3.  Active and Inactive User Account Report by selection date and time
*   **REQ-TR-18 Check-in and Check-out:** The system shall able to check-in or check-out documents in order to prevent duplicate update on same document.
*   **REQ-TR-19 Language Support (EN/TC/SC):** The system shall provide web pages in English, Traditional Chinese, and Simplified Chinese.
*   **REQ-TR-20 System Performance:** The system performance will be periodically monitored in order to dig out any performance bottleneck.
*   **REQ-TR-21 Reports and statistics for monitor system performance:** The reports and statistics of system performance can be generated using system monitoring tool.
*   **REQ-TR-22 Ad-hoc and periodic updates on the contents:** The system allows authorized BD users to edit the case information. Develop an automatic function to delete the records by customization.
*   **REQ-TR-23 Provide refined Login & Authentication / FULL Audit features:** The Login information will be record in audit and stored in database.
*   **REQ-TR-24 Login user account login by user ID and password:** In case the OSDP is malfunctioned, the system provide another interface for BD/EDB/SWD users to login the system using username and password.
*   **REQ-TR-25 Version control of source code:** The source code of the system will be kept in Version Control System and providing versioning support.
*   **REQ-TR-26 System log tracking:** The system provides logging to file for all functions and events.
*   **REQ-TR-27 Scalable system frame design:** The system provides High Availability (HA) in the system design so that to minimize single point of failure. Also, it can increase the HA by adding extra nodes whenever it needs.
*   **REQ-TR-28 Data exchange with other system securely:** The system will connect other system using secure method such as HTTPS if it is applicable.
*   **REQ-TR-29 Security measurement:** The system will be designed with security in first priority and security control will be added in different layers such as application, network, database?etc.
*   **REQ-TR-30 Help check email notification:** The system will send email notification using internal BD email server and external GCIS email server. The email server should be monitored by system administrator.
*   **REQ-TR-31 Email notification for all batch jobs:** Once the batch job is finished, an email notification will be sent to system administrator.
*   **REQ-TR-32 Conform to the Interoperability Framework:** The system is designed and developed using standard and well-design application framework i.e. .Net 6
*   **REQ-TR-33 Manage System Parameters:** The system parameters will be placed in configuration file and will not hardcode in the coding.
*   **REQ-TR-34 Allow System Access by EDB and SWD:** The EDB/SWD users are required to login their OSDP and access SCS. The user authorization control will be maintained in SCS.
*   **REQ-TR-35 Independent System (Not depended on other BD system):** The system is designed to separate the front-end program for applicant/AP/RSE and the back-end program for internal BD users. Also, the system will be run independently no matter there were down time of other system, except BCIS.
*   **REQ-TR-36 Logout automatically for inactive for 30 minutes:** For SSO users, the logout will be done on ODSP. For special case i.e. login using username and password, the system will terminate the session after a certain time such as 30 mins.
*   **REQ-TR-37 Centralized log management:** The log files will be stored in centralized folder if it is applicable.
*   **REQ-TR-38 Handle around 300 user accounts of EDB and SWD for Single Sign On:** The system will be tested to handle concurrent users to access SCS. In case there is any bottleneck in hardware level, it can increase the throughput by adding more nodes.
*   **REQ-TR-39 Paper Less:** The system will generate and save different documents in the system and BD users will keep the documents in hard copy of the filing system.
*   **REQ-TR-40 PDF template and mapping field for letter generation:** The generated documents will be in PDF format.

## 6. Constraints

### 6.1 Complexity of Address Identification

Due to the complexity of address identification, the system may not be able to create cases. In this connection, case creation will be passed to BCIS. Once the application is created in BCIS, the data will be sent back to SCS for workflow processing.

### 6.2 Signature of AP/RSE

When an applicant sends an application by post, the system shall verify the AP/RSE information provided by MWMS 2.0. However, the handwritten signature needs to be verified by the Registry using eyeball.

## 7. Appendices

*   **Appendix 1:** 3-Tier BSR System (Diagram)
*   **Appendix 2:** Sample of School and CCC Certificates and Notices (Documents)
*   **Appendix 3:** Sample of Letter of Requirement (LoR) (Document)
*   **Appendix 4:** Information Security Requirement (Table)
*   **Appendix 5:** Sample of Utilisation Report (Image)