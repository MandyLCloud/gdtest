<img src="media/image1.jpg" style="width:2.03125in;height:1.52083in"
alt="BDlogo" />

**USER ACCEPTANCE TEST PLAN**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">COMBINED SYSTEM DEVELOPMENT SERVICES</span>**

**<span class="smallcaps">FOR PILOT PROJECT OF</span>**

**<span class="smallcaps">COMMON DIGITAL PLATFORM FOR SITE SUPERVISION
(CDPSS)</span>**

**<span class="smallcaps">FOR THE</span>**

**<span class="smallcaps">BUILDINGS DEPARTMENT</span>**

Version 1.0

**April 2024**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR

|                  |                                    |
|------------------|------------------------------------|
| **Distribution** |                                    |
| Copy No.         | Holder                             |
| 1                | Buildings Department (BD)          |
| 2                | Master Concept (Hong Kong) Limited |

|                       |                      |                                      |                           |           |                    |
|----------|-------------------------|---------|---------|-----------|---------|
| **Amendment History** |                      |                                      |                           |           |                    |
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

<table>
<colgroup>
<col style="width: 47%" />
<col style="width: 52%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Prepared By: <u>Kenny Lam</u></p>
<p>Project Manager</p>
<p>Master Concept (Hong Kong) Limited</p></td>
<td><p>Endorsed By: <u>.</u></p>
<p>Buildings Department</p></td>
</tr>
<tr class="even">
<td>Date: <u>16/4/2024</u></td>
<td>Date:</td>
</tr>
</tbody>
</table>

