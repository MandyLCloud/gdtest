# Acceptance Test Plan and Result: Licensing Self-Certification Portal & Common Digital Platform for Site Supervision

This document synthesizes information from multiple User Acceptance Test Plan (UATP) documents to provide a comprehensive overview of the testing process and results for the Buildings Department's Licensing Self-Certification Portal (LSCP) and the Common Digital Platform for Site Supervision (CDPSS).

## System Overview

The Licensing Self-Certification Portal (LSCP) and the Common Digital Platform for Site Supervision (CDPSS) are systems designed to streamline the application, processing, and management of certifications, notices, and related processes within the Buildings Department (BD).  The systems aim to improve efficiency, accessibility, and data management.

*   **LSCP:** Focuses on self-certification processes for Educational Premises (EP) and Child Care Centres (CCC).
*   **CDPSS:** Focuses on site supervision and monitoring activities.

## Objectives of the UAT

The primary objectives of the User Acceptance Testing (UAT) are to:

*   Verify the functionality of the delivered system within the specific context of the Buildings Department.
*   Confirm that all required functionalities have been implemented.
*   Ensure that the system operates according to the defined scope and requirements.

## Testing Environment

The UAT is conducted at the Buildings Department's premises, utilizing a dedicated UAT environment located in the WKGO office. The testing environment uses non-production hardware and software.

## Scope

The UAT encompasses a wide range of functionalities across both web and mobile platforms. Key areas of testing include:

*   **User Management:** Registration, login (including iAM Smart integration), password management, and user administration.
*   **Site Projects and Supervision Plan Management:** Creation, editing, viewing, and management of site projects and supervision plans.
*   **TCP Management:** Assignment, acceptance, unassignment, and temporary replacement of Technically Competent Persons (TCPs).
*   **Form Management:** Creation, filling, uploading, and viewing of various forms (Form A, Form B, PNAP APP-158 Appendix B).
*   **Reporting:** Generation and download of management statistics and reports.
*   **Site Monitoring:** Creation, editing, and filing of site-monitoring schemes and measurement records.
*   **iAM Smart Integration:** Verification of login and data retrieval via iAM Smart.
*   **Notifications:** Testing of email and SMS notifications.
*   **BD Internal User Management:** Management of BD internal user accounts and privileges.

## Functional Requirements and Test Cases

The following sections detail the functional requirements and test cases executed during the UAT.  Each test case includes an Acceptance ID, Tester role, Test Date/Time, Functionality being tested, and the Result (Success or Fail).

### User Management

#### Public User Registration

*   **Acceptance ID:** 3.1.1.1 (Web), 4.1.1.1 (Mobile)
*   **Tester:** TCP / AP/RSE/RGE/AS
*   **Functionality:** Successful registration of a new public user account.
*   **Test Case (Web):**
    1.  Click the "Register" button on the login page.
    2.  Input required information (User Family Name, Given Name, Chinese Name, Password, Confirm Password, HK Identity Card Number, Email address).
    3.  Select the appropriate qualification (e.g., Technically Competent Person (TCP)).
    4.  Click the activation link in the registration email.
    5.  Click "Login" and enter email and password.
*   **Test Case (Mobile):** Similar steps as Web, adapted for the mobile interface.
*   **Expected Result:** User successfully registered and logged in.
*   **Result:** Successful

#### Public Login

*   **Acceptance ID:** 3.1.2.1 (Web), 4.1.2.1 (Mobile)
*   **Tester:** TCP / AP/RSE/RGE/AS
*   **Functionality:** System generates a one-time password (OTP) for user login.
*   **Test Case:**
    1.  Navigate to the login page.
    2.  Enter registered email address and password.
    3.  Click the "Login" button.
*   **Expected Result:** User receives an OTP in their registered email address.
*   **Result:** Successful

*   **Acceptance ID:** 3.1.2.4 (Web), 4.1.2.4 (Mobile)
*   **Tester:** TCP / AP/RSE/RGE/AS
*   **Functionality:** User logs in using the generated OTP.
*   **Test Case:**
    1.  Enter the received OTP in the "One-Time Password" field.
    2.  Click the "Login" button.
*   **Expected Result:** User successfully logs into the system.
*   **Result:** Successful

*   **Acceptance ID:** 3.1.2.5 (Web)
*   **Tester:** TCP / AP/RSE/RGE/AS
*   **Functionality:** System allows users to reset their password.
*   **Test Case:**
    1.  Click the "Forget Password" link on the login page.
    2.  Enter the registered email address.
