# Program Specification: Combined System Development Services for Rates Exemption Information System (REIS)

## Overview

This document combines information from multiple files to provide a comprehensive program specification for the Combined System Development Services of the Rates Exemption Information System (REIS) for the Home Affairs Department (HAD). It includes user requirements, program specifications, and technical details.

## 1. User Requirements

This section outlines the user requirements for the Self-Certification System (SCS).

### 1.1 Proposed System Overview

The SCS aims to efficiently manage applications for certificates and notices related to Educational Premises (EP) and Child Care Centers (CCC), and to provide building safety comments for Non-Local Higher and Professional Education (Regulation) Ordinance [NLHP(R)O] applications. The system will support both electronic and paper submissions.

### 1.2 Future Business Process

The following business processes will be supported:

1.  Application for e-Certificates and e-Notice for EP (e-application)
2.  Application for Alteration for EP/CCC (e-application)
3.  Application for Certificates and Notice for EP (paper application)
4.  Application for Alteration for EP/CCC (paper application)
5.  Random Audit Check
6.  Application for Approval for use of the premises for conducting course under the Non-Local-Higher and Professional Education (Regulation) Ordinance [NLHP(R)O] (e-application)
7.  Application for Approval for use of the premises for conducting course under the Non-Local-Higher and Professional Education (Regulation) Ordinance [NLHP(R)O] (paper application)
8.  Application for Periodic Inspection for CCC
9.  Application for inclusion of Temporary Structures in the Pre-accepted Temporary Structure (PTS) Register for user under TPPE license

### 1.3 Functional Requirements

The system must support the following functional requirements:

