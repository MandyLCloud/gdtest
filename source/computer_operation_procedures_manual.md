# Computer Operation Procedures Manual - Analysis

This document consolidates information extracted from the provided text, focusing on the requirements, constraints, and appendices related to the Computer Operation Procedures Manual for the SCS system.

## 1. System Overview

The SCS system requires various interfaces with other systems like BD Website, Minor Works, ESH, ERKS, and BRAVO. It also has a set of technical requirements focusing on availability, security, and performance. The system integrates Cloud GCIS and On-Premises environments.

## 2. Interface Requirements (REQ-IR)

The system needs to interface with the following systems:

*   **REQ-IR-02 Interface with BD Website:** Displays a list of pre-accepted proprietary temporary structure data on the BD website.
    *   Priority: High
    *   Frequency of Use: Ad-hoc
*   **REQ-IR-03 Interface with Minor Works:** Receives AP/RSE data from MWMS 2.0 via sFTP upload on a daily basis.  Provides a departmental portal link to CRM of MWMS to view AP/RSE information.
    *   Priority: High
    *   Frequency of Use: Ad-hoc
*   **REQ-IR-04 Interface with ESH:** Provides information and hyperlinks of SCS to ESH for viewing related case information and redirecting to SCS.
    *   Priority: High
    *   Frequency of Use: Ad-hoc
*   **REQ-IR-05 Interface with ERKS:** Imports e-Certificates, e-notices, reply letters, and other documents into ERKS for record keeping.
    *   Priority: High
    *   Frequency of Use: Ad-hoc
*   **REQ-IR-06 Interface with BRAVO:** Redirects to BRAVO using a specific URL with parameters like CASE_NUMBER, YEAR, BLOCK_ID, SEARCH_TYPE, SUBJECT_CODE, and SPECIAL_CAT.
    *   Priority: High
    *   Frequency of Use: Ad-hoc

## 3. Technical Requirements (REQ-TR)

The following technical requirements are crucial for the SCS system:

| Req. ID   | Requirement Name                               | Target Users | Priority |
| :-------- | :--------------------------------------------- | :----------- | :------- |
| REQ-TR-01 | 24x7 Internet and Intranet                     | System Admin | H        |
| REQ-TR-02 | Integrated Cloud GCIS and On Premises          | System Admin | H        |
| REQ-TR-03 | Input Validation                               | System Admin | H        |
| REQ-TR-04 | Record Relocation from GCIS to On Premises     | System Admin | H        |
| REQ-TR-05 | High Availability                              | System Admin | H        |
| REQ-TR-06 | Monitoring and Alert Generation                | System Admin | H        |
| REQ-TR-07 | DR Drill                                       | System Admin | H        |
| REQ-TR-08 | UTF-8, Unicode or HKSCS                         | System Admin | H        |
| REQ-TR-09 | System Logging                                 | System Admin | H        |
| REQ-TR-10 | High Configurable                              | System Admin | H        |
| REQ-TR-11 | Backup and Recovery                              | System Admin | H        |
| REQ-TR-12 | Operation System and Browser Compatibility     | System Admin | H        |
| REQ-TR-13 | Review and Update privilege                      | System Admin | H        |
| REQ-TR-14 | Health Check                                   | System Admin | H        |
| REQ-TR-15 | Encryption on All Communications               | System Admin | H        |
| REQ-TR-16 | Version Control for application                | System Admin | NA       |
| REQ-TR-17 | Monthly Usage Statistics and Ad-hoc Statistics | System Admin | H        |
| REQ-TR-18 | Check-in and Check-out                         | System Admin | NA       |
| REQ-TR-19 | Language support (EN/TC/SC)                    | System Admin | H        |
| REQ-TR-20 | System Performance                             | System Admin | H        |
| REQ-TR-21 | Reports and statistics for monitor system performance | System Admin | H        |
| REQ-TR-22 | Ad-hoc and periodic updates on the contents    | System Admin | H        |
| REQ-TR-23 | Provide refined Login & Authentication / FULL Audit features | System Admin | H        |
| REQ-TR-24 | Login user account login by user ID and password | BD/SWD/EBD/MC | H        |
| REQ-TR-25 | Version control of source code                 | System Admin | H        |
| REQ-TR-26 | System log tracking                            | System Admin | H        |
| REQ-TR-27 | Scalable system frame design                    | System Admin | H        |
| REQ-TR-28 | Data exchange with other system securely       | System Admin | H        |
| REQ-TR-29 | Security measurement                           | System Admin | H        |
| REQ-TR-30 | Help check email notification                  | System Admin | H        |
| REQ-TR-31 | Email notification for all batch jobs          | System Admin | H        |
| REQ-TR-32 | Conform to the Interoperability Framework      | System Admin | H        |
| REQ-TR-33 | Manage System Parameters                       | System Admin | H        |
| REQ-TR-34 | Allow System Access by EBD and SWD             | System Admin | H        |
| REQ-TR-35 | Independent System (Not depended on other BD system) | System Admin | H        |
| REQ-TR-36 | Logout automatically for inactive for 30 minutes | System Admin | H        |
| REQ-TR-37 | Centralized log Management                     | System Admin | H        |
| REQ-TR-38 | Handle around 300 user accounts of EDB and SWD for Single Sign On | System Admin | H        |
| REQ-TR-39 | Paper Less                                     | System Admin | H        |
| REQ-TR-40 | PDF template and mapping field for letter generation | System Admin | H        |

