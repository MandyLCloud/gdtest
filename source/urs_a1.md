<img src="media/image1.jpg" style="width:1.30903in;height:1.30903in" />

**User Requirements Specifications (T223)**

**of**

**Category 3, Minor Group –**

**Combined System Development Services for**

**Self-Certification System**

**for the Buildings Department**

Version: 1.1

**Nov 2022**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 86%" />
</colgroup>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Distribution</strong></td>
</tr>
<tr class="even">
<td>Copy No.</td>
<td>Holder</td>
</tr>
<tr class="odd">
<td>1</td>
<td><blockquote>
<p>Buildings Department (BD)</p>
</blockquote></td>
</tr>
<tr class="even">
<td>2</td>
<td><blockquote>
<p>Master Concept (Hong Kong) Limited</p>
</blockquote></td>
</tr>
</tbody>
</table>

|                       |                      |                                      |                           |           |                    |
|----------|-------------------------|---------|---------|---------|-----------|
| **Amendment History** |                      |                                      |                           |           |                    |
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date      | Approval Reference |
| 1                     | First draft          | N/A                                  | 0.1                       | 19/5/2022 |                    |
|                       |                      |                                      |                           |           |                    |
| 2                     | Second draft         | All                                  | 0.2                       | 21/6/2022 |                    |
|                       |                      |                                      |                           |           |                    |
| 3                     | Third draft          | All                                  | 0.3                       | 20/7/2022 |                    |
|                       |                      |                                      |                           |           |                    |
| 4                     | Fourth draft         | All                                  | 0.4                       | 9/8/2022  |                    |
|                       |                      |                                      |                           |           |                    |
| 5                     | Fair Version         | All                                  | 1.0                       | 30/8/2022 |                    |
|                       |                      |                                      |                           |           |                    |
| 6                     | Release              | All                                  | 1.1                       | 8/11/2022 |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |

**TABLE OF CONTENTS**

# 