| Req. ID   | Requirement Name                                                 | Target Users                                  | Priority |
| :-------- | :--------------------------------------------------------------- | :-------------------------------------------- | :------- |
| REQ-GR-07 | Single Sign On                                                   | BD Users/EDB User/ SWD User                   | High     |
| REQ-GR-08 | Preview Document                                                 | All Users                                     | High     |
| REQ-GR-09 | Print Document                                                   | BD Users                                      | High     |
| REQ-GR-10 | Upload Document                                                  | BD Users/EDB User/SWD User/Applicant/AP/RSE   | High     |
| REQ-GR-11 | Management Statistics and Reports                                | BD Users                                      | High     |
| REQ-GR-12 | e-submission                                                     | Applicant/AP/RSE                              | High     |
| REQ-GR-13 | e-processing                                                     | BD Users/EDB User/SWD User                    | High     |
| REQ-GR-14 | e-tracking                                                       | All Users                                     | High     |
| REQ-GR-15 | Centralised data repository of the application supporting documents | BD Users/EDB User/SWD User/                   | High     |
| REQ-GR-16 | Search and Capture                                               | BD Users/EDB User/SWD User/                   | High     |
| REQ-GR-17 | Handle new applications                                          | BD Users/EDB User/SWD User/                   | High     |
| REQ-GR-18 | Handle alteration applications                                   | BD Users/EDB User/SWD User/                   | High     |
| REQ-GR-19 | Handle Self Certification Submissions                            | BD Users                                      | High     |
| REQ-GR-20 | Handle Periodic Inspection for CCC                               | BD Users                                      | High     |
| REQ-GR-21 | Handle PTS for TPPE                                              | BD Users                                      | High     |
| REQ-GR-22 | Data repository                                                  | BD Users                                      | High     |
| REQ-GR-23 | Easy retrieval of the records                                    | BD Users                                      | High     |
| REQ-GR-24 | User and Delegation Administration                               | User Administrators of BD Users/EDB User/SWD User | High     |
| REQ-GR-25 | Generate Application Number                                      | Applicant                                     | High     |
| REQ-GR-26 | Withdraw Application                                             | Applicant                                     | High     |
| REQ-WR-01 | Input Application Data                                           | Registry                                      | High     |
| REQ-WR-02 | Create Structural Information Report                             | TO                                            | High     |
| REQ-WR-03 | Provide Comment via SSE                                          | SE                                            | High     |
| REQ-WR-04 | Perform Site Inspection                                          | SO                                            | High     |
| REQ-WR-05 | Building Safety Requirements Check                               | BS                                            | High     |
| REQ-WR-06 | Generate Reply Letter, e-Certificates and e-Notice              | BS/SBS                                        | High     |
| REQ-WR-07 | Generate Letter of Requirement                                   | BS/SBS                                        | High     |
| REQ-WR-08 | Endorse Application                                              | SBS                                           | High     |
| REQ-WR-09 | Endorse Objection                                                | CBS                                           | High     |
| REQ-WR-10 | AP/RSE Verification                                              | Registry                                      | High     |
| REQ-WR-11 | Check Essential Documents                                        | SO/BS                                         | High     |
| REQ-WR-12 | Digital Signing of Document                                      | Applicant/AP/RSE/ BD Users                    | High     |
| REQ-WR-13 | Random Audit Check                                               | BD Users                                      | High     |
| REQ-WR-14 | Outstanding Application Alert                                    | SO/TO/BS/SE/SSE/SBS                           | High     |
| REQ-WR-15 | Input Application Form                                           | Applicant                                     | High     |
| REQ-WR-16 | Input memo data                                                  | EDB/SWD                                       | High     |
| REQ-WR-17 | Search Case Information                                          | BD Users                                      | High     |
| REQ-FRM-1  | Verify certificate against the copy from Hong Kong Post and DigiSign | System                                            | High     |
| REQ-FRM-2  | Route form to corresponding user                                     | System                                            | High     |
| REQ-FRM-3  | Encrypt restricted data in the form                                  | System                                            | High     |
| REQ-FRM-4  | Submit public form via online                                        | System                                            | High     |
| REQ-FRM-5  | Extract data from form                                               | System                                            | High     |
| REQ-FRM-6  | Store the extracted data in the database                             | System                                            | High     |
| REQ-FRM-7  | Search function for all record                                       | System                                            | High     |
| REQ-FRM-8  | Auto-reply to acknowledge receiving the form                         | System                                            | High     |
| REQ-FRM-9  | Maintenance function of the form                                     | System                                            | High     |
| REQ-FRM-10 | Resubmit the form data                                               | System                                            | High     |
| REQ-FRM-11 | Update of the disclaimer of the forms                                | System                                            | High     |
| REQ-FRM-12 | Handle eform and Hardcopy form                                       | System                                            | High     |
| REQ-PRO-1  | Verify CRM certification record                                      | BD Users/EDB User/SWD User                        | High     |
| REQ-PRO-2  | Reassign Case to other officer                                       | BD Users/EDB User/SWD User                        | High     |
| REQ-PRO-3  | Form status query                                                    | BD Users/EDB User/SWD User                        | High     |
| REQ-PRO-4  | Automatically Bring up Outstanding Cases                             | BD Users/EDB User/SWD User                        | High     |
| REQ-PRO-5  | To Do List                                                           | BD Users/EDB User/SWD User                        | High     |
| REQ-PRO-6  | Case History Summary                                                 | BD Users/EDB User/SWD User                        | High     |
| REQ-PRO-7  | Mark Notes and remark for internal use.                              | BD Users/EDB User/SWD User                        | High     |
| REQ-PRO-8  | Re-direct to BCIS for case checking                                  | BD Users                                          | High     |
| REQ-PRO-9  | Handle upload soft-copy                                              | BD Users/EDB User/SWD User                        | High     |
| REQ-PRO-10 | Export outstanding case                                              | BD Users/EDB User/SWD User                        | High     |
| REQ-PRO-11 | Handle referral Case                                                 | BD Users/EDB User/SWD User                        | High     |

### 1.4 Non-Functional Requirements

The system must adhere to the following non-functional requirements:

