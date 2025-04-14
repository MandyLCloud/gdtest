# Program Specification: Self-Certification System for the Buildings Department

## Introduction

This document merges information from various sources to provide a comprehensive program specification for the Self-Certification System (SCS) developed for the Buildings Department (BD). It covers the purpose, scope, functional and non-functional requirements, constraints, and technical details of the system.

## 1. Purpose

This document contains the detailed program specification of all programs used within the implementation of the Rates Exemption Information System (REIS) for the HAD.

## 2. Scope

This program specification provides information on the program codes and software modules produced in the Implementation of the REIS.

The SCS encompasses the following functionalities:

-   Capture of Rates Exemptions Application
-   Update and amend of Rates Exemption Application
-   Uploading of application file
-   Notification of urgent case of application and review
-   Checking and notification of outstanding case of application and review
-   Generation of Case Summary
-   Rates Exemption Application Endorsement
-   Generation of Minute list
-   File Approval of Exemption Application
-   Capture of Approved Case Review Information
-   Generation of Random Checking Case
-   Capture of Random Checking Case Results
-   Generation of Matching List Interface file
-   Capture of Matching List Checking Results
-   Generate Memo for application and review
-   Generate Batch Letters
-   Enquiry of Rates Exemption Application Information
-   Enquiry of Rates Exemption Review Case Information
-   Report Generation
-   Access Control
-   Update of System parameter
-   Update of System code table
-   Generation and enquiry of audit log

## 3. System Overview

The proposed Self-Certification System (SCS) allows Buildings Department (BD) users to receive, process and manage the application for certificates and notice required under Education Ordinance (Cap.279) and Child Care Services Ordinance (Cap. 243) for the registration of non-purpose built Educational Premises (EP) and Child Care Centre (CCC) and to provide building safety comment to Education Bureau upon applications for conducting courses of non-local higher and professional education under NLHPE(R) Rules (Cap.493B) respectively in an effective and efficient manner.

The system also allows applicant/Authorized Person (AP)/Registered Structure Engineer (RSE) or users in Social Welfare Department (SWD) and Education Bureau (EDB\*) to submit application forms and electronic documents to BD through internet/intranet in order to speed up the registration process.

Furthermore, the system is a single repository to store all applications and supporting documents that can facilitate BD users to find documents easily.

\* Including Joint Office for Kindergartens and Child Care Centres (JOKCCC) of Education Bureau

## 4. User Profiles

| No. | User Role | Responsibilities | Branch/Division/Section/Unit | Staff Post/Rank | Stakeholder Group |
|---|---|---|---|---|---|
| 1 | Applicant | Submit application form to BD | N/A | N/A | N/A |
| 2 | AP/RSE | Ensure building safety that meets BD?s requirements | N/A | N/A | N/A |
| 3 | EDB User | Submit application form to BD for EP | N/A | N/A | N/A |
| 4 | SWD/EDB(JOKCCC) User | Submit application form to BD for CCC | N/A | N/A | N/A |
| 5 | Registry | Data input to SCS | LU | Registry | BD |
| 6 | SE | Provide comment via SSE to BS | LU | SE | BD |
| 7 | SSE | Provide comment | LU | SSE | BD |
| 8 | SO | Perform site inspection and prepare inspection report | LU | SO | BD |
| 9 | BS | Check Building Safety Requirement (BSR) | LU | BS | BD |
| 10 | TO | Obtain structural information and report to SE | LU | TO | BD |
| 11 | SBS | Endorse and approve application | LU | SBS | BD |
| 12 | CBS | Endorse objection cases | LU | CBS | BD |
| 13 | System Admin | Perform system administration of SCS | ITU/MC | System Admin | BD |
| 14 | User Admin | Perform user administration of SCS | LU/ITU/EBD/SWD | User Admin | BD/EBD/SWD |

## 5. Functional Requirements