*   **Expected Result:** User receives an email with a reset password link.
*   **Result:** Successful

*   **Acceptance ID:** 3.1.2.6 (Web)
*   **Tester:** TCP / AP/RSE/RGE/AS
*   **Functionality:** System allows only one active user session.
*   **Test Case:**
    1.  Log in to the system on one device.
    2.  Attempt to log in again using the same credentials on a different device.
*   **Expected Result:** The initial device is redirected to the login screen, indicating session termination.
*   **Result:** Successful

#### User Management - Others

*   **Acceptance ID:** 3.1.3.1 (Web)
*   **Tester:** TCP
*   **Functionality:** User can successfully change their password.
*   **Test Case:**
    1.  Navigate to the account details page.
    2.  Enter the current password.
    3.  Enter a new password and confirm it.
    4.  Click "Submit."
*   **Expected Result:** System displays a success message, and the password is changed.
*   **Result:** Successful

*   **Acceptance ID:** 3.1.3.6 (Web)
*   **Tester:** TCP
*   **Functionality:** User can update personal information.
*   **Test Case:**
    1.  Navigate to the "Update Account Info" page.
    2.  Edit personal information (e.g., name, phone number).
    3.  Click "Submit."
*   **Expected Result:** User's personal information is updated successfully.
*   **Result:** Successful

## Site Projects and Supervision Plan Management

### Search Responsible Site Project

*   **Acceptance ID:** 3.2.2.1 (Web)
*   **Tester:** AP/RSE/RGE/AS
*   **Functionality:** Head of Stream can search for responsible site projects.
*   **Test Case:**
    1.  Input a BD reference number in the "Search by Site Project BD Reference" field.
*   **Expected Result:** The system lists site projects matching the BD reference and for which the user is responsible.
*   **Result:** Successful

### Create new Site Project

*   **Acceptance ID:** 3.2.3.1 (Web)
*   **Tester:** AP/RSE/RGE/AS
*   **Functionality:** Creating a new site project.
*   **Test Case:**
    1.  Click "Create Site Project."
    2.  Input a BD reference number.
    3.  Click "Create."
    4.  Input site address, lot number, and select a responsible stream.
    5.  Click "Submit."
*   **Expected Result:** A new site project is created successfully.
*   **Result:** Successful

### Edit and update Site Project Detail

*   **Acceptance ID:** 3.2.4.1 (Web)
*   **Tester:** AP/RSE/RGE/AS
*   **Functionality:** Editing and updating site project details.
*   **Test Case:**
    1.  Click "Edit" on a site project.
    2.  Modify site address, lot number, and tentative commencement date.
    3.  Click "Submit."
*   **Expected Result:** Site project information is updated successfully.
*   **Result:** Successful

### Supervision Plan Detail View

*   **Acceptance ID:** 3.2.6.1 (Web)
*   **Tester:** AP/RSE/RGE/AS
*   **Functionality:** Viewing supervision plan details.
*   **Test Case:**
    1.  Click "View" on a supervision plan from the "Site Project Detail" page.
*   **Expected Result:** The system displays the supervision plan details.
*   **Result:** Successful

### Supervision Plan Detail Management

*   **Acceptance ID:** 3.2.8.1 (Web)
*   **Tester:** AP/RSE/RGE/AS
*   **Functionality:** Editing supervision plan details.
*   **Test Case:**
    1.  Click "Edit" on a supervision plan.
    2.  Modify the type of building works, specific type of works, and grade of TCP.
    3.  Click "Submit."
*   **Expected Result:** Supervision plan details are updated successfully.
*   **Result:** Successful

## TCP management

### Assign TCPs

*   **Acceptance ID:** 3.3.1.1 (Web)
*   **Tester:** AP, RSE, RGE, and AS
*   **Functionality:** Searching TCP by Name.
*   **Test Case:**
    1.  Go to ?List of TCPs? page.
    2.  Input the Name of TCP in ?Search Name? field.
*   **Expected Result:** All the matched TCPs will be Shown
*   **Result:** Successful

