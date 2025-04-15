# Computer Operation Procedures Manual - Analysis

This document summarizes the key information extracted from the provided text, focusing on system requirements, interfaces, technical specifications, constraints, and security considerations for the SCS (System) project.

## 1. System Overview

The document outlines the requirements for the SCS system, which appears to be a system used by the Building Department (BD) in conjunction with other systems like BCIS, BD Website, Minor Works Management System (MWMS), ESH, ERKS, and BRAVO. The system aims to manage AP/RSE data and related processes.  It will have both a front-end accessible via the internet and a back-end for internal BD users.

## 2. Functional Requirements

### 2.1. Interface Requirements (REQ-IR)

*   **REQ-IR-01: Interface with BCIS:**  The system needs to link to the DV tables of BCIS and conduct a study for easy retrieval of records, comparing data storage between SCS and BCIS.
*   **REQ-IR-02: Interface with BD Website:** The system should display a list of pre-accepted proprietary temporary structure data on the BD website.
*   **REQ-IR-03: Interface with Minor Works:** The system should provide an sFTP upload account for MWMS 2.0 to collect AP/RSE data (User Name, Registration Number, HKID, Expiry Date, etc.) on a daily basis.  SCS will host an sFTP server for this.  A departmental portal link will redirect to CRM of MWMS to view detailed AP/RSE information.
*   **REQ-IR-04: Interface with ESH:**  SCS will provide information and hyperlinks to ESH for viewing related case information and redirection to SCS.
*   **REQ-IR-05: Interface with ERKS:** e-Certificates, e-notices, reply letters, and other documents need to be imported into the ERKS system for record keeping.
*   **REQ-IR-06: Interface with BRAVO:** The system should redirect to BRAVO using a specified URL (<https://dp2.bd.hksarg/bravo/intranetSignOn>) and URL calls with parameters like CASE_NUMBER, YEAR, BLOCK_ID, SEARCH_TYPE, SUBJECT_CODE, and SPECIAL_CAT.

### 2.2. General Functional Requirements

*   Licensing nature enquiry.

## 3. Technical Requirements (REQ-TR)

The document details a comprehensive list of technical requirements, all with High priority unless otherwise noted.  These requirements are primarily targeted towards System Administrators.

*   **REQ-TR-01:** 24x7 Internet and Intranet availability.
*   **REQ-TR-02:** Integrated Cloud GCIS and On-Premises architecture.
*   **REQ-TR-03:** Input Validation to prevent security attacks (SQL Injection, DDOS). CAPTCHA for form submission.
*   **REQ-TR-04:** Record Relocation from GCIS to On-Premises functionality.
*   **REQ-TR-05:** High Availability (active-active application server, DR capability).
*   **REQ-TR-06:** Monitoring and Alert Generation (log server, email alerts, security audit logs for 12 months).
*   **REQ-TR-07:** DR Drill testing (Recovery Time Objective (RTO) of 1 day).
*   **REQ-TR-08:** UTF-8, Unicode, or HKSCS support.
*   **REQ-TR-09:** System Logging (functions, tasks, processes, user actions for at least 12 months).
*   **REQ-TR-10:** High Configurability (avoid hard coding).
*   **REQ-TR-11:** Backup and Recovery (daily incremental, weekly full, full backups kept for 6 months, archive outdated information no more than twice per year).
*   **REQ-TR-12:** Operation System and Browser Compatibility (Windows, Mac OS X, Linux, iOS, Android with Edge, Safari, Firefox, Chrome).
*   **REQ-TR-13:** Review and Update Privilege functionality.
*   **REQ-TR-14:** Health Check functionality (hyperlink for System Administration).
*   **REQ-TR-15:** Encryption on All Communications (HTTPS).
*   **REQ-TR-16:** Version Control for application (NA priority).
*   **REQ-TR-17:** Monthly Usage Statistics and Ad-hoc Statistics (SQL query execution, CSV export, Utilisation Survey, Active/Inactive User Account Report).
*   **REQ-TR-18:** Check-in and Check-out (NA priority).
*   **REQ-TR-19:** Language Support (EN/TC/SC).
*   **REQ-TR-20:** System Performance monitoring.
*   **REQ-TR-21:** Reports and statistics for monitor system performance.
*   **REQ-TR-22:** Ad-hoc and periodic updates on the contents (authorized BD users to edit case information, automatic record deletion).
*   **REQ-TR-23:** Refined Login & Authentication / FULL Audit features (login information recorded in audit and stored in database).
*   **REQ-TR-24:** Login user account login by user ID and password (backup login method if OSDP malfunctions).
*   **REQ-TR-25:** Version control of source code.
*   **REQ-TR-26:** System log tracking.
*   **REQ-TR-27:** Scalable system frame design (High Availability, ability to add nodes).
*   **REQ-TR-28:** Data exchange with other system securely (HTTPS).
*   **REQ-TR-29:** Security measurement (security in different layers).
*   **REQ-TR-30:** Help check email notification (internal BD and external GCIS email servers).
*   **REQ-TR-31:** Email notification for all batch jobs.
*   **REQ-TR-32:** Conform to the Interoperability Framework (.Net 6).
*   **REQ-TR-33:** Manage System Parameters (configuration files).
*   **REQ-TR-34:** Allow System Access by EDB and SWD (OSDP login, user authorization control in SCS).
*   **REQ-TR-35:** Independent System (Not depended on other BD system) (separate front-end and back-end, independent operation except for BCIS).
*   **REQ-TR-36:** Logout automatically for inactive for 30 minutes (SSO logout on ODSP, session termination for username/password login).
*   **REQ-TR-37:** Centralized log Management (centralized folder for log files).
*   **REQ-TR-38:** Handle around 300 user accounts of EDB and SWD for Single Sign On (concurrent user testing, ability to add nodes).
*   **REQ-TR-39:** Paper Less (generate and save documents).
*   **REQ-TR-40:** PDF template and mapping field for letter generation.

## 4. Constraints

*   **Complexity of Address Identification:**  Case creation may be passed to BCIS due to address identification complexity.
*   **Signature of AP/RSE:** Handwritten signatures on applications sent by post need to be verified by Registry using eyeball.

## 5. Security Considerations (Appendix 4)

The document includes a list of information security requirements covering:

*   **Network security controls:** Disabling unnecessary services, securing administrative consoles, network segregation, firewall rule review, DDoS response plans, CDN configuration.
*   **Endpoint protection:** Anti-malware software, security patches.
*   **Access controls:** User account review, privilege management, strong password policy.
*   **Logging and monitoring:** Sufficient log retention (at least six months for email and internet access), proper configuration of security solutions (IDPS, WAF), regular log checking.
*   **Backup:** Reliable and secure backups, restoration tests, multiple generations of offline backups.
*   **Incident response:** Up-to-date incident response procedure, web defacement coverage, inventory list of IT systems.

## 6. Infrastructure Information

*   **IP Address:** 12.1.2.172 (appears twice, suggesting a key server or service).

## 7. Appendices

The document references several appendices:

*   **Appendix 1:** 3-Tier BSR System (diagram).
*   **Appendix 2:** Sample of School and CCC Certificates and Notices (PDF examples).
*   **Appendix 3:** Sample of Letter of Requirement (LoR) (PDF example).
*   **Appendix 4:** Information Security Requirement (detailed list - summarized above).
*   **Appendix 5:** Sample of Utilisation Report (image).

## 8. Conclusion

This analysis provides a comprehensive overview of the requirements and constraints for the SCS system.  It highlights the importance of integration with other systems, robust technical specifications, and a strong focus on security.  The appendices provide valuable context and examples for the system's functionality.  Further investigation into the specific details of the referenced systems (BCIS, MWMS, ESH, ERKS, BRAVO, GCIS) would be beneficial for a more complete understanding.