### General Requirements

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
| REQ-GR-01 | User Registration | Applicant/AP/RSE | NA |
| REQ-GR-02 | Login with Username & Password | Applicant/AP/RSE | NA |
| REQ-GR-03 | Registration and Login through iAM Smart | Applicant/AP/RSE | NA |
| REG-GR-04 | Change Password | Applicant/AP/RSE | NA |
| REG-GR-05 | Forget Password | Applicant/AP/RSE | NA |
| REG-GR-06 | Logout | Applicant/AP/RSE | NA |
| REQ-GR-07 | Single Sign On | BD Users/EDB User/ SWD User | H |
| REQ-GR-08 | Preview Document | All Users | H |
| REQ-GR-09 | Print Document | BD Users | H |
| REQ-GR-10 | Upload Document | BD Users/EDB User/SWD User/Applicant/AP/RSE | H |
| REQ-GR-11 | Management Statistics and Reports | BD Users | H |
| REQ-GR-12 | e-submission | Applicant/AP/RSE | H |
| REQ-GR-13 | e-processing | BD Users/EDB User/SWD User | H |
| REQ-GR-14 | e-tracking | All Users | H |
| REQ-GR-15 | Centralised data repository of the application supporting documents | BD Users/EDB User/SWD User/ | H |
| REQ-GR-16 | Search and Capture | BD Users/EDB User/SWD User/ | H |
| REQ-GR-17 | Handle new applications | BD Users/EDB User/SWD User/ | H |
| REQ-GR-18 | Handle alteration applications | BD Users/EDB User/SWD User/ | H |
| REQ-GR-19 | Handle Self Certification Submissions | BD Users | H |
| REQ-GR-20 | Handle Periodic Inspection for CCC | BD Users | H |
| REQ-GR-21 | Handle PTS for TPPE | BD Users | H |
| REQ-GR-22 | Data repository | BD Users | H |
| REQ-GR-23 | Easy retrieval of the records | BD Users | H |
| REQ-GR-24 | User and Delegation Administration | User Administrators of BD Users/EDB User/SWD User | H |
| REQ-GR-25 | Generate Application Number | Applicant | H |
| REQ-GR-26 | Withdraw Application | Applicant | H |

#### REQ-GR-07 Single Sign On

The system shall allow BD users, EDB users and SWD users to login the
system without inputting username and password once they logged in their
Open Source Departmental Portal (OSDP) through Government Backbone
Network (GNET). To logout the system, the users are required to logout
in OSDP.

| Users | Portal |
|---|---|
| BD Users | BD OSDP |
| EDB Users | EDB OSDP |
| SWD Users | SWD OSDP |

User administration account shall be created for EDB and SWD in order to
maintain their user accounts and access rights in SCS.

#### REQ-GR-08 Preview Document

The system shall allow logged on users to preview uploaded document in
browser. The document format should be in PDF format or image format
such as JPEG, PNG or TIFF.

#### REQ-GR-09 Print Document

The system shall allow BD users to print out various documents for
record keeping. The documents include:

1.  Application form
2.  Layout Plans
3.  Acknowledgment email
4.  Proforma
5.  Inspection Report
6.  Letter of Requirement
7.  Reply Letter, e-Certificates/ Certificates and
    e-Notice/Notice/Schedule of PTS for TPPE
8.  Others (i.e. S.J. Report, APP-13)
9.  Register of PTS for TPPE

#### REQ-GR-10 Upload Document

The system shall allow logged on users to upload documents including
layout plan, supporting documents?etc.

Virus scanning shall be performed for each uploaded file.

Plans shall be in flattened PDF format not larger than 25MB each and
digitally signed by Hongkong Post certificate or by iAM Smart. Total
files? size shall be within 100MB regardless the number of files. It is
configurable of maximum size of upload document.

#### REQ-GR-11 Management Statistics and Reports

The system shall allow BD users to generate statistics and reports for
School/CCC/PTS for TPPE on demand. The reports are:

1.  Total Received Cases
2.  Total Replied Cases
3.  Total Outstanding Cases
4.  Total Overdue Cases
5.  Total Audit Cases and corresponding results
6.  Total applications through e-submission and paper submission
7.  Total opted and Non-opt cases
8.  Total accepted and rejected PTS cases
9.  Outstanding cases with reminder
10. Performance report

The report layout and format could be refined in SA&D.

#### REQ-GR-12 e-submission

\(a\) Mobile-friendliness;

\(b\) Field validations such as field format and field limit checking;

\(c\) Cross-field validations;

\(d\) Conditional display;

\(e\) Form pre-filling function using iAM Smart, or with other
government backend systems where applicable;

\(f\) Single and multiple digital signatures using iAM Smart