**  
**

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
APP-158 Appendix B) ("Form APP-158”)
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
[257](#report-for-list-of-heads-of-stream-and-their-responsible-sites-1)](#report-for-list-of-heads-of-stream-and-their-responsible-sites-1)

[4.10.2. Report for List of TCPs and assigned sites/supervision plans
[260](#report-for-list-of-tcps-and-assigned-sitessupervision-plans-1)](#report-for-list-of-tcps-and-assigned-sitessupervision-plans-1)

[4.10.3. Report for List of non-conformities (Form B)
[261](#report-for-list-of-non-conformities-form-b-1)](#report-for-list-of-non-conformities-form-b-1)

[4.10.4. Report for List of inspection records of Form APP-158
[262](#report-for-list-of-inspection-records-of-form-app-158-1)](#report-for-list-of-inspection-records-of-form-app-158-1)

[4.10.5. Report for List of inspection records of Form A
[263](#report-for-list-of-inspection-records-of-form-a-1)](#report-for-list-of-inspection-records-of-form-a-1)

[4.10.6. Report for List of Supervision Plans (SP)
[264](#report-for-list-of-supervision-plans-sp-1)](#report-for-list-of-supervision-plans-sp-1)

[4.10.7. Report for List of Sites
[265](#report-for-list-of-sites-1)](#report-for-list-of-sites-1)

[4.11. Activities Reports
[266](#activities-reports-1)](#activities-reports-1)

[4.11.1. Report for Monitoring Point
[266](#report-for-monitoring-point-1)](#report-for-monitoring-point-1)

[4.11.2. Report for 3A level changes
[267](#report-for-3a-level-changes-1)](#report-for-3a-level-changes-1)

[4.11.3. Report for List of site-monitoring activities
[268](#report-for-list-of-site-monitoring-activities-1)](#report-for-list-of-site-monitoring-activities-1)

[4.11.4. Report for List of inspection item checklist changes
[269](#report-for-list-of-inspection-item-checklist-changes-1)](#report-for-list-of-inspection-item-checklist-changes-1)

[4.11.5. Report for List of site activities
[269](#report-for-list-of-site-activities-1)](#report-for-list-of-site-activities-1)

[4.12. Unfiled Record Reminder
[270](#unfiled-record-reminder-1)](#unfiled-record-reminder-1)

[5.User Acceptance Test Results
[272](#user-acceptance-test-results)](#user-acceptance-test-results)

[Appendix 1 – User Acceptance Test Incident Report
[272](#appendix-1-user-acceptance-test-incident-report)](#appendix-1-user-acceptance-test-incident-report)

# Introduction

This document is the User Acceptance Test Plan (UATP) for Combined
System Development Services for the Pilot Project of Common Digital
Platform for Site Supervision of the Buildings Department.

## Objectives of the UAT

It is helpful to know the definition of UAT and the purpose of it.
Therefore, the objectives of the User Acceptance Test should be agreed
upon in advance. The objectives of the UAT are

-   Checking that the delivered functionality works in BD’s specific
    domain.

-   Checking that all functionality required has been delivered.

-   Checking that the delivered functionality works according to
    specified and approved scope and requirements.

## Schedule 

|                                   |             |             |             |             |
|-------------------|------------|-------------|-------------|-----------------|
| Items                             | Planned     |             | Actual      |             |
| Test Plan                         | 17 Mar 2023 | 7 Apr 2023  | 17 Mar 2023 | 7 Apr 2023  |
| Round 1                           | 17 Apr 2023 | 28 Apr 2023 | 17 Apr 2023 | 28 Apr 2023 |
| Round 1 Fix                       | 1 May 2023  | 6 Jun 2023  | 1 May 2023  | 6 Jun 2023  |
| Round 2                           | 7 Jun 2023  | 23 Jun 2023 | 7 Jun 2023  | 23 Jun 2023 |
| Round2 Fix                        | 26 Jun 2023 | 3 Jul 2023  | 26 Jun 2023 | 3 Jul 2023  |
| Round 3                           | 5 Jul 2023  | 28 Jul 2023 | 5 Jul 2023  | 28 Jul 2023 |
| Round 3 Fix                       | 31 Jul 2023 | 4 Aug 2023  | 31 Jul 2023 | 4 Aug 2023  |
| Round 4                           | 7 Aug 2023  | 25 Aug 2023 | 7 Aug 2023  | 25 Aug 2023 |
| Round 4 Fix                       | 28 Aug 2023 | 22 Sep 2023 | 28 Aug 2023 | 22 Sep 2023 |
| Round 5                           | 25 Sep 2023 | 13 Oct 2023 | 25 Sep 2023 | 30 Oct 2023 |
| Round 5 Fix                       | 16 Oct 2023 | 25 Oct 2023 | 1 Nov 2023  | 7 Nov 2023  |
| Presentation to Senior Management | 17 Oct 2023 | 17 Oct 2023 | 17 Oct 2023 | 17 Oct 2023 |
| UAT Acceptance                    | 26 Oct 2023 | 30 Oct 2023 | 8 Nov 2023  | 6 Dec 2023  |

# Testing Environment

## Testing Location 

The User Acceptance Test will be performed at BD’s premises under the
UAT environment located in BD office at WKGO.

## Hardware and Software Requirement

Hardware and software of non-production environments should be used for
UAT.

# Test Case for Web

## User Management

### Public User registration

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.1</td>
<td><blockquote>
<p>TCP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>successful case for registering new account</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester clicks the “Register” button on the system login
page.</p></li>
<li><p>Tester inputs the below information to the relevant fields for
registering the new account as TCP role</p>
<ol type="a">
<li><p>User Family Name (English) – Chan</p></li>
<li><p>User Given Name (English) – Tai Man</p></li>
<li><p>User Name (中文) – 陳大文</p></li>
<li><p>Password – Aa@123456</p></li>
<li><p>Confirm Password – Aa@123456</p></li>
<li><p>HK Identity Card Number - P924916(1)</p></li>
<li><p>Email address - <a
href="mailto:peter.chan@hotmail.com"><u>peter.chan@hotmail.com</u></a></p></li>
</ol></li>
<li><p>Tester clicks “Technically Competent Person (TCP)” box in
“Qualification” session</p></li>
<li><p>Tester gets into the registered email box and clicks on the
activation link</p></li>
<li><p>Tester clicks “Login” button on the page redirected from the
activation link</p></li>
<li><p>Tester input the email address and password</p></li>
</ol>
<p><img src="media/image2.png"
style="width:6.63542in;height:3.72222in" /></p>
<p><img src="media/image3.png"
style="width:6.63542in;height:3.55556in" /></p>
<p><img src="media/image4.png"
style="width:6.63542in;height:4.15278in" /></p>
<p><img src="media/image5.png"
style="width:6.63542in;height:4.20833in" /></p>
<p><img src="media/image6.png"
style="width:6.63542in;height:4.09722in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Tester registered the new account successfully</td>
</tr>
</tbody>
</table>

### Public login

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 35%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.1.2.1</p>
</blockquote></td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>System generates a one-time password when the user accesses the
system.</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>In reference to the account registered in acceptance
ID 3.1.1.1</p>
<ol type="1">
<li><p>TCP goes to user login page</p></li>
<li><p>TCP inputs peter.chan@hotmail.com in the Email field</p></li>
<li><p>TCP inputs Aa@123456 in Password field</p></li>
<li><p>TCP presses Login button</p></li>
</ol>
<p><img src="media/image7.png"
style="width:6.97917in;height:6.14583in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP should receive a one-time password (OTP) in his
registered email address generated by the system</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.1.2.4</p>
</blockquote></td>
<td><blockquote>
<p>TCP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>User use one time password to login into system</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>In reference to acceptance ID 3.1.1.10</p>
<ol type="1">
<li><p>TCP inputs the one-time password received from his registered
email address into One-Time Password field</p></li>
<li><p>TCP presses Login button</p></li>
</ol>
<p><img src="media/image8.png"
style="width:5.77083in;height:4.0625in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">User login into system successfully</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.1.2.5</p>
</blockquote></td>
<td><blockquote>
<p>TCP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>System allow user to reset password</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP presses Forget Password link on the login page (picture
1)</p></li>
<li><p>TCP inputs his registered email address into the email field
(picture 2)</p></li>
<li><p>System prompts out notification message (picture 3)</p></li>
</ol>
<p><strong><u>Picture 1</u></strong></p>
<p><img src="media/image9.png"
style="width:5.77083in;height:5.05208in" /></p>
<p><strong><u>Picture 2</u></strong></p>
<p><img src="media/image10.png"
style="width:5.80208in;height:3.79167in" /></p>
<p><strong><u>Picture 3</u></strong></p>
<p><img src="media/image11.png"
style="width:5.75in;height:3.80208in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">User receives an email with reset password link from his
registered email address</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.6</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>System only allows each user to have one single user session on the
server</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>User log into system successfully as in Acceptance ID
3.1.1.1</p></li>
<li><p>User then log into system again but using another device</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">The device for the initial login is redirected back to
the login screen</td>
</tr>
</tbody>
</table>

### User Management - Others

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td><blockquote>
<p>TCP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for user to change password</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP enters into account detail page after successful login as in
Acceptance ID 3.1.1.1</p></li>
<li><p>TCP input Aa@123456 into “Current Password” field</p></li>
<li><p>TCP input aA173173@ into “New Password” field</p></li>
<li><p>TCP input aA173173@ into “Confirm your new password”
field</p></li>
<li><p>TCP press “Submit” button</p></li>
</ol>
<p><img src="media/image12.png"
style="width:6.52083in;height:1.69444in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>System displays successful message and TCP has
changed the password</p>
<p><img src="media/image13.png"
style="width:3.34375in;height:0.70833in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.1.3.6</p>
</blockquote></td>
<td><blockquote>
<p>TCP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for updating personal information in “Update Account
Info” page</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>In reference to Acceptance ID 5.1.1, user enters into “Account
Detail” page</p></li>
<li><p>TCP inputs below information to the relevant fields</p></li>
</ol>
<ul>
<li><p>User Given Name (English) – Chi Keung</p></li>
<li><p>Chinese Full Name – 陳志強</p></li>
<li><p>Phone Number – 61236123</p></li>
</ul>
<ol start="3" type="1">
<li><p>User press “Submit” button</p></li>
</ol>
<p><img src="media/image14.png"
style="width:6.52083in;height:2.68056in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>User changes his name and phone number
successfully</p>
<p><img src="media/image15.png"
style="width:3.15625in;height:0.67708in" /></p></td>
</tr>
</tbody>
</table>

## Site Projects and Supervision Plan Management

### Search Responsible Site Project

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.2.2.1</p>
</blockquote></td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for Head of Stream searches for site project, which
they are responsible for</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Head of Stream input the BD reference of the site
project that he is responsible for in “Search by Site Project BD
Reference” field</p>
<p><img src="media/image16.png"
style="width:6.52083in;height:2.88889in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>System lists out the site project(s) that matches
with the BD reference and is responsible by the Head of Stream</p>
<p><img src="media/image17.png"
style="width:6.52083in;height:2.22222in" /></p></td>
</tr>
</tbody>
</table>

### Create new Site Project 

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.2.3.1</p>
</blockquote></td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for creating new Site Project</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester press “Create Site Project” button on “Site Projects” page
(Picture 1)</p></li>
<li><p>Tester inputs assigned BD Reference in “Search by Site Project BD
Reference” field (Picture 3)</p></li>
<li><p>Tester press “Create” button under the “Action” column (Picture
3)</p></li>
<li><p>Tester inputs below information in “Create Site Project” page
(Picture 4)</p>
<ol type="a">
<li><p>Site Address</p></li>
<li><p>Lot No.</p></li>
<li><p>Site Address</p></li>
<li><p>Select Responsible Stream</p></li>
</ol></li>
<li><p>Tester press “Submit” button</p></li>
</ol>
<p><strong><u>Picture 1</u></strong></p>
<p><img src="media/image18.png"
style="width:6.52083in;height:3.19444in" /></p>
<p><strong><u>Picture 2</u></strong></p>
<p><img src="media/image19.png"
style="width:6.52083in;height:2.56944in" /></p>
<p><strong><u>Picture 3</u></strong></p>
<p><img src="media/image20.png"
style="width:6.52083in;height:2.52778in" /></p>
<p><strong><u>Picture 4</u></strong></p>
<p><img src="media/image21.png"
style="width:6.52083in;height:2.98611in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">The new project is created successfully</td>
</tr>
</tbody>
</table>

### Edit and update Site Project Detail

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.2.4.1</p>
</blockquote></td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for editing and updating site project detail</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester presses “Edit” button on “Site Projects” page</p></li>
<li><p>Tester edits and update information in below field</p>
<ol type="a">
<li><p>Site Address</p></li>
<li><p>Lot No.</p></li>
<li><p>Tentative Commencement Date</p></li>
</ol></li>
</ol>
<p><img src="media/image22.png"
style="width:6.52083in;height:3.93056in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">The site project information has been edited
successfully</td>
</tr>
</tbody>
</table>

### List out Site Project

### View Site Project Detail

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.2.6.1</p>
</blockquote></td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>AP/RSE/RGE/AS views the site project details</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>On “Site Projects” page, Tester clicks “View” button
for the site project that he wants to view</p>
<p><img src="media/image23.png"
style="width:6.52083in;height:3.80556in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can view the site project details such as the
stream of site project, site address, tentative commencement date
etc.</p>
<p><img src="media/image24.png"
style="width:6.52083in;height:3.15278in" /></p></td>
</tr>
</tbody>
</table>

### Supervision Plan Detail View

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.2.7.1</p>
</blockquote></td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>AP/RSE/RGE/AS views the supervision plan details in the site
project</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>On “Site Project Detail” page, Tester clicks “View”
button on the supervision plan that he wants to view</p>
<p><img src="media/image25.png"
style="width:6.52083in;height:3.45833in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can view the supervision plan details in
reference to below picture</p>
<p><img src="media/image26.png"
style="width:6.52083in;height:6.44444in" /></p></td>
</tr>
</tbody>
</table>

### Supervision Plan Detail Management

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td><blockquote>
<p>3.2.8.1</p>
</blockquote></td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for AP/RSE/RGE/AS to edit the supervision plan detail
of the project</p>
</blockquote></td>
<td>successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>On “Site Project Detail” page, Tester clicks “Edit” button on the
supervision plan that he wants to Edit</p></li>
<li><p>Tester change value of fields as below</p>
<ol type="a">
<li><p>Type of building works and street works → Ground Investigation
field works</p></li>
<li><p>Specific type of building works and street works → GIFW</p></li>
<li><p>T1 - T4 Grade of TCP → Suggested TCP assigned number → 2</p></li>
</ol></li>
<li><p>Tester clicks “Submit” button</p></li>
</ol>
<p><img src="media/image25.png"
style="width:6.52083in;height:3.45833in" /></p>
<p><img src="media/image27.png"
style="width:6.52083in;height:3.19444in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Tester changed supervision plan details
successfully</td>
</tr>
</tbody>
</table>

## TCP management

### Assign TCPs

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.1.1</td>
<td>AP, RSE, RGE and AS</td>
<td></td>
<td><blockquote>
<p>Search TCP by Name</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Go to “List of TCPs” page</p></li>
<li><p>Input the Name of TCP in “Search Name” field</p></li>
</ol>
<p><img src="media/image28.png"
style="width:6.52083in;height:2.80556in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">All the matched TCPs will be Shown</td>
</tr>
</tbody>
</table>

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.1.4</td>
<td>AP, RSE, RGE and AS</td>
<td></td>
<td><blockquote>
<p>Add TCP into project</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Go to “List of TCPs” page</p></li>
<li><p>Click “Assign TCP” button</p></li>
<li><p>Input the username that you want to assign as TCP in “Search by
Name” field</p></li>
<li><p>Add “Add” button</p></li>
<li><p>Select “Grade of TCP”</p></li>
<li><p>Click “I confirm the personal above is qualified for his/her
grade of TCP as declared.”</p></li>
<li><p>The Page shown message shown the TCP adding request sent to TCP
and awaiting TCP accept</p></li>
<li><p>Tester switch the role and use TCP account to login into system
again</p></li>
<li><p>Tester accepts TCP invitation</p></li>
</ol>
<p><img src="media/image29.png"
style="width:6.52083in;height:3.30556in" /></p>
<p><img src="media/image30.png"
style="width:6.52083in;height:2.15278in" /></p>
<p><img src="media/image31.png"
style="width:6.52083in;height:3.125in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">HOS assign TCP successfully</td>
</tr>
</tbody>
</table>

### Request TCP acceptance 

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.2.1</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Accept “Assign TCP” Request</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>After completing Acceptance ID 3.3.1.4, TCP receives an
assignment request email generated from the system.</p></li>
<li><p>TCP clicks on the accept link to accept being TCP in the
assignment request email.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">The user should be redirected to the notification page,
notifying him he has been assigned as TCP of the project</td>
</tr>
</tbody>
</table>

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.2.2</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Reject “Assign TCP” Request</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>After completing Acceptance ID 3.3.1.4, TCP receives an
assignment request email generated from the system.</p></li>
<li><p>TCP clicks on the reject link to reject being TCP in the
assignment request email.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">The user should be redirected to the notification page,
notifying him he has rejected to be TCP of the project</td>
</tr>
</tbody>
</table>

### Unassign TCPs

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.3.1</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Unassign the assigned TCPs from project</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Go to “List of TCPs” page</p></li>
<li><p>Input “Tai Man” in the first name field and “Chan” in the last
name field</p></li>
<li><p>Press “Search” button</p></li>
<li><p>Click the row of “Chan Tai Man” in the display result and then
press “Remove” button</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP “Chan Tai Man” should be unassigned as TCP role</td>
</tr>
</tbody>
</table>

### Temporary replacement of TCP

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.4.1</td>
<td>AP, RSE, RGE and AS</td>
<td></td>
<td><blockquote>
<p>Temporary replacement of TCP</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Go to “List of TCPs” page</p></li>
<li><p>Input “Siu Ming” in the first name field and “Chan” in the last
name field</p></li>
<li><p>Press “Search” button</p></li>
<li><p>Click the row of “Chan Siu Ming” in the display result and then
press “Temporary Replacement” button</p></li>
<li><p>Search “Wong Hoi Yen” name and then press “Replace”
button</p></li>
<li><p>Set effective start date and end date of the replacement
period</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Wong Hoi Yen should receive invitation email for being
temporary TCP</td>
</tr>
</tbody>
</table>

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.4.2</td>
<td>AP, RSE, RGE and AS</td>
<td></td>
<td></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Continue from Acceptance ID 5.3.4.1, Wong Hoi Yen clicks the link
for acceptance of being temporary TCP received from her email</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Wong Hoi Yen becomes temporary TCP</td>
</tr>
</tbody>
</table>

## Form A

### Create Form A template

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.1.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Create Form A template</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester clicks “Create Form A template” button</p></li>
<li><p>Tester selects “Chan Tai Man” in the “Name” field</p></li>
<li><p>Tester inputs project start date and estimate project end date in
the respective fields</p></li>
<li><p>Tester clicks on “A1 to A6” checkboxes</p></li>
<li><p>Tester clicks “Save” button</p></li>
</ol>
<blockquote>
<p><img src="media/image32.png"
style="width:6.52083in;height:4.84722in" /></p>
</blockquote></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">An new Form A template is created</td>
</tr>
</tbody>
</table>

### Create Form A 

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.2.1</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Create Form A</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP chooses a Form A template they are responsible for (Picture
1).</p></li>
<li><p>TCP setup the frequency and the start date of the Form A (Picture
2).</p></li>
</ol>
<p><strong><u>Picture 1</u></strong></p>
<p><img src="media/image33.png"
style="width:6.52083in;height:4.15278in" /></p>
<p><strong><u>Picture 2</u></strong></p>
<p><img src="media/image34.png"
style="width:6.52083in;height:5.83333in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">An new Form A is created</td>
</tr>
</tbody>
</table>

### Fill Form A

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.3.1</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Select or amend different tasks item status</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Users select all ‘S’ or ‘N/A’ status</p></li>
<li><p>Users don’t select one of the item status</p></li>
<li><p>Users press ‘amend’ to correct the wrong status after save as
draft</p></li>
</ol>
<p><img src="media/image35.png"
style="width:4.80208in;height:3.16667in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">User can review the updated item status</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.3.2</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Review previous updated history</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester open the draft created in Acceptance ID 5.4.3.1</p></li>
<li><p>Tester amend the value of the filled item</p></li>
</ol>
<p><img src="media/image36.png"
style="width:4.9567in;height:3.2733in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Tester is able to review the revision history of the
drafted Form A</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.3.3</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Import inspection record files</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP downloads Form A template from DWSS</p></li>
<li><p>TCP fills the relevant fields and upload the file to
system</p></li>
</ol>
<p><img src="media/image37.png"
style="width:4.70035in;height:3.16667in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Users successfully upload the record files</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.3.4</td>
<td>TCP</td>
<td></td>
<td>Review the imported file records</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Users import wrong format file</p></li>
</ol>
<p><img src="media/image38.png"
style="width:4.73169in;height:3.2733in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Users can preview all the records from imported
files</td>
</tr>
</tbody>
</table>

### Upload PDF, PNG on Form A and Quality Supervision Form (PNAP APP-158 Appendix B) ("Form APP-158”)

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.4.1</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Upload PDF, PNG on Form A and Quality Supervision Form ("Form
APP-158”)</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP fills value in relevant Form APP-158 fields and select “S” on
the radio button</p></li>
<li><p>TCP clicks “Choose file” button in “Upload Photo” area</p></li>
<li><p>TCP upload a photo (size limit - 5MB) and select “QC3” in the
drop down list</p></li>
<li><p>TCP clicks the “Upload” button</p></li>
</ol>
<p><img src="media/image39.png"
style="width:6.52083in;height:3.75in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Upload PDF, PNG on Form A and Quality Supervision Form
(PNAP APP-158 Appendix B) ("Form APP-158”) successfully</td>
</tr>
</tbody>
</table>

### View Form A Result and History

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.5.1</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>View Form A Result and History</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP goes to Form A dashboard page</p></li>
<li><p>TCP search the Form A by inputting the type of works and then
press “Search” button</p></li>
<li><p>TCP double clicks on the row of the result</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>TCP should be able to view the Form A result and
history</p>
<blockquote>
<p><img src="media/image33.png"
style="width:6.52083in;height:4.15278in" /></p>
<p><img src="media/image40.png"
style="width:6.52083in;height:2.26389in" /></p>
</blockquote></td>
</tr>
</tbody>
</table>

### Download, Import and Export Records

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.6.1</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Download Form A Site Inspection Import Template</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP press download “Form A Template” button to download
the Form A template</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP is expected to view the Form A template in excel
format with pre-defined contents</td>
</tr>
</tbody>
</table>

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.6.2</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Import Form A Site Inspection Records by Excel</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP fills the relevant fields in the imported Form A
template</p></li>
<li><p>TCP uploaded the filled Form A to system</p></li>
</ol>
<p><img src="media/image41.png"
style="width:6.52083in;height:3.625in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">System records the details of the submitted Form A</td>
</tr>
</tbody>
</table>

## Form B

### Create Form B

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.1</td>
<td><blockquote>
<p>TCP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for creating new Form B</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP clicks the “Form B” button on the Supervision Plan Detail
page.</p></li>
<li><p>TCP clicks “Create Report” button</p></li>
<li><p>TCP inputs the date discovered and non-conformity
details</p></li>
<li><p>TCP clicks “Save as Draft” button</p></li>
</ol>
<p><img src="media/image42.png"
style="width:6.63542in;height:7.91667in" /></p>
<p><img src="media/image43.png"
style="width:6.63542in;height:3.70833in" /></p>
<p><img src="media/image44.png"
style="width:6.63542in;height:3.06944in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP creates new Form B successfully</td>
</tr>
</tbody>
</table>

###  

### Save Form B Part 1 as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.1</td>
<td><blockquote>
<p>TCP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for saving Form B Part 1 as draft</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP clicks the “Form B” button on the Supervision Plan Detail
page.</p></li>
<li><p>TCP searches for Form B by date discovered or / and Name of TCP
created Form B.</p></li>
<li><p>TCP edits the discover date and non-conformity details</p></li>
<li><p>TCP clicks “Save as Draft” button</p></li>
</ol>
<p><img src="media/image45.png"
style="width:6.63542in;height:7.05556in" /></p>
<p><img src="media/image43.png"
style="width:6.63542in;height:3.70833in" /></p>
<p><img src="media/image44.png"
style="width:6.63542in;height:3.06944in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP edits draft of Form B successfully</p></li>
<li><p>User should be able to edit the details of the drafted Form B and
save the edited draft again</p></li>
</ol></td>
</tr>
</tbody>
</table>

###  

### Upload attachments when Form B Part 1 is Saved as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td>TCP</td>
<td></td>
<td>Successful case for uploading attachment when Form B Part 1 is saved
as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.2.1, TCP opens the same
Form B draft created before</p></li>
<li><p>TCP clicks the “Upload” button</p></li>
<li><p>TCP attach a PNG file to the system</p></li>
<li><p>TCP clicks “Save” button</p></li>
</ol>
<p><img src="media/image46.png"
style="width:6.63542in;height:3.30556in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP can upload the PNG file to the Form B draft</p></li>
<li><p>TCP can view and download the PNG file from the Form B draft
after the PNG file is uploaded to the Form B draft</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Complete Form B Part 1

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.4.1</td>
<td>TCP</td>
<td></td>
<td>Successful case for completing Form B Part 1</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.2.1, TCP opens the same
Form B created before</p></li>
<li><p>TCP presses the “Complete” button on the Form B draft</p></li>
</ol>
<p><img src="media/image47.png"
style="width:6.63542in;height:3.80556in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP completes Form B part 1 successfully</p></li>
<li><p>The status of Form B part 1 changed from “Save as Draft” to
“Completed”</p></li>
<li><p>TCP can view the “Heads of Stream' response to Part 1” section
after complete the Form B part 1</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Upload attachments when Form B Part 1 is Completed

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.5.1</td>
<td>AP, TCP</td>
<td></td>
<td>Successful case for uploading attachments when Form B part 1 is
completed</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.4.1, TCP opens the same
Form B created before</p></li>
<li><p>TCP presses the “Upload” button</p></li>
<li><p>TCP selects and attach the PNG file</p></li>
<li><p>TCP presses the “Save” button</p></li>
</ol>
<p><img src="media/image48.png"
style="width:6.63542in;height:3.81944in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Both AP and TCP can view and download the new attached
PNG file</td>
</tr>
</tbody>
</table>

### Save Response to Form B Part 1 as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.6.1</td>
<td>AP, TCP</td>
<td></td>
<td>Successful case for saving response to Form B part 1 as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AP opens the Form B part 1 completed by TCP in acceptance ID
3.1.4.1</p></li>
<li><p>In “Heads of Stream' response to Part 1” section, AP clicks the
“No” button</p></li>
<li><p>AP clicks the ‘Save as Draft” button</p></li>
</ol>
<p><img src="media/image49.png"
style="width:6.63542in;height:3.30556in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Both AP and TCP can view Head of Stream response in the Form
B</p></li>
<li><p>The status of “Heads of Stream' response to Part 1” changed to
“Saved as Draft”</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Complete Response to Form B Part 1

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.7.1</td>
<td>AP, TCP</td>
<td></td>
<td>Successful case for completing response to Form B Part 1</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.6.1, AP opens the same
Form B created before</p></li>
<li><p>AP clicks on the “Complete” button</p></li>
</ol>
<p><img src="media/image50.png"
style="width:6.63542in;height:3.16667in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Both AP and TCP can view Form B part 2 after AP completed the
response to part 1</p></li>
<li><p>The status of “Heads of Stream' response to Part 1” changed to
“Completed”</p></li>
</ol></td>
</tr>
</tbody>
</table>

###  

### Report Imminent Danger to BD in Form B Part 1

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.8.1</td>
<td>AP, BD Officer</td>
<td></td>
<td>Successful case for reporting imminent danger to BD in Form B part
1</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.1.1, AP opens the same
Form B created before</p></li>
<li><p>AP clicks the “Yes” button in the field of “The non-conformity
shall pose an imminent danger” inside the “Heads of Stream' response to
Part 1” section</p></li>
<li><p>AP clicks the “Report imminent danger to BD” button</p></li>
</ol>
<p><img src="media/image51.png"
style="width:6.63542in;height:4.01389in" /></p>
<p><img src="media/image52.png"
style="width:6.63542in;height:1.33333in" /></p>
<p><img src="media/image53.png"
style="width:6.63542in;height:0.88889in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AP can view the wording of “imminent danger has been reported to
BD” in “Heads of Stream' response to Part 1” section</p></li>
<li><p>The status in “Heads of Stream' response to Part 1” section
changed to “Reported to BD”</p></li>
<li><p>BD Officer receives email notification regarding the posed
imminent danger</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Save Form B Part 2 as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.9.1</td>
<td>TCP Representative, TCP</td>
<td></td>
<td>Successful case for saving Form B part 2 as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.7.1, TCP Rep opens the
same Form B created before</p></li>
<li><p>TCP Rep selects RC stream user in the drop down list of
“Instruction for rectification given to”</p></li>
<li><p>TCP Rep inputs the instruction detail of rectification in
“Details of Instruction” field</p></li>
<li><p>TCP Rep inputs 08/05/2023 as the date for giving instruction to
TCP user</p></li>
<li><p>TCP Rep clicks “Save as Draft” button</p></li>
</ol>
<p><img src="media/image54.png"
style="width:6.63542in;height:4.04167in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP Rep receives email notification regarding part 2 draft has
been saved</p></li>
<li><p>Both TCP and TCP Rep can view the details of the part 2
draft</p></li>
<li><p>Status of Form B part 2 changed to “Saved as Draft”</p></li>
</ol>
<p><img src="media/image55.png"
style="width:6.63542in;height:0.93056in" /></p></td>
</tr>
</tbody>
</table>

### Report RC fail to comply and Material Concern to BD

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.10.1</td>
<td>BD Officer, AP</td>
<td></td>
<td>Successful case for reporting material concern to BD</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.9.1, AP opens the same
Form B created before</p></li>
<li><p>AP press the “Report material concern to BD” button</p></li>
</ol>
<p><img src="media/image56.png"
style="width:6.63542in;height:4.08333in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Wording of “RC failure to compile rectification work has been
reported to BD” appears in Part 2</p></li>
<li><p>Both BD Officer and AP receives email notification</p></li>
</ol>
<p><img src="media/image57.png"
style="width:6.63542in;height:4.05556in" /></p>
<p><img src="media/image58.png"
style="width:6.63542in;height:1.20833in" /></p></td>
</tr>
</tbody>
</table>

### Upload attachment when Form B Part 2 is Saved as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.11.1</td>
<td>TCP Rep</td>
<td></td>
<td>Successful case for uploading attachment when Form B Part 2 is Saved
as Draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.10.1, TCP Rep opens the
same Form B created before</p></li>
<li><p>TCP Rep selects today date in “Date of rectification works
certified completion” field</p></li>
<li><p>TCP Rep presses the “Upload” button</p></li>
<li><p>TCP Rep selects the PNG file that he desires to upload</p></li>
<li><p>TCP Rep presses the “Save as Draft” button</p></li>
</ol>
<p><img src="media/image59.png"
style="width:6.63542in;height:4.29167in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP Rep can view and download the uploaded PNG file in
Form B part 2</td>
</tr>
</tbody>
</table>

### Complete Form B Part 2

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.12.1</td>
<td>AP</td>
<td></td>
<td>Successful case for completing Form B Part 2</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.11.1, AP opens the same
Form B created before</p></li>
<li><p>AP presses “Complete” button in the Form B part 2</p></li>
</ol>
<p><img src="media/image60.png"
style="width:6.63542in;height:3.31944in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Status of Form B part 2 changed to “Completed”</p></li>
<li><p>All AP, TCP Rep and TCP can view the “Heads of Stream' response
to Part 2” section</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Save Response to Form B Part 2 as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.14.1</td>
<td>AP, TCP Rep, TCP</td>
<td></td>
<td>Successful case for saving response to Form B part 2 as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.11.1, AP opens the same
Form B created before</p></li>
<li><p>AP presses the “No” button in “The non-conformity shall pose an
imminent danger.” field in “Heads of Stream' response to Part 2”
section</p></li>
<li><p>AP presses the “Save as Draft” button</p></li>
</ol>
<p><img src="media/image61.png"
style="width:6.63542in;height:5.38889in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Status in “Heads of Stream' response to Part 2” section changed
to “Saved as Draft”</p></li>
<li><p>All AP, TCP Rep and TCP can view the saved response in the “Heads
of Stream' response to Part 2” section</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Complete Response to Form B Part 2

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.15.1</td>
<td>AP</td>
<td></td>
<td>Successful case for completing response to Form B Part 2</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.14.1, AP opens the same
Form B created before</p></li>
<li><p>AP presses the “Complete” button</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Status of Form B part 2 changed to “Completed”</p></li>
<li><p>All AP, TCP Rep and TCP can view the “Heads of Stream' response
to Part 2” section</p></li>
</ol>
<p><img src="media/image61.png"
style="width:6.63542in;height:5.38889in" /></p></td>
</tr>
</tbody>
</table>

### Report Imminent Danger to BD in Form B Part 2

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.16.1</td>
<td>AP</td>
<td></td>
<td>Successful case for reporting imminent danger to BD in Form B part
2</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.14.1, AP opens the same
Form B created before</p></li>
<li><p>AP clicks the “Yes” button in “The non-conformity shall pose an
imminent danger” field</p></li>
<li><p>AP clicks the “Report imminent danger to BD” button</p></li>
</ol>
<p><img src="media/image62.png"
style="width:6.63542in;height:5.22222in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Displays the user ID of the AP who report imminent danger to
BD</p></li>
<li><p>Displays grade and stream of the AP who report imminent danger to
BD</p></li>
<li><p>Display the status as “Reported to BD”</p></li>
<li><p>Display the date when AP reported the imminent danger to
BD</p></li>
<li><p>AP receives notification email from system</p></li>
</ol>
<p><img src="media/image63.png"
style="width:4.26042in;height:2.40625in" /></p></td>
</tr>
</tbody>
</table>

## PNAP APP-158 Appendix B (Record of Quality Supervision)

### Create PNAP APP-158 template

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.1.1</td>
<td>AP</td>
<td></td>
<td>Successful case for creating PNAP APP-158 template</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AP presses “View” button on the site project in which he wants to
create App-158</p></li>
<li><p>AP presses “View” button on the supervision plan in which he
wants to create App-158</p></li>
<li><p>AP clicks the “APP-158” button</p></li>
<li><p>AP clicks “Create Template” button</p></li>
<li><p>AP selects “Superstructive Works - General Building Works” in
Type of Works field</p></li>
<li><p>AP selects “T1” in Responsible Grade of TCP field</p></li>
<li><p>AP selects a TCP name in Responsible TCP field</p></li>
</ol>
<p><img src="media/image64.png"
style="width:6.63542in;height:1.86111in" /></p>
<p><img src="media/image65.png"
style="width:6.63542in;height:3.13889in" /></p>
<p><img src="media/image66.png"
style="width:6.63542in;height:2.83333in" /></p>
<p><img src="media/image67.png"
style="width:6.63542in;height:5.83333in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AP creates the PNAP APP-158 template successfully</td>
</tr>
</tbody>
</table>

###  

### Create PNAP APP-158 Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.2.1</td>
<td>TCP</td>
<td></td>
<td>Successful case for creating PNAP APP-158 draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the PNAP APP-158 template created in acceptance ID
3.2.1.1, TCP clicks the “View” button on the APP-158 template AP created
before</p></li>
<li><p>TCP clicks the “Create New Records” button</p></li>
<li><p>TCP inputs the record date and then press “Next” button</p></li>
<li><p>TCP inputs value in QB1 to QB5 Location/Details and
Remedial/Remark fields and click “S” in Result field for each
item</p></li>
<li><p>TCP clicks the “Save as Draft” button</p></li>
</ol>
<p><img src="media/image68.png"
style="width:6.63542in;height:1.73611in" /></p>
<p><img src="media/image69.png"
style="width:6.63542in;height:1.88889in" /></p>
<p><img src="media/image70.png"
style="width:6.63542in;height:2.97222in" /></p>
<p><img src="media/image71.png"
style="width:6.63542in;height:3.5in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AP created draft of PNAP APP-158 successfully</td>
</tr>
</tbody>
</table>

###  

### File PNAP APP-158

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.3.1</td>
<td>AP</td>
<td></td>
<td>Successful case for filing PNAP APP-158</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the drafted app-158 created in acceptance ID 3.2.2.1,
AP opens the app-158 record drafted by TCP</p></li>
<li><p>AP presses the “File” button</p></li>
</ol>
<p><img src="media/image72.png"
style="width:6.63542in;height:3.15278in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AP created app-158 successfully and the status of
app-158 changed to “Filed”</td>
</tr>
</tbody>
</table>

### Upload PDF, PNG on PNAP APP-158

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.4.1</td>
<td>TCP, AP</td>
<td></td>
<td>Successful case for uploading PNG on drafted PNAP APP-158
record</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the drafted app-158 created in acceptance ID 3.2.2.1,
TCP opens the app-158 record drafted</p></li>
<li><p>TCP click “Upload” button</p></li>
<li><p>TCP select a file to upload</p></li>
<li><p>TCP select from dropdown an item related to the file</p></li>
<li><p>TCP click “Save as Draft” button</p></li>
</ol>
<p><img src="media/image73.png"
style="width:6.63542in;height:4.11111in" /><img src="media/image74.png"
style="width:6.63542in;height:4.48611in" /><img src="media/image75.png"
style="width:6.63542in;height:4.36111in" /><img src="media/image76.png"
style="width:6.63542in;height:4.40278in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP uploaded the file successfully. AP open the drafted
PNAP APP-158 record and view the uploaded file</td>
</tr>
</tbody>
</table>

###  

### View PNAP APP-158 Result and History

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.5.1</td>
<td>AP, TCP</td>
<td></td>
<td>Successful case for viewing PNAP APP-158 Results and History</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the app-158 filed in acceptance ID 3.2.3.1, TCP opens
the app-158 record.</p></li>
<li><p>TCP views record results and status as Filed</p></li>
<li><p>TCP clicks “View History” button to open Version History
pop-up</p></li>
<li><p>TCP select version number from dropdown to view record result
history</p></li>
</ol>
<p><img src="media/image77.png"
style="width:6.63542in;height:2.76389in" /></p>
<p><img src="media/image78.png"
style="width:6.63542in;height:4.52778in" /><img src="media/image79.png"
style="width:6.63542in;height:3.68056in" /><img src="media/image80.png"
style="width:6.63542in;height:3.16667in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP viewed the filed record history successfully.</td>
</tr>
</tbody>
</table>

### Download PNAP APP-158 Import Template

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.6.1</td>
<td>TCP</td>
<td></td>
<td>Successful case for downloading PNAP APP-158 Import Template</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the PNAP APP-158 template created in acceptance ID
3.2.1.1, TCP clicks the “View” button on the APP-158 template AP created
before</p></li>
<li><p>TCP click “Create Form” to create new PNAP APP-158 form, or click
“View” to open drafted PNAP APP-158 form.</p></li>
<li><p>TCP click “Download record import template” to download the
import template as excel</p></li>
<li><p>TCP open the excel file to view downloaded template with template
details and item details</p></li>
<li><p>TCP input results, location/details and remedial/remark for each
inspection item</p></li>
</ol>
<p><img src="media/image81.png"
style="width:6.63542in;height:2.70833in" /><img src="media/image82.png"
style="width:6.63542in;height:4in" /><img src="media/image83.png"
style="width:6.63542in;height:4.44444in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"></td>
</tr>
</tbody>
</table>

### Import PNAP APP-158 Records

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.7.1</td>
<td>TCP</td>
<td></td>
<td>Successful case for importing PNAP APP-158 record from template</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the PNAP APP-158 template created in acceptance ID
3.2.1.1, TCP clicks the “View” button on the APP-158 template AP created
before</p></li>
<li><p>TCP click “Create Form” to create new PNAP APP-158 form, or click
“View” to open drafted PNAP APP-158 form.</p></li>
<li><p>User click “Import template”</p></li>
<li><p>Following the import template downloaded and filled in acceptance
ID 3.2.7.1, user select the import template to upload</p></li>
<li><p>User preview the result of the import and click “Confirm” to
confirm import.</p></li>
<li><p>Results are imported to system and user view the imported result
saved as Draft</p></li>
</ol>
<p><img src="media/image81.png"
style="width:6.63542in;height:2.70833in" /></p>
<p><img src="media/image82.png"
style="width:6.63542in;height:4in" /><img src="media/image84.png"
style="width:6.63542in;height:4.66667in" /><img src="media/image85.png"
style="width:6.63542in;height:4.84722in" /><img src="media/image86.png"
style="width:6.63542in;height:4.58333in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP imported records successfully. Results are saved as
draft</td>
</tr>
</tbody>
</table>

##  

## Users Details Management

### Search Public User

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.1.1</td>
<td>BD admin</td>
<td></td>
<td>Successful case for BD admin to view Public Users</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Login as BD admin</p></li>
<li><p>BD admin user search public users by entering email or / and
english full name</p></li>
<li><p>BD admin user click “Search” to begin search</p></li>
</ol>
<p><img src="media/image87.png"
style="width:6.63542in;height:4.54167in" /></p>
<p><img src="media/image88.png"
style="width:6.63542in;height:3.68056in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">User searched public users successfully.</td>
</tr>
</tbody>
</table>

### Edit Public User

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.2.1</td>
<td>BD admin</td>
<td></td>
<td>Successful case for BD admin to edit Public Users</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the public user selected in acceptance ID 3.3.1.1, BD
admin user click “Edit” button to view details of public user</p></li>
<li><p>BD admin user edit details of public user and click “Submit” to
update public user account</p></li>
</ol>
<p><img src="media/image88.png"
style="width:6.63542in;height:3.68056in" /></p>
<p><img src="media/image89.png"
style="width:6.63542in;height:4.52778in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Details of public user is updated successfully</td>
</tr>
</tbody>
</table>

### Inactivate Public User

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.3.1</td>
<td>BD admin</td>
<td></td>
<td>Successful case for BD admin to inactivate Public Users</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the user searched in acceptance ID 3.3.1.1, BD admin
user click “Inactivate” to inactivate public user that is not
responsible of or assigned to any site project</p></li>
<li><p>BD admin user click “Confirm” in the pop-up to confirm the
inactivation.</p></li>
</ol>
<p><img src="media/image90.png"
style="width:6.63542in;height:3.01389in" /></p>
<p><img src="media/image91.png"
style="width:6.63542in;height:3.68056in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Public user account is inactivated and is not allowed to
login the system</td>
</tr>
</tbody>
</table>

### Activate Public User

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.4.1</td>
<td>BD admin</td>
<td></td>
<td>Successful case for BD admin to activate Public Users</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the user inactivated in acceptance ID 3.3.3.1, BD admin
user click “Reactivate” to reactivate public user that is inactive in
the system</p></li>
<li><p>BD admin user click “Confirm” in the pop-up to confirm the
activation.</p></li>
</ol>
<p><img src="media/image92.png"
style="width:6.63542in;height:3.36111in" /></p>
<p><img src="media/image93.png"
style="width:6.63542in;height:3.09722in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Public user account is reactivated and is allowed to
login the system</td>
</tr>
</tbody>
</table>

###  

### View Public User responsible site projects as Head of Stream 

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.5.1</td>
<td>BD admin</td>
<td></td>
<td>Successful case for BD admin to view Public User’s responsible site
project</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>BD admin user search user by “Search by Role” filter to select
user of registered qualification (AP, RSE, RGE, AS)</p></li>
<li><p>BD admin user click “Edit” button, then click “Resign”
button</p></li>
<li><p>BD admin user view the site projects the select user is
responsible of as a Head of Stream</p></li>
</ol>
<p><img src="media/image94.png"
style="width:6.63542in;height:3.125in" /><img src="media/image95.png"
style="width:6.63542in;height:2.93056in" /><img src="media/image96.png"
style="width:6.63542in;height:4.08333in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"></td>
</tr>
</tbody>
</table>

###  

### Removal of Head of Stream by BD admin due to resignation or removal from Register

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.6.1</td>
<td>BD admin</td>
<td></td>
<td>Successful case for BD admin to remove Head of Stream from site
project</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the site projects displayed in acceptance ID 3.3.6.1,
BD admin user click “Resign” button to open resignation popup</p></li>
<li><p>BD admin user select the resignation date of Head of Stream and
number of days of Grace Period.</p></li>
<li><p>BD admin user click “Save” to confirm the resignation</p></li>
</ol>
<p><img src="media/image96.png"
style="width:6.63542in;height:4.08333in" /><img src="media/image97.png"
style="width:6.63542in;height:4.61111in" /><img src="media/image98.png"
style="width:6.63542in;height:3.55556in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">BD admin user starts resignation process. After Grace
Period passed, site project is ended and all public users are not
allowed to access the ended site project</td>
</tr>
</tbody>
</table>

## Site-monitoring

### Create site-monitoring scheme

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.1</td>
<td><blockquote>
<p>AS</p>
</blockquote></td>
<td></td>
<td>Successful case for creating new site-monitoring scheme</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AS enters into any responsible site project</p></li>
<li><p>AS clicks “List of Site-monitoring Schemes” button</p></li>
<li><p>AS clicks “Create Scheme” button</p></li>
<li><p>AS inputs the scheme details such as name of scheme, type of
work, type of monitoring etc.</p></li>
<li><p>AS adds monitoring point to the scheme</p></li>
<li><p>AS clicks “Save” button</p></li>
</ol>
<p><img src="media/image99.png"
style="width:6.63542in;height:2.90278in" /></p>
<p><img src="media/image100.png"
style="width:6.63542in;height:1.80556in" /></p>
<p><img src="media/image101.png"
style="width:6.63542in;height:2.38889in" /></p>
<p><img src="media/image102.png"
style="width:6.63542in;height:3.125in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS creates new site monitoring scheme successfully</td>
</tr>
</tbody>
</table>

### Edit Site-monitoring scheme (3A level)

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.1</td>
<td><blockquote>
<p>AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for editing 3A level</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AS enters into any site project</p></li>
<li><p>AS clicks “List of Site-monitoring Schemes” button</p></li>
<li><p>AS clicks on the scheme that he wants to edit with</p></li>
<li><p>AS clicks “Edit Scheme” button</p></li>
<li><p>AS amends value of 3A level</p></li>
<li><p>AS clicks “Save” button</p></li>
</ol>
<p><img src="media/image103.png"
style="width:6.63542in;height:2.15278in" /></p>
<p><img src="media/image104.png"
style="width:6.63542in;height:2.63889in" /></p>
<p><img src="media/image105.png"
style="width:6.63542in;height:2.22222in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS edits 3A level values successfully</td>
</tr>
</tbody>
</table>

### Edit Site-monitoring scheme (adding monitoring points)

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td>AS</td>
<td></td>
<td>Successful case for adding monitoring point</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.2.1, AS clicks “Edit
Scheme” button</p></li>
<li><p>AS clicks the “Add Point” button to add new monitoring
points.</p></li>
<li><p>AS may click “Custom Start Date” and “Custom End Date” to set
tentative start and end date of the new monitoring point.</p></li>
<li><p>AS clicks the “Save” button</p></li>
</ol>
<p><img src="media/image106.png"
style="width:6.63542in;height:2.375in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS adds an new monitoring point successfully</td>
</tr>
</tbody>
</table>

### Edit Site-monitoring scheme (adding monitoring points)

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td>AS</td>
<td></td>
<td>Successful case for editing monitoring point</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol start="5" type="1">
<li><p>Following the steps in acceptance ID 3.1.2.1, AS clicks “Edit
Scheme” button</p></li>
<li><p>AS click “Custom Start Date” and “Custom End Date” to set
tentative start and end date of an existing monitoring point.</p></li>
<li><p>AS clicks the “Save” button</p></li>
</ol>
<p><img src="media/image106.png"
style="width:6.63542in;height:2.375in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS edits an monitoring point successfully</td>
</tr>
</tbody>
</table>

### Save measurement records as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.4.1</td>
<td>RC TCP</td>
<td></td>
<td>Successful case for TCP to save measurement records as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.1.1, RC TCP opens the
Site-monitoring scheme.</p></li>
<li><p>RC TCP click “Create” button to navigate to the “Manual Input
Measurement Record” page.</p></li>
<li><p>RC TCP enter measurement records on each monitoring point and
click “Submit”</p></li>
<li><p>RC TCP preview the measurement records and comparison with 3A
levels.</p></li>
<li><p>RC TCP click “Confirm” to save the measurement records as
draft.</p></li>
</ol>
<p><img src="media/image107.png"
style="width:6.63542in;height:2.05556in" /><img src="media/image108.png"
style="width:6.63542in;height:3.31944in" /></p>
<p><img src="media/image109.png"
style="width:3.40868in;height:4.65802in" /></p>
<p><img src="media/image110.png"
style="width:6.63542in;height:3.26389in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>RC TCP saves measurement records as draft successfully.</p></li>
<li><p>If the records exceed any 3A levels, the system notify RC
Representative accordingly.</p></li>
</ol>
<p><img src="media/image111.png"
style="width:6.63542in;height:1.30556in" /></p></td>
</tr>
</tbody>
</table>

### Download the import measurement template

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.5.1</td>
<td>RC TCP</td>
<td></td>
<td>Successful case for RC TCP to download import measurement
template</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.1.1, RC TCP opens the
Site-Monitoring scheme.</p></li>
<li><p>RC TCP presses the “Download Template as Excel” button</p></li>
<li><p>RC TCP download the excel of import measurement template to local
machine.</p></li>
</ol>
<p><img src="media/image112.png"
style="width:6.63542in;height:2.84722in" /></p>
<p><img src="media/image113.png"
style="width:3.02326in;height:4.47102in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">RC TCP download the excel of import measurement template
to local machine successfully.</td>
</tr>
</tbody>
</table>

### Import the measurement records

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.6.1</td>
<td>RC TCP</td>
<td></td>
<td>Successful case for importing site-monitoring measurement
records</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.5.1, RC TCP click
“Import data from Excel Template” in the Site-Monitoring
scheme.</p></li>
<li><p>RC TCP presses the “Upload” button and select the import template
filled with measurement data</p></li>
<li><p>RC TCP preview the import measurement data and their comparison
with 3A levels.</p></li>
<li><p>RC TCP click “Confirm” to save all the data as draft.</p></li>
<li><p>If the records exceed 3A levels, a confirmation box pop up. RC
TCP click “Yes” button to confirm filing.</p></li>
</ol>
<p><img src="media/image114.png"
style="width:6.63542in;height:2.08333in" /></p>
<p><img src="media/image115.png"
style="width:6.63542in;height:2.23611in" /><img src="media/image116.png"
style="width:6.63542in;height:2.26389in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>RC TCP saves measurement records as draft successfully.</p></li>
<li><p>If the records exceed any 3A levels, the system notify RC
Representative accordingly.</p></li>
</ol>
<p><img src="media/image111.png"
style="width:6.63542in;height:1.30556in" /></p></td>
</tr>
</tbody>
</table>

### File/amend measurement records

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.7.1</td>
<td>AS, RC TCP</td>
<td></td>
<td>Successful case for file/amend measurement records</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.4.1 or 3.1.6.1, AS opens
the same site-monitoring scheme.</p></li>
<li><p>AS review the measurement records and the comparison with 3A
levels</p></li>
<li><p>AS click “File” button to file the measurement records.</p></li>
<li><p>If the records exceed 3A levels, a confirmation box pop up. As
click “Yes” button to confirm filing.</p></li>
</ol>
<p><img src="media/image117.png"
style="width:6.63542in;height:2.15278in" /></p>
<p><img src="media/image118.png"
style="width:6.63542in;height:3.68056in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AS file the measurement records successfully.</p></li>
<li><p>A record history version is created successfully.</p></li>
<li><p>If the records exceed Alert levels, the system notifies AP
stream, RSE stream, RGE stream, AS stream and responsible BD Officers
accordingly.</p></li>
</ol>
<p><img src="media/image119.png"
style="width:6.63542in;height:3.31944in" /><img src="media/image120.png"
style="width:6.63542in;height:1.375in" /></p></td>
</tr>
</tbody>
</table>

### View site-monitoring measurement record results

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.8.1</td>
<td>TCP Representative, Head of Stream</td>
<td></td>
<td>Successful case for viewing measurement record results</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.4.1 or 3.1.6.1, TCP,
Representative and Head of Stream of all streams can open the
site-monitoring scheme</p></li>
<li><p>User can view the measurement record result table and
chart.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>User view the measurement record result table and
chart successfully</p>
<p><img src="media/image121.png"
style="width:6.63542in;height:3.34722in" /></p></td>
</tr>
</tbody>
</table>

### Filter on Site-monitoring records view

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.9.1</td>
<td>TCP Representative, Head of Stream</td>
<td></td>
<td>Successful case for filtering measurement record results</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.9.1, user can filter the
site-monitoring scheme measurement record</p></li>
<li><p>User can filter the records by selecting measurement date
range.</p></li>
<li><p>User can also filter the records in chart by selecting the
monitoring points and 3A levels.</p></li>
</ol>
<p><img src="media/image122.png"
style="width:6.63542in;height:1.66667in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>User view filtered records successfully</p>
<p><img src="media/image123.png"
style="width:6.63542in;height:1.55556in" /></p></td>
</tr>
</tbody>
</table>

### View measurement record history

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.10.1</td>
<td>TCP Representative, Head of Stream</td>
<td></td>
<td>Successful case for viewing measurement record history</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.7.1, users open the
site-monitoring scheme.</p></li>
<li><p>User selects measurement date in table and views measurement
record history filed by AS.</p></li>
<li><p>User select the version number of measurement record to view
history records and file date</p></li>
</ol>
<p><img src="media/image124.png"
style="width:6.63542in;height:1.61111in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>User view measurement record history by versions
successfully.</p>
<p><img src="media/image125.png"
style="width:6.63542in;height:2.75in" /></p>
<p><img src="media/image126.png"
style="width:6.63542in;height:2.75in" /></p></td>
</tr>
</tbody>
</table>

## BD Internal Login as BD Officer

### Departmental Login

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.1.1</td>
<td>BD Internal User</td>
<td></td>
<td>Successful case for BD Internal User to login via Departmental
Portal</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>BD Internal User (Officer or Admin) copy and paste the following
URL to browser and enter: “https://dsp.bd.ccgo.hksarg/cdpssuat”</p></li>
<li><p>BD Internal User login Departmental Portal with own DP Login ID
and password</p></li>
<li><p>BD Internal User successfully log in CDPSS via Departmental
Portal</p></li>
</ol>
<p><img src="media/image127.png"
style="width:6.63542in;height:1.33333in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">BD Internal Users log in CDPSS successfully via
Departmental Portal.</td>
</tr>
</tbody>
</table>

### BD Internal User Detail Management

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.2.1</td>
<td>BD Internal User</td>
<td></td>
<td>Successful case for BD Internal User to update personal and post
details</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the user login successfully in acceptance ID 3.2.1.1,
BD Internal user click on personal full name on top-right corner to
navigate to BD Internal User Detail page.</p></li>
<li><p>BD Internal User update details of personal information</p></li>
<li><p>BD Internal User edit the post information to update his/her
access right.</p></li>
<li><p>BD Internal User click “Submit” to complete the update.</p></li>
</ol>
<p><img src="media/image128.png"
style="width:6.63542in;height:0.44444in" /></p>
<p><img src="media/image129.png"
style="width:6.63542in;height:5.59722in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Account of BD Internal User is updated
successfully.</td>
</tr>
</tbody>
</table>

##  BD Internal Users Details Management

### Search BD Internal Users

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.1.1</td>
<td>BD admin</td>
<td></td>
<td>Successful case for BD admin to view BD Internal Users</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Login as BD admin</p></li>
<li><p>BD admin user clicks “BD User Administration”</p></li>
<li><p>BD admin user search BD internal users by entering email or / and
post title</p></li>
<li><p>BD admin user click “Search” to begin search</p></li>
</ol>
<p><img src="media/image130.png"
style="width:6.63542in;height:3.29167in" /></p>
<p><img src="media/image131.png"
style="width:6.63542in;height:3.02778in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>BD Admin Users searched BD Admin Users
successfully.</p>
<p><img src="media/image132.png"
style="width:6.63542in;height:1.73611in" /></p></td>
</tr>
</tbody>
</table>

### Create BD Internal User

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.2.1</td>
<td>BD admin</td>
<td></td>
<td>Successful case for BD admin to create BD Internal Users</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the public user selected in acceptance ID 3.3.1.1, BD
admin user click “Add” button to set up Departmental Login for BD
Internal Users.</p></li>
<li><p>BD admin user enter Departmental Login ID and Department ID of BD
Internal User.</p></li>
<li><p>BD admin user click “Save” to add the new user.</p></li>
</ol>
<p><img src="media/image133.png"
style="width:6.63542in;height:3.36111in" /><img src="media/image134.png"
style="width:6.63542in;height:3.27778in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Account of BD Internal User is created successfully. The
BD Internal User may login CDPSS via Departmental Portal.</td>
</tr>
</tbody>
</table>

### Edit BD Internal User

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.3.1</td>
<td>BD admin</td>
<td></td>
<td>Successful case for BD admin to edit BD Internal Users</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the user searched in acceptance ID 3.3.1.1, BD admin
user click “Edit” to navigate to BD Internal User Detail page.</p></li>
<li><p>BD admin user update details of BD Internal Users.</p></li>
<li><p>BD admin user edit the post information of BD Internal Users to
update their access right.</p></li>
<li><p>BD admin user click “Submit” to complete the update.</p></li>
</ol>
<p><img src="media/image135.png"
style="width:6.63542in;height:3.375in" /></p>
<p><img src="media/image136.png"
style="width:6.63542in;height:5.58333in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Account of BD Internal User is updated
successfully.</td>
</tr>
</tbody>
</table>

##  iAM Smart Integration

### Login via iAM Smart

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.1.1</td>
<td>Public user with iAM Smart account</td>
<td></td>
<td>Successful case for linkup and login via iAM Smart</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Public user enter CDPSS website login page</p></li>
<li><p>Public user click “Login with iAM Smart” button</p></li>
<li><p>Public user enters iAM Smart online service page.</p></li>
<li><p>Public user follows the instruction to prepare iAM Smart App on
his mobile device.</p></li>
<li><p>Public user scan the QR code shown on web.</p></li>
<li><p>If public user login CDPSS via iAM Smart for the 1st time, user
is redirected to CDPSS login page to enter email and password for linkup
confirmation.</p></li>
<li><p>Public user login CDPSS successfully.</p></li>
</ol>
<p><img src="media/image137.png"
style="width:6.63542in;height:4.56944in" /></p>
<p><img src="media/image138.png"
style="width:6.63542in;height:4.56944in" /></p>
<p><img src="media/image139.png"
style="width:6.63542in;height:3.34722in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Public user link up iAM Smart with CDPSS (if not
already) and login CDPSS successfully.</p>
<p>Note: Public user does not receive TOTP when login via iAM
Smart</p></td>
</tr>
</tbody>
</table>

## Notification

### View Notification List

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.1</td>
<td><blockquote>
<p>All users</p>
</blockquote></td>
<td></td>
<td>Successful case for viewing the notification list</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>On home page, tester clicks the “Notification”
icon</p>
<p><img src="media/image140.png"
style="width:6.64236in;height:1.93125in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester successfully views different kind of email
notification on the screen with relevant email subject, email sender
address and email sent date.</p>
<p><img src="media/image141.png"
style="width:6.64236in;height:2.97431in" /></p></td>
</tr>
</tbody>
</table>

### View Notification Details

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.1</td>
<td><blockquote>
<p>All users</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for viewing the notification details</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester clicks “View” button on notification list</p>
<p><img src="media/image142.png"
style="width:6.64236in;height:2.97986in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can see the contents of email notification
including email subject, email sender, email receipients,</p>
<p><img src="media/image143.png"
style="width:6.64236in;height:2.20278in" /></p></td>
</tr>
</tbody>
</table>

###  

### Clickable Link in Notification

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td><blockquote>
<p>All users</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for redirecting to another page by clicking on the
clink in notification</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester clicks on the link in the notification</p>
<p><img src="media/image144.png"
style="width:6.64236in;height:2.14444in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">System redirects the tester to relevant system
page.</td>
</tr>
</tbody>
</table>

###  

### Manage and opt-out email notification

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.4.1</td>
<td><blockquote>
<p>Hos, Rep, AP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for opt-out the email notification</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester clicks on the username icon on top right corner of home
page (Picture 1).</p></li>
<li><p>Tester turns on the “Opt-Out Notifications” button and then press
“Submit” button.</p></li>
</ol>
<p><strong><u>Picture 1</u></strong></p>
<p><img src="media/image145.png"
style="width:6.64236in;height:2.24375in" /></p>
<p><strong><u>Picture 2</u></strong></p>
<p><img src="media/image146.png"
style="width:6.64236in;height:2.57778in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester no longer receives email notification from
their registered email address but can still view the email notification
details from notification list.</p>
<p><img src="media/image147.png"
style="width:6.64236in;height:3.28403in" /></p></td>
</tr>
</tbody>
</table>

###  

##  Information Reports

### Report for List of Heads of Stream and their Responsible Sites

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.1.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for list of Heads of Stream
and their responsible sites</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of Heads of Stream and their responsible
sites” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol>
<p><img src="media/image148.png"
style="width:6.64236in;height:3.21111in" /></p>
<p><img src="media/image149.png"
style="width:6.64236in;height:3.38264in" /></p>
<p><img src="media/image150.png"
style="width:6.64236in;height:2.58125in" /></p>
<p><img src="media/image151.png"
style="width:6.64236in;height:2.60625in" /></p>
<p><img src="media/image152.png"
style="width:6.64236in;height:3.2125in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Given Name</p></li>
<li><p>English Last Name</p></li>
<li><p>Chinese Full Name (if any)</p></li>
<li><p>Email address</p></li>
<li><p>Responsible Site Reference</p></li>
<li><p>Responsible Site Project Stream</p></li>
<li><p>Registration Number</p></li>
<li><p>Number of responsible Supervision Plans</p></li>
<li><p>Number of Responsible Form A Template</p></li>
<li><p>Number of Responsible non-conformities (Form B)</p></li>
<li><p>Number of Responsible Form App-158 Template</p></li>
<li><p>Creation Date of Site</p></li>
<li><p>Tentative Commencement Date of Site</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of TCPs and assigned sites/supervision plans

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.2.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of TCPs and assigned
sites/supervision plans</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of TCPs and assigned sites/supervision
plans” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Given Name</p></li>
<li><p>English Last Name</p></li>
<li><p>Chinese Full Name</p></li>
<li><p>Email address</p></li>
<li><p>Assigned Site Reference</p></li>
<li><p>Assigned Supervision Plan Stream</p></li>
<li><p>Assigned Supervision Plan Type of building works and street
works</p></li>
<li><p>Assigned Supervision Plan Specific type of building works and
street works</p></li>
<li><p>Grade</p></li>
<li><p>Is Representative</p></li>
<li><p>Number of Responsible Form A Template</p></li>
<li><p>Number of Responsible non-conformities (Form B)</p></li>
<li><p>Number of Responsible Form App-158 Template</p></li>
<li><p>Number of Site-monitoring Scheme</p></li>
<li><p>Assignment Start Date</p></li>
<li><p>Assignment End Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of non-conformities (Form B)

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.3.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of non-conformities
(Form B)</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of non-conformities (Form B)” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Reference</p></li>
<li><p>Site Address</p></li>
<li><p>Site Lot Number</p></li>
<li><p>Stream</p></li>
<li><p>Part 1: Date Discovered</p></li>
<li><p>Part 1: Details of non-conformities</p></li>
<li><p>Part 1: Pose Imminent Danger</p></li>
<li><p>English Full Name of TCP Completing Part 1</p></li>
<li><p>Grade of TCP completing Part 1</p></li>
<li><p>Date of completing Part 1</p></li>
<li><p>English Full Name of Head of Stream responding Imminent danger
posed in Part 1</p></li>
<li><p>Date of Head of Stream responding Imminent danger posed in Part
1</p></li>
<li><p>Date of AP reporting Part 1 to BD</p></li>
<li><p>Part 2: English Full Name of TCP Instruction for rectification
given to</p></li>
<li><p>Part 2: Email address of TCP Instruction for rectification given
to</p></li>
<li><p>Part 2: Stream of RC TCP Instruction for rectification given
to</p></li>
<li><p>Part 2: Grade of TCP Instruction for rectification given
to</p></li>
<li><p>Part 2: Instruction issue date</p></li>
<li><p>Part 2: Details of Instructions</p></li>
<li><p>Part 2: Date of rectification works certified completion</p></li>
<li><p>Date of AP reporting RC fail to comply to BD (To be developed
later)</p></li>
<li><p>English Full Name of TCP completing Part 2</p></li>
<li><p>Grade of TCP completing Part 2</p></li>
<li><p>Date of completing Part 2</p></li>
<li><p>English Full Name of Head of Stream responding Imminent danger
posed in Part 2</p></li>
<li><p>Date of Head of Stream responding Imminent danger posed in Part
2</p></li>
<li><p>Date of AP reporting Part 2 to BD</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of inspection records of Form APP-158

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.4.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of inspection records
of Form APP-158</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of inspection records of Form APP-158” as
the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Reference</p></li>
<li><p>Site Address</p></li>
<li><p>Site Lot Number</p></li>
<li><p>Stream</p></li>
<li><p>Types of Work</p></li>
<li><p>Responsible TCP English Full Name</p></li>
<li><p>Responsible TCP Grade</p></li>
<li><p>Responsible TCP Email Address</p></li>
<li><p>Responsible Representative English Full Name</p></li>
<li><p>Responsible Representative Grade</p></li>
<li><p>Responsible Representative Email Address</p></li>
<li><p>Responsible Head of Stream English Full Name</p></li>
<li><p>Responsible Head of Stream Registration Number</p></li>
<li><p>Responsible Head of Stream Email Address</p></li>
<li><p>Record Date</p></li>
<li><p>First File Date</p></li>
<li><p>Last File Date</p></li>
<li><p>Inspection Total Number Item</p></li>
<li><p>Inspection Status for S</p></li>
<li><p>Inspection Status for NS</p></li>
<li><p>Inspection Status for NA</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of inspection records of Form A

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.5.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of inspection records
of Form A</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of inspection records of Form A” as the
report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Address</p></li>
<li><p>Site Lot Number</p></li>
<li><p>Stream</p></li>
<li><p>Types of Work</p></li>
<li><p>Responsible TCP English Full Name</p></li>
<li><p>Responsible TCP Grade</p></li>
<li><p>Responsible TCP Email Address</p></li>
<li><p>Responsible Representative English Full Name</p></li>
<li><p>Responsible Representative Grade</p></li>
<li><p>Responsible Representative Email Address</p></li>
<li><p>Responsible Head of Stream English Full Name</p></li>
<li><p>Responsible Head of Stream Registration Number</p></li>
<li><p>Responsible Head of Stream Email Address</p></li>
<li><p>Record Date</p></li>
<li><p>First File Date</p></li>
<li><p>Last File Date</p></li>
<li><p>Inspection Total Number Item</p></li>
<li><p>Inspection Status for S</p></li>
<li><p>Inspection Status for NS</p></li>
<li><p>Inspection Status for NA</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of Supervision Plans (SP)

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.6.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of Supervision Plans
(SP)</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of Supervision Plans (SP)” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Reference</p></li>
<li><p>Site Address</p></li>
<li><p>Site Lot Number</p></li>
<li><p>Site Responsible AP English Full Name</p></li>
<li><p>Site Responsible AP Registration Number</p></li>
<li><p>Site Responsible AP Email Address</p></li>
<li><p>Site Responsible RSE English Full Name</p></li>
<li><p>Site Responsible RSE Registration Number</p></li>
<li><p>Site Responsible RSE Email Address</p></li>
<li><p>Site Responsible RGE English Full Name</p></li>
<li><p>Site Responsible RGE Registration Number</p></li>
<li><p>Site Responsible RGE Email Address</p></li>
<li><p>Site Responsible AS English Full Name</p></li>
<li><p>Site Responsible AS Registration Number</p></li>
<li><p>Site Responsible AS Email Address</p></li>
<li><p>Total Number of Active AP TCP</p></li>
<li><p>Total Number of Active RSE TCP</p></li>
<li><p>Total Number of Active RGE TCP</p></li>
<li><p>Total Number of Active RC TCP</p></li>
<li><p>Type of building works and street works</p></li>
<li><p>Specific type of building works and street works</p></li>
<li><p>Total Number of Form A Templates</p></li>
<li><p>Total Number of Form A Records</p></li>
<li><p>Total Number of Form B</p></li>
<li><p>Total Number of Form App-158 Templates</p></li>
<li><p>Total Number of Form App-158 Records</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of Sites

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.7.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of Sites</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of Sites” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Reference</p></li>
<li><p>Site Address</p></li>
<li><p>Lot Number</p></li>
<li><p>Responsible AP English Full Name</p></li>
<li><p>Responsible AP Registration Number</p></li>
<li><p>Responsible AP Email Address</p></li>
<li><p>Responsible RSE English Full Name</p></li>
<li><p>Responsible RSE Registration Number</p></li>
<li><p>Responsible RSE Email Address</p></li>
<li><p>Responsible RGE English Full Name</p></li>
<li><p>Responsible RGE Registration Number</p></li>
<li><p>Responsible RGE Email Address</p></li>
<li><p>Responsible AS English Full Name</p></li>
<li><p>Responsible AS Registration Number</p></li>
<li><p>Responsible AS Email Address</p></li>
<li><p>Total Number of Active AP TCP</p></li>
<li><p>Total Number of Active RSE TCP</p></li>
<li><p>Total Number of Active RGE TCP</p></li>
<li><p>Total Number of Active RC TCP</p></li>
<li><p>Tentative Commencement Date</p></li>
<li><p>Total Number of Supervision Plans</p></li>
<li><p>Total Number of Form A Templates</p></li>
<li><p>Total Number of Form A Records</p></li>
<li><p>Total Number of Form B</p></li>
<li><p>Total Number of Form App-158 Templates</p></li>
<li><p>Total Number of Form App-158 Records</p></li>
<li><p>Total Number of Site-Monitoring Schemes</p></li>
<li><p>Total Number of Site-Monitoring Records</p></li>
<li><p>Total Number of Site-Monitoring Alerts Notifications</p></li>
<li><p>Total Number of Site-Monitoring Alarm Notifications</p></li>
<li><p>Total Number of Site-Monitoring Action Notifications</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of site-monitoring records with 3A levels filter

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.8.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of site-monitoring
records with 3A levels filter</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on the system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of site-monitoring records with 3A levels
filter” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on the “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Reference</p></li>
<li><p>Site Address</p></li>
<li><p>Site Lot Number</p></li>
<li><p>Name of Scheme</p></li>
<li><p>Type of Monitoring</p></li>
<li><p>Alert Level (Positive)</p></li>
<li><p>Alarm Level (Positive)</p></li>
<li><p>Action Level (Positive)</p></li>
<li><p>Alert Level (Negative)</p></li>
<li><p>Alarm Level (Negative)</p></li>
<li><p>Action Level (Negative)</p></li>
<li><p>Record Date</p></li>
<li><p>First File Date</p></li>
<li><p>Last File Date</p></li>
<li><p>Monitoring Point Total Number Item</p></li>
<li><p>Total Alert Levels</p></li>
<li><p>Total Alarm Levels</p></li>
<li><p>Total Action Levels</p></li>
</ul></td>
</tr>
</tbody>
</table>

##  Activities Reports

### Report for Monitoring Point

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.1.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for Monitoring Point</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “Monitoring Point” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Role of user (AS/Rep/TCP)</p></li>
<li><p>Site Reference</p></li>
<li><p>Site-monitoring scheme name</p></li>
<li><p>Monitoring Point Changed (Hide and To Be Developed
later)</p></li>
<li><p>Monitoring Point Actual</p></li>
<li><p>Start Date</p></li>
<li><p>End Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for 3A level changes

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.2.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for 3A level changes</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “3A level changes” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Role of user (AS/Rep/TCP)</p></li>
<li><p>Site Reference</p></li>
<li><p>Site-monitoring scheme name</p></li>
<li><p>Level changed (Alert/Alarm/Action)</p></li>
<li><p>Previous value</p></li>
<li><p>Updated value</p></li>
<li><p>Action Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of site-monitoring activities

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.3.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of site-monitoring
activities</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of site-monitoring activities” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Role of user (AS/Rep/TCP)</p></li>
<li><p>Site Reference</p></li>
<li><p>Site-monitoring scheme name</p></li>
<li><p>Action Description (Create Scheme/ Save as Draft / Import records
/ File)</p></li>
<li><p>Action Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of inspection item checklist changes

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.4.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of inspection item
checklist changes</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of inspection item checklist changes” as the
report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Role of user (AP/RSE/RGE/AS/Rep/TCP)</p></li>
<li><p>Stream of user</p></li>
<li><p>Site Reference</p></li>
<li><p>Template Name</p></li>
<li><p>Inspection Form (Form A / Form App-158)</p></li>
<li><p>Changed Template Item Description</p></li>
<li><p>Action (Addition/removal)</p></li>
<li><p>Action Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of site activities

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.5.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of site
activities</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of site activities” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Site Reference of recorded site</p></li>
<li><p>Action Date</p></li>
<li><p>Related Module (Site/Form A/Form B/Form
App-158/Site-monitoring)</p></li>
<li><p>Action Description (Create Template / Save as Draft / Import
records / File / Upload attachment)</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Notification reports

### Report for List of site inspection reminders

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.1.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of site inspection
reminders</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of site inspection reminders” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Reminder Subject</p></li>
<li><p>Reminder To Recipients</p></li>
<li><p>Reminder CC Recipients</p></li>
<li><p>Reminder Content</p></li>
<li><p>Reminder Send Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for list of site inspection notifications

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.2.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for list of site inspection
notifications</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “list of site inspection notifications” as the
report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Notification Subject</p></li>
<li><p>Notification To Recipients</p></li>
<li><p>Notification CC Recipients</p></li>
<li><p>Notification Content</p></li>
<li><p>Notification Send Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of site-monitoring alerts

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.3.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of site-monitoring
alerts</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of site-monitoring alerts” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Alert Subject</p></li>
<li><p>Level of alert (Alert/Alarm/Action)</p></li>
<li><p>Alert To Recipients</p></li>
<li><p>Alert CC Recipients</p></li>
<li><p>Alert Content</p></li>
<li><p>Alert Send Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Unfiled Record Reminder

|         |          |     |                                                                                 |     |
|-----------|--------|-------|------------------------------------|-----------|
| 3.5.1.1 | TCP, HOS |     | Successful case for Unfiled Record Reminder for Level 5 Frequency of Inspection |     |

<u>Required number of filed records for different inspection frequency
are as below</u>

<img src="media/image153.png" style="width:3.0427in;height:3.61247in" />

### Unfiled Record Reminder for Level 5 Frequency of Inspection

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.3.2</td>
<td>RC TCP, AS HOS</td>
<td></td>
<td>Successful case for assigning a TCP to supervision plan</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>HOS creates a supervision plan with Level 5 inspection
frequency.</p></li>
<li><p>HOS set the working date of the supervision plan from Monday to
Friday.</p></li>
<li><p>HOS assigns a TCP into a Form A Template which has Actual Start
Date = 01 Aug under the supervision plan.</p></li>
<li><p>TCP creates a draft record in Form A on 3 Aug</p></li>
<li><p>HOS deliberately does not file the draft record of Form A created
by the TCP</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">HOS will receive email notification for unfiled record
on 14 Aug</td>
</tr>
</tbody>
</table>

## Batch file for site monitoring records

### Unfiled Record Reminder for Level 5 Frequency of Inspection

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.6.1.1</td>
<td>RC TCP, AS HOS</td>
<td></td>
<td>Successful case for Batch file for site monitoring records</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP from RC stream create draft records on 2 different days
(Picture 1)</p></li>
<li><p>AS from RC stream press “Batch File” button (Picture 2)</p></li>
<li><p>AS from RC stream select all two days records and then press
“Confirm” button (Picture 3)</p></li>
</ol>
<p><strong><u>Picture 1</u></strong></p>
<p><img src="media/image154.png"
style="width:2.11701in;height:2.50617in" /></p>
<p><strong><u>Picture 2</u></strong></p>
<p><img src="media/image155.png"
style="width:6.63542in;height:2.77778in" /></p>
<p><strong><u>Picture 3</u></strong></p>
<p><img src="media/image156.png"
style="width:6.63542in;height:1.88889in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS from RC stream file the records by bulk
successfully</td>
</tr>
</tbody>
</table>

## Create, Update and Remove BD Officer from Site Project

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1</td>
<td><blockquote>
<p>BD Officer</p>
</blockquote></td>
<td></td>
<td>Successful case for create, update and remove BD Officer from Site
Project</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>BD Officer clicks “Edit” button of the existing Site
Project</p></li>
</ol>
<p><img src="media/image157.png"
style="width:6.64236in;height:1.64236in" /></p>
<ol start="2" type="1">
<li><p>Select the post title from the dropdown list and then press
‘Save’ button</p></li>
</ol>
<p><img src="media/image158.png"
style="width:6.64236in;height:2.25486in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>System displays the name and email of the BD Officer besides the
post title.</p></li>
<li><p>The newly added BD Officer can view and monitor the Site Project
as well as receiving email notification for relevant alerts.</p></li>
</ol>
<p><img src="media/image141.png"
style="width:6.64236in;height:2.97431in" /></p></td>
</tr>
</tbody>
</table>

## New Type of Monitoring for Site Monitoring

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2</td>
<td><blockquote>
<p>AS</p>
</blockquote></td>
<td></td>
<td>Successful case for creating new type of monitoring for site
monitoring</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AS presses “Create Scheme” button on site monitoring
page</p></li>
</ol>
<p><img src="media/image159.png"
style="width:6.65208in;height:2.85625in" /></p>
<ol start="2" type="1">
<li><p>AS input values in below mandatory fields and select “Service
Settlement (Ground)” in “Type of Monitoring” field</p>
<ol type="i">
<li><p>Name of Scheme</p></li>
<li><p>Type of Works</p></li>
<li><p>3A Level</p></li>
<li><p>Name of Monitoring Stations</p></li>
<li><p>Initial Reading of Monitoring Stations</p></li>
</ol></li>
</ol>
<p><img src="media/image160.png"
style="width:6.65208in;height:2.88889in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS creates new site monitoring scheme with “Service
Settlement (Ground)” type of monitoring</td>
</tr>
</tbody>
</table>

# 4. Test Case for Mobile

## User Management

### Public User registration

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>successful case for registering new account</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Remark: AP tests on behalf of AP, RSE, RGE and AS</p>
<ol type="1">
<li><p>Upon the launch of the app, on the login page, press “Register”
at the bottom.</p></li>
</ol>
<blockquote>
<p><img src="media/image161.jpg"
style="width:3.52326in;height:5.45912in" /></p>
</blockquote>
<ol start="2" type="1">
<li><p>AP fill in his information (refer to the testing information
provided in separate document) to the relevant fields for registering
the new account as Head of Stream</p></li>
<li><p>AP then finally need to tick to agree both “Declaration of the
applicant” and “Terms and conditions”, and press “Submit” button at the
bottom</p></li>
</ol>
<p><img src="media/image162.jpg"
style="width:2.67882in;height:5.53416in" /><img src="media/image163.jpg"
style="width:2.68973in;height:5.54413in" /><img src="media/image164.jpg"
style="width:2.68993in;height:5.53484in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AP registers a new account in CDPSS as Head of Stream
successfully and receives an email with Account Activation Email
Notification and an activation link</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 15%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.2</td>
<td>AP</td>
<td></td>
<td><blockquote>
<p>fail case for register new account – wrong username (English)</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Remark: AP tests on behalf of AP, RSE, RGE and AS</p>
<ol type="1">
<li><p>AP inputs the same information as in Acceptance ID 3.1.1.1 except
changing the value in User Name (English) field to “Chan Tai大 Man” on
the Registration page, and press “Submit”</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>AP fails to register a new account in CDPSS since
there is Chinese word existing in the field of User Name (English)</p>
<p><img src="media/image165.jpg"
style="width:6.61458in;height:2.01389in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.3</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Fail case for register new account – wrong password</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Remark: AP tests on behalf of AP, RSE, RGE and AS</p>
<ol type="1">
<li><p>AP clicks the “Register” button on the User Management
page.</p></li>
<li><p>AP inputs the same information as in Acceptance ID 3.1.1 except
changing value of the “password” and “confirm password” field to
“1234567890"</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>AP fails to register a new account in CDPSS since the
password is invalid (no English alphabet existing in the password)</p>
<p><img src="media/image166.jpg"
style="width:6.47917in;height:1.91667in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 34%" />
<col style="width: 34%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.4</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Fail case for register new account – value in confirm password field
does not consist with password field</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Remark: AP tests on behalf of AP, RSE, RGE and AS</p>
<ol type="1">
<li><p>AP click the “Create User” button on the User Management
page.</p></li>
<li><p>AP inputs the same information as in Acceptance ID 3.1.1.1 except
changing the value in “Confirm Password” field to
“aA666666666@”</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>AP fails to register a new account in CDPSS since the
value in “Confirm Password” field does not consist with the value in
“Password” field</p>
<p><img src="media/image167.jpg"
style="width:7.11458in;height:5.36111in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 34%" />
<col style="width: 34%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.5</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Fail case for register new account – wrong AP registration number</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Remark: AP tests on behalf of AP, RSE, RGE and AS</p>
<ol type="1">
<li><p>AP clicks the “Create User” button on the User Management
page.</p></li>
<li><p>AP inputs the same information as in Acceptance ID 3.1.1.1 except
changing the AP registration number to “AP(A) 123/456”</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>AP fails to register a new account in CDPSS since the
AP registration number is not registered in CDPSS</p>
<p><img src="media/image168.jpg"
style="width:7.11458in;height:9.40278in" /></p></td>
</tr>
</tbody>
</table>

### Public login

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 35%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>System generates a one-time password when the user accesses the
system.</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>In reference to the account registered in acceptance
ID 3.1.1.1, input email and password, then press the Login button</p>
<p><img src="media/image169.jpg"
style="width:2.96076in;height:4.48876in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>The mobile app should show one-time password page and
wait for input, and user should receive a one-time password (OTP) in his
registered email address generated by the system after a short
while.</p>
<p><img src="media/image170.jpg"
style="width:3.18585in;height:4.25246in" /><img src="media/image171.jpg"
style="width:3.3891in;height:2.70038in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 11%" />
<col style="width: 38%" />
<col style="width: 37%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.2</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td><blockquote>
<p>Fail case for system to generate one time password when user access
into system - wrong email address</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="4">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="4">N/A</td>
</tr>
<tr class="odd">
<td colspan="4"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="4">In reference to the account registered in acceptance ID
3.1.1.1, input an incorrect email address and press login button</td>
</tr>
<tr class="odd">
<td colspan="4"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="4"><p>Error message of “Incorrect email / password” should
prompt out since user inputs the wrong email address</p>
<p><img src="media/image172.jpg"
style="width:3.56673in;height:5.56496in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.3</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Fail case for system to generate one time password when user access
into system - wrong password</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5">In reference to the account registered in acceptance ID
3.1.1.1, input correct email address but with wrong password</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Error message of “Incorrect email / password” should
prompt out since user inputs the wrong password</p>
<p><img src="media/image173.jpg"
style="width:2.75911in;height:4.31496in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.4</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>User use one time password to login into system</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>In reference to acceptance ID 3.1.1.10</p>
<ol type="1">
<li><p>APUser inputs the one-time password received from his registered
email address into One-Time Password field</p></li>
<li><p>APUser presses Login button</p></li>
</ol>
<p><img src="media/image174.jpg"
style="width:2.91958in;height:3.85663in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>User login into system successfully and a list of
owned site project will be shown, which if it is a new account, the list
should be empty</p>
<p><img src="media/image175.jpg"
style="width:4.20582in;height:3.04559in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.5</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>System allow user to reset password</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>User press Forget Password link on the login page (picture
1)</p></li>
<li><p>User input his registered email address into the email field
(picture 2)</p></li>
<li><p>System prompts out notification message (picture 3)</p></li>
</ol>
<p><strong><u>Picture 1</u></strong></p>
<p><img src="media/image161.jpg"
style="width:3.52326in;height:5.45912in" /></p>
<p><strong><u>Picture 2</u></strong></p>
<p><img src="media/image176.jpg"
style="width:3.26341in;height:3.83164in" /></p>
<p><strong><u>Picture 3</u></strong></p>
<p><img src="media/image177.jpg"
style="width:2.91054in;height:2.75246in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>User receives an email with reset password link from
his registered email address, and shall proceed to reset the password
via the link under web interface</p>
<p><img src="media/image178.jpg"
style="width:3.72161in;height:2.8358in" /></p></td>
</tr>
</tbody>
</table>

### User Management - Others

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for user to change password</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>After successful login as in Acceptance ID 3.1.1.1, user press
the top right person icon to enter user information page</p></li>
</ol>
<blockquote>
<p><img src="media/image179.jpg"
style="width:3.9816in;height:2.2961in" /></p>
</blockquote>
<ol start="2" type="1">
<li><p>User input existing password into “Current password”
field</p></li>
<li><p>User input a new password into “New password” field</p></li>
<li><p>User input repeat the new password into “Confirm new password”
field</p></li>
</ol>
<blockquote>
<p><img src="media/image180.jpg"
style="width:3.70634in;height:7.59621in" /></p>
</blockquote>
<ol start="5" type="1">
<li><p>User press “Submit” button</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>System displays successful message and go back to
previous page</p>
<p><img src="media/image181.jpg"
style="width:4.39826in;height:1.23657in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.2</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Fail case for user to change password - retype new password does not
consist with new password</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>User enters into account detail page after successful login as in
Acceptance ID 3.1.1.1</p></li>
<li><p>User input the updated password from Acceptance ID 3.1.3.1 into
“Current password” field</p></li>
<li><p>User input aA173173173@ into “New password” field</p></li>
<li><p>User input 1234 into “Confirm new password” field</p></li>
<li><p>User press “Submit” button</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>System prompts out error message and user fails to
change his password since “New password” and “Confirm new password”
field does not consist with the new password</p>
<p><img src="media/image182.jpg"
style="width:3.49201in;height:1.94125in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.3</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Fail case for user to change password - new password does not meet
requirement of minimum length</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>User enters into account detail page after successful login as in
Acceptance ID 3.1.1.1</p></li>
<li><p>User input aA1@ into “Password” field</p></li>
<li><p>User input aA1@ into “Retype the new password” field</p></li>
<li><p>User press “Submit” button</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>System prompts an error message and the user fails to
change his password since the new password aA1@ does not meet the
requirement of minimum length for the password character.</p>
<p><img src="media/image183.jpg"
style="width:6.52083in;height:2.81944in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.4</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Fail case for user to change password - new password does not meet
the requirement of mixed-case alphabetic character</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>User enters into account detail page after successful login as in
Acceptance ID 5.1.1</p></li>
<li><p>User input bb173173173@ into “New password” field</p></li>
<li><p>User input bb173173173@ into “Retype the new password”
field</p></li>
<li><p>User press “Submit” button</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>System prompts out error message and user fails to
change his password since new password bb173173173@ does not meet the
requirement of mixed-case alphabetic character</p>
<p><img src="media/image183.jpg"
style="width:6.52083in;height:2.81944in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.5</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Fail case for user to change password - new password does not meet
the requirement of having at least one special characters</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>User enters into account detail page after successful login as in
Acceptance ID 5.1.1</p></li>
<li><p>User input aA168762989@ into “Your current password”
field</p></li>
<li><p>User input aA123456 into “New password” field</p></li>
<li><p>User input aA123456 into “Retype the new password” field</p></li>
<li><p>User press “Submit” button</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>System prompts out error message and user fails to
change his password since new password aA123456 does not meet the
requirement of having at least one special characters</p>
<p><img src="media/image183.jpg"
style="width:6.52083in;height:2.81944in" /></p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.6</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for updating personal information in “Update Account
Info” page</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>In reference to Acceptance ID 5.1.1, user enters into “Update
Account Info” page</p></li>
<li><p>User inputs below information to the relevant fields</p></li>
</ol>
<ul>
<li><p>Salutation – Mr.</p></li>
<li><p>English Family Name – Chan</p></li>
<li><p>English Given Name – Tai Man</p></li>
<li><p>Chinese Full Name – 陳大文</p></li>
<li><p>HKID - P6742177</p></li>
<li><p>Phone Number – 61236123</p></li>
</ul>
<ol start="3" type="1">
<li><p>User press “Submit” button</p></li>
</ol>
<p><img src="media/image184.jpg"
style="width:3.15264in;height:5.56496in" /><img src="media/image185.jpg"
style="width:3.25243in;height:3.34222in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">User changes his phone number to 61236123
successfully</td>
</tr>
</tbody>
</table>

|     |     |     |     |     |
|-----|-----|-----|-----|-----|
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |
|     |     |     |     |     |

## Site Projects and Supervision Plan management

### Search responsible Site Project

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.1.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for Head of Stream searches for site project, which
they are responsible for - single search result</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AP press the bottom right “Add” button and reach the “Available
site project” list page</p></li>
</ol>
<blockquote>
<p><img src="media/image186.jpg"
style="width:3.43993in;height:1.31882in" /></p>
</blockquote>
<ol start="2" type="1">
<li><p>AP search site project by inputting BD reference</p></li>
</ol>
<blockquote>
<p><img src="media/image187.jpg"
style="width:3.03824in;height:2.38788in" /></p>
</blockquote></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>System prompts detail of the site project in
reference to the inputted BD reference</p>
<p><img src="media/image188.jpg"
style="width:3.10162in;height:1.93728in" /></p></td>
</tr>
</tbody>
</table>

### Create Site Project from submitted Supervision plan

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.2.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for creating Site Project from the submitted
Supervision plan</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester press on an available site project from the list</p></li>
</ol>
<blockquote>
<p><img src="media/image187.jpg"
style="width:3.03824in;height:2.38788in" /></p>
</blockquote>
<ol start="2" type="1">
<li><p>Tester fill in the “Lot No.” field</p></li>
<li><p>Tester press “Submit” button on the site project info
page</p></li>
</ol>
<blockquote>
<p><img src="media/image189.jpg"
style="width:3.19869in;height:4.4608in" /></p>
</blockquote></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>The new project is created successfully, and app will
go back to site project list page with the new site project on list.</p>
<p><img src="media/image190.jpg"
style="width:3.29984in;height:1.1017in" /></p></td>
</tr>
</tbody>
</table>

### Edit and update Site Project Detail

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.3.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for editing and updating site project detail</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester select a site project on site project list by pressing one
site project</p></li>
</ol>
<blockquote>
<p><img src="media/image191.jpg"
style="width:2.95035in;height:2.45077in" /></p>
</blockquote>
<ol start="2" type="1">
<li><p>Tester then press the edit button for the project</p></li>
</ol>
<blockquote>
<p><img src="media/image192.jpg"
style="width:3.35417in;height:3.91524in" /></p>
</blockquote>
<ol start="3" type="1">
<li><p>Tester can then amend the address and lot number of the site
project</p></li>
</ol>
<blockquote>
<p><img src="media/image193.jpg"
style="width:3.38542in;height:4.6992in" /></p>
</blockquote>
<ol start="4" type="1">
<li><p>Tester press submit button on the page after amending</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>The app will go back to site project detail page with
the address and lot number updated accordingly.</p>
<p><img src="media/image194.jpg"
style="width:2.88542in;height:5.72854in" /></p></td>
</tr>
</tbody>
</table>

### Create Supervision Plan under a Site Project

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.4.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>AP/RSE/RGE/AS create a supervision plan under a site project</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester select a site project from the site projects list to reach
site project detail page</p></li>
</ol>
<blockquote>
<p><img src="media/image195.jpg"
style="width:2.90868in;height:2.32539in" /></p>
</blockquote>
<ol start="2" type="1">
<li><p>Tester press “Create” button in “Supervision Plans”
section</p></li>
</ol>
<blockquote>
<p><img src="media/image196.jpg"
style="width:2.83565in;height:5.67955in" /></p>
</blockquote>
<ol start="3" type="1">
<li><p>Tester fill in the create supervision plan form by providing type
of works, approval date, grade, inspection frequency and count of TCPs
involved in this plan</p></li>
</ol>
<blockquote>
<p><img src="media/image197.jpg"
style="width:2.99797in;height:4.73163in" /><img src="media/image198.jpg"
style="width:2.80451in;height:3.77398in" /></p>
</blockquote>
<ol start="4" type="1">
<li><p>Tester then press the submit to create the supervision
plan</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester is able to create a supervision plan with
details and back to site project list page, with supervision plan listed
at the bottom of the page.</p>
<p><img src="media/image199.jpg"
style="width:3.15868in;height:2.36144in" /></p></td>
</tr>
</tbody>
</table>

### Supervision Plan Detail View

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.5.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>AP/RSE/RGE/AS views the supervision plan detail of the project</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester, in site project detail page, see the list of supervision
plans under that site project</p></li>
</ol>
<blockquote>
<p><img src="media/image199.jpg"
style="width:2.80451in;height:2.09667in" /></p>
</blockquote>
<ol start="2" type="1">
<li><p>Tester then press a supervision plan in that project</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester is able to view the details of the supervision
plan</p>
<blockquote>
<p><img src="media/image200.jpg"
style="width:2.89826in;height:4.52904in" /></p>
</blockquote></td>
</tr>
</tbody>
</table>

## Form A

### Create Form A template

Before proceeding with the test cases below, the new supervision plan
should have at least one TCP being assigned.

This TCP assignment function is only available in web version, please
follow the Acceptance ID to perform.

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.1.1</td>
<td><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Create Form A template</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>In the supervision plan detail page, tester clicks “Form A”
button</p></li>
</ol>
<blockquote>
<p><img src="media/image201.jpg"
style="width:3.32535in;height:2.61884in" /></p>
</blockquote>
<ol start="2" type="1">
<li><p>Tester press “Create template” button</p></li>
</ol>
<blockquote>
<p><img src="media/image202.jpg"
style="width:3.27326in;height:2.65626in" /></p>
</blockquote>
<ol start="3" type="1">
<li><p>Tester fill in the Form A template creation form with the Type of
works, grade of TCP responsible of the form A template, items to be
included in the form A template, and add extra inspection item as
needed.</p></li>
</ol>
<blockquote>
<p><img src="media/image203.jpg"
style="width:3.4485in;height:6.82538in" /></p>
</blockquote>
<ol start="4" type="1">
<li><p>Tester clicks “Create” button</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>The app go back to the form A template list page with
the new form A template on list.</p>
<p><img src="media/image204.jpg"
style="width:3.45222in;height:3.04413in" /></p></td>
</tr>
</tbody>
</table>

### Create Form A 

<table style="width:100%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 13%" />
<col style="width: 37%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.2.1</td>
<td>TCP</td>
<td></td>
<td><blockquote>
<p>Create Form A</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester login as TCP that is being added to the same supervision
plan as Acceptance ID 3.4.1.1, and being assigned to the TCP grade with
the form A template set.</p></li>
<li><p>TCP selects the site project, supervision plan and reaches the
Form A template list page, which should find the assigned Form A
template.</p></li>
</ol>
<blockquote>
<p><img src="media/image205.jpg"
style="width:2.7316in;height:2.19924in" /></p>
</blockquote>
<ol start="3" type="1">
<li><p>TCP presses the form A template and reaches the record
page.</p></li>
<li><p>TCP select a date to expand, and press “Create”</p></li>
</ol>
<blockquote>
<p><img src="media/image206.jpg"
style="width:2.90868in;height:6.00451in" /></p>
</blockquote>
<ol start="5" type="1">
<li><p>TCP pick the status of each inspection point (S / NS /
NA).</p></li>
</ol>
<blockquote>
<p><img src="media/image207.jpg"
style="width:2.96076in;height:3.81683in" /></p>
</blockquote>
<ol start="6" type="1">
<li><p>Press “Save as draft” button to save the inspection
record.</p></li>
<li><p>Press the right button of that item to bring up the attachment
popup, press the “+” button.</p></li>
</ol>
<blockquote>
<p><img src="media/image208.jpg"
style="width:2.93993in;height:1.99126in" /></p>
</blockquote>
<ol start="8" type="1">
<li><p>Select an attachment file from the device.</p></li>
<li><p>File will be uploaded and listed in the popup, close the
popup.</p></li>
</ol>
<blockquote>
<p><img src="media/image209.jpg"
style="width:2.83576in;height:2.24234in" /><img src="media/image210.jpg"
style="width:3.54935in;height:3.81016in" /></p>
</blockquote></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">An new Form A is created in “Draft” state with
attachment</td>
</tr>
</tbody>
</table>

### File Form A

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 11%" />
<col style="width: 12%" />
<col style="width: 41%" />
<col style="width: 21%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.3.1</td>
<td>AP / RSE / RGE / AS</td>
<td></td>
<td><blockquote>
<p>File a draft Form A record</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Login as AP / RSE / RGE / AS of the supervision plan that has
Form A record drafted by TCP as in Acceptance ID 3.4.2.1</p></li>
<li><p>Navigate to that Form A template, and press into the Form A
record page</p></li>
<li><p>Tester should found the drafted Form A record and can view its
status, but not able to edit the inspection item state.</p></li>
</ol>
<blockquote>
<p><img src="media/image211.jpg"
style="width:3.9191in;height:6.46088in" /></p>
</blockquote>
<ol start="4" type="1">
<li><p>When AP / RSE / RGE / AS consider the result is ok, he can file
this Form A record by pressing “File”.</p></li>
<li><p>The record status will becomes “Filed”, “History” button will be
shown and allow to view it filing history</p></li>
</ol>
<blockquote>
<p><img src="media/image212.jpg"
style="width:3.53368in;height:3.66351in" /></p>
</blockquote>
<ol start="6" type="1">
<li><p>Repeat Acceptance ID 3.4.2.1 as TCP to change inspection item
status and “Save as Draft” again, which the status will become “Draft
after Filed”</p></li>
</ol>
<blockquote>
<p><img src="media/image213.jpg"
style="width:3.53368in;height:3.6785in" /></p>
</blockquote>
<ol start="7" type="1">
<li><p>Back to this page as a AP / RSE / RGE / AS, the “File” button
will be available again and can file the updated inspection items
status.</p></li>
</ol>
<blockquote>
<p><img src="media/image214.jpg"
style="width:3.38785in;height:3.51232in" /></p>
<p><img src="media/image215.jpg"
style="width:3.3566in;height:4.88748in" /></p>
</blockquote></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AP / RSE / RGE / AS can review Form A records drafted by
TCP and file the record, and TCP can draft again and let AP / RSE / RGE
/ AS to amend, i.e. file again.</td>
</tr>
</tbody>
</table>

## Form B

### Create Form B

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.1</td>
<td><blockquote>
<p>TCP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for creating new Form B</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP clicks the “Form B” button on the Supervision Plan Detail
page.</p></li>
<li><p>TCP clicks “Create Report” button</p></li>
<li><p>TCP inputs the date discovered and non-conformity
details</p></li>
<li><p>TCP clicks “Save as Draft” button</p></li>
</ol>
<p><img src="media/image216.jpg"
style="width:3.03368in;height:6.56174in" /> <img
src="media/image217.jpg" style="width:3.03368in;height:6.58531in" /></p>
<p><img src="media/image218.jpg"
style="width:2.9075in;height:6.29853in" /> <img src="media/image219.jpg"
style="width:2.90868in;height:6.30039in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP reach the page to create a new Form B
successfully</td>
</tr>
</tbody>
</table>

### Save Form B Part 1 as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.1</td>
<td><blockquote>
<p>TCP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for saving Form B Part 1 as draft</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP clicks the “Form B” button on the Supervision Plan Detail
page.</p></li>
<li><p>TCP searches for Form B by date discovered or / and Name of TCP
created Form B.</p></li>
<li><p>TCP edits the discover date and non-conformity details</p></li>
<li><p>TCP clicks “Save as Draft” button</p></li>
</ol>
<p><img src="media/image217.jpg"
style="width:3.03368in;height:6.58531in" /> <img
src="media/image220.jpg" style="width:3.03605in;height:6.5902in" /></p>
<p><img src="media/image221.jpg"
style="width:2.96568in;height:6.42022in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP fill Part 1 of Form B and save as draft successfully</p></li>
<li><p>User should be able to edit the details of the drafted Form B and
save the edited draft again</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Upload attachments when Form B Part 1 is Saved as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td>TCP</td>
<td></td>
<td>Successful case for uploading attachment when Form B Part 1 is saved
as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.2.1, TCP opens the same
Form B draft created before</p></li>
<li><p>TCP clicks the “+” button below “File Upload” section</p></li>
<li><p>TCP choose an image from the device, the application will mark
the file as pending for upload</p></li>
<li><p>TCP clicks “Save as draft” button or “Complete” button to submit
the file to the system</p></li>
</ol>
<p><img src="media/image222.jpg"
style="width:3.08519in;height:6.67022in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP can upload the PNG file to the Form B draft</p></li>
<li><p>TCP can view and download the file from this Form B after the
file is uploaded to the Form B draft by pressing the file icon or file
name</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Complete Form B Part 1

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.4.1</td>
<td>TCP</td>
<td></td>
<td>Successful case for completing Form B Part 1</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.2.1, TCP opens the same
Form B created before</p></li>
<li><p>TCP presses the “Complete” button on the Form B draft</p></li>
</ol>
<p><img src="media/image223.jpg"
style="width:3.0441in;height:6.60335in" /> <img src="media/image224.jpg"
style="width:3.05711in;height:6.61813in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP completes Form B part 1 successfully</p></li>
<li><p>The status of Form B part 1 changed from “Save as Draft” to
“Completed”</p></li>
<li><p>TCP can view the “Heads of Stream' response to Part 1” section
after complete the Form B part 1, but cannot edit and no button to
submit</p></li>
<li><p>TCP can still able to upload file</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Upload attachments when Form B Part 1 is Completed

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.5.1</td>
<td>AP, TCP</td>
<td></td>
<td>Successful case for uploading attachments when Form B part 1 is
completed</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.4.1, TCP opens the same
Form B created before</p></li>
<li><p>TCP presses the “+” button</p></li>
<li><p>TCP selects and attach a file</p></li>
<li><p>TCP presses the “Save” button</p></li>
</ol>
<p><img src="media/image225.jpg"
style="width:3.25122in;height:7.0348in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Both AP and TCP can view and download the new attached
file</td>
</tr>
</tbody>
</table>

### Save Response to Form B Part 1 as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.6.1</td>
<td>AP, TCP</td>
<td></td>
<td>Successful case for saving response to Form B part 1 as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AP opens the Form B part 1 completed by TCP in acceptance ID
3.1.4.1</p></li>
<li><p>In “Heads of Stream' response to Part 1” section, AP clicks the
“No” button</p></li>
<li><p>AP clicks the ‘Save as Draft” button</p></li>
</ol>
<p><img src="media/image226.jpg"
style="width:2.81493in;height:6.0875in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Both AP and TCP can view Head of Stream response in the Form
B</p></li>
<li><p>The status of “Heads of Stream' response to Part 1” changed to
“Saved as Draft”</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Complete Response to Form B Part 1

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.7.1</td>
<td>AP, TCP</td>
<td></td>
<td>Successful case for completing response to Form B Part 1</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.6.1, AP opens the same
Form B created before</p></li>
<li><p>AP clicks on the “Complete” button</p></li>
</ol>
<p><img src="media/image227.jpg"
style="width:2.75184in;height:5.95147in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Both AP and TCP can view Form B part 2 after AP completed the
response to part 1</p></li>
<li><p>The status of “Heads of Stream' response to Part 1” changed to
“Completed”</p></li>
<li><p>Part 2 of the Form B will be shown and available for
edit</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Report Imminent Danger to BD in Form B Part 1

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.8.1</td>
<td>AP, BD Officer</td>
<td></td>
<td>Successful case for reporting imminent danger to BD in Form B part
1</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.1.1, AP opens the same
Form B created before</p></li>
<li><p>AP clicks the “Yes” button in the field of “The non-conformity
shall pose an imminent danger” inside the “Heads of Stream' response to
Part 1” section</p></li>
<li><p>AP clicks the “Report imminent danger to BD” button</p></li>
</ol>
<p><img src="media/image228.jpg"
style="width:3.18221in;height:6.88897in" /> <img
src="media/image229.jpg"
style="width:3.15868in;height:6.83424in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AP can view the wording of “imminent danger has been reported to
BD” in “Heads of Stream' response to Part 1” section</p></li>
<li><p>The status in “Heads of Stream' response to Part 1” section
changed to “Reported to BD”</p></li>
<li><p>BD Officer receives email notification regarding the posed
imminent danger</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Save Form B Part 2 as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.9.1</td>
<td>TCP Representative, TCP</td>
<td></td>
<td>Successful case for saving Form B part 2 as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.7.1, TCP Rep opens the
same Form B created before</p></li>
<li><p>TCP Rep selects RC stream user in the drop down list of
“Instruction for rectification given to”</p></li>
<li><p>TCP Rep inputs the instruction detail of rectification in
“Details of Instruction” field</p></li>
<li><p>TCP Rep inputs the date for giving instruction to TCP
user</p></li>
<li><p>TCP Rep clicks “Save as Draft” button</p></li>
</ol>
<p><img src="media/image230.jpg"
style="width:3.22552in;height:6.98272in" /></p>
<p><img src="media/image55.png"
style="width:6.63542in;height:0.93056in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>TCP Rep receives email notification regarding part 2 draft has
been saved</p></li>
<li><p>Both TCP and TCP Rep can view the details of the part 2
draft</p></li>
<li><p>Status of Form B part 2 changed to “Saved as Draft”</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Report RC fail to comply and Material Concern to BD

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.10.1</td>
<td>BD Officer, AP</td>
<td></td>
<td>Successful case for reporting material concern to BD</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.9.1, AP opens the same
Form B created before</p></li>
<li><p>AP press the “Report material concern to BD” button</p></li>
</ol>
<p><img src="media/image231.jpg"
style="width:3.11004in;height:6.73272in" /></p>
<p><img src="media/image58.png"
style="width:6.63542in;height:1.20833in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Wording of “RC failure to compile rectification work has been
reported to BD” appears in Part 2</p></li>
<li><p>Both BD Officer and AP receives email notification</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Upload attachment when Form B Part 2 is Saved as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.11.1</td>
<td>TCP Rep</td>
<td></td>
<td>Successful case for uploading attachment when Form B Part 2 is Saved
as Draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.10.1, TCP Rep opens the
same Form B created before</p></li>
<li><p>TCP Rep selects today date in “Date of rectification works
certified completion” field</p></li>
<li><p>TCP Rep presses the “Upload” button</p></li>
<li><p>TCP Rep selects the PNG file that he desires to upload</p></li>
<li><p>TCP Rep presses the “Save as Draft” button</p></li>
</ol>
<p><img src="media/image232.jpg"
style="width:2.65868in;height:5.75211in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP Rep can view and download the uploaded PNG file in
Form B part 2</td>
</tr>
</tbody>
</table>

### Complete Form B Part 2

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.12.1</td>
<td>AP</td>
<td></td>
<td>Successful case for completing Form B Part 2</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.11.1, AP opens the same
Form B created before</p></li>
<li><p>AP presses “Complete” button in the Form B part 2</p></li>
</ol>
<p><img src="media/image233.jpg"
style="width:2.75496in;height:5.9582in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Status of Form B part 2 changed to “Completed”</p></li>
<li><p>All AP, TCP Rep and TCP can view the “Heads of Stream' response
to Part 2” section</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Save Response to Form B Part 2 as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.14.1</td>
<td>AP, TCP Rep, TCP</td>
<td></td>
<td>Successful case for saving response to Form B part 2 as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.11.1, AP opens the same
Form B created before</p></li>
<li><p>AP presses the “No” button in “The non-conformity shall pose an
imminent danger.” field in “Heads of Stream' response to Part 2”
section</p></li>
<li><p>AP presses the “Save as Draft” button</p></li>
</ol>
<p><img src="media/image233.jpg"
style="width:2.75496in;height:5.9582in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Status in “Heads of Stream' response to Part 2” section changed
to “Saved as Draft”</p></li>
<li><p>All AP, TCP Rep and TCP can view the saved response in the “Heads
of Stream' response to Part 2” section</p></li>
</ol></td>
</tr>
</tbody>
</table>

### Complete Response to Form B Part 2

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.15.1</td>
<td>AP</td>
<td></td>
<td>Successful case for completing response to Form B Part 2</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.14.1, AP opens the same
Form B created before</p></li>
<li><p>AP presses the “Complete” button</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Status of Form B part 2 changed to “Completed”</p></li>
<li><p>All AP, TCP Rep and TCP can view the “Heads of Stream' response
to Part 2” section</p></li>
</ol>
<p><img src="media/image234.jpg"
style="width:3.02343in;height:6.54522in" /></p></td>
</tr>
</tbody>
</table>

### Report Imminent Danger to BD in Form B Part 2

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.16.1</td>
<td>AP</td>
<td></td>
<td>Successful case for reporting imminent danger to BD in Form B part
2</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.14.1, AP opens the same
Form B created before</p></li>
<li><p>AP clicks the “Yes” button in “The non-conformity shall pose an
imminent danger” field</p></li>
<li><p>AP clicks the “Report imminent danger to BD” button</p></li>
</ol>
<p><img src="media/image235.jpg"
style="width:3.18853in;height:6.89228in" /> <img
src="media/image236.jpg"
style="width:3.20035in;height:6.92847in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Displays the user ID of the AP who report imminent danger to
BD</p></li>
<li><p>Displays grade and stream of the AP who report imminent danger to
BD</p></li>
<li><p>Display the status as “Reported to BD”</p></li>
<li><p>Display the date when AP reported the imminent danger to
BD</p></li>
<li><p>AP receives notification email from system</p></li>
</ol></td>
</tr>
</tbody>
</table>

## PNAP APP-158 Appendix B (Record of Quality Supervision)

### Create PNAP APP-158 template

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.1.1</td>
<td>AP</td>
<td></td>
<td>Successful case for creating PNAP APP-158 template</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AP presses “View” button on the site project in which he wants to
create App-158</p></li>
<li><p>AP presses “View” button on the supervision plan in which he
wants to create App-158</p></li>
<li><p>AP clicks the “APP-158” button</p></li>
<li><p>AP clicks “Create Template” button</p></li>
<li><p>AP selects “Superstructive Works - General Building Works” in
Type of Works field</p></li>
<li><p>AP selects “T1” in Responsible Grade of TCP field</p></li>
<li><p>AP selects a TCP name in Responsible TCP field</p></li>
</ol>
<p><img src="media/image237.jpg"
style="width:3.00883in;height:6.50355in" /></p>
<p><img src="media/image238.jpg"
style="width:3.27302in;height:7.07978in" /><img src="media/image239.jpg"
style="width:3.25243in;height:7.05925in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AP creates the PNAP APP-158 template successfully</td>
</tr>
</tbody>
</table>

### Create PNAP APP-158 Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.2.1</td>
<td>TCP</td>
<td></td>
<td>Successful case for creating PNAP APP-158 draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the PNAP APP-158 template created in acceptance ID
3.2.1.1, TCP clicks the “View” button on the APP-158 template AP created
before</p></li>
<li><p>TCP clicks the “Create New Records” button</p></li>
<li><p>TCP inputs the record date and then press “Next” button</p></li>
<li><p>TCP inputs value in QB1 to QB5 Location/Details and
Remedial/Remark fields and click “S” in Result field for each
item</p></li>
<li><p>TCP clicks the “Save as Draft” button</p></li>
</ol>
<p><img src="media/image240.jpg"
style="width:3.06493in;height:6.64068in" /> <img
src="media/image241.jpg" style="width:3.11701in;height:6.74448in" /><img
src="media/image242.jpg"
style="width:3.1774in;height:6.87855in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP created draft of PNAP APP-158 successfully</td>
</tr>
</tbody>
</table>

### File PNAP APP-158

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.3.1</td>
<td>AP</td>
<td></td>
<td>Successful case for filing PNAP APP-158</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the drafted app-158 created in acceptance ID 3.2.2.1,
AP opens the app-158 record drafted by TCP</p></li>
<li><p>AP presses the “File” button</p></li>
</ol>
<p><img src="media/image243.jpg"
style="width:2.43993in;height:5.28508in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AP created app-158 successfully and the status of
app-158 changed to “Filed”</td>
</tr>
</tbody>
</table>

### Upload PDF, PNG on PNAP APP-158

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.4.1</td>
<td>TCP, AP</td>
<td></td>
<td>Successful case for uploading PNG on drafted PNAP APP-158
record</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the drafted app-158 created in acceptance ID 3.2.2.1,
TCP opens the app-158 record drafted</p></li>
<li><p>TCP click button with clip icon on the corresponding
item</p></li>
<li><p>TCP click the plus button on the popup and select a file to
upload</p></li>
<li><p>TCP click “Save as Draft” button</p></li>
</ol>
<p><img src="media/image244.jpg"
style="width:2.13785in;height:4.6419in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP uploaded the file successfully. AP open the drafted
PNAP APP-158 record and view the uploaded file</td>
</tr>
</tbody>
</table>

### View PNAP APP-158 Result and History

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.5.1</td>
<td>AP, TCP</td>
<td></td>
<td>Successful case for viewing PNAP APP-158 Results and History</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the app-158 filed in acceptance ID 3.2.3.1, TCP opens
the app-158 record.</p></li>
<li><p>TCP views record results and status as Filed</p></li>
<li><p>TCP clicks “View History” button to open Version History
pop-up</p></li>
<li><p>TCP select version number from dropdown to view record result
history</p></li>
</ol>
<p><img src="media/image245.png"
style="width:2.6066in;height:5.64395in" /> <img src="media/image246.jpg"
style="width:2.594in;height:5.60772in" /></p>
<p><img src="media/image247.jpg"
style="width:3.2159in;height:6.96188in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">TCP viewed the filed record history successfully.</td>
</tr>
</tbody>
</table>

## Site-monitoring

### Create site-monitoring scheme

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.1</td>
<td><blockquote>
<p>AS</p>
</blockquote></td>
<td></td>
<td>Successful case for creating new site-monitoring scheme</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AS enters into any responsible site project</p></li>
<li><p>AS clicks “List of Site-monitoring Schemes” button</p></li>
<li><p>AS clicks “Create Scheme” button</p></li>
<li><p>AS inputs the scheme details such as name of scheme, type of
work, type of monitoring etc.</p></li>
<li><p>AS adds monitoring point to the scheme</p></li>
<li><p>AS clicks “Create” button</p></li>
</ol>
<p><img src="media/image248.jpg"
style="width:2.11701in;height:4.60505in" /><img src="media/image249.jpg"
style="width:2.13785in;height:4.61436in" /></p>
<p><img src="media/image250.jpg"
style="width:2.09618in;height:4.5671in" /><img src="media/image251.jpg"
style="width:2.09618in;height:4.55643in" /><img src="media/image252.jpg"
style="width:2.11701in;height:4.59573in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS creates new site monitoring scheme successfully</td>
</tr>
</tbody>
</table>

### Edit Site-monitoring scheme (3A level)

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.1</td>
<td><blockquote>
<p>AS</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for editing 3A level</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AS enters into any site project</p></li>
<li><p>AS clicks “List of Site-monitoring Schemes” button</p></li>
<li><p>AS clicks on the scheme that he wants to edit with</p></li>
<li><p>AS clicks “Edit Scheme” button</p></li>
<li><p>AS amends value of 3A level</p></li>
<li><p>AS clicks “Save” button</p></li>
</ol>
<p><img src="media/image253.jpg"
style="width:2.06679in;height:4.48927in" /><img src="media/image254.jpg"
style="width:2.06329in;height:4.47885in" /><img src="media/image255.jpg"
style="width:2.07535in;height:4.48328in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS edits 3A level values successfully</td>
</tr>
</tbody>
</table>

### Edit Site-monitoring scheme (adding monitoring points)

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td>AS</td>
<td></td>
<td>Successful case for adding monitoring point</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.2.1, AS clicks “Edit
Scheme” button</p></li>
<li><p>AS clicks the “Add Point” button to add new monitoring
points.</p></li>
<li><p>AS may click “Custom Start Date” and “Custom End Date” to set
tentative start and end date of the new monitoring point.</p></li>
<li><p>AS clicks the “Add” button on the popup to add the point</p></li>
<li><p>AS clicks the “Save” button to save the updated scheme</p></li>
</ol>
<p><img src="media/image256.jpg"
style="width:2.38785in;height:5.17944in" /><img src="media/image257.jpg"
style="width:2.38199in;height:5.1527in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS adds an new monitoring point successfully</td>
</tr>
</tbody>
</table>

### Edit Site-monitoring scheme (adding monitoring points)

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td>AS</td>
<td></td>
<td>Successful case for editing monitoring point</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol start="6" type="1">
<li><p>Following the steps in acceptance ID 3.1.2.1, AS clicks “Edit
Scheme” button</p></li>
<li><p>AS click “Custom Start Date” and “Custom End Date” to set
tentative start and end date of an existing monitoring point.</p></li>
<li><p>AS clicks the “Save” button</p></li>
</ol>
<p><img src="media/image256.jpg"
style="width:2.38785in;height:5.17944in" /><img src="media/image258.jpg"
style="width:2.36791in;height:5.13187in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">AS edits an monitoring point successfully</td>
</tr>
</tbody>
</table>

### Save measurement records as Draft

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.4.1</td>
<td>RC TCP</td>
<td></td>
<td>Successful case for TCP to save measurement records as draft</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.1.1, RC TCP opens the
Site-monitoring scheme.</p></li>
<li><p>RC TCP click “Create” button to navigate to the “Manual Input
Measurement Record” page.</p></li>
<li><p>RC TCP enter measurement records on each monitoring point and
click “Save”</p></li>
<li><p>RC TCP preview the measurement records and comparison with 3A
levels.</p></li>
<li><p>RC TCP click “Save” to save the measurement records as
draft.</p></li>
</ol>
<p><img src="media/image259.jpg"
style="width:2.753in;height:5.94844in" /><img src="media/image260.jpg"
style="width:2.7462in;height:5.93802in" /><img src="media/image261.jpg"
style="width:2.74836in;height:5.95478in" /><img src="media/image262.jpg"
style="width:2.77633in;height:5.99645in" /></p>
<p><img src="media/image263.jpg"
style="width:3.00899in;height:6.51397in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>RC TCP saves measurement records as draft successfully.</p></li>
<li><p>If the records exceed any 3A levels, the system notify RC
Representative accordingly.</p></li>
</ol>
<p><img src="media/image111.png"
style="width:6.63542in;height:1.30556in" /></p></td>
</tr>
</tbody>
</table>

### File/amend measurement records

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.7.1</td>
<td>AS, RC TCP</td>
<td></td>
<td>Successful case for file/amend measurement records</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.4.1 or 3.1.6.1, AS opens
the same site-monitoring scheme.</p></li>
<li><p>AS review the measurement records and the comparison with 3A
levels</p></li>
<li><p>AS click “File” button to file the measurement records.</p></li>
<li><p>If the records exceed 3A levels, a confirmation box pop up. As
click “Yes” button to confirm filing.</p></li>
</ol>
<p><img src="media/image264.jpg"
style="width:2.21986in;height:4.80563in" /><img src="media/image265.jpg"
style="width:2.21496in;height:4.78812in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>AS file the measurement records successfully.</p></li>
<li><p>A record history version is created successfully.</p></li>
<li><p>If the records exceed Alert levels, the system notifies AP
stream, RSE stream, RGE stream, AS stream and responsible BD Officers
accordingly.</p></li>
</ol>
<p><img src="media/image120.png"
style="width:6.63542in;height:1.375in" /></p></td>
</tr>
</tbody>
</table>

### View site-monitoring measurement record results

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.8.1</td>
<td>TCP Representative, Head of Stream</td>
<td></td>
<td>Successful case for viewing measurement record results</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.4.1 or 3.1.6.1, TCP,
Representative and Head of Stream of all streams can open the
site-monitoring scheme</p></li>
<li><p>User can view the measurement record result table and
chart.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>User view the measurement record result table and
chart successfully</p>
<p><img src="media/image266.jpg"
style="width:2.57588in;height:5.57647in" /></p></td>
</tr>
</tbody>
</table>

### Filter on Site-monitoring records view

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.9.1</td>
<td>TCP Representative, Head of Stream</td>
<td></td>
<td>Successful case for filtering measurement record results</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.9.1, user can filter the
site-monitoring scheme measurement record</p></li>
<li><p>User can filter the records by selecting measurement date
range.</p></li>
<li><p>User can also filter the records in chart by selecting the
monitoring points and 3A levels.</p></li>
</ol>
<p><img src="media/image267.jpg"
style="width:2.8069in;height:6.07647in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>User view filtered records successfully</p>
<p><img src="media/image268.jpg"
style="width:2.86945in;height:6.21188in" /></p></td>
</tr>
</tbody>
</table>

### View measurement record history

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.10.1</td>
<td>TCP Representative, Head of Stream</td>
<td></td>
<td>Successful case for viewing measurement record history</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Following the steps in acceptance ID 3.1.7.1, users open the
site-monitoring scheme.</p></li>
<li><p>User selects measurement date in table and views measurement
record history filed by AS.</p></li>
<li><p>User select the version number of measurement record to view
history records and file date</p></li>
</ol>
<p><img src="media/image269.jpg"
style="width:2.92719in;height:6.33688in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>User view measurement record history by versions
successfully.</p>
<p><img src="media/image270.jpg"
style="width:3.18993in;height:6.90677in" /></p></td>
</tr>
</tbody>
</table>

## BD Internal Login as BD Officer

### Login with Time-based One Time Password

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.1.1</td>
<td>BD Internal User</td>
<td></td>
<td>Successful case for BD Internal User to login with Time-based One
Time Password</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>BD Internal User (Officer or Admin) should first, by using
Departmental portal, login to CDPSS on web and setup local password and
Time-based One Time Password</p></li>
<li><p>BD Internal User login CDPSS app with BD email address and local
password</p></li>
<li><p>BD Internal User provide 6-digit Time-based One Time Password
generated from the choice of authenticator user choice (e.g. Google
Authenticator app)</p></li>
</ol>
<p><img src="media/image271.jpg"
style="width:2.40868in;height:5.20902in" /><img src="media/image272.jpg"
style="width:2.41236in;height:5.2152in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">BD Internal Users log in CDPSS successfully via
Departmental Portal.</td>
</tr>
</tbody>
</table>

## iAM Smart Integration

### Login via iAM Smart

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.1.1</td>
<td>Public user with iAM Smart account</td>
<td></td>
<td>Successful case for linkup and login via iAM Smart</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Public user enter CDPSS website login page</p></li>
<li><p>Public user click “Login with iAM Smart” button</p></li>
<li><p>Public user enters iAM Smart app, and after login, iAM Smart app
will ask for permission to login CDPSS.</p></li>
<li><p>If public user login CDPSS via iAM Smart for the 1st time, CDPSS
will ask for permission to get user info from iAM Smart, user will be
directed back to iAM Smart app, and upon agree, CDPSS will match user’s
HKID with existing account.</p></li>
<li><p>If account is found, CDPSS will show a popup to notice user that
the account binding is completed, where CDPSS will directly login user
next time when user login with iAM Smart. Otherwise the user will be
treated as new comer and bring up the registration form, with info
fromiAM Smart prefilled.</p></li>
<li><p>Public user login CDPSS successfully.</p></li>
</ol>
<p><img src="media/image273.png"
style="width:2.39826in;height:5.2313in" /><img src="media/image274.png"
style="width:2.40868in;height:5.23112in" /><img src="media/image275.png"
style="width:2.39962in;height:5.22875in" /><img src="media/image276.png"
style="width:2.39472in;height:5.22562in" /><img src="media/image277.png"
style="width:2.61154in;height:5.66312in" /><img src="media/image278.png"
style="width:2.61701in;height:5.65913in" /><img src="media/image279.png"
style="width:2.6066in;height:5.6959in" /><img src="media/image280.png"
style="width:2.62743in;height:5.69769in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Public user link up iAM Smart with CDPSS (if not
already) and login CDPSS successfully.</p>
<p>Note: Public user does not receive OTP when login via iAM
Smart</p></td>
</tr>
</tbody>
</table>

## Notification

### View Notification List

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.1.1</td>
<td><blockquote>
<p>All users</p>
</blockquote></td>
<td></td>
<td>Successful case for viewing the notification list</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>On home page, tester clicks the bell icon on the top
right corner, next to the logout button.</p>
<p><img src="media/image281.jpg"
style="width:2.50727in;height:5.42022in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester successfully views different kind of email
notification on the screen with relevant email subject and email sent
date.</p>
<p><img src="media/image282.jpg"
style="width:3.40837in;height:7.37855in" /></p></td>
</tr>
</tbody>
</table>

### View Notification Details

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.2.1</td>
<td><blockquote>
<p>All users</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for viewing the notification details</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester clicks a notification record</p>
<p><img src="media/image282.jpg"
style="width:2.88785in;height:6.25091in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can see the contents of email notification
including email subject, email sender, email receipients,</p>
<p><img src="media/image283.jpg"
style="width:3.08598in;height:6.68063in" /></p></td>
</tr>
</tbody>
</table>

###  

### Clickable Link in Notification

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.3.1</td>
<td><blockquote>
<p>All users</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for redirecting to another page by clicking on the
clink in notification</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester clicks on the link in the notification</p>
<p><img src="media/image284.jpg"
style="width:2.6691in;height:5.7735in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>System redirects the tester to relevant system
page.</p>
<p><img src="media/image285.jpg"
style="width:3.02343in;height:6.54522in" /></p></td>
</tr>
</tbody>
</table>

###  

### Manage and opt-out email notification

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 52%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.4.1</td>
<td><blockquote>
<p>Hos, Rep, AP</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>Successful case for opt-out the email notification</p>
</blockquote></td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester clicks on the user icon on top right corner of home page
(Picture 1).</p></li>
<li><p>Tester turns on the “Opt-Out Notifications” button and then press
“Submit” button.</p></li>
</ol>
<p><strong><u>Picture 1</u></strong></p>
<p><img src="media/image286.jpg"
style="width:2.36836in;height:5.12855in" /></p>
<p><strong><u>Picture 2</u></strong></p>
<p><img src="media/image287.jpg"
style="width:2.95035in;height:6.38603in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">Tester no longer receives email notification from their
registered email address but can still view the email notification
details from notification list.</td>
</tr>
</tbody>
</table>

###  

## Information Reports

### Report for List of Heads of Stream and their Responsible Sites

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.1.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for list of Heads of Stream
and their responsible sites</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Reports” menu item on the left
menu, open by tapping the top left menu icon.</p></li>
<li><p>Tester clicks the “Add” button at the bottom</p></li>
<li><p>Tester selects “List of Heads of Stream and their responsible
sites” as the report type.</p></li>
<li><p>Tester selects the BD Reference number(s) in “Related Site
Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol>
<p><img src="media/image288.jpg"
style="width:2.49343in;height:5.39938in" /><img src="media/image289.jpg"
style="width:2.49355in;height:5.4027in" /></p>
<p><img src="media/image290.jpg"
style="width:2.50164in;height:5.42022in" /><img src="media/image291.jpg"
style="width:2.4818in;height:5.37145in" /></p></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Given Name</p></li>
<li><p>English Last Name</p></li>
<li><p>Chinese Full Name (if any)</p></li>
<li><p>Email address</p></li>
<li><p>Responsible Site Reference</p></li>
<li><p>Responsible Site Project Stream</p></li>
<li><p>Registration Number</p></li>
<li><p>Number of responsible Supervision Plans</p></li>
<li><p>Number of Responsible Form A Template</p></li>
<li><p>Number of Responsible non-conformities (Form B)</p></li>
<li><p>Number of Responsible Form App-158 Template</p></li>
<li><p>Creation Date of Site</p></li>
<li><p>Tentative Commencement Date of Site</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of TCPs and assigned sites/supervision plans

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.2.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of TCPs and assigned
sites/supervision plans</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of TCPs and assigned sites/supervision
plans” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Given Name</p></li>
<li><p>English Last Name</p></li>
<li><p>Chinese Full Name</p></li>
<li><p>Email address</p></li>
<li><p>Assigned Site Reference</p></li>
<li><p>Assigned Supervision Plan Stream</p></li>
<li><p>Assigned Supervision Plan Type of building works and street
works</p></li>
<li><p>Assigned Supervision Plan Specific type of building works and
street works</p></li>
<li><p>Grade</p></li>
<li><p>Is Representative</p></li>
<li><p>Number of Responsible Form A Template</p></li>
<li><p>Number of Responsible non-conformities (Form B)</p></li>
<li><p>Number of Responsible Form App-158 Template</p></li>
<li><p>Number of Site-monitoring Scheme</p></li>
<li><p>Assignment Start Date</p></li>
<li><p>Assignment End Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of non-conformities (Form B)

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.3.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of non-conformities
(Form B)</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of non-conformities (Form B)” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Reference</p></li>
<li><p>Site Address</p></li>
<li><p>Site Lot Number</p></li>
<li><p>Stream</p></li>
<li><p>Part 1: Date Discovered</p></li>
<li><p>Part 1: Details of non-conformities</p></li>
<li><p>Part 1: Pose Imminent Danger</p></li>
<li><p>English Full Name of TCP Completing Part 1</p></li>
<li><p>Grade of TCP completing Part 1</p></li>
<li><p>Date of completing Part 1</p></li>
<li><p>English Full Name of Head of Stream responding Imminent danger
posed in Part 1</p></li>
<li><p>Date of Head of Stream responding Imminent danger posed in Part
1</p></li>
<li><p>Date of AP reporting Part 1 to BD</p></li>
<li><p>Part 2: English Full Name of TCP Instruction for rectification
given to</p></li>
<li><p>Part 2: Email address of TCP Instruction for rectification given
to</p></li>
<li><p>Part 2: Stream of RC TCP Instruction for rectification given
to</p></li>
<li><p>Part 2: Grade of TCP Instruction for rectification given
to</p></li>
<li><p>Part 2: Instruction issue date</p></li>
<li><p>Part 2: Details of Instructions</p></li>
<li><p>Part 2: Date of rectification works certified completion</p></li>
<li><p>Date of AP reporting RC fail to comply to BD (To be developed
later)</p></li>
<li><p>English Full Name of TCP completing Part 2</p></li>
<li><p>Grade of TCP completing Part 2</p></li>
<li><p>Date of completing Part 2</p></li>
<li><p>English Full Name of Head of Stream responding Imminent danger
posed in Part 2</p></li>
<li><p>Date of Head of Stream responding Imminent danger posed in Part
2</p></li>
<li><p>Date of AP reporting Part 2 to BD</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of inspection records of Form APP-158

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.1.4.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of inspection records
of Form APP-158</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of inspection records of Form APP-158” as
the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Reference</p></li>
<li><p>Site Address</p></li>
<li><p>Site Lot Number</p></li>
<li><p>Stream</p></li>
<li><p>Types of Work</p></li>
<li><p>Responsible TCP English Full Name</p></li>
<li><p>Responsible TCP Grade</p></li>
<li><p>Responsible TCP Email Address</p></li>
<li><p>Responsible Representative English Full Name</p></li>
<li><p>Responsible Representative Grade</p></li>
<li><p>Responsible Representative Email Address</p></li>
<li><p>Responsible Head of Stream English Full Name</p></li>
<li><p>Responsible Head of Stream Registration Number</p></li>
<li><p>Responsible Head of Stream Email Address</p></li>
<li><p>Record Date</p></li>
<li><p>First File Date</p></li>
<li><p>Last File Date</p></li>
<li><p>Inspection Total Number Item</p></li>
<li><p>Inspection Status for S</p></li>
<li><p>Inspection Status for NS</p></li>
<li><p>Inspection Status for NA</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of inspection records of Form A

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.5.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of inspection records
of Form A</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of inspection records of Form A” as the
report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Address</p></li>
<li><p>Site Lot Number</p></li>
<li><p>Stream</p></li>
<li><p>Types of Work</p></li>
<li><p>Responsible TCP English Full Name</p></li>
<li><p>Responsible TCP Grade</p></li>
<li><p>Responsible TCP Email Address</p></li>
<li><p>Responsible Representative English Full Name</p></li>
<li><p>Responsible Representative Grade</p></li>
<li><p>Responsible Representative Email Address</p></li>
<li><p>Responsible Head of Stream English Full Name</p></li>
<li><p>Responsible Head of Stream Registration Number</p></li>
<li><p>Responsible Head of Stream Email Address</p></li>
<li><p>Record Date</p></li>
<li><p>First File Date</p></li>
<li><p>Last File Date</p></li>
<li><p>Inspection Total Number Item</p></li>
<li><p>Inspection Status for S</p></li>
<li><p>Inspection Status for NS</p></li>
<li><p>Inspection Status for NA</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of Supervision Plans (SP)

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.6.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of Supervision Plans
(SP)</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of Supervision Plans (SP)” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Reference</p></li>
<li><p>Site Address</p></li>
<li><p>Site Lot Number</p></li>
<li><p>Site Responsible AP English Full Name</p></li>
<li><p>Site Responsible AP Registration Number</p></li>
<li><p>Site Responsible AP Email Address</p></li>
<li><p>Site Responsible RSE English Full Name</p></li>
<li><p>Site Responsible RSE Registration Number</p></li>
<li><p>Site Responsible RSE Email Address</p></li>
<li><p>Site Responsible RGE English Full Name</p></li>
<li><p>Site Responsible RGE Registration Number</p></li>
<li><p>Site Responsible RGE Email Address</p></li>
<li><p>Site Responsible AS English Full Name</p></li>
<li><p>Site Responsible AS Registration Number</p></li>
<li><p>Site Responsible AS Email Address</p></li>
<li><p>Total Number of Active AP TCP</p></li>
<li><p>Total Number of Active RSE TCP</p></li>
<li><p>Total Number of Active RGE TCP</p></li>
<li><p>Total Number of Active RC TCP</p></li>
<li><p>Type of building works and street works</p></li>
<li><p>Specific type of building works and street works</p></li>
<li><p>Total Number of Form A Templates</p></li>
<li><p>Total Number of Form A Records</p></li>
<li><p>Total Number of Form B</p></li>
<li><p>Total Number of Form App-158 Templates</p></li>
<li><p>Total Number of Form App-158 Records</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of Sites

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.2.7.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of Sites</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of Sites” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>Site Reference</p></li>
<li><p>Site Address</p></li>
<li><p>Lot Number</p></li>
<li><p>Responsible AP English Full Name</p></li>
<li><p>Responsible AP Registration Number</p></li>
<li><p>Responsible AP Email Address</p></li>
<li><p>Responsible RSE English Full Name</p></li>
<li><p>Responsible RSE Registration Number</p></li>
<li><p>Responsible RSE Email Address</p></li>
<li><p>Responsible RGE English Full Name</p></li>
<li><p>Responsible RGE Registration Number</p></li>
<li><p>Responsible RGE Email Address</p></li>
<li><p>Responsible AS English Full Name</p></li>
<li><p>Responsible AS Registration Number</p></li>
<li><p>Responsible AS Email Address</p></li>
<li><p>Total Number of Active AP TCP</p></li>
<li><p>Total Number of Active RSE TCP</p></li>
<li><p>Total Number of Active RGE TCP</p></li>
<li><p>Total Number of Active RC TCP</p></li>
<li><p>Tentative Commencement Date</p></li>
<li><p>Total Number of Supervision Plans</p></li>
<li><p>Total Number of Form A Templates</p></li>
<li><p>Total Number of Form A Records</p></li>
<li><p>Total Number of Form B</p></li>
<li><p>Total Number of Form App-158 Templates</p></li>
<li><p>Total Number of Form App-158 Records</p></li>
<li><p>Total Number of Site-Monitoring Schemes</p></li>
<li><p>Total Number of Site-Monitoring Records</p></li>
<li><p>Total Number of Site-Monitoring Alerts Notifications</p></li>
<li><p>Total Number of Site-Monitoring Alarm Notifications</p></li>
<li><p>Total Number of Site-Monitoring Action Notifications</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Activities Reports

### Report for Monitoring Point

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.1.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for Monitoring Point</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “Monitoring Point” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Role of user (AS/Rep/TCP)</p></li>
<li><p>Site Reference</p></li>
<li><p>Site-monitoring scheme name</p></li>
<li><p>Monitoring Point Changed (Hide and To Be Developed
later)</p></li>
<li><p>Monitoring Point Actual</p></li>
<li><p>Start Date</p></li>
<li><p>End Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for 3A level changes

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.2.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for 3A level changes</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “3A level changes” as the report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Role of user (AS/Rep/TCP)</p></li>
<li><p>Site Reference</p></li>
<li><p>Site-monitoring scheme name</p></li>
<li><p>Level changed (Alert/Alarm/Action)</p></li>
<li><p>Previous value</p></li>
<li><p>Updated value</p></li>
<li><p>Action Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of site-monitoring activities

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.3.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of site-monitoring
activities</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of site-monitoring activities” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Role of user (AS/Rep/TCP)</p></li>
<li><p>Site Reference</p></li>
<li><p>Site-monitoring scheme name</p></li>
<li><p>Action Description (Create Scheme/ Save as Draft / Import records
/ File)</p></li>
<li><p>Action Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of inspection item checklist changes

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.4.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of inspection item
checklist changes</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of inspection item checklist changes” as the
report type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Role of user (AP/RSE/RGE/AS/Rep/TCP)</p></li>
<li><p>Stream of user</p></li>
<li><p>Site Reference</p></li>
<li><p>Template Name</p></li>
<li><p>Inspection Form (Form A / Form App-158)</p></li>
<li><p>Changed Template Item Description</p></li>
<li><p>Action (Addition/removal)</p></li>
<li><p>Action Date</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Report for List of site activities

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 53%" />
<col style="width: 13%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.3.5.1</td>
<td>BD Officer</td>
<td></td>
<td>Successful case for generating report for List of site
activities</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>Tester (BD Officer) clicks the “Report” icon on system
homepage.</p></li>
<li><p>Tester clicks the “Generate New Report” button.</p></li>
<li><p>Tester selects “List of site activities” as the report
type.</p></li>
<li><p>Tester inputs and selects the BD Reference number(s) in “Related
Site Reference” field.</p></li>
<li><p>Tester selects the report period.</p></li>
<li><p>Tester clicks on “Create” button.</p></li>
<li><p>Tester clicks the “Download” button from the generated report in
the report list.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5"><p>Tester can find below column headers and relevant
records in the report</p>
<ul>
<li><p>English Full Name of user</p></li>
<li><p>Email address of user</p></li>
<li><p>Site Reference of recorded site</p></li>
<li><p>Action Date</p></li>
<li><p>Related Module (Site/Form A/Form B/Form
App-158/Site-monitoring)</p></li>
<li><p>Action Description (Create Template / Save as Draft / Import
records / File / Upload attachment)</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Unfiled Record Reminder

<u>Required number of filed records for different inspection frequency
are as below</u>

<img src="media/image153.png" style="width:3.0427in;height:3.61247in" />

1.  **Unfiled Record Reminder for Level 5 Frequency of Inspection**

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 52%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Acceptance ID</td>
<td>Tester</td>
<td>Test Date Time</td>
<td>Functionality</td>
<td>Success or Fail</td>
</tr>
<tr class="even">
<td>3.4.1.1</td>
<td>TCP, HOS</td>
<td></td>
<td>Successful case for Unfiled Record Reminder for Level 5 Frequency of
Inspection</td>
<td>Successful</td>
</tr>
<tr class="odd">
<td colspan="5">Test Data Input</td>
</tr>
<tr class="even">
<td colspan="5">N/A</td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Test Case</strong></td>
</tr>
<tr class="even">
<td colspan="5"><ol type="1">
<li><p>HOS creates a supervision plan with Level 5 inspection
frequency.</p></li>
<li><p>HOS set the working date of the supervision plan from Monday to
Friday.</p></li>
<li><p>HOS assigns a TCP into a Form A Template which has Actual Start
Date = 01 Aug under the supervision plan.</p></li>
<li><p>TCP creates a draft record in Form A on 3 Aug</p></li>
<li><p>HOS deliberately does not file the draft record of Form A created
by the TCP</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="5"><strong>Expected Result</strong></td>
</tr>
<tr class="even">
<td colspan="5">HOS will receive email notification for unfiled record
on 14 Aug</td>
</tr>
</tbody>
</table>

# 5.User Acceptance Test Results

![](media/image292.emf) ![](media/image293.emf) ![](media/image294.emf)

## Appendix 1 – User Acceptance Test Incident Report

![](media/image295.emf)