[1 USER REQUIREMENTS [1](#user-requirements)](#user-requirements)

[1.1 PROPOSED SYSTEM OVERVIEW
[1](#proposed-system-overview)](#proposed-system-overview)

[1.1.1 DESCRIPTION OF PROPOSED SYSTEM
[1](#description-of-proposed-system)](#description-of-proposed-system)

[1.1.2 SYSTEM USER PROFILE
[3](#system-user-profile)](#system-user-profile)

[1.2 FUTURE BUSINESS PROCESS
[4](#future-business-process)](#future-business-process)

[1.2.1 LIST OF FUTURE BUSINESS PROCESS
[4](#list-of-future-business-process)](#list-of-future-business-process)

[1.2.1.1 Application for e-Certificates and e-Notice for EP
(e-application)
[6](#application-for-e-certificates-and-e-notice-for-ep-e-application)](#application-for-e-certificates-and-e-notice-for-ep-e-application)

[1.2.1.2 Application for Alteration for EP/CCC (e-application)
[7](#application-for-alteration-for-epccc-e-application)](#application-for-alteration-for-epccc-e-application)

[1.2.1.3 Application for Certificates and Notice for EP (paper
application)
[9](#application-for-certificates-and-notice-for-ep-paper-application)](#application-for-certificates-and-notice-for-ep-paper-application)

[1.2.1.4 Application for Alteration for EP/CCC (paper application)
[10](#application-for-alteration-for-epccc-paper-application)](#application-for-alteration-for-epccc-paper-application)

[1.2.1.5 Random Audit Check [12](#_Toc118379690)](#_Toc118379690)

[1.2.1.6 Application for Approval for use of the premises for conducting
course under the Non-Local-Higher and Professional Education
(Regulation) Ordinance \[NLHP(R)O\] (e-application)
[13](#application-for-approval-for-use-of-the-premises-for-conducting-course-under-the-non-local-higher-and-professional-education-regulation-ordinance-nlhpro-e-application)](#application-for-approval-for-use-of-the-premises-for-conducting-course-under-the-non-local-higher-and-professional-education-regulation-ordinance-nlhpro-e-application)

[1.2.1.7 Application for Approval for use of the premises for conducting
course under the Non-Local-Higher and Professional Education
(Regulation) Ordinance \[NLHP(R)O\] (paper application)
[14](#application-for-approval-for-use-of-the-premises-for-conducting-course-under-the-non-local-higher-and-professional-education-regulation-ordinance-nlhpro-paper-application)](#application-for-approval-for-use-of-the-premises-for-conducting-course-under-the-non-local-higher-and-professional-education-regulation-ordinance-nlhpro-paper-application)

[1.2.1.8 Application for Periodic Inspection for CCC
[15](#application-for-periodic-inspection-for-ccc)](#application-for-periodic-inspection-for-ccc)

[1.2.1.9 Application for inclusion of Temporary Structures in the
Pre-accepted Temporary Structure (PTS) Register for user under TPPE
license
[16](#application-for-inclusion-of-temporary-structures-in-the-pre-accepted-temporary-structure-pts-register-for-user-under-tppe-license)](#application-for-inclusion-of-temporary-structures-in-the-pre-accepted-temporary-structure-pts-register-for-user-under-tppe-license)

[1.3 FUNCTIONAL REQUIREMENTS
[17](#functional-requirements)](#functional-requirements)

[1.3.1 LIST OF FUNCTIONAL REQUIREMENTS
[17](#list-of-functional-requirements)](#list-of-functional-requirements)

[1.3.1.1 REQ-GR-01 User Registration
[20](#req-gr-01-user-registration)](#req-gr-01-user-registration)

[1.3.1.2 REQ-GR-02 Login with Username & Password
[20](#req-gr-02-login-with-username-password)](#req-gr-02-login-with-username-password)

[1.3.1.3 REQ-GR-03 Login through iAM Smart
[21](#req-gr-03-login-through-iam-smart)](#req-gr-03-login-through-iam-smart)

[1.3.1.4 REQ-GR-04 Change Password
[21](#req-gr-04-change-password)](#req-gr-04-change-password)

[1.3.1.5 REQ-GR-05 Forget Password
[21](#req-gr-05-forget-password)](#req-gr-05-forget-password)

[1.3.1.6 REQ-GR-06 Logout [22](#req-gr-06-logout)](#req-gr-06-logout)

[1.3.1.7 REQ-GR-07 Single Sign On
[22](#req-gr-07-single-sign-on)](#req-gr-07-single-sign-on)

[1.3.1.8 REQ-GR-08 Preview Document
[23](#req-gr-08-preview-document)](#req-gr-08-preview-document)

[1.3.1.9 REQ-GR-09 Print Document
[23](#req-gr-09-print-document)](#req-gr-09-print-document)

[1.3.1.10 REQ-GR-10 Upload Document
[24](#req-gr-10-upload-document)](#req-gr-10-upload-document)

[1.3.1.11 REQ-GR-11 Management Statistics and Reports
[24](#req-gr-11-management-statistics-and-reports)](#req-gr-11-management-statistics-and-reports)

[1.3.1.12 REQ-GR-12 e-submission
[25](#req-gr-12-e-submission)](#req-gr-12-e-submission)

[1.3.1.13 REQ-GR-13 e-processing
[26](#req-gr-13-e-processing)](#req-gr-13-e-processing)

[1.3.1.14 REQ-GR-14 e-tracking
[27](#req-gr-14-e-tracking)](#req-gr-14-e-tracking)

[1.3.1.15 REQ-GR-15 Centralised data repository of the application
supporting documents
[27](#req-gr-15-centralised-data-repository-of-the-application-supporting-documents)](#req-gr-15-centralised-data-repository-of-the-application-supporting-documents)

[1.3.1.16 REQ-GR-16 Search and Capture
[27](#req-gr-16-search-and-capture)](#req-gr-16-search-and-capture)

[1.3.1.17 REQ-GR-17 Handle new application
[28](#req-gr-17-handle-new-application)](#req-gr-17-handle-new-application)

[1.3.1.18 REQ-GR-18 Handle alteration application
[28](#req-gr-18-handle-alteration-application)](#req-gr-18-handle-alteration-application)

[1.3.1.19 REQ-GR-19 Handle Self Certification Submissions
[29](#req-gr-19-handle-self-certification-submissions)](#req-gr-19-handle-self-certification-submissions)

[1.3.1.20 REQ-GR-20 Handle Periodic Inspection for CCC
[29](#req-gr-20-handle-periodic-inspection-for-ccc)](#req-gr-20-handle-periodic-inspection-for-ccc)

[1.3.1.21 REQ-GR-21 Handle PTS for TPPE
[29](#req-gr-21-handle-pts-for-tppe)](#req-gr-21-handle-pts-for-tppe)

[1.3.1.22 REQ-GR-22 Data repository
[30](#req-gr-22-data-repository)](#req-gr-22-data-repository)

[1.3.1.23 REQ-GR-23 Easy retrieval of the records
[30](#req-gr-23-easy-retrieval-of-the-records)](#req-gr-23-easy-retrieval-of-the-records)

[1.3.1.24 REQ-GR-24 User and Delegation Administration
[31](#req-gr-24-user-and-delegation-administration)](#req-gr-24-user-and-delegation-administration)

[1.3.1.25 REQ-GR-25 Generate Application Number
[31](#req-gr-25-generate-application-number)](#req-gr-25-generate-application-number)

[1.3.1.26 REQ-GR-26 Withdraw Application
[32](#req-gr-26-withdraw-application)](#req-gr-26-withdraw-application)

[1.3.1.27 REQ-WR-01 Input Application Data
[32](#req-wr-01-input-application-data)](#req-wr-01-input-application-data)

[1.3.1.28 REQ-WR-02 Create Structural Information Report
[32](#req-wr-02-create-structural-information-report)](#req-wr-02-create-structural-information-report)

[1.3.1.29 REQ-WR-03 Provide Comment via SSE
[33](#req-wr-03-provide-comment-via-sse)](#req-wr-03-provide-comment-via-sse)

[1.3.1.30 REQ-WR-04 Perform Site Inspection
[33](#req-wr-04-perform-site-inspection)](#req-wr-04-perform-site-inspection)

[1.3.1.31 REQ-WR-05 Building Safety Requirements Check
[34](#req-wr-05-building-safety-requirements-check)](#req-wr-05-building-safety-requirements-check)

[1.3.1.32 REQ-WR-06 Generate Reply Letter, e-Certificates and e-Notice
[34](#req-wr-06-generate-reply-letter-e-certificates-and-e-notice)](#req-wr-06-generate-reply-letter-e-certificates-and-e-notice)

[1.3.1.33 REQ-WR-07 Generate Letter of Requirement
[35](#req-wr-07-generate-letter-of-requirement)](#req-wr-07-generate-letter-of-requirement)

[1.3.1.34 REQ-WR-08 Endorse Application
[35](#req-wr-08-endorse-application)](#req-wr-08-endorse-application)

[1.3.1.35 REQ-WR-09 Endorse Objection
[35](#req-wr-09-endorse-objection)](#req-wr-09-endorse-objection)

[1.3.1.36 REQ-WR-10 AP/RSE Verification
[36](#req-wr-10-aprse-verification)](#req-wr-10-aprse-verification)

[1.3.1.37 REQ-WR-11 Check Essential Documents
[36](#req-wr-11-check-essential-documents)](#req-wr-11-check-essential-documents)

[1.3.1.38 REQ-WR-12 Digital Signing of document
[37](#req-wr-12-digital-signing-of-document)](#req-wr-12-digital-signing-of-document)

[1.3.1.39 REQ-WR-13 Random Audit Check
[37](#req-wr-13-random-audit-check)](#req-wr-13-random-audit-check)

[1.3.1.40 REQ-WR-14 Outstanding Application Alert
[37](#req-wr-14-outstanding-application-alert)](#req-wr-14-outstanding-application-alert)

[1.3.1.41 REQ-WR-15 Input Application Form
[38](#req-wr-15-input-application-form)](#req-wr-15-input-application-form)

[1.3.1.42 REQ-WR-16 Input memo data
[38](#req-wr-16-input-memo-data)](#req-wr-16-input-memo-data)

[1.3.1.43 REQ-WR-17 Search Case Information
[39](#req-wr-17-search-case-information)](#req-wr-17-search-case-information)

[1.3.1.44 REQ-FRM-1 Verify certificate against the copy from Hong Kong
Post and DigiSign
[39](#req-frm-1-verify-certificate-against-the-copy-from-hong-kong-post-and-digisign)](#req-frm-1-verify-certificate-against-the-copy-from-hong-kong-post-and-digisign)

[1.3.1.45 REQ-FRM-2 Route form to corresponding user
[39](#req-frm-2-route-form-to-corresponding-user)](#req-frm-2-route-form-to-corresponding-user)

[1.3.1.46 REQ-FRM-3 Encrypt restricted data in the form
[40](#req-frm-3-encrypt-restricted-data-in-the-form)](#req-frm-3-encrypt-restricted-data-in-the-form)

[1.3.1.47 REQ-FRM-4 Submit public form via online
[40](#req-frm-4-submit-public-form-via-online)](#req-frm-4-submit-public-form-via-online)

[1.3.1.48 REQ-FRM-5 Extract data from form
[41](#req-frm-5-extract-data-from-form)](#req-frm-5-extract-data-from-form)

[1.3.1.49 REQ-FRM-6 Store the extracted data in the database
[41](#req-frm-6-store-the-extracted-data-in-the-database)](#req-frm-6-store-the-extracted-data-in-the-database)

[1.3.1.50 REQ-FRM-7 Search function for all record
[41](#req-frm-7-search-function-for-all-record)](#req-frm-7-search-function-for-all-record)

[1.3.1.51 REQ-FRM-8 Auto reply to acknowledge receiving the form
[42](#req-frm-8-auto-reply-to-acknowledge-receiving-the-form)](#req-frm-8-auto-reply-to-acknowledge-receiving-the-form)

[1.3.1.52 REQ-FRM-9 Maintenance function of the form.
[42](#req-frm-9-maintenance-function-of-the-form.)](#req-frm-9-maintenance-function-of-the-form.)

[1.3.1.53 REQ-FRM-10 Resubmit the form data
[42](#req-frm-10-resubmit-the-form-data)](#req-frm-10-resubmit-the-form-data)

[1.3.1.54 REQ-FRM-11 Update of the disclaimer of the forms
[43](#req-frm-11-update-of-the-disclaimer-of-the-forms)](#req-frm-11-update-of-the-disclaimer-of-the-forms)

[1.3.1.55 REQ-FRM-12 Handle e-form and hardcopy form
[43](#req-frm-12-handle-e-form-and-hardcopy-form)](#req-frm-12-handle-e-form-and-hardcopy-form)

[1.3.1.56 REQ-PRO-1 Verify CRM certification record
[43](#req-pro-1-verify-crm-certification-record)](#req-pro-1-verify-crm-certification-record)

[1.3.1.57 REQ-PRO-2 Reassign case to other officer
[44](#req-pro-2-reassign-case-to-other-officer)](#req-pro-2-reassign-case-to-other-officer)

[1.3.1.58 REQ-PRO-3 Form status query
[44](#req-pro-3-form-status-query)](#req-pro-3-form-status-query)

[1.3.1.59 REQ-PRO-4 Automatically bring up outstanding cases.
[45](#req-pro-4-automatically-bring-up-outstanding-cases.)](#req-pro-4-automatically-bring-up-outstanding-cases.)

[1.3.1.60 REQ-PRO-5 To-Do List
[45](#req-pro-5-to-do-list)](#req-pro-5-to-do-list)

[1.3.1.61 REQ-PRO-6 Case History Summary
[45](#req-pro-6-case-history-summary)](#req-pro-6-case-history-summary)

[1.3.1.62 REQ-PRO-7 Mark notes and remark for internal use.
[46](#req-pro-7-mark-notes-and-remark-for-internal-use.)](#req-pro-7-mark-notes-and-remark-for-internal-use.)

[1.3.1.63 REQ-PRO-8 Re-direct to BCIS for case checking
[46](#req-pro-8-re-direct-to-bcis-for-case-checking)](#req-pro-8-re-direct-to-bcis-for-case-checking)

[1.3.1.64 REQ-PRO-9 Handle upload soft copy
[46](#req-pro-9-handle-upload-soft-copy)](#req-pro-9-handle-upload-soft-copy)

[1.3.1.65 REQ-PRO-10 Export outstanding case
[47](#req-pro-10-export-outstanding-case)](#req-pro-10-export-outstanding-case)

[1.3.1.66 REQ-PRO-11 Handle referral case
[47](#req-pro-11-handle-referral-case)](#req-pro-11-handle-referral-case)

[1.4 NON-FUNCTIONAL REQUIREMENTS
[48](#non-functional-requirements)](#non-functional-requirements)

[1.4.1 LIST OF NON-FUNCTIONAL REQUIREMENTS
[48](#list-of-non-functional-requirements)](#list-of-non-functional-requirements)

[1.4.1.1 REQ-CR-01 SMS Alert
[48](#req-cr-01-sms-alert)](#req-cr-01-sms-alert)

[1.4.1.2 REQ-CR-02 Email Notification
[49](#req-cr-02-email-notification)](#req-cr-02-email-notification)

[1.4.1.3 REQ-CR-03 Fax Copy of LoR, Certificates, and Notice
[49](#req-cr-03-fax-copy-of-lor-certificates-and-notice)](#req-cr-03-fax-copy-of-lor-certificates-and-notice)

[1.4.1.4 REQ-UR-01 Common Look & Feel
[49](#req-ur-01-common-look-feel)](#req-ur-01-common-look-feel)

[1.4.1.5 REQ-UR-02 W3C WCAG 2.1
[50](#req-ur-02-w3c-wcag-2.1)](#req-ur-02-w3c-wcag-2.1)

[1.4.1.6 REQ-UR-03 Privacy Disclaimer
[51](#req-ur-03-privacy-disclaimer)](#req-ur-03-privacy-disclaimer)

[1.4.1.7 REQ-UR-04 Assistive Technology Testing
[52](#req-ur-04-assistive-technology-testing)](#req-ur-04-assistive-technology-testing)

[1.4.1.8 REQ-SR-01 SRAA [52](#req-sr-01-sraa)](#req-sr-01-sraa)

[1.4.1.9 REQ-SR-02 PIA and PCA
[52](#req-sr-02-pia-and-pca)](#req-sr-02-pia-and-pca)

[1.4.1.10 REQ-SR-03 Encryption and Decryption of Classified Data
[53](#req-sr-03-encryption-and-decryption-of-classified-data)](#req-sr-03-encryption-and-decryption-of-classified-data)

[1.4.1.11 REQ-SR-04 System Audit
[53](#req-sr-04-system-audit)](#req-sr-04-system-audit)

[1.4.1.12 REQ-SR-05 System Control
[54](#req-sr-05-system-control)](#req-sr-05-system-control)

[1.4.1.13 REQ-IR-01 Interface with BCIS
[54](#req-ir-01-interface-with-bcis)](#req-ir-01-interface-with-bcis)

[1.4.1.14 REQ-IR-02 Interface with BD Website
[55](#req-ir-02-interface-with-bd-website)](#req-ir-02-interface-with-bd-website)

[1.4.1.15 REQ-IR-03 Interface with Minor Works
[55](#req-ir-03-interface-with-minor-works)](#req-ir-03-interface-with-minor-works)

[1.4.1.16 REQ-IR-04 Interface with ESH
[56](#req-ir-04-interface-with-esh)](#req-ir-04-interface-with-esh)

[1.4.1.17 REQ-IR-05 Interface with ERKS
[56](#req-ir-05-interface-with-erks)](#req-ir-05-interface-with-erks)

[1.4.1.18 REQ-IR-06 Interface with BRAVO
[56](#req-ir-06-interface-with-bravo)](#req-ir-06-interface-with-bravo)

[1.5 TECHNICAL REQUIREMENTS
[57](#technical-requirements)](#technical-requirements)

[1.5.1 LIST OF TECHNICAL REQUIREMENTS
[57](#list-of-technical-requirements)](#list-of-technical-requirements)

[1.5.1.1 REQ-TR-01 24x7 Internet and Intranet
[59](#req-tr-01-24x7-internet-and-intranet)](#req-tr-01-24x7-internet-and-intranet)

[1.5.1.2 REQ-TR-02 Integrated Cloud GCIS and On Premises
[59](#req-tr-02-integrated-cloud-gcis-and-on-premises)](#req-tr-02-integrated-cloud-gcis-and-on-premises)

[1.5.1.3 REQ-TR-03 Input Validation
[59](#req-tr-03-input-validation)](#req-tr-03-input-validation)

[1.5.1.4 REQ-TR-04 Record Relocation from GCIS to On Premises
[60](#req-tr-04-record-relocation-from-gcis-to-on-premises)](#req-tr-04-record-relocation-from-gcis-to-on-premises)

[1.5.1.5 REQ-TR-05 High Availability
[60](#req-tr-05-high-availability)](#req-tr-05-high-availability)

[1.5.1.6 REQ-TR-06 Monitoring and Alert Generation
[61](#req-tr-06-monitoring-and-alert-generation)](#req-tr-06-monitoring-and-alert-generation)

[1.5.1.7 REQ-TR-07 DR Drill
[61](#req-tr-07-dr-drill)](#req-tr-07-dr-drill)

[1.5.1.8 REQ-TR-08 UTF-8, Unicode or HKSCS
[61](#req-tr-08-utf-8-unicode-or-hkscs)](#req-tr-08-utf-8-unicode-or-hkscs)

[1.5.1.9 REQ-TR-09 System Logging
[62](#req-tr-09-system-logging)](#req-tr-09-system-logging)

[1.5.1.10 REQ-TR-10 High Configurable
[62](#req-tr-10-high-configurable)](#req-tr-10-high-configurable)

[1.5.1.11 REQ-TR-11 Backup and Recovery
[63](#req-tr-11-backup-and-recovery)](#req-tr-11-backup-and-recovery)

[1.5.1.12 REQ-TR-12 Operation System and Browser Compatibility
[63](#req-tr-12-operation-system-and-browser-compatibility)](#req-tr-12-operation-system-and-browser-compatibility)

[1.5.1.13 REQ-TR-13 Review and Update Privilege
[64](#req-tr-13-review-and-update-privilege)](#req-tr-13-review-and-update-privilege)

[1.5.1.14 REQ-TR-14 Health Check
[64](#req-tr-14-health-check)](#req-tr-14-health-check)

[1.5.1.15 REQ-TR-15 Encryption on All Communications
[65](#req-tr-15-encryption-on-all-communications)](#req-tr-15-encryption-on-all-communications)

[1.5.1.16 REQ-TR-16 Version Control for application
[65](#req-tr-16-version-control-for-application)](#req-tr-16-version-control-for-application)

[1.5.1.17 REQ-TR-17 Monthly Usage Statistics and Ad-hoc Statistics
[65](#req-tr-17-monthly-usage-statistics-and-ad-hoc-statistics)](#req-tr-17-monthly-usage-statistics-and-ad-hoc-statistics)

[1.5.1.18 REQ-TR-18 Check-in and Check-out
[66](#req-tr-18-check-in-and-check-out)](#req-tr-18-check-in-and-check-out)

[1.5.1.19 REQ-TR-19 Language Support (EN/TC/SC)
[66](#req-tr-19-language-support-entcsc)](#req-tr-19-language-support-entcsc)

[1.5.1.20 REQ-TR-20 System Performance
[66](#req-tr-20-system-performance)](#req-tr-20-system-performance)

[1.5.1.21 REQ-TR-21 Reports and statistics for monitor system
performance
[67](#req-tr-21-reports-and-statistics-for-monitor-system-performance)](#req-tr-21-reports-and-statistics-for-monitor-system-performance)

[1.5.1.22 REQ-TR-22 Ad-hoc and periodic updates on the contents
[67](#req-tr-22-ad-hoc-and-periodic-updates-on-the-contents)](#req-tr-22-ad-hoc-and-periodic-updates-on-the-contents)

[1.5.1.23 REQ-TR-23 Provide refined Login & Authentication / FULL Audit
features
[68](#req-tr-23-provide-refined-login-authentication-full-audit-features)](#req-tr-23-provide-refined-login-authentication-full-audit-features)

[1.5.1.24 REQ-TR-24 Login user account login by user ID and password
[68](#req-tr-24-login-user-account-login-by-user-id-and-password)](#req-tr-24-login-user-account-login-by-user-id-and-password)

[1.5.1.25 REQ-TR-25 Version control of source code
[68](#req-tr-25-version-control-of-source-code)](#req-tr-25-version-control-of-source-code)

[1.5.1.26 REQ-TR-26 System log tracking
[69](#req-tr-26-system-log-tracking)](#req-tr-26-system-log-tracking)

[1.5.1.27 REQ-TR-27 Scalable system frame design
[69](#req-tr-27-scalable-system-frame-design)](#req-tr-27-scalable-system-frame-design)

[1.5.1.28 REQ-TR-28 Data exchange with other system securely
[70](#req-tr-28-data-exchange-with-other-system-securely)](#req-tr-28-data-exchange-with-other-system-securely)

[1.5.1.29 REQ-TR-29 Security measurement
[70](#req-tr-29-security-measurement)](#req-tr-29-security-measurement)

[1.5.1.30 REQ-TR-30 Help check email notification
[70](#req-tr-30-help-check-email-notification)](#req-tr-30-help-check-email-notification)

[1.5.1.31 REQ-TR-31 Email notification for all batch jobs
[71](#req-tr-31-email-notification-for-all-batch-jobs)](#req-tr-31-email-notification-for-all-batch-jobs)

[1.5.1.32 REQ-TR-32 Conform to the Interoperability Framework
[71](#req-tr-32-conform-to-the-interoperability-framework)](#req-tr-32-conform-to-the-interoperability-framework)

[1.5.1.33 REQ-TR-33 Manage System Parameters
[71](#req-tr-33-manage-system-parameters)](#req-tr-33-manage-system-parameters)

[1.5.1.34 REQ-TR-34 Allow System Access by EDB and SWD
[72](#req-tr-34-allow-system-access-by-edb-and-swd)](#req-tr-34-allow-system-access-by-edb-and-swd)

[1.5.1.35 REQ-TR-35 Independent System (Not depended on other BD system)
[72](#req-tr-35-independent-system-not-depended-on-other-bd-system)](#req-tr-35-independent-system-not-depended-on-other-bd-system)

[1.5.1.36 REQ-TR-36 Logout automatically for inactive for 30 minutes
[73](#req-tr-36-logout-automatically-for-inactive-for-30-minutes)](#req-tr-36-logout-automatically-for-inactive-for-30-minutes)

[1.5.1.37 REQ-TR-37 Centralized log management
[73](#req-tr-37-centralized-log-management)](#req-tr-37-centralized-log-management)

[1.5.1.38 REQ-TR-38 Handle around 300 user accounts of EDB and SWD for
Single Sign On
[73](#req-tr-38-handle-around-300-user-accounts-of-edb-and-swd-for-single-sign-on)](#req-tr-38-handle-around-300-user-accounts-of-edb-and-swd-for-single-sign-on)

[1.5.1.39 REQ-TR-39 Paper Less
[74](#req-tr-39-paper-less)](#req-tr-39-paper-less)

[1.5.1.40 REQ-TR-40 PDF template and mapping field for letter generation
[74](#req-tr-40-pdf-template-and-mapping-field-for-letter-generation)](#req-tr-40-pdf-template-and-mapping-field-for-letter-generation)

[2 CONSTRAINTS LIST [75](#constraints-list)](#constraints-list)

[2.1 Complexity of Address Identification
[75](#complexity-of-address-identification)](#complexity-of-address-identification)

[2.2 Signature of AP/RSE [75](#signature-of-aprse)](#signature-of-aprse)

[Appendix 1 – 3-Tier BSR System
[76](#appendix-1-3-tier-bsr-system)](#appendix-1-3-tier-bsr-system)

[Appendix 2 – Sample of School and CCC Certificates and Notices
[77](#appendix-2-sample-of-school-and-ccc-certificates-and-notices)](#appendix-2-sample-of-school-and-ccc-certificates-and-notices)

[Appendix 3 – Sample of Letter of Requirement (LoR)
[79](#appendix-3-sample-of-letter-of-requirement-lor)](#appendix-3-sample-of-letter-of-requirement-lor)

[Appendix 4 –Information Security Requirement
[80](#appendix-4-information-security-requirement)](#appendix-4-information-security-requirement)

[Appendix 5 –Sample of Utilisation Report
[81](#appendix-5-sample-of-utilisation-report)](#appendix-5-sample-of-utilisation-report)

# USER REQUIREMENTS

This document describes a complete list of user requirements for the
proposed Self-Certification System (SCS).

## PROPOSED SYSTEM OVERVIEW

The proposed Self-Certification System (SCS) allows Buildings Department
(BD) users to receive, process and manage the application for
certificates and notice required under Education Ordinance (Cap.279) and
Child Care Services Ordinance (Cap. 243) for the registration of
non-purpose built Educational Premises (EP) and Child Care Centre (CCC)
and to provide building safety comment to Education Bureau upon
applications for conducting courses of non-local higher and professional
education under NLHPE(R) Rules (Cap.493B) respectively in an effective
and efficient manner.

The system also allows applicant/Authorized Person (AP)/Registered
Structure Engineer (RSE) or users in Social Welfare Department (SWD) and
Education Bureau (EDB\*) to submit application forms and electronic
documents to BD through internet/intranet in order to speed up the
registration process.

Furthermore, the system is a single repository to store all applications
and supporting documents that can facilitate BD users to find documents
easily.

\* Including Joint Office for Kindergartens and Child Care Centres
(JOKCCC) of Education Bureau

### DESCRIPTION OF PROPOSED SYSTEM 

The following diagram shows a high-level business diagram of SCS.

<img src="media/image2.png" style="width:6.625in;height:7.26528in" />

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 74%" />
</colgroup>
<thead>
<tr class="header">
<th>Business Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Application for Certificates and Notice / Alteration for EP</p>
<p>(e-application)</p></td>
<td>The process is to allow applicant to apply e-certificates/ e-notice
for EP through internet in which application/AP/RSE can submit digital
signed documents to BD and BD to issue digital signed documents to
EDB/Applicant/AP/RSE.</td>
</tr>
<tr class="even">
<td><p>Application for Certificates and Notice / Alteration for EP</p>
<p>(paper application)</p></td>
<td>The process is to allow applicant to apply certificates/ notice for
EP by post.</td>
</tr>
<tr class="odd">
<td><p>Application for Certificates / Alteration for CCC</p>
<p>(e-application)</p></td>
<td>The process is to allow applicant/SWD/EDB(JOKCCC) to apply
–e-certificates for CCC through internet/intranet in which
application/AP/RSE can submit digital signed documents to BD and BD to
issue digital signed document to SWD/EDB(JOKCCC)/Applicant/AP/RSE.</td>
</tr>
<tr class="even">
<td><p>Application for Certificates / Alteration for CCC</p>
<p>(paper application)</p></td>
<td>The process is to allow applicant/SWD/EDB(JOKCCC) to apply
certificates for CCC by post.</td>
</tr>
<tr class="odd">
<td>Random Audit Check</td>
<td>The process is to allow BD users to perform random audit check of
the completed applications.</td>
</tr>
<tr class="even">
<td><p>Application for Approval /Alteration for use of the premises for
conducting course under the Non-Local-Higher and Professional Education
(Regulation) Ordinance [NLHPE(R)O]</p>
<p>(e-application)</p></td>
<td>The process is to allow applicant/ EDB to seek BD’s comment on
approval for use of the premises for conducting course under the
NLHPE(R)O through internet/intranet in which applicant/AP/RSE can submit
digital signed documents to BD and BD to issue digital signed documents
to EDB/Applicant/AP/RSE.</td>
</tr>
<tr class="odd">
<td><p>Application for Approval/ Alteration for use of the premises for
conducting course under the NLHPE(R)O</p>
<p>(paper application)</p></td>
<td>The process is to allow applicant/ EDB to seek BD’s comment on
approval for use of the premises for conducting course under the
NLHPE(R)O by post.</td>
</tr>
<tr class="even">
<td><p>Application for Structural inspection for CCC</p>
<p>(paper application)</p></td>
<td>The process is to allow applicant to apply periodic inspection for
CCC by post.</td>
</tr>
<tr class="odd">
<td>Application for inclusion of Temporary Structures in the
Pre-accepted Temporary Structure (PTS) Register for use under TPPE
license</td>
<td>The process is to allow BD users to store PTS details, generate PTS
register and assign register number for PTS.</td>
</tr>
</tbody>
</table>

### SYSTEM USER PROFILE

The following table describes system users who participate in the SCS.

<table>
<colgroup>
<col style="width: 5%" />
<col style="width: 14%" />
<col style="width: 40%" />
<col style="width: 13%" />
<col style="width: 13%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th>No.</th>
<th>User Role</th>
<th>Responsibilities</th>
<th>Branch/Division/Section/Unit</th>
<th>Staff Post/Rank</th>
<th>Stakeholder Group</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Applicant</td>
<td>Submit application form to BD</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
</tr>
<tr class="even">
<td>2</td>
<td>AP/RSE</td>
<td>Ensure building safety that meets BD’s requirements</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
</tr>
<tr class="odd">
<td>3</td>
<td>EDB User</td>
<td>Submit application form to BD for EP</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
</tr>
<tr class="even">
<td>4</td>
<td>SWD/EDB(JOKCCC) User</td>
<td>Submit application form to BD for CCC</td>
<td>N/A</td>
<td>N/A</td>
<td>N/A</td>
</tr>
<tr class="odd">
<td>5</td>
<td>Registry</td>
<td>Data input to SCS</td>
<td>LU</td>
<td>Registry</td>
<td>BD</td>
</tr>
<tr class="even">
<td>6</td>
<td>SE</td>
<td>Provide comment via SSE to BS</td>
<td>LU</td>
<td>SE</td>
<td>BD</td>
</tr>
<tr class="odd">
<td>7</td>
<td>SSE</td>
<td>Provide comment</td>
<td>LU</td>
<td>SSE</td>
<td>BD</td>
</tr>
<tr class="even">
<td>8</td>
<td>SO</td>
<td>Perform site inspection and prepare inspection report</td>
<td>LU</td>
<td>SO</td>
<td>BD</td>
</tr>
<tr class="odd">
<td>9</td>
<td>BS</td>
<td>Check Building Safety Requirement (BSR)</td>
<td>LU</td>
<td>BS</td>
<td>BD</td>
</tr>
<tr class="even">
<td>10</td>
<td>TO</td>
<td>Obtain structural information and report to SE</td>
<td>LU</td>
<td>TO</td>
<td>BD</td>
</tr>
<tr class="odd">
<td>11</td>
<td>SBS</td>
<td>Endorse and approve application</td>
<td>LU</td>
<td>SBS</td>
<td>BD</td>
</tr>
<tr class="even">
<td>12</td>
<td>CBS</td>
<td>Endorse objection cases</td>
<td>LU</td>
<td>CBS</td>
<td>BD</td>
</tr>
<tr class="odd">
<td>13</td>
<td>System Admin</td>
<td>Perform system administration of SCS</td>
<td>ITU/MC</td>
<td>System Admin</td>
<td>BD</td>
</tr>
<tr class="even">
<td>14</td>
<td>User Admin</td>
<td>Perform user administration of SCS</td>
<td><p>LU/ITU/</p>
<p>EBD/SWD</p></td>
<td>User Admin</td>
<td>BD/EBD/SWD</td>
</tr>
</tbody>
</table>

## FUTURE BUSINESS PROCESS

### LIST OF FUTURE BUSINESS PROCESS

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 80%" />
</colgroup>
<thead>
<tr class="header">
<th>Process ID</th>
<th>Business Process Title</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BP-001</td>
<td><p>Application for e-Certificates and e-Notice / Alteration for
EP</p>
<p>(e-application)</p></td>
</tr>
<tr class="even">
<td>BP-002</td>
<td><p>Application for Certificates and Notice / Alteration for EP</p>
<p>(paper application)</p></td>
</tr>
<tr class="odd">
<td>BP-003</td>
<td><p>Application for e-Certificates / Alteration for CCC</p>
<p>(e-application)</p></td>
</tr>
<tr class="even">
<td>BP-004</td>
<td><p>Application for Certificates / Alteration for CCC</p>
<p>(paper application)</p></td>
</tr>
<tr class="odd">
<td>BP-005</td>
<td>Random Audit Check</td>
</tr>
<tr class="even">
<td>BP-006</td>
<td><p>Application for approval/ Alteration for use of the premises for
conducting course under the NLHPE(R)O</p>
<p>(e-application)</p></td>
</tr>
<tr class="odd">
<td>BP-007</td>
<td><p>Application for approval/ Alteration for use of the premises for
conducting course under the NLHPE(R)O</p>
<p>(paper application)</p></td>
</tr>
<tr class="even">
<td>BP-008</td>
<td>Application for periodic inspection for CCC</td>
</tr>
<tr class="odd">
<td>BP-009</td>
<td>Application for inclusion of Temporary Structures in the
Pre-accepted Temporary Structure (PTS) Register for use under TPPE
license</td>
</tr>
</tbody>
</table>

#### Application for e-Certificates and e-Notice for EP (e-application)

<img src="media/image3.png" style="width:6.37642in;height:8.66832in" />

#### Application for Alteration for EP/CCC (e-application)

<img src="media/image4.png" style="width:6.33445in;height:8.60396in" />**<u>  
</u>**

**<u>Opt for SCS Sub-Workflow (e-application)</u>**

<img src="media/image5.png" style="width:5.76389in;height:6.66667in" />

Standard Form SC(S) -1 - Opt for SCS (New Application for EP)

Standard Form SC(S) -2 - Opt for SCS (Alteration Application for EP)

Standard Form SC(C) -1 - Opt for SCS (New Application for CCC)

Standard Form SC(C) -2 - Opt for SCS (Alteration Application for CCC)

Standard Form SC(N) -1 - Opt for SCS \[Application for EP (NLHPE)\]

#### Application for Certificates and Notice for EP (paper application)

<img src="media/image6.png" style="width:5.59766in;height:9.07426in" />

#### Application for Alteration for EP/CCC (paper application)

<img src="media/image7.png" style="width:6.625in;height:9.22153in" />**<u>  
</u>**

**<u>Opt for SCS Sub-Workflow (paper submission)</u>**

<img src="media/image8.png" style="width:5.83333in;height:7.36111in" />

Standard Form SC(S) -1 - Opt for SCS (New Application for EP)

Standard Form SC(S) -2 - Opt for SCS (Alteration Application for EP)

Standard Form SC(C) -1 - Opt for SCS (New Application for CCC)

Standard Form SC(C) -2 - Opt for SCS (Alteration Application for CCC)

Standard Form SC(N) -1 - Opt for SCS \[Application for EP (NLHPE)\]

#### Random Audit Check

<img src="media/image9.png" style="width:4.68735in;height:9.17582in" />

#### Application for Approval for use of the premises for conducting course under the Non-Local-Higher and Professional Education (Regulation) Ordinance \[NLHP(R)O\] (e-application)

<img src="media/image10.png" style="width:5.40139in;height:8.48052in" />

#### Application for Approval for use of the premises for conducting course under the Non-Local-Higher and Professional Education (Regulation) Ordinance \[NLHP(R)O\] (paper application)

<img src="media/image11.png" style="width:5.45121in;height:8.49451in" />

#### Application for Periodic Inspection for CCC

<img src="media/image12.png" style="width:6.625in;height:5.2875in" />

#### Application for inclusion of Temporary Structures in the Pre-accepted Temporary Structure (PTS) Register for user under TPPE license

<img src="media/image13.png" style="width:6.625in;height:4.42639in" />

## FUNCTIONAL REQUIREMENTS

The proposed system shall possess the following general characteristics:

For each user requirement, the requirement ID, requirement title,
priority as well as proposed solution are documented.

The requirements will be prioritized into the following categories:

|                     |                                                                                                                                                   |
|----------------------|--------------------------------------------------|
| **Priority**        | **Description**                                                                                                                                   |
| High (H)            | The functional requirements would be included in the proposed system.                                                                             |
| Medium (M)          | Assessment would be made on the feasibility to include the functional requirements in the proposed system.                                        |
| Low (L)             | Assessment would be made on the feasibility to include the functional requirements in the proposed system.                                        |
| Not applicable (NA) | The functional requirements would not be included in the proposed system as user representative confirmed these requirements were not applicable. |

A unique ID is assigned to each requirement and the format of a
Requirement ID is as follows:

Requirement ID = \[‘REQ’\] + \[-\] + \[Category\] + \[-\] + \[Sequence\]

*The sequence is a 2-digit serial number starting from 01*

| Category | Description                 |
|----------|-----------------------------|
| GR       | General Requirement         |
| WR       | Workflow Requirement        |
| CR       | Communication Requirement   |
| UR       | User Interface Requirement  |
| SR       | Security Requirement        |
| IR       | Interface Requirement       |
| TR       | Technical Requirement       |
| FRM      | Form Requirement            |
| FRO      | Form Processing Requirement |

### LIST OF FUNCTIONAL REQUIREMENTS

|                             |                                                                      |                                                   |              |
|---------------|----------------------------|--------------------|----------|
| **Req. ID**                 | **Requirement Name**                                                 | **Target Users**                                  | **Priority** |
| General Requirement         |                                                                      |                                                   |              |
| REQ-GR-01                   | User Registration                                                    | Applicant/AP/RSE                                  | NA           |
| REQ-GR-02                   | Login with Username & Password                                       | Applicant/AP/RSE                                  | NA           |
| REQ-GR-03                   | Registration and Login through iAM Smart                             | Applicant/AP/RSE                                  | NA           |
| REG-GR-04                   | Change Password                                                      | Applicant/AP/RSE                                  | NA           |
| REG-GR-05                   | Forget Password                                                      | Applicant/AP/RSE                                  | NA           |
| REG-GR-06                   | Logout                                                               | Applicant/AP/RSE                                  | NA           |
| REQ-GR-07                   | Single Sign On                                                       | BD Users/EDB User/ SWD User                       | H            |
| REQ-GR-08                   | Preview Document                                                     | All Users                                         | H            |
| REQ-GR-09                   | Print Document                                                       | BD Users                                          | H            |
| REQ-GR-10                   | Upload Document                                                      | BD Users/EDB User/SWD User/Applicant/AP/RSE       | H            |
| REQ-GR-11                   | Management Statistics and Reports                                    | BD Users                                          | H            |
| REQ-GR-12                   | e-submission                                                         | Applicant/AP/RSE                                  | H            |
| REQ-GR-13                   | e-processing                                                         | BD Users/EDB User/SWD User                        | H            |
| REQ-GR-14                   | e-tracking                                                           | All Users                                         | H            |
| REQ-GR-15                   | Centralised data repository of the application supporting documents  | BD Users/EDB User/SWD User/                       | H            |
| REQ-GR-16                   | Search and Capture                                                   | BD Users/EDB User/SWD User/                       | H            |
| REQ-GR-17                   | Handle new applications                                              | BD Users/EDB User/SWD User/                       | H            |
| REQ-GR-18                   | Handle alteration applications                                       | BD Users/EDB User/SWD User/                       | H            |
| REQ-GR-19                   | Handle Self Certification Submissions                                | BD Users                                          | H            |
| REQ-GR-20                   | Handle Periodic Inspection for CCC                                   | BD Users                                          | H            |
| REQ-GR-21                   | Handle PTS for TPPE                                                  | BD Users                                          | H            |
| REQ-GR-22                   | Data repository                                                      | BD Users                                          | H            |
| REQ-GR-23                   | Easy retrieval of the records                                        | BD Users                                          | H            |
| REQ-GR-24                   | User and Delegation Administration                                   | User Administrators of BD Users/EDB User/SWD User | H            |
| REQ-GR-25                   | Generate Application Number                                          | Applicant                                         | H            |
| REQ-GR-26                   | Withdraw Application                                                 | Applicant                                         | H            |
| Workflow Requirement        |                                                                      |                                                   |              |
| REQ-WR-01                   | Input Application Data                                               | Registry                                          | H            |
| REQ-WR-02                   | Create Structural Information Report                                 | TO                                                | H            |
| REQ-WR-03                   | Provide Comment via SSE                                              | SE                                                | H            |
| REQ-WR-04                   | Perform Site Inspection                                              | SO                                                | H            |
| REQ-WR-05                   | Building Safety Requirements Check                                   | BS                                                | H            |
| REQ-WR-06                   | Generate Reply Letter, e-Certificates and e-Notice                   | BS/SBS                                            | H            |
| REQ-WR-07                   | Generate Letter of Requirement                                       | BS/SBS                                            | H            |
| REQ-WR-08                   | Endorse Application                                                  | SBS                                               | H            |
| REQ-WR-09                   | Endorse Objection                                                    | CBS                                               | H            |
| REQ-WR-10                   | AP/RSE Verification                                                  | Registry                                          | H            |
| REQ-WR-11                   | Check Essential Documents                                            | SO/BS                                             | H            |
| REQ-WR-12                   | Digital Signing of Document                                          | Applicant/AP/RSE/ BD Users                        | H            |
| REQ-WR-13                   | Random Audit Check                                                   | BD Users                                          | H            |
| REQ-WR-14                   | Outstanding Application Alert                                        | SO/TO/BS/SE/SSE/SBS                               | H            |
| REQ-WR-15                   | Input Application Form                                               | Applicant                                         | H            |
| REQ-WR-16                   | Input memo data                                                      | EDB/SWD                                           | H            |
| REQ-WR-17                   | Search Case Information                                              | BD Users                                          | H            |
| Form Requirement            |                                                                      |                                                   |              |
| REQ-FRM-1                   | Verify certificate against the copy from Hong Kong post and DigiSign | System                                            | H            |
| REQ-FRM-2                   | Route form to corresponding user                                     | System                                            | H            |
| REQ-FRM-3                   | Encrypt restricted data in the form                                  | System                                            | H            |
| REQ-FRM-4                   | Submit public form via online                                        | System                                            | H            |
| REQ-FRM-5                   | Extract data from form                                               | System                                            | H            |
| REQ-FRM-6                   | Store the extracted data in the database                             | System                                            | H            |
| REQ-FRM-7                   | Search function for all record                                       | System                                            | H            |
| REQ-FRM-8                   | Auto-reply to acknowledge receiving the form                         | System                                            | H            |
| REQ-FRM-9                   | Maintenance function of the form                                     | System                                            | H            |
| REQ-FRM-10                  | Resubmit the form data                                               | System                                            | H            |
| REQ-FRM-11                  | Update of the disclaimer of the forms                                | System                                            | H            |
| REQ-FRM-12                  | Handle eform and Hardcopy form                                       | System                                            | H            |
| From Processing Requirement |                                                                      |                                                   |              |
| REQ-PRO-1                   | Verify CRM certification record                                      | BD Users/EDB User/SWD User                        | H            |
| REQ-PRO-2                   | Reassign Case to other officer                                       | BD Users/EDB User/SWD User                        | H            |
| REQ-PRO-3                   | Form status query                                                    | BD Users/EDB User/SWD User                        | H            |
| REQ-PRO-4                   | Automatically Bring up Outstanding Cases                             | BD Users/EDB User/SWD User                        | H            |
| REQ-PRO-5                   | To Do List                                                           | BD Users/EDB User/SWD User                        | H            |
| REQ-PRO-6                   | Case History Summary                                                 | BD Users/EDB User/SWD User                        | H            |
| REQ-PRO-7                   | Mark Notes and remark for internal use.                              | BD Users/EDB User/SWD User                        | H            |
| REQ-PRO-8                   | Re-direct to BCIS for case checking                                  | BD Users                                          | H            |
| REQ-PRO-9                   | Handle upload soft-copy                                              | BD Users/EDB User/SWD User                        | H            |
| REQ-PRO-10                  | Export outstanding case                                              | BD Users/EDB User/SWD User                        | H            |
| REQ-PRO-11                  | Handle referral Case                                                 | BD Users/EDB User/SWD User                        | H            |

#### 

#### REQ-GR-01 User Registration

**Priority:**

Not applicable

LU confirmed that applicant would use reference number and OTP instead
of this function.

**Functional Requirement:**

The system shall allow applicant or AP/RSE to register user account
through Internet. Personal information such as name, email address,
mobile number…etc will be stored in the system.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-02 Login with Username & Password

**Priority:**

Not applicable

LU confirmed that applicant would use reference number and OTP instead
of this function.

**Functional Requirement:**

The system shall allow registered applicant or AP/RSE to login the
system using username and password.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-03 Login through iAM Smart

**Priority:**

Not applicable

LU confirmed that applicant would use reference number and OTP instead
of this function.

**Functional Requirement:**

Instead of logging in using username and password, the system shall
allow applicant or AP/RSE to login through iAM Smart mobile application.

For more details about iAM Smart, please refer to
<https://www.iamsmart.gov.hk/en/>.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-04 Change Password

**Priority:**

Not applicable

LU confirmed that applicant would use reference number and OTP instead
of this function.

**Functional Requirement:**

The system shall allow logged-in applicant or AP/RSE to change password.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-05 Forget Password

**Priority:**

Not applicable

LU confirmed that applicant would use reference number and OTP instead
of this function.

**Functional Requirement:**

When applicant or AP/RSE forget password, the system shall provide
hyperlink to reset password through registered email address.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-06 Logout

**Priority:**

Not applicable

LU confirmed that applicant would use reference number and OTP instead
of this function.

**Functional Requirement:**

Once applicant or AP/RSE logged in the system, the system shall allow
the user to logout.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-07 Single Sign On

**Priority:**

High

**Functional Requirement:**

The system shall allow BD users, EDB users and SWD users to login the
system without inputting username and password once they logged in their
Open Source Departmental Portal (OSDP) through Government Backbone
Network (GNET). To logout the system, the users are required to logout
in OSDP.

| Users     | Portal   |
|-----------|----------|
| BD Users  | BD OSDP  |
| EDB Users | EDB OSDP |
| SWD Users | SWD OSDP |

User administration account shall be created for EDB and SWD in order to
maintain their user accounts and access rights in SCS.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-08 Preview Document

**Priority:**

High

**Functional Requirement:**

The system shall allow logged on users to preview uploaded document in
browser. The document format should be in PDF format or image format
such as JPEG, PNG or TIFF.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-09 Print Document

**Priority:**

High

**Functional Requirement:**

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

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-10 Upload Document

**Priority:**

High

**Functional Requirement:**

The system shall allow logged on users to upload documents including
layout plan, supporting documents…etc.

Virus scanning shall be performed for each uploaded file.

Plans shall be in flattened PDF format not larger than 25MB each and
digitally signed by Hongkong Post certificate or by iAM Smart. Total
files’ size shall be within 100MB regardless the number of files. It is
configurable of maximum size of upload document.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-11 Management Statistics and Reports

**Priority:**

High

**Functional Requirement:**

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

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-12 e-submission

**Priority:**

High

**Functional Requirement for e-submission form:**

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

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-13 e-processing

**Priority:**

High

**Functional Requirement:**

The processing of application of new/alteration of EP/ CCC and Periodic
Inspection for CCC will be handled in Workflows by BD users. For
details, please refer to Workflow Requirements.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-14 e-tracking

**Priority:**

High

**Functional Requirement:**

The processing of application of new/alteration of EP/ CCC and Periodic
Inspection for CCC will be handled in Workflows by BD users. For
details, please refer to Workflow Requirements.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-15 Centralised data repository of the application supporting documents

**Priority:**

High

**Functional Requirement:**

The uploaded and generated documents will be stored in database and file
systems.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-16 Search and Capture

**Priority:**

High

**Functional Requirement:**

Please refer to REQ-WF-17.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-17 Handle new application

**Priority:**

High

**Functional Requirement:**

The workflow will handle new application for EP or CCC. For details,
please refer to workflow requirements.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-18 Handle alteration application

**Priority:**

High

**Functional Requirement:**

The workflow will handle alteration application for EP or CCC. For
details, please refer to workflow requirements.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-19 Handle Self Certification Submissions

**Priority:**

High

**Functional Requirement:**

The workflow will handle alteration application for EP or CCC. For
details, please refer to workflow requirements.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-20 Handle Periodic Inspection for CCC

**Priority:**

High

**Functional Requirement:**

The workflow will handle periodic inspection for CCC. For details,
please refer to workflow requirements.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-21 Handle PTS for TPPE

**Priority:**

High

**Functional Requirement:**

The workflow will handle update of PTS for TPPE. For details, please
refer to workflow requirements.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-22 Data repository

**Priority:**

High

**Functional Requirement:**

All data will be stored in centralized place i.e. Database and File
System (i.e. SAN)

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-23 Easy retrieval of the records

**Priority:**

High

**Functional Requirement:**

The system provides a search function for BD users to look up case
information. For details, please refer to REQ-WR-17.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-24 User and Delegation Administration

**Priority:**

High

**Functional Requirement:**

The system provides administration to delegate task from one person to
another person for a certain period of time. During the delegation, the
tasks will be routed to delegated person instead of original person.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-25 Generate Application Number

**Priority:**

High

**Functional Requirement:**

The system shall generate an Application Number when applicant submits a
new licensing application for EP or CCC. The pattern of Application
Number will be:

YYYY(12 or 13)NNNN

YYYY – 4 digits of the Year

12 – for EP

13 – for CCC

NNNN – Sequence number in the Year

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-GR-26 Withdraw Application

**Priority:**

High

**Functional Requirement:**

The system shall allow applicant to withdraw application any time.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-01 Input Application Data

**Priority:**

High

**Functional Requirement:**

The system shall allow registry to input application data and upload
scanned documents to the system when application is received by post.

Structural address with autocomplete function shall be provided,
including on Tradional Chinese and English.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-02 Create Structural Information Report

**Priority:**

High

**Functional Requirement:**

The system shall allow Technical Officer (TO) to create Structural
Information Report.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-03 Provide Comment via SSE

**Priority:**

High

**Functional Requirement:**

The system shall allow Senior Structural Engineer (SSE) to provide
comments about the application.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-04 Perform Site Inspection

**Priority:**

High

**Functional Requirement:**

The system shall allow Survey Officer (SO) to record Site Inspection,
retrieve approved plans from BRAVO and prepare / generate inspection
report. The Site Inspection data should include:

1.  Date of Site Inspection

2.  Site photo

3.  Others

Also, the system allows SO to draw annotation on PDF file of Layout Plan
and upload site photos.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-05 Building Safety Requirements Check

**Priority:**

High

**Functional Requirement:**

The system shall allow Building Surveyor (BS) to check the building
safety using 3-tier Building Safety Requirements (BSR) System. For
details of 3-tier BSR, please refer to appendix 1

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-06 Generate Reply Letter, e-Certificates and e-Notice

**Priority:**

High

**Functional Requirement:**

When the application complies all building safety requirements, the
system shall generate Reply Letter, e-Certificates and e-Notices and
send to applicant or EDB/SWD users. For sample of certificates of School
and CCC, please refer to Appendix 2.

The documents are required to digitally signed by BD officer

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-07 Generate Letter of Requirement

**Priority:**

High

**Functional Requirement:**

When the application is not fully complied to building safety
requirements, the system shall generate Letter of Requirement (LoR). For
sample of LoR, please refer to Appendix 3.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-08 Endorse Application

**Priority:**

High

**Functional Requirement:**

The system shall allow Senior Building Surveyor (SBS) to approve/reject
the application.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-09 Endorse Objection

**Priority:**

High

**Functional Requirement:**

The system shall allow Chief Building Surveyor (CBS) to approve/reject
the objection case. The objection case refers to Category 3 of 3-Tier
BSR system.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-10 AP/RSE Verification

**Priority:**

High

**Functional Requirement:**

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

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-11 Check Essential Documents

**Priority:**

High

**Functional Requirement:**

The system shall allow Building Surveyor (BS) and Structural Engineer
(SE) to check whether all essential documents are submitted.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-12 Digital Signing of document

**Priority:**

High

**Functional Requirement:**

The system shall allow applicant or AP/RSE to digitally sign documents
using Hong Kong Post e-cert or iAM Smart+.

Also, the Reply Letter, e-Certificates and e-Notices will be digitally
signed using BD certificate.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-13 Random Audit Check

**Priority:**

High

**Functional Requirement:**

The system will immediately perform random audit check when the
certificates and notices are issued and allow BS to check the audit
items. The probability of random audit check is 60%, which is
configurable.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-14 Outstanding Application Alert

**Priority:**

High

**Functional Requirement:**

The system will send email notification to officer when application is
to be due/ overdue/ outstanding (i.e. no action after target complete
date) and the cases selected for audit.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-15 Input Application Form

**Priority:**

High

**Functional Requirement:**

The applicant/AP/RSE can submit application form, layout plans and other
documents for application of new/ alteration of EP and CCC. The
submitted documents will be digitally signed by Hong Kong Post e-Cert or
iAM Smart app. Once the application form is submitted, the system will
trigger a new workflow for internal BD users to handle the application.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-16 Input memo data

**Priority:**

High

**Functional Requirement:**

BD/EDB/SWD users can submit memo data including uploading documents in
SCS.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-WR-17 Search Case Information

**Priority:**

High

**Functional Requirement:**

BD/SWD/EDB users can search all case information including uploaded
documents, BSR status…etc in SCS.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-1 Verify certificate against the copy from Hong Kong Post and DigiSign 

**Priority:**

High

**Functional Requirement:**

The certificate to sign documents will be verified if the CA is from
Hong Kong Post and DigiSign. The other CA certificate will not be
accepted.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-2 Route form to corresponding user

**Priority:**

High

**Functional Requirement:**

In the workflow, the case will be routed to delegated person base on
user mapping from BCIS.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-3 Encrypt restricted data in the form

**Priority:**

High

**Functional Requirement:**

The system will encrypted classified data before storing in database and
handle up to Restricted Information.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-4 Submit public form via online

**Priority:**

High

**Functional Requirement:**

Please refer to REQ-WR-15.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-5 Extract data from form

**Priority:**

High

**Functional Requirement:**

All data of submitted form by applicant/AR/RSE will be saved in
database.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-6 Store the extracted data in the database

**Priority:**

High

**Functional Requirement:**

All data of submitted form by applicant/AR/RSE will be saved in
database.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-7 Search function for all record

**Priority:**

High

**Functional Requirement:**

Please refer to REQ-WR-16.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-8 Auto reply to acknowledge receiving the form

**Priority:**

High

**Functional Requirement:**

An acknowledge letter will be generated and send to application (for
1<sup>st</sup> submission only).

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-9 Maintenance function of the form.

**Priority:**

High

**Functional Requirement:**

In case the form data or layout is change, a Change Request will be made
in order to change coding.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-10 Resubmit the form data

**Priority:**

High

**Functional Requirement:**

Applicant can re-submit the revised layout plan or other documents once
he receives LoR from BD.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-11 Update of the disclaimer of the forms

**Priority:**

High

**Functional Requirement:**

The disclaimer of the forms can be directly updated in the program file
i.e. .aspx.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-FRM-12 Handle e-form and hardcopy form

**Priority:**

High

**Functional Requirement:**

The system will handle e-form and hardcopy form submitted by applicant.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-1 Verify CRM certification record

**Priority:**

High

**Functional Requirement:**

The system will automatically verify AP/RSE information against CRM
record. However, if paper application, BD user i.e. Registry is required
to manually verify the handwriting signature and other data of AP/RSE.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-2 Reassign case to other officer

**Priority:**

High

**Functional Requirement:**

The assigned task can be re-assigned to another person in ad-hoc by
system administrator.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-3 Form status query

**Priority:**

High

**Functional Requirement:**

Please refer to REQ-WR-17.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-4 Automatically bring up outstanding cases.

**Priority:**

High

**Functional Requirement:**

Please refer to REQ-WR-14.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-5 To-Do List

**Priority:**

High

**Functional Requirement:**

The system provides a tasks list i.e. to-do list for all BD users to
handle the case in the workflow.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-6 Case History Summary

**Priority:**

High

**Functional Requirement:**

Please refer to REQ-WF-17

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-7 Mark notes and remark for internal use.

**Priority:**

High

**Functional Requirement:**

The workflow provides comments or notes to BD users to handle the case.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-8 Re-direct to BCIS for case checking

**Priority:**

High

**Functional Requirement:**

There will be a hyperlink to BCIS to see the case information when the
case is save in BCIS.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-9 Handle upload soft copy

**Priority:**

High

**Functional Requirement:**

All uploaded documents will be saved in centralised file system.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-10 Export outstanding case

**Priority:**

High

**Functional Requirement:**

Please refer to REQ-GR-11.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-PRO-11 Handle referral case

**Priority:**

High

**Functional Requirement:**

Please refer to REQ-WR-16.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

## NON-FUNCTIONAL REQUIREMENTS

### LIST OF NON-FUNCTIONAL REQUIREMENTS

|                           |                                              |                  |              |
|----------------|---------------------------|-------------------|----------|
| **Req. ID**               | **Requirement Name**                         | **Target Users** | **Priority** |
| Communication Requirement |                                              |                  |              |
| REQ-CR-01                 | SMS Alert                                    | All Users        | H            |
| REQ-CR-02                 | Email Notification                           | All Users        | H            |
| REQ-CR-03                 | Fax Copy of LoR, Certificates, and Notice    | All Users        | H            |
|                           |                                              |                  |              |
| Webpage Requirement       |                                              |                  |              |
| REQ-UR-01                 | Common Look & Feel                           | All Users        | H            |
| REQ-UR-02                 | W3C WCAG 2.1                                 | All Users        | H            |
| REQ-UR-03                 | Privacy Disclaimer                           | All Users        | H            |
| REQ-UR-04                 | Assistive Technology Testing                 | All Users        | H            |
|                           |                                              |                  |              |
| Security Requirement      |                                              |                  |              |
| REQ-SR-01                 | SRAA                                         | System Admin     | H            |
| REQ-SR-02                 | PIA and PCA                                  | System Admin     | H            |
| REQ-SR-03                 | Encryption and Decryption of Classified Data | System Admin     | H            |
| REQ-SR-04                 | System Audit                                 | System Admin     | H            |
| REQ-SR-05                 | System Control                               | System Admin     | H            |
|                           |                                              |                  |              |
| Interface Requirement     |                                              |                  |              |
| REQ-IR-01                 | Interface with BCIS                          | System Admin     | H            |
| REQ-IR-02                 | Interface with BD Website                    | System Admin     | H            |
| REQ-IR-03                 | Interface with Minor Works                   | System Admin     | H            |
| REQ-IR-04                 | Interface with ESH                           | System Admin     | H            |
| REQ-IR-05                 | Interface with ERKS                          | System Admin     | H            |
| REQ-IR-06                 | Interface with BRAVO                         | System Admin     | H            |

#### REQ-CR-01 SMS Alert

**Priority:**

High

**Functional Requirement:**

The system shall send SMS alert to users through-out the workflow. Here
are scenarios to send out SMS and their contents.

-   As an acknowledgement of each form submission;

-   Notification of LoR issued;

-   Notification of Certificate and Notice issued.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-CR-02 Email Notification

**Priority:**

High

**Functional Requirement:**

The system shall send Email notification to users through-out the
workflow. Here are scenarios to send out Email and their contents.

-   As an acknowledgement of each form submission;

-   Notification of LoR issued;

-   Notification of Certificate and Notice issued.

-   Reminder to AP/RSE for o/s audit case.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-CR-03 Fax Copy of LoR, Certificates, and Notice

**Priority:**

High

**Functional Requirement:**

The system shall send the LoR, Certificates, and Notice to applicant
through Fax.

#### REQ-UR-01 Common Look & Feel

**Priority:**

High

**Functional Requirement:**

The system shall conform design and guideline of Common Look & Feel
(CLF) of the HKSAR government.

<img src="media/image14.png" style="width:6.625in;height:3.10625in" />

Ensure SCS conforming to the latest version of the Common Look & Feel
(CLF), Mobile Friendly and Web Accessibility standard. The responsive
web / mobile friendly design shall allow the contents of SCS be adapted
to different layouts in a real-time manner in response to the different
screen sizes and resolutions

The design shall comply with the latest version of the CLF and conform
to the W3C HTML5 standard as listed in Section 6 of this work assignment
for details to better support modern browsers or mobile devices, i.e. a
responsive web design. The Contractor shall ensure all web pages of SCS
shall be compatible with popular web browsers, operating systems, screen
readers, etc.

For details, please refer to
<https://itginfo.ccgo.hksarg/content/clf/home.html>

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-UR-02 W3C WCAG 2.1

**Priority:**

High

**Functional Requirement:**

The system shall conform to W3C WCAG 2.1 Level AA standard to facilitate
access by people of disabilities. Various testing will be done
including:

1.  Code scanning – Detect any non-conformance to WCAG 2.1 Level AA
    > standard by using well-known software tools;

2.  Visual review – Verify the accessibility by visual browsing and by
    > automatic tool to reveal any accessibility problems, including but
    > not limited to insufficient colour contrast, keyboard traps, too
    > small font size, etc.;

3.  Assistive Technology (AT) tools testing – Test SCS with AT tools
    > such as screen readers, screen magnifiers and voice controls;

4.  Human testing - perform visual review on desktop and mobile
    > versions;

For more details, please refer to
<https://www.ogcio.gov.hk/en/our_work/community/web_mobileapp_accessibility/promulgating_resources/handbook/>

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-UR-03 Privacy Disclaimer

**Priority:**

High

**Functional Requirement:**

The system shall provide a privacy disclaimer in website in order to
conform to Personal Data (Privacy) Ordinance (Cap 486).

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-UR-04 Assistive Technology Testing

**Priority:**

High

**Functional Requirement:**

To conform W3C WCAG 2.1 Level AA standard, a set of tools such as screen
readers, screen magnifiers and voice controls will be used for the
testing.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-SR-01 SRAA

**Priority:**

High

**Functional Requirement:**

Security Risk Assessment Audit (SRAA) exercise will be executed in order
to address all security issues. All vulnerabilities found and necessary
safeguards recommended by Security Auditors should be fixed and
implemented accordingly.

Appendix 4 –Information Security Requirement

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-SR-02 PIA and PCA

**Priority:**

High

**Functional Requirement:**

Privacy Impact Assessment (PIA) and Privacy Compliance Audit (PCA) will
be executed in order to address all privacy issues. All vulnerabilities
found and necessary safeguards recommended by Auditors should be fixed
and implemented accordingly.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-SR-03 Encryption and Decryption of Classified Data

**Priority:**

High

**Functional Requirement:**

All classified data such as HKID will be encrypted during transmission
or stored in file system or database. The encryption and decryption
should use strong symmetric encryption algorithms such as AES 256bit or
use Hash function such as SHA-256.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-SR-04 System Audit

**Priority:**

High

**Functional Requirement:**

Important events such as create case, login…etc will be logged and
stored in database for auditing purpose

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-SR-05 System Control

**Priority:**

High

**Functional Requirement:**

The security control to access to the system will be guarded using tools
such as Firewall, network control, physical access control..etc.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-IR-01 Interface with BCIS

**Priority:**

High

**Functional Requirement:**

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

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-IR-02 Interface with BD Website

**Priority:**

High

**Functional Requirement:**

The system shall display list of Pre-accepted Proprietary Temporary
structure data in BD website.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-IR-03 Interface with Minor Works

**Priority:**

High

**Functional Requirement:**

The system shall provide sFTP upload account to MWMS 2.0 in order to
collect AP/RSE data such as User Name, Registration Number, HKID, Expiry
Date, etc on a daily basis. SCS will setup a sFTP server in order to
receive AP/RSE data and update database accordingly.

The SCS system can use Departmental Portal link to redirect to CRM of
MWMS to view the detail AP/RSE information as same as ESH.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-IR-04 Interface with ESH

**Priority:**

High

**Functional Requirement:**

Case of information and hyper link of SCS will be provided to ESH to
view relating case information and redirect to SCS respectively.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-IR-05 Interface with ERKS

**Priority:**

High

**Functional Requirement:**

The e-Certificates, e-notices, reply letter and other documents are
required to import into ERKS system for record keeping. The detailed
interface specification and implementation will be done in SM&S stage.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-IR-06 Interface with BRAVO

**Priority:**

High

**Functional Requirement:**

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

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

## TECHNICAL REQUIREMENTS

### LIST OF TECHNICAL REQUIREMENTS

<table>
<colgroup>
<col style="width: 22%" />
<col style="width: 41%" />
<col style="width: 23%" />
<col style="width: 11%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Req. ID</strong></td>
<td><strong>Requirement Name</strong></td>
<td><strong>Target Users</strong></td>
<td><strong>Priority</strong></td>
</tr>
<tr class="even">
<td colspan="4">Technical Requirement</td>
</tr>
<tr class="odd">
<td>REQ-TR-01</td>
<td>24x7 Internet and Intranet</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-02</td>
<td>Integrated Cloud GCIS and On Premises</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-03</td>
<td>Input Validation</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-04</td>
<td>Record Relocation from GCIS to On Premises</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-05</td>
<td>High Availability</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-06</td>
<td>Monitoring and Alert Generation</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-07</td>
<td>DR Drill</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-08</td>
<td>UTF-8, Unicode or HKSCS</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-09</td>
<td>System Logging</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-10</td>
<td>High Configurable</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-11</td>
<td>Backup and Recovery</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-12</td>
<td>Operation System and Browser Compatibility</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-13</td>
<td>Review and Update privilege</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-14</td>
<td>Health Check</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-15</td>
<td>Encryption on All Communications</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-16</td>
<td>Version Control for application</td>
<td>System Admin</td>
<td>NA</td>
</tr>
<tr class="odd">
<td>REQ-TR-17</td>
<td>Monthly Usage Statistics and Ad-hoc Statistics</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-18</td>
<td>Check-in and Check-out</td>
<td>System Admin</td>
<td>NA</td>
</tr>
<tr class="odd">
<td>REQ-TR-19</td>
<td>Language support (EN/TC/SC)</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-20</td>
<td>System Performance</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-20</td>
<td>Record relocation</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-21</td>
<td>Reports and statistics for monitor system performance;</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-22</td>
<td>Ad-hoc and periodic updates on the contents</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-23</td>
<td>Provide refined Login &amp; Authentication/ FULL Audit features</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-24</td>
<td>Login user account login by user ID &amp; password.</td>
<td>BD/SWD/EBD/MC</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-25</td>
<td>Version control of source code</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-26</td>
<td>System log tracking</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-27</td>
<td>Scalable system frame design</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-28</td>
<td>Data exchange with other system securely</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-29</td>
<td>Security measurement</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-30</td>
<td>Help check email notification</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-31</td>
<td>Email notification for all batch jobs</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-32</td>
<td>Conform to the Interoperability Framework</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-33</td>
<td>Manage System Parameters</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-34</td>
<td>Allow System Access by EBD and SWD</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-35</td>
<td><p>Independent System</p>
<p>(Not dependent on other BD systems)</p></td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-36</td>
<td>Logout automatically for inactive for 30 minutes</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-37</td>
<td>Centralized log Management</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-38</td>
<td>Handle around 300 user accounts of EDB and SWD for single sign
on</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="even">
<td>REQ-TR-39</td>
<td>Paper Less</td>
<td>System Admin</td>
<td>H</td>
</tr>
<tr class="odd">
<td>REQ-TR-40</td>
<td>PDF template and mapping field for letter generation.</td>
<td>System Admin</td>
<td>H</td>
</tr>
</tbody>
</table>

#### REQ-TR-01 24x7 Internet and Intranet

**Priority:**

High

**Functional Requirement:**

The system shall provide 24x7 website for AP/RSE through Internet and BD
or B/D users through Intranet/GNET. The system shall maintain higher
availability except maintenance period or exceptional handling.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-02 Integrated Cloud GCIS and On Premises

**Priority:**

High

**Functional Requirement:**

The system shall integrate GCIS in the Cloud and On Premises in BD. The
front-end functions for AP/RSE will be placed in GCIS whereas the
back-end functions for BD users will be placed in on premises in BD.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-03 Input Validation

**Priority:**

High

**Functional Requirement:**

The system shall validate all data input before storing in the system in
order to prevent security attacks such as SQL Injection.

CAPCHA for form submission will be implemented in order to prevent DDOS
attack.

Input validation is performed to ensure only properly formed data is
entering the workflow in an information system, preventing malformed
data from persisting in the database and triggering malfunction of
various downstream components.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-04 Record Relocation from GCIS to On Premises

**Priority:**

High

**Functional Requirement:**

The system shall provide function to relocate record from GCIS to on
premises.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-05 High Availability

**Priority:**

High

**Functional Requirement:**

The system shall retain high availability as possible as it can such as
active-active application server and DR capability.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-06 Monitoring and Alert Generation

**Priority:**

High

**Functional Requirement:**

A log server shall be setup to monitor server’s healthiness and alert
administrator by email in critical situations. Security Audit logs shall
also be kept in the log server. Logs shall be kept for 12 months.

System, Application, equipment will be monitoring and alert email will
be triggered if any warning and failure.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-07 DR Drill

**Priority:**

High

**Functional Requirement:**

DR Drill test will be conducted in order to test the procedures if
disaster occurs.

downtime requirements. The duration of time of Recovery Time Objective
RTO is 1 day

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-08 UTF-8, Unicode or HKSCS

**Priority:**

High

**Functional Requirement:**

The system shall support webpage using UTF-8, Unicode or ISO10646
Standard and Hong Kong Supplementary Character Set (HKSCS) coded in
ISO10646.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-09 System Logging

**Priority:**

High

**Functional Requirement:**

The system shall able to record and keep track of all functions, tasks
and processes run in the system and actions taken by all users. The
system log, user activity log and transaction log of SCS should be
produced and kept for at least 12 months and achieve all logs

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-10 High Configurable

**Priority:**

High

**Functional Requirement:**

The system shall be highly configurable in coding and avoid hard coding
as far as possible

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-11 Backup and Recovery

**Priority:**

High

**Functional Requirement:**

The system shall execute periodic backup to external storage device. The
backup schedule should be:

-   Incremental backup on a daily basis

-   Full backup on a weekly basis

Full backup shall be kept for 6 months.

Archive outdated information, when required but no more than twice per
year

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-12 Operation System and Browser Compatibility

**Priority:**

High

**Functional Requirement:**

The system shall support the following combinations of popular operating
system and browsers.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 13%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>  Operating System</strong></p>
<p><strong>Browser</strong></p></td>
<td><p><strong>Microsoft Windows </strong></p>
<p><strong>8.1</strong></p></td>
<td><strong>Microsoft Windows 10 and 11</strong></td>
<td><strong>Mac OS X</strong></td>
<td><strong>Linux</strong></td>
<td><strong>iOS</strong></td>
<td><strong>Android</strong></td>
</tr>
<tr class="even">
<td><strong>Microsoft Edge </strong></td>
<td>Not<br />
applicable</td>
<td><strong>Yes</strong></td>
<td>Not<br />
applicable</td>
<td>Not<br />
applicable</td>
<td>Not<br />
applicable</td>
<td>Not<br />
applicable </td>
</tr>
<tr class="odd">
<td><strong>Safari</strong></td>
<td>Not<br />
applicable</td>
<td>Not<br />
applicable</td>
<td><strong>Yes</strong></td>
<td>Not<br />
applicable </td>
<td><strong>Yes</strong></td>
<td>Not<br />
applicable </td>
</tr>
<tr class="even">
<td><strong>Mozilla Firefox</strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
</tr>
<tr class="odd">
<td><strong>Google Chrome </strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
<td><strong>Yes</strong></td>
</tr>
</tbody>
</table>

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-13 Review and Update Privilege

**Priority:**

High

**Functional Requirement:**

The system shall provide function to review and update user privilege.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-14 Health Check

**Priority:**

High

**Functional Requirement:**

The system shall provide function to perform health check of the system.
A health check hyperlink will be provided to System Administration to
check the system on a regular basis.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-15 Encryption on All Communications

**Priority:**

High

**Functional Requirement:**

The communication and data transfer between client and server or server
to server will be encrypted using HTTPS.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-16 Version Control for application

**Priority:**

High

**Functional Requirement:**

Programming versioning shall be maintained.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-17 Monthly Usage Statistics and Ad-hoc Statistics

**Priority:**

High

**Functional Requirement:**

1.  Allow data administrator to run “Select” SQL statement through the
    application website. Results shall be exportable as CSV excel file.
    (e.g. No contain HKID )

2.  Appendix 4 - Utilisation Survey

3.  Active and Inactive User Account Report by selection date and time

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-18 Check-in and Check-out

**Priority:**

Not applicable

**Functional Requirement:**

The system shall able to check-in or check-out documents in order to
prevent duplicate update on same document.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-19 Language Support (EN/TC/SC)

**Priority:**

High

**Functional Requirement:**

The system shall provide web page in 3 languages that is English,
Traditional Chinese and Simplified Chinese for users to choose.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-20 System Performance

**Priority:**

High

**Functional Requirement:**

The system performance will be periodically monitored in order to dig
out any performance bottleneck

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-21 Reports and statistics for monitor system performance

**Priority:**

High

**Functional Requirement:**

The reports and statistics of system performance can be generated using
system monitoring tool.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-22 Ad-hoc and periodic updates on the contents

**Priority:**

High

**Functional Requirement:**

The system allows authorized BD users to edit the case information.

Develop an automatic function to delete the records by customization

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-23 Provide refined Login & Authentication / FULL Audit features

**Priority:**

High

**Functional Requirement:**

The Login information will be record in audit and stored in database.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-24 Login user account login by user ID and password

**Priority:**

High

**Functional Requirement:**

In case the OSDP is malfunctioned, the system provide another interface
for BD/EDB/SWD users to login the system using username and password.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-25 Version control of source code

**Priority:**

High

**Functional Requirement:**

The source code of the system will be kept in Version Control System and
providing versioning support.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-26 System log tracking

**Priority:**

High

**Functional Requirement:**

The system provides logging to file for all functions and events.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-27 Scalable system frame design

**Priority:**

High

**Functional Requirement:**

The system provides High Availability (HA) in the system design so that
to minimize single point of failure. Also, it can increase the HA by
adding extra nodes whenever it needs.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-28 Data exchange with other system securely

**Priority:**

High

**Functional Requirement:**

The system will connect other system using secure method such as HTTPS
if it is applicable.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-29 Security measurement

**Priority:**

High

**Functional Requirement:**

The system will be designed with security in first priority and security
control will be added in different layers such as application, network,
database…etc.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-30 Help check email notification

**Priority:**

High

**Functional Requirement:**

The system will send email notification using internal BD email server
and external GCIS email server. The email server should be monitored by
system administrator.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-31 Email notification for all batch jobs

**Priority:**

High

**Functional Requirement:**

Once the batch job is finished, an email notification will be sent to
system administrator.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-32 Conform to the Interoperability Framework

**Priority:**

High

**Functional Requirement:**

The system is designed and developed using standard and well-design
application framework i.e. .Net 6

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-33 Manage System Parameters

**Priority:**

High

**Functional Requirement:**

The system parameters will be placed in configuration file and will not
hardcode in the coding.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-34 Allow System Access by EDB and SWD

**Priority:**

High

**Functional Requirement:**

The EDB/SWD users are required to login their OSDP and access SCS. The
user authorization control will be maintained in SCS.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-35 Independent System (Not depended on other BD system)

**Priority:**

High

**Functional Requirement:**

The system is designed to separate the front-end program for
applicant/AP/RSE and the back-end program for internal BD users. Also,
the system will be run independently no matter there were down time of
other system, except BCIS.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-36 Logout automatically for inactive for 30 minutes

**Priority:**

High

**Functional Requirement:**

For SSO users, the logout will be done on ODSP. For special case i.e.
login using username and password, the system will terminate the session
after a certain time such as 30 mins.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-37 Centralized log management

**Priority:**

High

**Functional Requirement:**

The log files will be stored in centralized folder if it is applicable

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-38 Handle around 300 user accounts of EDB and SWD for Single Sign On

**Priority:**

High

**Functional Requirement:**

The system will be tested to handle concurrent users to access SCS. In
case there is any bottleneck in hardware level, it can increase the
throughput by adding more nodes.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-39 Paper Less

**Priority:**

High

**Functional Requirement:**

The system will generate and save different documents in the system and
BD users will keep the documents in hard copy of the filing system.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

#### REQ-TR-40 PDF template and mapping field for letter generation

**Priority:**

High

**Functional Requirement:**

The generated documents will be in PDF format.

**Non-functional Requirement:**

Nil

**Frequency of use:**

Ad-hoc

# CONSTRAINTS LIST 

Constraints list identifies any possible constraints and impacts to
system design and implementation of the proposed system.

## Complexity of Address Identification

Due to complexity of address identification, the system may not be able
to create case. In this connection, the case creation will be passed to
BCIS. Once the application was created in BCIS, the data will be sent
back to SCS for workflow process.

## Signature of AP/RSE

When applicant sends application by post, the system shall verify the
AP/RSE information provided by MWMS 2.0. However, the hand writing
signature needs to be verified by Registry using eyeball.

# Appendix 1 – 3-Tier BSR System

<img src="media/image15.emf" style="width:6.625in;height:4.68125in" />

# Appendix 2 – Sample of School and CCC Certificates and Notices

<img src="media/image16.emf" style="width:4.90205in;height:6.93443in"
alt="/Users/jeffreyman/Downloads/bd/TPCS/from bd/existing workflows/Notice &amp; Cert (Sch).pdf" />

<img src="media/image17.emf" style="width:5.25551in;height:7.43443in"
alt="/Users/jeffreyman/Downloads/bd/TPCS/from bd/existing workflows/Cert (CCC).pdf" />

# Appendix 3 – Sample of Letter of Requirement (LoR)

<img src="media/image18.emf" style="width:5.45252in;height:7.71311in"
alt="/Users/jeffreyman/Downloads/bd/TPCS/from bd/existing workflows/Bldg safety req&#39;t (Sch).pdf" />

# Appendix 4 –Information Security Requirement 

| \#                          | Item                                                                                                                                                                                                                                            |
|----------|--------------------------------------------------------------|
| Network security controls　 |                                                                                                                                                                                                                                                 |
| 1                           | Ensure all unnecessary services are disabled in the network devices (e.g. unnecessary ping traffic and requests from unauthorised network ports)                                                                                                |
| 2                           | Ensure administrative consoles are not Internet-accessible and/or can only be accessible from trusted addresses.                                                                                                                                |
| 3                           | Ensure networks are properly segregated so that critical and normal services can utilise different network connections.                                                                                                                         |
| 4                           | Review firewall rules, intrusion detection and protection systems and remove obsolete rules or established connections, especially for temporary rules that may have been left beyond their expected lifetime.                                  |
| 5                           | Review DDoS response plans including roles and responsibilities for various stakeholders (e.g. ISP and anti-DDoS service providers), internal procedures and escalation protocols etc.                                                          |
| 6                           | Check that networks protected by a content delivery network (CDN) solution only allow incoming traffic from the specific source IP addresses of the CDN and the original Internet-facing IP addresses are not disclosed to unauthorised parties |
| Endpoint protection　       |                                                                                                                                                                                                                                                 |
| 7                           | Ensure anti-malware software is installed and confirm that it is active on all systems and that signatures are updating correctly.                                                                                                              |
| 8                           | Ensure the latest security patches are applied to the operating systems and applications, in particular for Internet-facing systems and websites.                                                                                               |
| Access controls　           |                                                                                                                                                                                                                                                 |
| 9                           | Review user accounts and remove any obsolete accounts. If multi-factor authentication (MFA) is enabled, check if it is properly configured.                                                                                                     |
| 10                          | Carefully review the user privileges and activities so as to identify and cease suspicious users from gaining unauthorised access.  Management may tighten user privilege and grant permissions only when strictly necessary.                   |
| 11                          | Ensure strong password policy is adopted, in particular for all mission ciritical sytems and information systems containing classified data.                                                                                                    |
| Logging and monitoring　    |                                                                                                                                                                                                                                                 |
| 12                          | Review the existing logging mechianism to ensure sufficient logs are retained.  For email systems and internet access service, ensure that your logs are kept for at least six months.                                                          |
| 13                          | Ensure all security solutions including intrusion detection/prevention system (IDPS) and web application firewall (WAF), are properly configured for identifying and reporting any suspicious activities.                                       |
| 14                          | Ensure log records are in place with regular checking, especially for alerts generated by anti-malware and security solutions.                                                                                                                  |
| 15                          | Allocate sufficient manpower and resources for monitoring and responding to potential cyber attacks.                                                                                                                                            |
| Backup　                    |                                                                                                                                                                                                                                                 |
| 16                          | Ensure backups of data and systems are reliable and secure.  Perform restoration tests from your backups to assure speedy system recovery.                                                                                                      |
| 17                          | Ensure multiple generations of offline backups are maintained and detached from the network and system.                                                                                                                                         |
| Incident response　         |                                                                                                                                                                                                                                                 |
| 18                          | Review the existing incident response procedure is up to date and confirm that escalation routes and contact details are all up to date.                                                                                                        |
| 19                          | Ensure the escalated incident response plan covers web defacement apart from typical cyber attacks.                                                                                                                                             |
| 20                          | Review the inventory list of the IT systems, important assets and keys for effective monitoring and resources management in emergency situations is up to date                                                                                  |

# Appendix 5 –Sample of Utilisation Report

<img src="media/image19.png" style="width:6.625in;height:0.77222in" />

\<\<\< End of document \>\>\>