\(g\) Single and multiple digital signatures using digital certificates
issued by recognised certification authorities in Hong Kong;
https://www.gov.hk/en/residents/communication/infosec/digitalcert.htm (
i.e. HK Post, Digi-Sign)

\(h\) Saving of filled-in forms for later completion e.g. multiple
digital signatures .

\(i\) provide Photo compression option for system administrator ;

\(j\) Form Version control and duplicate submission checking;

\(k\) Submission of attachment file(s) ( photo, form, plan, and
according to PNAD of BD ), with size control and digital signatures ;

\(l\) Creation of PDF form template and generation of PDF file with data
submitted by public users incorporated, serving as a record of the
submitted data, for reference by the submission party and users; send
application number to user via email and sms;

\(m\) Preparation of an Excel template, if needed, for each of the form
to facilitate users to extract form data to Excel for processing and
analysis. Technical know-how on producing the template file will be
provided at the start of the assignment ; and

\(n\) Form data encryption;

\(o\) Save draft application in GCIS for two weeks.

Support:

\(i\) Either e-Cert (Organizational) / e-Cert (Personal) issued by a
Recognized Certification Authority (currently Hong Kong Post
Certification Authority or Digi-Sign Certification Services Limited)
under the latest provisions of the Electronic Transaction Ordinance
(Cap. 553)

\(ii\) Certificate Standard: X.509v3

\(iii\) 2048-bit RSA key

\(iv\) In \*.p12 file format

#### REQ-GR-13 e-processing

The processing of application of new/alteration of EP/ CCC and Periodic
Inspection for CCC will be handled in Workflows by BD users. For
details, please refer to Workflow Requirements.

#### REQ-GR-14 e-tracking

The processing of application of new/alteration of EP/ CCC and Periodic
Inspection for CCC will be handled in Workflows by BD users. For
details, please refer to Workflow Requirements.

#### REQ-GR-15 Centralised data repository of the application supporting documents

The uploaded and generated documents will be stored in database and file
systems.

#### REQ-GR-16 Search and Capture

Please refer to REQ-WR-17.

#### REQ-GR-17 Handle new application

The workflow will handle new application for EP or CCC. For details,
please refer to workflow requirements.

#### REQ-GR-18 Handle alteration application

The workflow will handle alteration application for EP or CCC. For
details, please refer to workflow requirements.

#### REQ-GR-19 Handle Self Certification Submissions

The workflow will handle alteration application for EP or CCC. For
details, please refer to workflow requirements.

#### REQ-GR-20 Handle Periodic Inspection for CCC

The workflow will handle periodic inspection for CCC. For details,
please refer to workflow requirements.

#### REQ-GR-21 Handle PTS for TPPE

The workflow will handle update of PTS for TPPE. For details, please
refer to workflow requirements.

#### REQ-GR-22 Data repository

All data will be stored in centralized place i.e. Database and File
System (i.e. SAN)

#### REQ-GR-23 Easy retrieval of the records

The system provides a search function for BD users to look up case
information. For details, please refer to REQ-WR-17.

#### REQ-GR-24 User and Delegation Administration

The system provides administration to delegate task from one person to
another person for a certain period of time. During the delegation, the
tasks will be routed to delegated person instead of original person.

#### REQ-GR-25 Generate Application Number

The system shall generate an Application Number when applicant submits a
new licensing application for EP or CCC. The pattern of Application
Number will be:

YYYY(12 or 13)NNNN

YYYY ? 4 digits of the Year

12 ? for EP

13 ? for CCC

NNNN ? Sequence number in the Year

#### REQ-GR-26 Withdraw Application

The system shall allow applicant to withdraw application any time.

### Workflow Requirements

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
| REQ-WR-01 | Input Application Data | Registry | H |
| REQ-WR-02 | Create Structural Information Report | TO | H |
| REQ-WR-03 | Provide Comment via SSE | SE | H |
| REQ-WR-04 | Perform Site Inspection | SO | H |
| REQ-WR-05 | Building Safety Requirements Check | BS | H |
| REQ-WR-06 | Generate Reply Letter, e-Certificates and e-Notice | BS/SBS | H |
| REQ-WR-07 | Generate Letter of Requirement | BS/SBS | H |
| REQ-WR-08 | Endorse Application | SBS | H |
| REQ-WR-09 | Endorse Objection | CBS | H |
| REQ-WR-10 | AP/RSE Verification | Registry | H |
| REQ-WR-11 | Check Essential Documents | SO/BS | H |
| REQ-WR-12 | Digital Signing of Document | Applicant/AP/RSE/ BD Users | H |
| REQ-WR-13 | Random Audit Check | BD Users | H |
| REQ-WR-14 | Outstanding Application Alert | SO/TO/BS/SE/SSE/SBS | H |
| REQ-WR-15 | Input Application Form | Applicant | H |
| REQ-WR-16 | Input memo data | EDB/SWD | H |
| REQ-WR-17 | Search Case Information | BD Users | H |