| Req. ID   | Requirement Name                         | Target Users | Priority |
| :-------- | :--------------------------------------- | :----------- | :------- |
| REQ-CR-01 | SMS Alert                                | All Users    | High     |
| REQ-CR-02 | Email Notification                       | All Users    | High     |
| REQ-CR-03 | Fax Copy of LoR, Certificates, and Notice | All Users    | High     |
| REQ-UR-01 | Common Look & Feel                       | All Users    | High     |
| REQ-UR-02 | W3C WCAG 2.1                              | All Users    | High     |
| REQ-UR-03 | Privacy Disclaimer                       | All Users    | High     |
| REQ-UR-04 | Assistive Technology Testing             | All Users    | High     |
| REQ-SR-01 | SRAA                                     | System Admin | High     |
| REQ-SR-02 | PIA and PCA                              | System Admin | High     |
| REQ-SR-03 | Encryption and Decryption of Classified Data | System Admin | High     |
| REQ-SR-04 | System Audit                             | System Admin | High     |
| REQ-SR-05 | System Control                           | System Admin | High     |
| REQ-IR-01 | Interface with BCIS                      | System Admin | High     |
| REQ-IR-02 | Interface with BD Website                | System Admin | High     |
| REQ-IR-03 | Interface with Minor Works               | System Admin | High     |
| REQ-IR-04 | Interface with ESH                       | System Admin | High     |
| REQ-IR-05 | Interface with ERKS                      | System Admin | High     |
| REQ-IR-06 | Interface with BRAVO                     | System Admin | High     |

### 1.5 Technical Requirements

The system must meet the following technical requirements:

| Req. ID   | Requirement Name                                       | Target Users | Priority |
| :-------- | :----------------------------------------------------- | :----------- | :------- |
| REQ-TR-01 | 24x7 Internet and Intranet                             | System Admin | High     |
| REQ-TR-02 | Integrated Cloud GCIS and On Premises                  | System Admin | High     |
| REQ-TR-03 | Input Validation                                       | System Admin | High     |
| REQ-TR-04 | Record Relocation from GCIS to On Premises            | System Admin | High     |
| REQ-TR-05 | High Availability                                      | System Admin | High     |
| REQ-TR-06 | Monitoring and Alert Generation                        | System Admin | High     |
| REQ-TR-07 | DR Drill                                               | System Admin | High     |
| REQ-TR-08 | UTF-8, Unicode or HKSCS                                | System Admin | High     |
| REQ-TR-09 | System Logging                                         | System Admin | High     |
| REQ-TR-10 | High Configurable                                      | System Admin | High     |
| REQ-TR-11 | Backup and Recovery                                    | System Admin | High     |
| REQ-TR-12 | Operation System and Browser Compatibility             | System Admin | High     |
| REQ-TR-13 | Review and Update Privilege                            | System Admin | High     |
| REQ-TR-14 | Health Check                                           | System Admin | High     |
| REQ-TR-15 | Encryption on All Communications                       | System Admin | High     |
| REQ-TR-17 | Monthly Usage Statistics and Ad-hoc Statistics         | System Admin | High     |
| REQ-TR-19 | Language support (EN/TC/SC)                            | System Admin | High     |
| REQ-TR-20 | System Performance                                     | System Admin | High     |
| REQ-TR-21 | Reports and statistics for monitor system performance   | System Admin | High     |
| REQ-TR-22 | Ad-hoc and periodic updates on the contents            | System Admin | High     |
| REQ-TR-23 | Provide refined Login & Authentication/ FULL Audit features | System Admin | High     |
| REQ-TR-24 | Login user account login by user ID & password          | BD/SWD/EBD/MC | High     |
| REQ-TR-25 | Version control of source code                          | System Admin | High     |
| REQ-TR-26 | System log tracking                                    | System Admin | High     |
| REQ-TR-27 | Scalable system frame design                            | System Admin | High     |
| REQ-TR-28 | Data exchange with other system securely               | System Admin | High     |
| REQ-TR-29 | Security measurement                                   | System Admin | High     |
| REQ-TR-30 | Help check email notification                          | System Admin | High     |
| REQ-TR-31 | Email notification for all batch jobs                  | System Admin | High     |
| REQ-TR-32 | Conform to the Interoperability Framework              | System Admin | High     |
| REQ-TR-33 | Manage System Parameters                               | System Admin | High     |
| REQ-TR-34 | Allow System Access by EBD and SWD                     | System Admin | High     |
| REQ-TR-35 | Independent System (Not depended on other BD systems) | System Admin | High     |
| REQ-TR-36 | Logout automatically for inactive for 30 minutes       | System Admin | High     |
| REQ-TR-37 | Centralized log Management                             | System Admin | High     |
| REQ-TR-38 | Handle around 300 user accounts of EDB and SWD for single sign on | System Admin | High     |
| REQ-TR-39 | Paper Less                                             | System Admin | High     |
| REQ-TR-40 | PDF template and mapping field for letter generation | System Admin | High     |

