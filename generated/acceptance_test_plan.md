## Table Formatting and UAT Plan Generation

Here's the output, including the formatted tables and the generated UAT plan:

**code.txt (No changes needed)**

This file does not contain tables requiring markdown formatting.

**urs_a1.md (No changes needed)**

This file does not contain tables requiring markdown formatting.

**uatp_i2.md (Tables formatted, UAT plan generated below)**

```markdown
<img src="media/image1.jpg" style="width:2.03125in;height:1.52083in"
alt="BDlogo" />

**USER ACCEPTANCE TEST PLAN**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR PILOT PROJECT OF**

**COMMON DIGITAL PLATFORM FOR SITE SUPERVISION
(CDPSS)**

**FOR THE**

**BUILDINGS DEPARTMENT**

Version 1.0

**April 2024**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR

| **Distribution** |                                    |
|------------------|------------------------------------|
| Copy No.         | Holder                             |
| 1                | Buildings Department (BD)          |
| 2                | Master Concept (Hong Kong) Limited |

| **Amendment History** |                      |                                      |                           |           |                    |
|-----------------------|----------------------|---------------------------------------|---------------------------|-----------|--------------------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date      | Approval Reference |
| 1                     | Baseline             |                                      | 1.0                       | 16/4/2024 |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |

|                   |                                           |
|-------------------|-------------------------------------------|
| Prepared By:      | Endorsed By:                            |
| Kenny Lam         | .                                         |
| Project Manager   | Buildings Department                      |
| Master Concept    |                                           |
| Date: 16/4/2024 | Date:                                     |

**TABLE OF CONTENTS**

[1 Introduction [9](#introduction)](#introduction)

[1.1. Objectives of the UAT [9](#_Toc159861217)](#_Toc159861217)

[1.2. Schedule [9](#_Toc159861218)](#_Toc159861218)

[2 Testing Environment [9](#_Toc159861219)](#_Toc159861219)

[2.1 Testing Location [9](#_Toc159861220)](#_Toc159861220)

[2.2 Hardware and Software Requirement
[9](#_Toc159861221)](#_Toc159861221)

[3 Test Case for Web [10](#test-case-for-web)](#test-case-for-web)

[3.1 User Management [10](#user-management)](#user-management)

[3.1.1 Public User registration
[10](#public-user-registration)](#public-user-registration)

[3.1.2 Public login [13](#public-login)](#public-login)

[3.1.3 User Management - Others
[19](#user-management---others)](#user-management---others)

[3.2 Site Projects and Supervision Plan Management
[20](#site-projects-and-supervision-plan-management)](#site-projects-and-supervision-plan-management)

[3.2.1 Search Responsible Site Project
[20](#search-responsible-site-project)](#search-responsible-site-project)

[3.2.2 Create new Site Project
[22](#create-new-site-project)](#create-new-site-project)

[3.2.3 Edit and update Site Project Detail
[24](#edit-and-update-site-project-detail)](#edit-and-update-site-project-detail)

[3.2.4 List out Site Project
[25](#list-out-site-project)](#list-out-site-project)

[3.2.5 View Site Project Detail
[25](#view-site-project-detail)](#view-site-project-detail)

[3.2.6 Supervision Plan Detail View
[26](#supervision-plan-detail-view)](#supervision-plan-detail-view)

[3.2.7 Supervision Plan Detail Management
[28](#supervision-plan-detail-management)](#supervision-plan-detail-management)

[3.3 TCP management [30](#tcp-management)](#tcp-management)

[3.3.1 Assign TCPs [30](#assign-tcps)](#assign-tcps)

[3.3.2 Request TCP acceptance
[32](#request-tcp-acceptance)](#request-tcp-acceptance)

[3.3.3 Unassign TCPs [33](#unassign-tcps)](#unassign-tcps)

[3.3.4 Temporary replacement of TCP
[34](#temporary-replacement-of-tcp)](#temporary-replacement-of-tcp)

[3.4 Form A [35](#form-a)](#form-a)

[3.4.1 Create Form A template
[35](#create-form-a-template)](#create-form-a-template)

[3.4.2 Create Form A [36](#create-form-a)](#create-form-a)

[3.4.3 Fill Form A [38](#fill-form-a)](#fill-form-a)

[3.4.4 Upload PDF, PNG on Form A and Quality Supervision Form (PNAP
APP-158 Appendix B) ("Form APP-158?)
[42](#upload-pdf-png-on-form-a-and-quality-supervision-form-pnap-app-158-appendix-b-form-app-158)](#upload-pdf-png-on-form-a-and-quality-supervision-form-pnap-app-158-appendix-b-form-app-158)

[3.4.5 View Form A Result and History
[43](#_Toc159861245)](#_Toc159861245)

[3.4.6 Download, Import and Export Records
[44](#download-import-and-export-records)](#download-import-and-export-records)

[3.5 Form B [46](#form-b)](#form-b)

[3.5.1 Create Form B [46](#create-form-b)](#create-form-b)

[3.5.3 Save Form B Part 1 as Draft
[49](#save-form-b-part-1-as-draft)](#save-form-b-part-1-as-draft)

[3.5.5 Upload attachments when Form B Part 1 is Saved as Draft
[52](#upload-attachments-when-form-b-part-1-is-saved-as-draft)](#upload-attachments-when-form-b-part-1-is-saved-as-draft)

[3.5.6 Complete Form B Part 1 [53](#_Toc159861251)](#_Toc159861251)

[3.5.7 Upload attachments when Form B Part 1 is Completed
[54](#upload-attachments-when-form-b-part-1-is-completed)](#upload-attachments-when-form-b-part-1-is-completed)

[3.5.8 Save Response to Form B Part 1 as Draft
[54](#save-response-to-form-b-part-1-as-draft)](#save-response-to-form-b-part-1-as-draft)

[3.5.9 Complete Response to Form B Part 1
[55](#complete-response-to-form-b-part-1)](#complete-response-to-form-b-part-1)

[3.5.11 Report Imminent Danger to BD in Form B Part 1
[57](#report-imminent-danger-to-bd-in-form-b-part-1)](#report-imminent-danger-to-bd-in-form-b-part-1)

[3.5.12 Save Form B Part 2 as Draft
[58](#save-form-b-part-2-as-draft)](#save-form-b-part-2-as-draft)

[3.5.13 Report RC fail to comply and Material Concern to BD
[59](#report-rc-fail-to-comply-and-material-concern-to-bd)](#report-rc-fail-to-comply-and-material-concern-to-bd)

[3.5.14 Upload attachment when Form B Part 2 is Saved as Draft
[61](#upload-attachment-when-form-b-part-2-is-saved-as-draft)](#upload-attachment-when-form-b-part-2-is-saved-as-draft)

[3.5.15 Complete Form B Part 2
[62](#complete-form-b-part-2)](#complete-form-b-part-2)

[3.5.16 Save Response to Form B Part 2 as Draft
[63](#save-response-to-form-b-part-2-as-draft)](#save-response-to-form-b-part-2-as-draft)

[3.5.17 Complete Response to Form B Part 2
[64](#complete-response-to-form-b-part-2)](#complete-response-to-form-b-part-2)

[3.5.18 Report Imminent Danger to BD in Form B Part 2
[65](#report-imminent-danger-to-bd-in-form-b-part-2)](#report-imminent-danger-to-bd-in-form-b-part-2)

[3.6 PNAP APP-158 Appendix B (Record of Quality Supervision)
[66](#pnap-app-158-appendix-b-record-of-quality-supervision)](#pnap-app-158-appendix-b-record-of-quality-supervision)

[3.6.1 Create PNAP APP-158 template
[67](#create-pnap-app-158-template)](#create-pnap-app-158-template)

[3.6.3 Create PNAP APP-158 Draft
[69](#create-pnap-app-158-draft)](#create-pnap-app-158-draft)

[3.6.5 File PNAP APP-158 [71](#file-pnap-app-158)](#file-pnap-app-158)

[3.6.6 Upload PDF, PNG on PNAP APP-158
[71](#upload-pdf-png-on-pnap-app-158)](#upload-pdf-png-on-pnap-app-158)

[3.6.8 View PNAP APP-158 Result and History
[75](#view-pnap-app-158-result-and-history)](#view-pnap-app-158-result-and-history)

[3.6.9 Download PNAP APP-158 Import Template
[77](#download-pnap-app-158-import-template)](#download-pnap-app-158-import-template)

[3.6.10 Import PNAP APP-158 Records
[79](#import-pnap-app-158-records)](#import-pnap-app-158-records)

[3.8 Users Details Management
[83](#users-details-management)](#users-details-management)

[3.8.1 Search Public User
[83](#search-public-user)](#search-public-user)

[3.8.2 Edit Public User [84](#edit-public-user)](#edit-public-user)

[3.8.3 Inactivate Public User
[85](#inactivate-public-user)](#inactivate-public-user)

[3.8.4 Activate Public User
[87](#activate-public-user)](#activate-public-user)

[3.8.6 View Public User responsible site projects as Head of Stream
[89](#view-public-user-responsible-site-projects-as-head-of-stream)](#view-public-user-responsible-site-projects-as-head-of-stream)

[3.8.8 Removal of Head of Stream by BD admin due to resignation or
removal from Register
[91](#removal-of-head-of-stream-by-bd-admin-due-to-resignation-or-removal-from-register)](#removal-of-head-of-stream-by-bd-admin-due-to-resignation-or-removal-from-register)

[3.9 Site-monitoring [92](#_Toc159861278)](#_Toc159861278)

[3.9.1 Create site-monitoring scheme
[93](#create-site-monitoring-scheme)](#create-site-monitoring-scheme)

[3.9.2 Edit Site-monitoring scheme (3A level)
[95](#edit-site-monitoring-scheme-3a-level)](#edit-site-monitoring-scheme-3a-level)

[3.9.3 Edit Site-monitoring scheme (adding monitoring points)
[97](#edit-site-monitoring-scheme-adding-monitoring-points)](#edit-site-monitoring-scheme-adding-monitoring-points)

[3.9.4 Edit Site-monitoring scheme (adding monitoring points)
[97](#edit-site-monitoring-scheme-adding-monitoring-points-1)](#edit-site-monitoring-scheme-adding-monitoring-points-1)

[3.9.5 Save measurement records as Draft
[98](#save-measurement-records-as-draft)](#save-measurement-records-as-draft)

[3.9.6 Download the import measurement template
[101](#download-the-import-measurement-template)](#download-the-import-measurement-template)

[3.9.7 Import the measurement records
[102](#import-the-measurement-records)](#import-the-measurement-records)

[3.9.8 File/amend measurement records
[103](#fileamend-measurement-records)](#fileamend-measurement-records)

[3.9.9 View site-monitoring measurement record results
[106](#view-site-monitoring-measurement-record-results)](#view-site-monitoring-measurement-record-results)

[3.9.10 Filter on Site-monitoring records view
[106](#filter-on-site-monitoring-records-view)](#filter-on-site-monitoring-records-view)

[3.9.11 View measurement record history
[107](#view-measurement-record-history)](#view-measurement-record-history)

[3.10 BD Internal Login as BD Officer
[109](#bd-internal-login-as-bd-officer)](#bd-internal-login-as-bd-officer)

[3.10.1 Departmental Login
[109](#departmental-login)](#departmental-login)

[3.10.2 BD Internal User Detail Management
[111](#bd-internal-user-detail-management)](#bd-internal-user-detail-management)

[3.11 BD Internal Users Details Management
[113](#bd-internal-users-details-management)](#bd-internal-users-details-management)

[3.11.1 Search BD Internal Users
[113](#search-bd-internal-users)](#search-bd-internal-users)

[3.11.2 Create BD Internal User
[114](#create-bd-internal-user)](#create-bd-internal-user)

[3.11.3 Edit BD Internal User
[115](#edit-bd-internal-user)](#edit-bd-internal-user)

[3.12 iAM Smart Integration
[117](#iam-smart-integration)](#iam-smart-integration)

[3.12.1 Login via iAM Smart
[117](#login-via-iam-smart)](#login-via-iam-smart)

[3.13 Notification [119](#notification)](#notification)

[3.13.1 View Notification List
[119](#view-notification-list)](#view-notification-list)

[3.13.2 View Notification Details
[121](#view-notification-details)](#view-notification-details)

[3.13.4 Clickable Link in Notification
[122](#clickable-link-in-notification)](#clickable-link-in-notification)

[3.13.6 Manage and opt-out email notification
[123](#manage-and-opt-out-email-notification)](#manage-and-opt-out-email-notification)

[3.14 Information Reports
[125](#information-reports)](#information-reports)

[3.14.1 Report for List of Heads of Stream and their Responsible Sites
[125](#report-for-list-of-heads-of-stream-and-their-responsible-sites)](#report-for-list-of-heads-of-stream-and-their-responsible-sites)

[3.14.2 Report for List of TCPs and assigned sites/supervision plans
[127](#report-for-list-of-tcps-and-assigned-sitessupervision-plans)](#report-for-list-of-tcps-and-assigned-sitessupervision-plans)

[3.14.3 Report for List of non-conformities (Form B)
[128](#report-for-list-of-non-conformities-form-b)](#report-for-list-of-non-conformities-form-b)

[3.14.4 Report for List of inspection records of Form APP-158
[129](#report-for-list-of-inspection-records-of-form-app-158)](#report-for-list-of-inspection-records-of-form-app-158)

[3.14.5 Report for List of inspection records of Form A
[130](#report-for-list-of-inspection-records-of-form-a)](#report-for-list-of-inspection-records-of-form-a)

[3.14.6 Report for List of Supervision Plans (SP)
[131](#report-for-list-of-supervision-plans-sp)](#report-for-list-of-supervision-plans-sp)

[3.14.7 Report for List of Sites
[133](#report-for-list-of-sites)](#report-for-list-of-sites)

[3.14.8 Report for List of site-monitoring records with 3A levels filter
[134](#report-for-list-of-site-monitoring-records-with-3a-levels-filter)](#report-for-list-of-site-monitoring-records-with-3a-levels-filter)

[3.15 Activities Reports
[135](#activities-reports)](#activities-reports)

[3.15.1 Report for Monitoring Point
[135](#report-for-monitoring-point)](#report-for-monitoring-point)

[3.15.2 Report for 3A level changes
[136](#report-for-3a-level-changes)](#report-for-3a-level-changes)

[3.15.3 Report for List of site-monitoring activities
[136](#report-for-list-of-site-monitoring-activities)](#report-for-list-of-site-monitoring-activities)

[3.15.4 Report for List of inspection item checklist changes
[137](#report-for-list-of-inspection-item-checklist-changes)](#report-for-list-of-inspection-item-checklist-changes)

[3.15.5 Report for List of site activities
[138](#report-for-list-of-site-activities)](#report-for-list-of-site-activities)

[3.16 Notification reports
[139](#notification-reports)](#notification-reports)

[3.16.1 Report for List of site inspection reminders
[139](#report-for-list-of-site-inspection-reminders)](#report-for-list-of-site-inspection-reminders)

[3.16.2 Report for list of site inspection notifications
[139](#report-for-list-of-site-inspection-notifications)](#report-for-list-of-site-inspection-notifications)

[3.16.3 Report for List of site-monitoring alerts
[140](#report-for-list-of-site-monitoring-alerts)](#report-for-list-of-site-monitoring-alerts)

[3.17 Unfiled Record Reminder
[141](#unfiled-record-reminder)](#unfiled-record-reminder)

[3.17.1 Unfiled Record Reminder for Level 5 Frequency of Inspection
[141](#unfiled-record-reminder-for-level-5-frequency-of-inspection)](#unfiled-record-reminder-for-level-5-frequency-of-inspection)

[3.18 Batch file for site monitoring records
[142](#batch-file-for-site-monitoring-records)](#batch-file-for-site-monitoring-records)

[3.18.1 Unfiled Record Reminder for Level 5 Frequency of Inspection
[142](#unfiled-record-reminder-for-level-5-frequency-of-inspection-1)](#unfiled-record-reminder-for-level-5-frequency-of-inspection-1)

[3.19 Create, Update and Remove BD Officer from Site Project
[143](#create-update-and-remove-bd-officer-from-site-project)](#create-update-and-remove-bd-officer-from-site-project)

[3.20 New Type of Monitoring for Site Monitoring
[145](#new-type-of-monitoring-for-site-monitoring)](#new-type-of-monitoring-for-site-monitoring)

[4. Test Case for Mobile
[146](#test-case-for-mobile)](#test-case-for-mobile)

[4.1. User Management [146](#user-management-1)](#user-management-1)

[4.1.1. Public User registration
[146](#public-user-registration-1)](#public-user-registration-1)

[4.1.2. Public login [155](#public-login-1)](#public-login-1)

[4.1.3. User Management - Others
[162](#user-management---others-1)](#user-management---others-1)

[4.2. Site Projects and Supervision Plan management
[170](#site-projects-and-supervision-plan-management-1)](#site-projects-and-supervision-plan-management-1)

[4.2.1. Search responsible Site Project
[170](#search-responsible-site-project-1)](#search-responsible-site-project-1)

[4.2.2. Create Site Project from submitted Supervision plan
[171](#create-site-project-from-submitted-supervision-plan)](#create-site-project-from-submitted-supervision-plan)

[4.2.3. Edit and update Site Project Detail
[172](#edit-and-update-site-project-detail-1)](#edit-and-update-site-project-detail-1)

[4.2.4. Create Supervision Plan under a Site Project
[175](#_Toc159861338)](#_Toc159861338)

[4.2.5. Supervision Plan Detail View
[177](#_Toc159861339)](#_Toc159861339)

[4.3. Form A [179](#form-a-1)](#form-a-1)

[4.3.1. Create Form A template
[179](#create-form-a-template-1)](#create-form-a-template-1)

[4.3.2. Create Form A [182](#create-form-a-1)](#create-form-a-1)

[4.3.3. File Form A [185](#file-form-a)](#file-form-a)

[4.4. Form B [189](#form-b-1)](#form-b-1)

[4.4.1. Create Form B [189](#create-form-b-1)](#create-form-b-1)

[4.4.2. Save Form B Part 1 as Draft
[192](#save-form-b-part-1-as-draft-1)](#save-form-b-part-1-as-draft-1)

[4.4.3. Upload attachments when Form B Part 1 is Saved as Draft
[195](#upload-attachments-when-form-b-part-1-is-saved-as-draft-1)](#upload-attachments-when-form-b-part-1-is-saved-as-draft-1)

[4.4.4. Complete Form B Part 1 [196](#_Toc159861348)](#_Toc159861348)

[4.4.5. Upload attachments when Form B Part 1 is Completed
[198](#upload-attachments-when-form-b-part-1-is-completed-1)](#upload-attachments-when-form-b-part-1-is-completed-1)

[4.4.6. Save Response to Form B Part 1 as Draft
[199](#save-response-to-form-b-part-1-as-draft-1)](#save-response-to-form-b-part-1-as-draft-1)

[4.4.7. Complete Response to Form B Part 1
[201](#complete-response-to-form-b-part-1-1)](#complete-response-to-form-b-part-1-1)

[4.4.8. Report Imminent Danger to BD in Form B Part 1
[203](#report-imminent-danger-to-bd-in-form-b-part-1-1)](#report-imminent-danger-to-bd-in-form-b-part-1-1)

[4.4.9. Save Form B Part 2 as Draft
[204](#_Toc159861353)](#_Toc159861353)

[4.4.10. Report RC fail to comply and Material Concern to BD
[207](#report-rc-fail-to-comply-and-material-concern-to-bd-1)](#report-rc-fail-to-comply-and-material-concern-to-bd-1)

[4.4.11. Upload attachment when Form B Part 2 is Saved as Draft
[209](#upload-attachment-when-form-b-part-2-is-saved-as-draft-1)](#upload-attachment-when-form-b-part-2-is-saved-as-draft-1)

[4.4.12. Complete Form B Part 2
[210](#complete-form-b-part-2-1)](#complete-form-b-part-2-1)

[4.4.13. Save Response to Form B Part 2 as Draft
[211](#save-response-to-form-b-part-2-as-draft-1)](#save-response-to-form-b-part-2-as-draft-1)

[4.4.14. Complete Response to Form B Part 2
[212](#complete-response-to-form-b-part-2-1)](#complete-response-to-form-b-part-2-1)

[4.4.15. Report Imminent Danger to BD in Form B Part 2
[214](#report-imminent-danger-to-bd-in-form-b-part-2-1)](#report-imminent-danger-to-bd-in-form-b-part-2-1)

[4.5. PNAP APP-158 Appendix B (Record of Quality Supervision)
[215](#pnap-app-158-appendix-b-record-of-quality-supervision-1)](#pnap-app-158-appendix-b-record-of-quality-supervision-1)

[4.5.1. Create PNAP APP-158 template
[216](#create-pnap-app-158-template-1)](#create-pnap-app-158-template-1)

[4.5.2. Create PNAP APP-158 Draft
[219](#create-pnap-app-158-draft-1)](#create-pnap-app-158-draft-1)

[4.5.3. File PNAP APP-158
[222](#file-pnap-app-158-1)](#file-pnap-app-158-1)

[4.5.4. Upload PDF, PNG on PNAP APP-158
[223](#_Toc159861364)](#_Toc159861364)

[4.5.5. View PNAP APP-158 Result and History
[225](#view-pnap-app-158-result-and-history-1)](#view-pnap-app-158-result-and-history-1)

[4.6. Site-monitoring [226](#site-monitoring-1)](#site-monitoring-1)

[4.6.1. Create site-monitoring scheme
[226](#create-site-monitoring-scheme-1)](#create-site-monitoring-scheme-1)

[4.6.2. Edit Site-monitoring scheme (3A level)
[229](#edit-site-monitoring-scheme-3a-level-1)](#edit-site-monitoring-scheme-3a-level-1)

[4.6.3. Edit Site-monitoring scheme (adding monitoring points)
[230](#_Toc159861369)](#_Toc159861369)

[4.6.4. Edit Site-monitoring scheme (adding monitoring points)
[231](#_Toc159861370)](#_Toc159861370)

[4.6.5. Save measurement records as Draft
[232](#save-measurement-records-as-draft-1)](#save-measurement-records-as-draft-1)

[4.6.6. File/amend measurement records
[235](#_Toc159861372)](#_Toc159861372)

[4.6.7. View site-monitoring measurement record results
[237](#view-site-monitoring-measurement-record-results-1)](#view-site-monitoring-measurement-record-results-1)

[4.6.8. Filter on Site-monitoring records view
[238](#filter-on-site-monitoring-records-view-1)](#filter-on-site-monitoring-records-view-1)

[4.6.9. View measurement record history
[240](#view-measurement-record-history-1)](#view-measurement-record-history-1)

[4.7. BD Internal Login as BD Officer
[242](#bd-internal-login-as-bd-officer-1)](#bd-internal-login-as-bd-officer-1)

[4.7.1. Login with Time-based One Time Password
[242](#login-with-time-based-one-time-password)](#login-with-time-based-one-time-password)

[4.8. iAM Smart Integration
[243](#iam-smart-integration-1)](#iam-smart-integration-1)

[4.8.1. Login via iAM Smart
[243](#login-via-iam-smart-1)](#login-via-iam-smart-1)

[4.9. Notification [248](#notification-1)](#notification-1)

[4.9.1. View Notification List
[248](#view-notification-list-1)](#view-notification-list-1)

[4.9.2. View Notification Details
[251](#view-notification-details-1)](#view-notification-details-1)

[4.9.3. Clickable Link in Notification
[253](#clickable-link-in-notification-1)](#clickable-link-in-notification-1)

[4.9.4. Manage and opt-out email notification
[255](#manage-and-opt-out-email-notification-1)](#manage-and-opt-out-email-notification-1)

[4.10. Information Reports
[257](#information-reports-1)](#information-reports-1)

[4.10.1. Report for List of Heads of Stream and their Responsible Sites
[257](#report-for-