#### REQ-WR-01 Input Application Data

The system shall allow registry to input application data and upload
scanned documents to the system when application is received by post.

Structural address with autocomplete function shall be provided,
including on Tradional Chinese and English.

#### REQ-WR-02 Create Structural Information Report

The system shall allow Technical Officer (TO) to create Structural
Information Report.

#### REQ-WR-03 Provide Comment via SSE

The system shall allow Senior Structural Engineer (SSE) to provide
comments about the application.

#### REQ-WR-04 Perform Site Inspection

The system shall allow Survey Officer (SO) to record Site Inspection,
retrieve approved plans from BRAVO and prepare / generate inspection
report. The Site Inspection data should include:

1.  Date of Site Inspection
2.  Site photo
3.  Others

Also, the system allows SO to draw annotation on PDF file of Layout Plan
and upload site photos.

#### REQ-WR-05 Building Safety Requirements Check

The system shall allow Building Surveyor (BS) to check the building
safety using 3-tier Building Safety Requirements (BSR) System.

#### REQ-WR-06 Generate Reply Letter, e-Certificates and e-Notice

When the application complies all building safety requirements, the
system shall generate Reply Letter, e-Certificates and e-Notices and
send to applicant or EDB/SWD users.

The documents are required to digitally signed by BD officer

#### REQ-WR-07 Generate Letter of Requirement

When the application is not fully complied to building safety
requirements, the system shall generate Letter of Requirement (LoR).

#### REQ-WR-08 Endorse Application

The system shall allow Senior Building Surveyor (SBS) to approve/reject
the application.

#### REQ-WR-09 Endorse Objection

The system shall allow Chief Building Surveyor (CBS) to approve/reject
the objection case. The objection case refers to Category 3 of 3-Tier
BSR system.

#### REQ-WR-10 AP/RSE Verification

The system shall verify the AP/RSE identity provided by Minor Works
Management System 2.0 (MWMS 2.0). The system should check the following
information of AP/RSE.

1.  User Name
2.  Registration Number
3.  Registration Status
4.  HKID
5.  Expiry Date
6.  Hand writing signature (for paper application)

The AP/RSE data will be synchronized from MWMS 2.0 on a daily basis.

#### REQ-WR-11 Check Essential Documents

The system shall allow Building Surveyor (BS) and Structural Engineer
(SE) to check whether all essential documents are submitted.

#### REQ-WR-12 Digital Signing of document

The system shall allow applicant or AP/RSE to digitally sign documents
using Hong Kong Post e-cert or iAM Smart app.

Also, the Reply Letter, e-Certificates and e-Notices will be digitally
signed using BD certificate.

#### REQ-WR-13 Random Audit Check

The system will immediately perform random audit check when the
certificates and notices are issued and allow BS to check the audit
items. The probability of random audit check is 60%, which is
configurable.

#### REQ-WR-14 Outstanding Application Alert

The system will send email notification to officer when application is
to be due/ overdue/ outstanding (i.e. no action after target complete
date) and the cases selected for audit.

#### REQ-WR-15 Input Application Form

The applicant/AP/RSE can submit application form, layout plans and other
documents for application of new/ alteration of EP and CCC. The
submitted documents will be digitally signed by Hong Kong Post e-Cert or
iAM Smart app. Once the application form is submitted, the system will
trigger a new workflow for internal BD users to handle the application.

#### REQ-WR-16 Input memo data

BD/EDB/SWD users can submit memo data including uploading documents in
SCS.

#### REQ-WR-17 Search Case Information

BD/SWD/EDB users can search all case information including uploaded
documents, BSR status?etc in SCS.