## 2. Constraints List

This section identifies potential constraints and their impact on the system.

### 2.1 Complexity of Address Identification

The system may not be able to create cases due to the complexity of address identification. In this scenario, case creation will be passed to BCIS.

### 2.2 Signature of AP/RSE

For paper applications, the system will verify AP/RSE information against MWMS 2.0, but handwriting signatures will require manual verification by the Registry.

## 3. Program Specifications

### 3.1 Program List

#### User Account Management

| Program ID | Program Name        |
| :--------- | :------------------ |
| ACS-001    | User Login          |
| ACS-002    | User Logout         |
| ACS-003    | Display System menu |
| ACS-004    | User Account Listing|
| ACS-005    | Create New User Account|
| ACS-006    | Update User Account|
| ACS-007    | Update User Role|
| ACS-008    | Access rights checking|
| ACS-009    | Change Password|

#### Processing Rates Exemption Application

| Program ID | Program Name                                                                       |
| :--------- | :--------------------------------------------------------------------------------- |
| RXA-001    | Display Summary List                                                               |
| RXA-002    | Notification of urgent case                                                        |
| RXA-003    | Open of Rates Exemption Application Record                                         |
| RXA-004    | Create New Rates Exemption Application Record                                      |
| RXA-005    | Check duplicate case                                                               |
| RXA-006    | Input Rates Exemption Application ? A - Applicant                                  |
| RXA-007    | Input Rates Exemption Application: B - Village House                               |
| RXA-008    | Input Rates Exemption Application: C - Application File                            |
| RXA-009    | Input Rates Exemption Application: C - Application File, Upload New File           |
| RXA-010    | Input Rates Exemption Application: C - Application File, Open / Delete File        |
| RXA-011    | Input Rates Exemption Application: D - Application Submission                      |
| RXA-012    | Update Rates Exemption Application: E - Application Update                         |
| RXA-013    | Update Rates Exemption Application: F - Generate Case Summary                      |
| RXA-014    | Update Rates Exemption Application: F - Display Case Summary                       |
| RXA-015    | Update Rates Exemption Application: G - Application Status                         |
| RXA-016    | Update Rates Exemption Application: G - Application Status, Generate New Memo / Letter |
| RXA-017    | Update Rates Exemption Application: G - Application Status, Input Response         |
| RXA-018    | Update Rates Exemption Application: Save and Submit                                |
| RXA-019    | Amend Rates Exemption Application                                                  |
| RXA-020    | Display Endorsement Summary List                                                   |
| RXA-021    | Generate Endorsement Summary                                                       |
| RXA-022    | Endorsement                                                                        |
| RXA-023    | Enquiry of Endorsed Records                                                        |
| RXA-024    | Revoke Endorsement                                                                 |
| RXA-025    | Display File Minute                                                                |
| RXA-026    | Generate File Minute                                                               |
| RXA-027    | Record Approval                                                                    |
| RXA-028    | Enquiry of Confirmed Approval Records                                              |
| RXA-029    | Revoke Approval                                                                    |
| RXA-030    | Batch Letters Generation                                                           |
| RXA-031    | Checking of outstanding case                                                       |

#### Review and Cancellation of Approved Rates Exemption Cases