*   **Acceptance ID:** 3.3.1.4 (Web)
*   **Tester:** AP, RSE, RGE, and AS
*   **Functionality:** Add TCP into project
*   **Test Case:**
    1.  Go to ?List of TCPs? page
    2.  Click ?Assign TCP? button
    3.  Input the username that you want to assign as TCP in ?Search by Name? field
    4.  Add ?Add? button
    5.  Select ?Grade of TCP?
    6.  Click ?I confirm the personal above is qualified for his/her grade of TCP as declared.?
    7.  The Page shown message shown the TCP adding request sent to TCP and awaiting TCP accept
    8.  Tester switch the role and use TCP account to login into system again
    9.  Tester accepts TCP invitation
*   **Expected Result:** HOS assign TCP successfully
*   **Result:** Successful

### Request TCP acceptance

*   **Acceptance ID:** 3.3.2.1 (Web)
*   **Tester:** TCP
*   **Functionality:** Accept ?Assign TCP? Request
*   **Test Case:**
    1.  After completing Acceptance ID 3.3.1.4, TCP receives an assignment request email generated from the system.
    2.  TCP clicks on the accept link to accept being TCP in the assignment request email.
*   **Expected Result:** The user should be redirected to the notification page, notifying him he has been assigned as TCP of the project
*   **Result:** Successful

*   **Acceptance ID:** 3.3.2.2 (Web)
*   **Tester:** TCP
*   **Functionality:** Reject ?Assign TCP? Request
*   **Test Case:**
    1.  After completing Acceptance ID 3.3.1.4, TCP receives an assignment request email generated from the system.
    2.  TCP clicks on the reject link to reject being TCP in the assignment request email.
*   **Expected Result:** The user should be redirected to the notification page, notifying him he has rejected to be TCP of the project
*   **Result:** Successful

### Unassign TCPs

*   **Acceptance ID:** 3.3.3.1 (Web)
*   **Tester:** TCP
*   **Functionality:** Unassign the assigned TCPs from project
*   **Test Case:**
    1.  Go to ?List of TCPs? page
    2.  Input ?Tai Man? in the first name field and ?Chan? in the last name field
    3.  Press ?Search? button
    4.  Click the row of ?Chan Tai Man? in the display result and then press ?Remove? button
*   **Expected Result:** TCP ?Chan Tai Man? should be unassigned as TCP role
*   **Result:** Successful

### Temporary replacement of TCP

*   **Acceptance ID:** 3.3.4.1 (Web)
*   **Tester:** AP, RSE, RGE and AS
*   **Functionality:** Temporary replacement of TCP
*   **Test Case:**
    1.  Go to ?List of TCPs? page
    2.  Input ?Siu Ming? in the first name field and ?Chan? in the last name field
    3.  Press ?Search? button
    4.  Click the row of ?Chan Siu Ming? in the display result and then press ?Temporary Replacement? button
    5.  Search ?Wong Hoi Yen? name and then press ?Replace? button
    6.  Set effective start date and end date of the replacement period
*   **Expected Result:** Wong Hoi Yen should receive invitation email for being temporary TCP
*   **Result:** Successful

*   **Acceptance ID:** 3.3.4.2 (Web)
*   **Tester:** AP, RSE, RGE and AS
*   **Functionality:** 
*   **Test Case:**
    1.  Continue from Acceptance ID 5.3.4.1, Wong Hoi Yen clicks the link for acceptance of being temporary TCP received from her email
*   **Expected Result:** Wong Hoi Yen becomes temporary TCP
*   **Result:** Successful

## Form A

### Create Form A template

Before proceeding with the test cases below, the new supervision plan should have at least one TCP being assigned.
This TCP assignment function is only available in web version.

*   **Acceptance ID:** 3.4.1.1 (Web)
*   **Tester:** AP/RSE/RGE/AS
*   **Functionality:** Create Form A template
*   **Test Case:**
    1.  Click ?Create Form A template? button
    2.  Select ?Chan Tai Man? in the ?Name? field
    3.  Input project start date and estimate project end date in the respective fields
    4.  Click on ?A1 to A6? checkboxes
    5.  Click ?Save? button
*   **Expected Result:** An new Form A template is created
*   **Result:** Successful

### Create Form A

*   **Acceptance ID:** 3.4.2.1 (Web)
*   **Tester:** TCP
*   **Functionality:** Create Form A
*   **Test Case:**
    1.  TCP chooses a Form A template they are responsible for.
    2.  TCP setup the frequency and the start date of the Form A.
*   **Expected Result:** An new Form A is created
*   **Result:** Successful