### Form Requirements

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
| REQ-FRM-1 | Verify certificate against the copy from Hong Kong post and DigiSign | System | H |
| REQ-FRM-2 | Route form to corresponding user | System | H |
| REQ-FRM-3 | Encrypt restricted data in the form | System | H |
| REQ-FRM-4 | Submit public form via online | System | H |
| REQ-FRM-5 | Extract data from form | System | H |
| REQ-FRM-6 | Store the extracted data in the database | System | H |
| REQ-FRM-7 | Search function for all record | System | H |
| REQ-FRM-8 | Auto-reply to acknowledge receiving the form | System | H |
| REQ-FRM-9 | Maintenance function of the form | System | H |
| REQ-FRM-10 | Resubmit the form data | System | H |
| REQ-FRM-11 | Update of the disclaimer of the forms | System | H |
| REQ-FRM-12 | Handle eform and Hardcopy form | System | H |

#### REQ-FRM-1 Verify certificate against the copy from Hong Kong Post and DigiSign 

The certificate to sign documents will be verified if the CA is from
Hong Kong Post and DigiSign. The other CA certificate will not be
accepted.

#### REQ-FRM-2 Route form to corresponding user

In the workflow, the case will be routed to delegated person base on
user mapping from BCIS.

#### REQ-FRM-3 Encrypt restricted data in the form

The system will encrypted classified data before storing in database and
handle up to Restricted Information.

#### REQ-FRM-4 Submit public form via online

Please refer to REQ-WR-15.

#### REQ-FRM-5 Extract data from form

All data of submitted form by applicant/AR/RSE will be saved in
database.

#### REQ-FRM-6 Store the extracted data in the database

All data of submitted form by applicant/AR/RSE will be saved in
database.

#### REQ-FRM-7 Search function for all record

Please refer to REQ-WR-16.

#### REQ-FRM-8 Auto-reply to acknowledge receiving the form

An acknowledge letter will be generated and send to application (for
1<sup>st</sup> submission only).

#### REQ-FRM-9 Maintenance function of the form.

In case the form data or layout is change, a Change Request will be made
in order to change coding.

#### REQ-FRM-10 Resubmit the form data

Applicant can re-submit the revised layout plan or other documents once
he receives LoR from BD.

#### REQ-FRM-11 Update of the disclaimer of the forms

The disclaimer of the forms can be directly updated in the program file
i.e. .aspx.

#### REQ-FRM-12 Handle eform and Hardcopy form

The system will handle e-form and hardcopy form submitted by applicant.

### From Processing Requirement

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
| REQ-PRO-1 | Verify CRM certification record | BD Users/EDB User/SWD User | H |
| REQ-PRO-2 | Reassign Case to other officer | BD Users/EDB User/SWD User | H |
| REQ-PRO-3 | Form status query | BD Users/EDB User/SWD User | H |
| REQ-PRO-4 | Automatically Bring up Outstanding Cases | BD Users/EDB User/SWD User | H |
| REQ-PRO-5 | To Do List | BD Users/EDB User/SWD User | H |
| REQ-PRO-6 | Case History Summary | BD Users/EDB User/SWD User | H |
| REQ-PRO-7 | Mark Notes and remark for internal use. | BD Users/EDB User/SWD User | H |
| REQ-PRO-8 | Re-direct to BCIS for case checking | BD Users | H |
| REQ-PRO-9 | Handle upload soft-copy | BD Users/EDB User/SWD User | H |
| REQ-PRO-10 | Export outstanding case | BD Users/EDB User/SWD User | H |
| REQ-PRO-11 | Handle referral Case | BD Users/EDB User/SWD User | H |

#### REQ-PRO-1 Verify CRM certification record

The system will automatically verify AP/RSE information against CRM
record. However, if paper application, BD user i.e. Registry is required
to manually verify the handwriting signature and other data of AP/RSE.

#### REQ-PRO-2 Reassign Case to other officer

The assigned task can be re-assigned to another person in ad-hoc by
system administrator.

#### REQ-PRO-3 Form status query

Please refer to REQ-WR-17.

#### REQ-PRO-4 Automatically Bring up Outstanding Cases

Please refer to REQ-WR-14.

#### REQ-PRO-5 To Do List

The system provides a tasks list i.e. to-do list for all BD users to
handle the case in the workflow.

#### REQ-PRO-6 Case History Summary

Please refer to REQ-WF-17

#### REQ-PRO-7 Mark notes and remark for internal use.