| Program ID | Program Name                                                                    |
| :--------- | :------------------------------------------------------------------------------ |
| REV-001    | Display Matching List                                                           |
| REV-002    | Generate New Matching List                                                      |
| REV-003    | Download Matching List                                                          |
| REV-004    | Enquiry Random Check Case                                                       |
| REV-005    | Generate New Random Check Cases                                                 |
| REV-006    | Print Random Check Cases                                                        |
| REV-007    | New Review of Approved Rates Exemption: Search Currently Approved Rates Exemption |
| REV-008    | Input Review Record: H - Review of Granted Rates Exemption                      |
| REV-009    | Input Review Record: I - Review Status                                          |
| REV-010    | Input Review Record: I - Input Response                                         |
| REV-011    | Input Review Record: I - Generate New Memo / letter                             |
| REV-012    | Input Review Record: I - Input Random Check Results                             |
| REV-013    | Input Review Record: I - Input Matching Check Results                           |
| REV-014    | Input Review Record: I - Memo from Other Depts / Confirmation letter from applicant |
| REV-015    | Input Review Record: J - Historical Rates Exemption Applications and Granted Cases |
| REV-016    | Input Review Record: Save and Submission                                        |

#### Record Enquiry and Report Generation

| Program ID | Program Name               |
| :--------- | :------------------------- |
| ENQ-001    | Rates Exemption Record Enquiry |
| ENQ-002    | Audit Log Enquiry              |
| ENQ-003    | Ad-hoc Report                  |

#### System Administration

| Program ID | Program Name   |
| :--------- | :------------- |
| GEN-001    | System Parameter |
| GEN-002    | Type of Breach |
| GEN-003    | District       |

#### Common Module

| Program ID | Program Name        |
| :--------- | :------------------ |
| COM-001    | Insertion new audit log |

#### Report

| Program ID | Program Name                                              |
| :--------- | :-------------------------------------------------------- |
| RPT-001    | RF0001- Application Listing                               |
| RPT-002    | RF0002-Outstanding Case Report                            |
| RPT-003    | RF0003-Approved cases/ Rejected cases/ Cancelled cases Report |
| RPT-004    | RF0004-Monthly Report                                     |
| RPT-005    | RF0005-Statistical Report                                 |
| RPT-006    | RF0006-Exception Report                                   |
| RPT-007    | RF0007-Performance Pledge Report                          |

### 3.2 Program Specifications

#### ACS-001 ? User Login

| Program ID:   | ACS-001                                                                                                                                              |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| Mode:         | Online                                                                                                                                               |
| Program Name: | User Login                                                                                                                                           |
| Description:  | This program is developed to allow user to input user login information. User authentication is performed based on user login information collected. |

> Program Environment:

| **Program Source**   | **Location**       | **Language / Compiler** |
| :----------------- | :----------------- | :---------------------- |
| login.aspx           | reis\\             | ASP.NET Web Form        |
| login.aspx.vb        | reis\\             | Code Behind VB.NET File |
| UserAccess.vb        | reis\class\ASC\\   | VB.NET Class            |
| RoleDAO.vb           | reis\class\model\\ | DAO VB.NET Class        |
| RolePermissionDAO.vb | reis\class\model\\ | DAO VB.NET Class        |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description** |
| :-------------- | :------------ | :-------------------------------- | :------------------ | :------------ | :-------------- |
| loginID       | X             | 20                                | \[Alphanumeric]    | Y             | Login ID        |
| password      | X             | 20                                | \[Alphanumeric]    | Y             | Password        |

> Processing Logic:

*   When login button is clicked:
    *   `UserAccess.login()` is called with userID and password as parameters.
    *   Retrieve user record from `REIS_USER`, if user record does not exist or user?s status inactive, error of user account does not exist is return.
    *   Encrypt password. password is validated if encrypted passwords are matched.
    *   Validate the login ID and password
    *   If the password is expired, error of invalid password is return.
    *   If user password is reset, action ?Change Expired Password? is triggered.
    *   If validation success, assign the user role and user access rights (refer to ACS-007) of the user to session.
    *   Check user notification of urgent case (refer to RXA-002).
    *   The web page of main page is displayed.
    *   If validation is fail, update `REIS_USER.ur_login_fail_count = ur_login_fail_count + 1`.
    *   Read system parameter for maximum login attempt allowed, if `ur_login_fail_count > parameter`, update `ur_rec_status` to inactive.