**Key Technical Requirements Details:**

*   **24x7 Availability (REQ-TR-01):**  The system must be available 24/7 via the internet and intranet, except during maintenance.
*   **Integrated Cloud and On-Premises (REQ-TR-02):** Front-end functions for AP/RSE are in GCIS (Cloud), while back-end functions for BD users are on-premises.
*   **Input Validation (REQ-TR-03):**  All data input must be validated to prevent security attacks like SQL injection. CAPTCHA is required for form submission to prevent DDOS attacks.
*   **Record Relocation (REQ-TR-04):** Functionality to move records between GCIS and on-premises.
*   **High Availability (REQ-TR-05):** Active-active application server and DR capability are required.
*   **Monitoring and Alerting (REQ-TR-06):** A log server monitors system health and alerts administrators via email. Security audit logs are kept for 12 months.
*   **DR Drill (REQ-TR-07):**  DR drills are conducted to test disaster recovery procedures. Recovery Time Objective (RTO) is 1 day.
*   **Character Set Support (REQ-TR-08):** Supports UTF-8, Unicode, or ISO10646 Standard and Hong Kong Supplementary Character Set (HKSCS).
*   **System Logging (REQ-TR-09):** Records all functions, tasks, processes, and user actions. Logs are kept for at least 12 months.
*   **High Configurability (REQ-TR-10):** Avoid hard coding as much as possible.
*   **Backup and Recovery (REQ-TR-11):**
    *   Incremental backup daily.
    *   Full backup weekly.
    *   Full backups are kept for 6 months.
    *   Archive outdated information no more than twice per year.
*   **OS and Browser Compatibility (REQ-TR-12):** Supports various combinations of Windows, Mac OS X, Linux, iOS, and Android with browsers like Microsoft Edge, Safari, Mozilla Firefox, and Google Chrome.
*   **Privilege Management (REQ-TR-13):** Function to review and update user privileges.
*   **Health Check (REQ-TR-14):**  A health check function is available for system administrators.
*   **Encryption (REQ-TR-15):** All communication and data transfer are encrypted using HTTPS.
*   **Version Control (REQ-TR-16, REQ-TR-25):** Programming versioning and source code version control are maintained.
*   **Statistics (REQ-TR-17):** Monthly usage statistics and ad-hoc statistics are available.
*   **Language Support (REQ-TR-19):** Supports English, Traditional Chinese, and Simplified Chinese.
*   **System Performance Monitoring (REQ-TR-20, REQ-TR-21):**  System performance is periodically monitored, and reports/statistics can be generated.
*   **Content Updates (REQ-TR-22):** Authorized BD users can edit case information.
*   **Login and Authentication (REQ-TR-23, REQ-TR-24):** Refined login & authentication with full audit features. Username/password login available as a backup.
*   **Scalability (REQ-TR-27):** Scalable system frame design with High Availability (HA).
*   **Secure Data Exchange (REQ-TR-28):** Secure data exchange with other systems using HTTPS.
*   **Security Measurement (REQ-TR-29):** Security controls are implemented in application, network, and database layers.
*   **Email Notifications (REQ-TR-30, REQ-TR-31):** Email notifications for help checks and batch job completion.
*   **Interoperability Framework (REQ-TR-32):** Conforms to the Interoperability Framework (e.g., .Net 6).
*   **System Parameters Management (REQ-TR-33):** System parameters are placed in configuration files.
*   **Access Control (REQ-TR-34):** Allows system access by EDB and SWD, with user authorization control in SCS.
*   **Independence (REQ-TR-35):** Independent system, not dependent on other BD systems (except BCIS).
*   **Session Timeout (REQ-TR-36):** Automatic logout for inactive sessions (30 minutes for username/password login).
*   **Centralized Log Management (REQ-TR-37):** Log files are stored in a centralized folder.
*   **Single Sign-On (REQ-TR-38):** Handles around 300 user accounts of EDB and SWD for Single Sign On.
*   **Paperless (REQ-TR-39):** System aims to be paperless.
*   **PDF Letter Generation (REQ-TR-40):** Generates documents in PDF format using templates and field mapping.