The workflow provides comments or notes to BD users to handle the case.

#### REQ-PRO-8 Re-direct to BCIS for case checking

There will be a hyperlink to BCIS to see the case information when the
case is save in BCIS.

#### REQ-PRO-9 Handle upload soft copy

All uploaded documents will be saved in centralised file system.

#### REQ-PRO-10 Export outstanding case

Please refer to REQ-GR-11.

#### REQ-PRO-11 Handle referral Case

Please refer to REQ-WR-16.

## 6. Non-Functional Requirements

### Communication Requirements

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
| REQ-CR-01 | SMS Alert | All Users | H |
| REQ-CR-02 | Email Notification | All Users | H |
| REQ-CR-03 | Fax Copy of LoR, Certificates, and Notice | All Users | H |

#### REQ-CR-01 SMS Alert

The system shall send SMS alert to users through-out the workflow. Here
are scenarios to send out SMS and their contents.

-   As an acknowledgement of each form submission;
-   Notification of LoR issued;
-   Notification of Certificate and Notice issued.

#### REQ-CR-02 Email Notification

The system shall send Email notification to users through-out the
workflow. Here are scenarios to send out Email and their contents.

-   As an acknowledgement of each form submission;
-   Notification of LoR issued;
-   Notification of Certificate and Notice issued.
-   Reminder to AP/RSE for o/s audit case.

#### REQ-CR-03 Fax Copy of LoR, Certificates, and Notice

The system shall send the LoR, Certificates, and Notice to applicant
through Fax.

### Webpage Requirements

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
| REQ-UR-01 | Common Look & Feel | All Users | H |
| REQ-UR-02 | W3C WCAG 2.1 | All Users | H |
| REQ-UR-03 | Privacy Disclaimer | All Users | H |
| REQ-UR-04 | Assistive Technology Testing | All Users | H |

#### REQ-UR-01 Common Look & Feel

The system shall conform design and guideline of Common Look & Feel
(CLF) of the HKSAR government.

Ensure SCS conforming to the latest version of the Common Look & Feel
(CLF), Mobile Friendly and Web Accessibility standard. The responsive
web / mobile friendly design shall allow the contents of SCS be adapted
to different layouts in a real-time manner in response to the different
screen sizes and resolutions

The design shall comply with the latest version of the CLF and conform
to the W3C HTML5 standard for details to better support modern browsers
or mobile devices, i.e. a responsive web design. The Contractor shall
ensure all web pages of SCS shall be compatible with popular web
browsers, operating systems, screen readers, etc.

For details, please refer to
<https://itginfo.ccgo.hksarg/content/clf/home.html>

#### REQ-UR-02 W3C WCAG 2.1

The system shall conform to W3C WCAG 2.1 Level AA standard to facilitate
access by people of disabilities. Various testing will be done
including:

1.  Code scanning ? Detect any non-conformance to WCAG 2.1 Level AA
    standard by using well-known software tools;
2.  Visual review ? Verify the accessibility by visual browsing and by
    automatic tool to reveal any accessibility problems, including but
    not limited to insufficient colour contrast, keyboard traps, too
    small font size, etc.;
3.  Assistive Technology (AT) tools testing ? Test SCS with AT tools
    such as screen readers, screen magnifiers and voice controls;
4.  Human testing - perform visual review on desktop and mobile
    versions;

For more details, please refer to
<https://www.ogcio.gov.hk/en/our_work/community/web_mobileapp_accessibility/promulgating_resources/handbook/>

#### REQ-UR-03 Privacy Disclaimer

The system shall provide a privacy disclaimer in website in order to
conform to Personal Data (Privacy) Ordinance (Cap 486).

#### REQ-UR-04 Assistive Technology Testing

To conform W3C WCAG 2.1 Level AA standard, a set of tools such as screen
readers, screen magnifiers and voice controls will be used for the
testing.

### Security Requirements

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
| REQ-SR-01 | SRAA | System Admin | H |
| REQ-SR-02 | PIA and PCA | System Admin | H |
| REQ-SR-03 | Encryption and Decryption of Classified Data | System Admin | H |
| REQ-SR-04 | System Audit | System Admin | H |
| REQ-SR-05 | System Control | System Admin | H |

#### REQ-SR-01 SRAA