#### ACS-002 ? User Logout

| Program ID:   | ACS-002                                                                   |
| :-------------- | :------------------------------------------------------------------------ |
| Mode:         | Online                                                                    |
| Program Name: | User Logout                                                               |
| Description:  | This program is developed to allow current login user to exit the system. |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
| :----------------- | :--------------- | :---------------------- |
| UserAccess.vb      | reis\class\ASC\\ | VB.NET Class            |

> Processing Logic:

*   When Logout is clicked:
    *   `UserAccess.logout()` is called to invalidate user current session.
    *   Redirect to login page.

#### ACS-003 ? Display System Menu

| Program ID:   | ACS-003                                                            |
| :-------------- | :----------------------------------------------------------------- |
| Mode:         | Online                                                             |
| Program Name: | Display System menu                                                |
| Description:  | This program is developed to show system menu after user is login. |

> Program Environment:

| **Program Source** | **Location** | **Language / Compiler** |
| :----------------- | :----------- | :---------------------- |
| menu.ascx          | reis\\       | Web User Control        |
| navigation.ascx    | reis\\       | Web User Control        |
| header.ascx        | reis\\       | Web User Control        |
| footer.ascx        | reis\\       | Web User Control        |

> Processing Logic:

*   <u>Display of System menu:</u>
    *   When user is not log in, system menu will not be displayed.
    *   When user is logged in, system menu will be also displayed (menu.ascx):
        *   Based on user access permission stored in the current session, only permitted function will be displayed (refer to ACS-008 for access rights checking).
*   <u>Display of Page Navigation (navigation.ascx):</u>
    *   Current web page address is retrieved from HTTP request header.
    *   Based on current web page address, navigation links are created and displayed.

#### ACS-004 ? User Account Listing

| Program ID:   | ACS-004                                                 |
| :-------------- | :------------------------------------------------------ |
| Mode:         | Online                                                  |
| Program Name: | User Account Listing                                    |
| Description:  | This program is developed to show list of user account. |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
| :----------------- | :----------------- | :---------------------- |
| userlist.aspx      | reis\\             | ASP.NET Web Form        |
| userlist.aspx.vb   | reis\\             | Code Behind VB.NET File |
| UserAccessMaint.vb | reis\class\ASC\\   | VB.NET Class            |
| UserDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**                                                                                 |
| :-------------- | :------------ | :-------------------------------- | :------------------ | :------------ | :---------------------------------------------------------------------------------------------- |
| userID        | N/A           | N/A                               | N/A                 | N/A           | User ID of selected record stored in the hidden form field used for record update and deletion. |

> Processing Logic:

*   <u>Display of User Account Listing:</u>
    *   Retrieve user accounts and their user role name from `REIS_USER` and `REIS_ROLE`.
    *   Displays list of user ordered by `UR_USERID`.
*   <u>When Add User is clicked:</u>
    *   Redirect to create new user account (refer to ACS-005).
*   <u>When Update of user account is clicked:</u>
    *   Redirect to update user account (refer to ACS-006) with userID as parameter.
*   <u>When Delete of user account is clicked:</u>
    *   `UserAccessMaint.deleteUser()` is called with userID as parameter.
    *   `UserDAO.inactivated()` is called:
        *   Update `UR_REC_STATUS = I`;
    *   Redirect to User Account Listing, the user account records are reloaded for displaying updated listing.

#### ACS-005 ? Create New User Account

| Program ID:   | ACS-005                                              |
| :-------------- | :--------------------------------------------------- |
| Mode:         | Online                                               |
| Program Name: | Create New User Account                              |
| Description:  | This program is developed to create new user account |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
| :----------------- | :----------------- | :---------------------- |
| usermaint.aspx     | reis\\             | ASP.NET Web Form        |
| usermaint.aspx.vb  | reis\\             | Code Behind VB.NET File |
| UserAccessMaint.vb | reis\class\ASC\\   | VB.NET Class            |
| UserDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |
| RoleDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |

> Input Parameters:

| **Parameter**   | **Data Type**           | **Maximum Length of input field** | **Validation Rule**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           