## 4. Constraints

*   **Complexity of Address Identification:** Case creation may be passed to BCIS due to address identification complexity. Data will be sent back to SCS after creation in BCIS.
*   **Signature of AP/RSE:** Hand-written signatures on applications sent by post need to be verified manually by the Registry.

## 5. Appendices

*   **Appendix 1 ? 3-Tier BSR System:** (Image reference: `media/image15.emf`) - Diagram of the 3-Tier BSR System Architecture.
*   **Appendix 2 ? Sample of School and CCC Certificates and Notices:** (Image references: `media/image16.emf`, `media/image17.emf`) - Samples of certificates and notices related to schools and CCC.
*   **Appendix 3 ? Sample of Letter of Requirement (LoR):** (Image reference: `media/image18.emf`) - Sample of a Letter of Requirement.
*   **Appendix 4 ? Information Security Requirement:**  A list of information security requirements covering network security controls, endpoint protection, access controls, logging and monitoring, backup, and incident response.
*   **Appendix 5 ? Sample of Utilisation Report:** (Image reference: `media/image19.png`) - Sample of a utilization report.

## 6. Information Security Requirements (Appendix 4)

| \#   | Item                                                                                                                                                                                                                                            |
| :--- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Network security controls** |                                                                                                                                                                                                                                                 |
| 1    | Ensure all unnecessary services are disabled in the network devices (e.g. unnecessary ping traffic and requests from unauthorised network ports)                                                                                                |
| 2    | Ensure administrative consoles are not Internet-accessible and/or can only be accessible from trusted addresses.                                                                                                                                |
| 3    | Ensure networks are properly segregated so that critical and normal services can utilise different network connections.                                                                                                                         |
| 4    | Review firewall rules, intrusion detection and protection systems and remove obsolete rules or established connections, especially for temporary rules that may have been left beyond their expected lifetime.                                  |
| 5    | Review DDoS response plans including roles and responsibilities for various stakeholders (e.g. ISP and anti-DDoS service providers), internal procedures and escalation protocols etc.                                                          |
| 6    | Check that networks protected by a content delivery network (CDN) solution only allow incoming traffic from the specific source IP addresses of the CDN and the original Internet-facing IP addresses are not disclosed to unauthorised parties |
| **Endpoint protection** |                                                                                                                                                                                                                                                 |
| 7    | Ensure anti-malware software is installed and confirm that it is active on all systems and that signatures are updating correctly.                                                                                                              |
| 8    | Ensure the latest security patches are applied to the operating systems and applications, in particular for Internet-facing systems and websites.                                                                                               |
| **Access controls** |                                                                                                                                                                                                                                                 |
| 9    | Review user accounts and remove any obsolete accounts. If multi-factor authentication (MFA) is enabled, check if it is properly configured.                                                                                                     |
| 10   | Carefully review the user privileges and activities so as to identify and cease suspicious users from gaining unauthorised access.? Management may tighten user privilege and grant permissions only when strictly necessary.                   |
| 11   | Ensure strong password policy is adopted, in particular for all mission ciritical sytems and information systems containing classified data.                                                                                                    |
| **Logging and monitoring** |                                                                                                                                                                                                                                                 |
| 12   | Review the existing logging mechianism to ensure sufficient logs are retained.? For email systems and internet access service, ensure that your logs are kept for at least six months.?                                                         |
| 13   | Ensure all security solutions including intrusion detection/prevention system (IDPS) and web application firewall (WAF), are properly configured for identifying and reporting any suspicious activities.                                       |
| 14   | Ensure log records are in place with regular checking, especially for alerts generated by anti-malware and security solutions.??                                                                                                                |
| 15   | Allocate sufficient manpower and resources for monitoring and responding to potential cyber attacks.                                                                                                                                            |
| **Backup** |                                                                                                                                                                                                                                                 |
| 16   | Ensure backups of data and systems are reliable and secure.? Perform restoration tests from your backups to assure speedy system recovery.??                                                                                                    |
| 17   | Ensure multiple generations of offline backups are maintained and detached from the network and system.                                                                                                                                         |
| **Incident response** |                                                                                                                                                                                                                                                 |
| 18   | Review the existing incident response procedure is up to date and confirm that escalation routes and contact details are all up to date.                                                                                                        |
| 19   | Ensure the escalated incident response plan covers web defacement apart from typical cyber attacks.?                                                                                                                                            |
| 20   | Review the inventory list of the IT systems, important assets and keys for effective monitoring and resources management in emergency situations is up to date                                                                                  |

This document provides a comprehensive overview of the SCS system's requirements, constraints, and security considerations. It serves as a foundation for developing and maintaining the Computer Operation Procedures Manual.