### File Form A

*   **Acceptance ID:** 3.4.3.1 (Web)
*   **Tester:** AP / RSE / RGE / AS
*   **Functionality:** File a draft Form A record
*   **Test Case:**
    1.  Login as AP / RSE / RGE / AS of the supervision plan that has Form A record drafted by TCP
    2.  Navigate to that Form A template, and press into the Form A record page
    3.  Tester should found the drafted Form A record and can view its status, but not able to edit the inspection item state.
    4.  When AP / RSE / RGE / AS consider the result is ok, he can file this Form A record by pressing ?File?.
    5.  The record status will becomes ?Filed?, ?History? button will be shown and allow to view it filing history
    6.  Repeat Acceptance ID 3.4.2.1 as TCP to change inspection item status and ?Save as Draft? again, which the status will become ?Draft after Filed?
    7.  Back to this page as a AP / RSE / RGE / AS, the ?File? button will be available again and can file the updated inspection items status.
*   **Expected Result:** AP / RSE / RGE / AS can review Form A records drafted by TCP and file the record, and TCP can draft again and let AP / RSE / RGE / AS to amend, i.e. file again.
*   **Result:** Successful

### Upload PDF, PNG on Form A and Quality Supervision Form (PNAP APP-158 Appendix B) ("Form APP-158?)