Security Risk Assessment Audit (SRAA) exercise will be executed in order
to address all security issues. All vulnerabilities found and necessary
safeguards recommended by Security Auditors should be fixed and
implemented accordingly.

#### REQ-SR-02 PIA and PCA

Privacy Impact Assessment (PIA) and Privacy Compliance Audit (PCA) will
be executed in order to address all privacy issues. All vulnerabilities
found and necessary safeguards recommended by Auditors should be fixed
and implemented accordingly.

#### REQ-SR-03 Encryption and Decryption of Classified Data

All classified data such as HKID will be encrypted during transmission
or stored in file system or database. The encryption and decryption
should use strong symmetric encryption algorithms such as AES 256bit or
use Hash function such as SHA-256.

#### REQ-SR-04 System Audit

Important events such as create case, login?etc will be logged and
stored in database for auditing purpose

#### REQ-SR-05 System Control

The security control to access to the system will be guarded using tools
such as Firewall, network control, physical access control..etc.

### Interface Requirements

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
| REQ-IR-01 | Interface with BCIS | System Admin | H |
| REQ-IR-02 | Interface with BD Website | System Admin | H |
| REQ-IR-03 | Interface with Minor Works | System Admin | H |
| REQ-IR-04 | Interface with ESH | System Admin | H |
| REQ-IR-05 | Interface with ERKS | System Admin | H |
| REQ-IR-06 | Interface with BRAVO | System Admin | H |

#### REQ-IR-01 Interface with BCIS

The system shall provide interfaces with BCIS in order to complete
certain tasks. The interfaces include:

1.  Receive list of address, file reference or other master data from
    BCIS to facilitate creation of case on a daily basis
2.  Send application data to BCIS to create case using stored procedures
    provided by BCIS in batch (To be confirmed)
3.  Update application date to BCIS using stored procedures provided by
    BCIS
4.  A reference link from the two systems of SCS and BCIS
5.  Transfer data from SCS to BCIS for statistics report
6.  Select block for create new address in BCIS by to-do-list and email
7.  Handling all input and edit 12 and 13 file Licensing case in SCS
    instead of BCIS
8.  Mapping with BCIS users such as User name, Post, File reference, DP
    login id, case officer
9.  Including Licensing nature Enquire
10. Link to DV tables of BCIS
11. Conduct a detailed study for easy retrieval of the records from SCS
    by comparing data storage against a reference link from the two
    systems of SCS and BCIS, and determine a solution most suited to
    user requirements.

#### REQ-IR-02 Interface with BD Website

The system shall display list of Pre-accepted Proprietary Temporary
structure data in BD website.

#### REQ-IR-03 Interface with Minor Works

The system shall provide sFTP upload account to MWMS 2.0 in order to
collect AP/RSE data such as User Name, Registration Number, HKID, Expiry
Date, etc on a daily basis. SCS will setup a sFTP server in order to
receive AP/RSE data and update database accordingly.

The SCS system can use Departmental Portal link to redirect to CRM of
MWMS to view the detail AP/RSE information as same as ESH.

#### REQ-IR-04 Interface with ESH

Case of information and hyper link of SCS will be provided to ESH to
view relating case information and redirect to SCS respectively.

#### REQ-IR-05 Interface with ERKS

The e-Certificates, e-notices, reply letter and other documents are
required to import into ERKS system for record keeping. The detailed
interface specification and implementation will be done in SM&S stage.

#### REQ-IR-06 Interface with BRAVO

The SCS system can use <https://dp2.bd.hksarg/bravo/intranetSignOn> to
redirect to BRAVO.

Also, the SCS system could be redirected to BRAVO through a URL call
with specified parameters. For example:
https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?
CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>

**<u>The URL syntax for reference:</u>**

\< Departmental Portal URL**\>/**bravo/BuildingSearchRedirection?

The following parameters shall be redirected from SCS to Intranet BRAVO
through URL GET/POST parameter passing.

**<u>with Case number and Year</u>**

CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>

**<u>with Block ID</u>**

BLOCK_ID=\<BLOCK_ID\>

**<u>with full File Reference No</u>**

SEARCH_TYPE=\<SEARCH_TYPE\>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT\>

### Technical Requirements

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
| REQ-TR-01 | 24x7 Internet and Intranet | System Admin | H |
| REQ-TR-02 | Integrated Cloud GCIS and On Premises | System Admin |