*   **Acceptance ID:** 3.4.4.1 (Web)
*   **Tester:** TCP, AP
*   **Functionality:** Upload PDF, PNG on Form A and Quality Supervision Form ("Form APP-158?)
*   **Test Case:**
    1.  TCP fills value in relevant Form APP-158 fields and select ?S? on the radio button
    2.  TCP clicks ?Upload Photo? button
    3.  TCP upload a photo (size limit - 5MB) and select ?QC3? in the drop down list
    4.  TCP clicks the ?Save as Draft? button
*   **Expected Result:** Upload PDF, PNG on Form A and Quality Supervision Form (PNAP APP-158 Appendix B) ("Form APP-158?) successfully
*   **Result:** Successful

### View Form A Result and History

*   **Acceptance ID:** 3.4.5.1 (Web)
*   **Tester:** TCP, AP
*   **Functionality:** View Form A Result and History
*   **Test Case:**
    1.  TCP goes to Form A dashboard page
    2.  TCP search the Form A by inputting the type of works and then press ?Search? button
    3.  TCP double clicks on the row of the result
*   **Expected Result:** TCP should be able to view the Form A result and history
*   **Result:** Successful

### Download, Import and Export Records

*   **Acceptance ID:** 3.4.6.1 (Web)
*   **Tester:** TCP
*   **Functionality:** Download Form A Site Inspection Import Template
*   **Test Case:** TCP press download ?Form A Template? button to download the Form A template
*   **Expected Result:** TCP is expected to view the Form A template in excel format with pre-defined contents
*   **Result:** Successful

*   **Acceptance ID:** 3.4.6.2 (Web)
*   **Tester:** TCP
*   **Functionality:** Import Form A Site Inspection Records by Excel
*   **Test Case:**
    1.  TCP fills the relevant fields in the imported Form A template
    2.  TCP uploaded the filled Form A to system
*   **Expected Result:** System records the details of the submitted Form A
*   **Result:** Successful

## Form B

### Create Form B

*   **Acceptance ID:** 3.1.1.1 (Mobile)
*   **Tester:** TCP
*   **Functionality:** Successful case for creating new Form B
*   **Test Case:**
    1.  TCP clicks the ?Form B? button on the Supervision Plan Detail page.
    2.  TCP clicks ?Create Report? button
    3.  TCP inputs the date discovered and non-conformity details
    4.  TCP clicks ?Save as Draft? button
*   **Expected Result:** TCP reach the page to create a new Form B successfully
*   **Result:** Successful

### Save Form B Part 1 as Draft

*   **Acceptance ID:** 3.1.2.1 (Mobile)
*   **Tester:** TCP
*   **Functionality:** Successful case for saving Form B Part 1 as draft
*   **Test Case:**
    1.  TCP clicks the ?Form B? button on the Supervision Plan Detail page.
    2.  TCP searches for Form B by date discovered or / and Name of TCP created Form B.
    3.  TCP edits the discover date and non-conformity details
    4.  TCP clicks ?Save as Draft? button
*   **Expected Result:**
    1.  TCP fill Part 1 of Form B and save as draft successfully
    2.  User should be able to edit the details of the drafted Form B and save the edited draft again
*   **Result:** Successful

### Upload attachments when Form B Part 1 is Saved as Draft

*   **Acceptance ID:** 3.1.3.1 (Mobile)
*   **Tester:** TCP
*   **Functionality:** Successful case for uploading attachment when Form B Part 1 is saved as draft
*   **Test Case:**
    1.  Following the steps in acceptance ID 3.1.2.1, TCP opens the same Form B draft created before
    2.  TCP clicks the ?+? button below ?File Upload? section
    3.  TCP choose an image from the device, the application will mark the file as pending for upload
    4.  TCP clicks ?Save as draft? button or ?Complete? button to submit the file to the system
*   **Expected Result:**
    1.  TCP can upload the PNG file to the Form B draft
    2.  TCP can view and download the file from this Form B after the file is uploaded to the Form B draft by pressing the file icon or file name
*   **Result:** Successful

### Complete Form B Part 1

*   **Acceptance ID:** 3.1.4.1 (Mobile)
*   **Tester:** TCP
*   **Functionality:** Successful case for completing Form B Part 1
*   **Test Case:**
    1.  Following the steps in acceptance ID 3.1.2.1, TCP opens the same Form B created before
    2.  TCP presses the ?Complete? button on the Form B draft
*   **Expected Result:**
    1.  TCP completes Form B part 1 successfully
    2.  The status of Form B part 1 changed from ?Save as Draft? to ?Completed?
    3.  TCP can view the ?Heads of Stream' response to Part 1? section after complete the Form B part 1, but cannot edit and no button to submit
    4.  TCP can still able to upload file
*   **Result:** Successful

### Upload attachments when Form B Part 1 is Completed

*   **Acceptance ID:** 3.1.5.1 (Mobile)
*   **Tester:** AP, TCP
*   **Functionality:** Successful case for uploading attachments when Form B part 1 is completed
*   **Test Case:**
    1.  Following the steps in acceptance ID 3.1.4.1, TCP opens the same Form B created before
    2.  TCP presses the ?+? button
    3.  TCP selects and attach a file
    4.  TCP presses the ?Save? button
*   **Expected Result:** Both AP and TCP can view and download the new attached file
*   **Result:** Successful

### Save Response to Form B Part 1 as Draft

*   **Acceptance ID:** 3.1.6.1 (Mobile)
*   **Tester:** AP, TCP Rep, TCP
*   **Functionality:** Successful case for saving response to Form B part 2 as draft
*   **Test Case:**
    1.  AP opens the Form B part 1 completed by TCP in acceptance ID 3.1.4.1
    2.  In ?Heads of Stream' response to Part 1? section, AP clicks the ?No? button
    3.  AP clicks the ?Save as Draft? button
*   **Expected Result:**
    1.  Status in ?Heads of Stream' response to Part 2? section changed to ?Saved as Draft?
    2.  All AP, TCP Rep and TCP can view the saved response in the ?Heads of Stream' response to Part 2? section
*   **Result:** Successful

### Complete Response to Form B Part 2

*   **Acceptance ID:** 3.1.7.1 (Mobile)
*   **Tester:** AP
*   **Functionality:** Successful case for completing response to Form B Part 2
*   **Test Case:**
    1.  Following the steps in acceptance ID 3.1.14.1, AP opens the same Form B created before
    2.  AP presses the ?Complete? button
*   **Expected Result:**
    1.  Status of Form B part 2 changed to ?Completed?
    2.  All AP, TCP Rep and TCP can view the ?Heads of Stream' response to Part 2? section
    3.  Part 2 of the Form B will be shown and available for edit
*   **Result:** Successful

### Report Imminent Danger to BD in Form B Part 2

*   **Acceptance ID:** 3.1.8.1 (Mobile)
*   **Tester:** AP, BD Officer
*   **Functionality:** Successful case for reporting imminent danger to BD in Form B part 2
*   **Test Case:**
    1.  Following the steps in acceptance ID 3.1.14.1, AP opens the same Form B created before
    2.  AP clicks the ?Yes? button in ?The non-conformity shall pose an imminent danger? field
    3.  AP clicks the ?Report imminent danger to BD? button
*   **Expected Result:**
    1.  Wording of ?RC failure to compile rectification work has been reported to BD? appears in Part 2
    2.  Both BD Officer and AP receives email notification
*   **Result:** Successful

## PNAP APP-158 Appendix B (Record of Quality Supervision)

### Create PNAP APP-158 template

*   **Acceptance ID:** 3.2.1.1 (Mobile)
*   **Tester:** AP
*   **Functionality:** Successful case for creating PNAP APP-158 template
*   **Test Case:**
    1.  AP presses ?View? button on the site project in which he wants to create App-158
    2.  AP presses ?View? button on the supervision plan in which he wants to create App-158
    3.  AP clicks the ?APP-158? button
    4.  AP clicks ?Create Template? button
    5.  AP selects ?Superstructive Works - General Building Works? in Type of Works field
    6.  AP selects ?T1? in Responsible Grade of TCP field
    7.  AP selects a TCP name in Responsible TCP field
*   **Expected Result:** AP creates the PNAP APP-158 template successfully
*   **Result:** Successful

### Create PNAP APP-158 Draft

*   **Acceptance ID:** 3.2.2.1 (Mobile)
*   **Tester:** TCP
*   **Functionality:** Successful case for creating PNAP APP-158 draft
*   **Test Case:**
    1.  Following the PNAP APP-158 template created in acceptance ID 3.2.1.1, TCP clicks the ?View? button on the APP-158 template AP created before
    2.  TCP clicks the ?Create New Records? button
    3.  TCP inputs the record date and then press ?Next? button
    4.  TCP inputs value in QB1 to QB5 Location/Details and Remedial/Remark fields and click ?S? in Result field for each item
    5.  TCP clicks the ?Save as Draft? button
*   **Expected Result:** AP created draft of PNAP APP-158 successfully
*   **Result:** Successful

### File PNAP APP-158

*   **Acceptance ID:** 3.2.3.1 (Mobile)
*   **Tester:** AP
*   **Functionality:** Successful case for filing PNAP APP-158
*   **Test Case:**
    1.  Following the drafted app-158 created in acceptance ID 3.2.2.1, AP opens the app-158 record drafted by TCP
    2.  AP presses the ?File? button
*   **Expected Result:** AP created app-158 successfully and the status of app-158 changed to ?Filed?
*   **Result:** Successful

### Upload PDF, PNG on PNAP APP-158

*   **Acceptance ID:** 3.2.4.1 (Mobile)
*   **Tester:** TCP, AP
*   **Functionality:** Successful case for uploading PNG on drafted PNAP APP-158 record
*   **Test Case:**
    1.  Following the drafted app-158 created in acceptance ID 3.2.2.1, TCP opens the app-158 record drafted
    2.  TCP click button with clip icon on the corresponding item
    3.  TCP click the plus button on the popup and select a file to upload
    4.  TCP click ?Save as Draft? button
*   **Expected Result:** TCP uploaded the file successfully. AP open the drafted PNAP APP-158 record and view the uploaded file
*   **Result:** Successful

## Site-monitoring

### Create site-monitoring scheme

*   **Acceptance ID:** 3.1.1.1 (Mobile)
*   **Tester:** AS
*   **Functionality:** Successful case for creating new site-monitoring scheme
*   **Test Case:**
    1.  AS enters into any responsible site project
    2.  AS clicks ?List of Site-monitoring Schemes? button
    3.  AS clicks ?Create Scheme? button
    4.  AS inputs the scheme details such as name of scheme, type of work, type of monitoring etc.
    5.  AS adds monitoring point to the scheme
    6.  AS clicks ?Create? button
*   **Expected Result:** AS creates new site monitoring scheme successfully
*   **Result:** Successful

### Edit Site-monitoring scheme (3A level)

*   **Acceptance ID:** 3.1.2.1 (Mobile)
*   **Tester:** AS
*   **Functionality:** Successful case for editing 3A level
*   **Test Case:**
    1.  AS enters into any site project
    2.  AS clicks ?List of Site-monitoring Schemes? button
    3.  AS clicks on the scheme that he wants to edit with
    4.  AS clicks ?Edit Scheme? button
    5.  AS amends value of 3A level
    6.  AS clicks ?Save? button
*   **Expected Result:** AS edits 3A level values successfully
*   **Result:** Successful

### Edit Site-monitoring scheme (adding monitoring points)

*   **Acceptance ID:** 3.1.3.1 (Mobile)
*   **Tester:** AS
*   **Functionality:** Successful case for adding monitoring point
*   **Test Case:**
    1.  Following the steps in acceptance ID 3.1.2.1, AS clicks ?Edit Scheme? button
    2.  AS clicks the ?Add Point? button to add new monitoring points.
    3.  AS may click ?Custom Start Date? and ?Custom End Date? to set tentative start and end date of the new monitoring point.
    4.  AS clicks the ?Add? button on the popup to add the point
    5.  AS clicks the ?Save? button to save the updated scheme
*   **Expected Result:** AS adds an new monitoring point successfully
*   **Result:** Successful

## BD Internal Login as BD Officer

### Login with Time-based One Time Password

*   **Acceptance ID:** 3.2.1.1 (Mobile)
*   **Tester:** BD Internal User
*   **Functionality:** Successful case for BD Internal User to login with Time-based One Time Password
*   **Test Case:**
    1.  BD Internal User (Officer or Admin) should first, by using Departmental portal, login to CDPSS on web and setup local password and Time-based One Time Password
    2.  BD Internal User login CDPSS app with BD email address and local password
    3.  BD Internal User provide 6-digit Time-based One Time Password generated from the choice of authenticator user choice (e.g. Google Authenticator app)
*   **Expected Result:** BD Internal Users log in CDPSS successfully via Departmental Portal.
*   **Result:** Successful

## iAM Smart Integration

### Login via iAM Smart

*   **Acceptance ID:** 3.3.1.1 (Mobile)
*   **Tester:** Public user with iAM Smart account
*   **Functionality:** Successful case for linkup and login via iAM Smart
*   **Test Case:**
    1.  Public user enter CDPSS website login page
    2.  Public user click ?Login with iAM Smart? button
    3.  Public user enters iAM Smart app, and after login, iAM Smart app will ask for permission to login CDPSS.
    4.  If public user login CDPSS via iAM Smart for the 1st time, CDPSS will ask for permission to get user info from iAM Smart, user will be directed back to iAM Smart app, and upon agree, CDPSS will match user?s HKID with existing account.
    5.  If account is found, CDPSS will show a popup to notice user that the account binding is completed, where CDPSS will directly login user next time when user login with iAM Smart. Otherwise the user will be treated as new comer and bring up the registration form, with info fromiAM Smart prefilled.
    6.  Public user login CDPSS successfully.
*   **Expected Result:** Public user link up iAM Smart with CDPSS (if not already) and login CDPSS successfully.  Note: Public user does not receive OTP when login via iAM Smart
*   **Result:** Successful

## Notification

### View Notification List

*   **Acceptance ID:** 3.1.1.1 (Mobile)
*   **Tester:** All users
*   **Functionality:** Successful case for viewing the notification list
*   **Test Case:** On home page, tester clicks the bell icon on the top right corner, next to the logout button.
*   **Expected Result:** Tester successfully views different kind of email notification on the screen with relevant email subject and email sent date.
*   **Result:** Successful

### View Notification Details

*   **Acceptance ID:** 3.1.2.1 (Mobile)
*   **Tester:** All users
*   **Functionality:** Successful case for viewing the notification details
*   **Test Case:** Tester clicks a notification record
*   **Expected Result:** Tester can see the contents of email notification including email subject, email sender, email receipients,
*   **Result:** Successful

### Clickable Link in Notification

*   **Acceptance ID:** 3.1.3.1 (Mobile)
*   **Tester:** All users
*   **Functionality:** Successful case for redirecting to another page by clicking on the clink in notification
*   **Test Case:** Tester clicks on the link in the notification
*   **Expected Result:** System redirects the tester to relevant system page.
*   **Result:** Successful

### Manage and opt-out email notification

*   **Acceptance ID:** 3.1.4.1 (Mobile)
*   **Tester:** Hos, Rep, AP
*   **Functionality:** Successful case for opt-out the email notification
*   **Test Case:**
    1.  Tester clicks on the username icon on top right corner of home page
    2.  Tester turns on the ?Opt-Out Notifications? button and then press ?Submit? button.
*   **Expected Result:** Tester no longer receives email notification from their registered email address but can still view the email notification details from notification list.
*   **Result:** Successful

## User Acceptance Test Results

The overall User Acceptance Test was [Pending].  Specific results for each test case are indicated in the "Success or Fail" column of the tables above.

## Appendix 1 ?