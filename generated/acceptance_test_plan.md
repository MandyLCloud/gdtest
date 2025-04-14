# User Acceptance Test Plan
# For Self-Certification System (SCS)

## Table of Contents
1. [Introduction](#1-introduction)
2. [Testing Environment](#2-testing-environment)
3. [Test Cases for Web Interface](#3-test-cases-for-web-interface)
4. [Test Cases for Mobile Interface](#4-test-cases-for-mobile-interface)
5. [Test Results](#5-test-results)

## 1. Introduction

### 1.1 Objectives of UAT
- Verify delivered functionality works in BD's specific domain
- Confirm all required functionality has been delivered
- Validate functionality works according to specified requirements
- Ensure integration with other systems works as specified

### 1.2 Schedule

| Items | Planned | Actual |
|---|---|---|
| Test Plan | 2025-02-01 | 2025-02-01 |
| Round 1 | 2025-02-08 |  |
| Round 1 Fix | 2025-02-15 |  |
| Round 2 | 2025-02-22 |  |
| Round 2 Fix | 2025-03-01 |  |
| Round 3 | 2025-03-08 |  |
| Round 3 Fix | 2025-03-15 |  |
| Round 4 | 2025-03-22 |  |
| Round 4 Fix | 2025-03-29 |  |
| Round 5 | 2025-04-05 |  |
| Round 5 Fix | 2025-04-12 |  |
| UAT Acceptance | 2025-04-19 |  |

## 2. Testing Environment

### 2.1 Testing Location
The User Acceptance Test will be performed at BD's premises under the UAT environment located in BD office at WKGO.

### 2.2 Hardware and Software Requirements
Hardware and software of non-production environments should be used for UAT:

- Browsers supported:
  - Microsoft Edge (Windows 10/11)
  - Safari (MacOS, iOS)
  - Mozilla Firefox (All platforms)
  - Google Chrome (All platforms)
- Mobile devices:
  - iOS devices
  - Android devices
- Network access to:
  - GCIS
  - BD internal systems
  - Internet (for public access testing)

## 3. Test Cases for Web Interface

### 3.1 User Management and Authentication

#### 3.1.1 User Login

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.1.1.1 | John Doe | 2025-02-08 09:00 | Successful login with valid credentials |  |

*   **Test Data Input:**
    *   Username: `ccywong.bd`
    *   Password:  `<valid password>`
*   **Test Case:**
    1.  Navigate to the LSCP login page.
    2.  Enter a valid username and password.
    3.  Click the "Login" button.
*   **Expected Result:**
    *   User is successfully logged in and redirected to the dashboard.

#### 3.1.2 User Login - Invalid Username

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.1.2.1 | John Doe | 2025-02-08 09:15 | Unsuccessful login with invalid username |  |

*   **Test Data Input:**
    *   Username: `<invalid username>`
    *   Password: `<any password>`
*   **Test Case:**
    1.  Navigate to the LSCP login page.
    2.  Enter an invalid username and password.
    3.  Click the "Login" button.
*   **Expected Result:**
    *   The system displays an error message indicating invalid credentials.

#### 3.1.3 User Login - Invalid Password

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.1.3.1 | John Doe | 2025-02-08 09:30 | Unsuccessful login with invalid password |  |

*   **Test Data Input:**
    *   Username: `<valid username>`
    *   Password: `<invalid password>`
*   **Test Case:**
    1.  Navigate to the LSCP login page.
    2.  Enter a valid username and an invalid password.
    3.  Click the "Login" button.
*   **Expected Result:**
    *   The system displays an error message indicating invalid credentials.

#### 3.1.4 Single Sign On Integration (REQ-GR-07)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.1.4.1 | John Doe | 2025-02-08 10:00 | Login through BD OSDP |  |
| 3.1.4.2 | Jane Smith | 2025-02-08 10:15 | Login through EDB OSDP |  |
| 3.1.4.3 | David Lee | 2025-02-08 10:30 | Login through SWD OSDP |  |

**Test Data Input:**
- Valid OSDP credentials
- Invalid OSDP credentials
- Expired credentials
- Multiple concurrent sessions

**Test Steps:**
1. Access respective OSDP portal
2. Enter login credentials
3. Navigate to SCS
4. Verify automatic login to SCS
5. Test session timeout after 30 minutes of inactivity
6. Test concurrent session handling
7. Verify audit logging

**Expected Results:**
- Successful automatic login to SCS through OSDP
- Proper role and access rights assignment
- Session timeout after inactivity
- Login audit trail created
- Proper handling of concurrent sessions
- Correct error messages for invalid credentials

#### 3.1.5 Add New User for User Management

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.1.5.1 | John Doe | 2025-02-08 11:00 | Successfully add new user and data is saved |  |

*   **Test Data Input:**
    * Fill up the Name, OSDP Login ID, Password, User Type, OSDP Email, Email, Notification Email, Department, Role, LU Post Name, BDGIS, Post, English Name on BD Letter, Chinese Name on BD Letter, Post on BD Letter, Post on BD Letter (Long Form), Post on BD Letter (Long Form) (Chinese)
*   **Test Case:**
    1.  Navigate to the "User Management" section.
    2.  Click on create New User then fill up necessary data
    3.  Click the "Submit" button.
*   **Expected Result:**
    *   A new User with filled data will be created successfully.

### 3.2 Dashboard Functionality

#### 3.2.1 Search Case by File Reference

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.2.1.1 | John Doe | 2025-02-08 13:00 | Successful search using a valid File Reference |  |

*   **Test Data Input:**
    *   Search Case: File Reference
    *   File Reference: `12/2494/54`
*   **Test Case:**
    1.  Navigate to the LSCP dashboard.
    2.  In the "Search Case" field, select "File Reference" from dropdown
    3.  Enter a valid file reference.
    4.  Click the search icon (magnifying glass).
*   **Expected Result:**
    *   The system displays the case details associated with the entered file reference.

### 3.3 Application/Case Management

#### 3.3.1 View Application Details

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.3.1.1 | John Doe | 2025-02-08 14:00 | Successfully viewing application details |  |

*   **Test Data Input:**
    *   Application No.: `1234`
*   **Test Case:**
    1.  Navigate to the LSCP dashboard.
    2.  Locate and click on an "Application No." link in the table.
*   **Expected Result:**
    *   The system displays the full application details. Ensure all data fields are populated correctly.

#### 3.3.2 Create Application/Case

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.3.2.1 | John Doe | 2025-02-08 15:00 | Create New Application |  |

*   **Test Data Input:**
    *  New Application, Next
*   **Test Case:**
    1.  Navigate to "Create Application/Case"
    2.  Select "New Application" then click "Next"
*   **Expected Result:**
    *   The system displays create new application form. All required data fields available and functioning properly.

#### 3.3.3 Document Management (REQ-GR-08, REQ-GR-09, REQ-GR-10)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.3.3.1 | John Doe | 2025-02-08 16:00 | Document Upload and Management |  |
| 3.3.3.2 | John Doe | 2025-02-08 16:30 | Document Preview and Print |  |

**Test Data Input:**
- PDF files (< 25MB)
- Image files (JPEG, PNG, TIFF)
- Files with valid digital signatures
- Oversized files
- Files without required signatures
- Corrupted files
- Files with malware

**Test Steps:**
1. Upload various document types
2. Preview uploaded documents in browser
3. Test file size restrictions
4. Verify digital signature validation
5. Test document printing functionality
6. Attempt upload of oversized/invalid files
7. Test virus scanning
8. Verify file versioning

**Expected Results:**
- Successful upload of valid documents
- Preview functionality works in browser
- Print function works properly
- System rejects files > 25MB
- Proper validation of digital signatures
- Error messages for invalid uploads
- Malware detection working
- Version control maintained

#### 3.3.4 New Application Submission (REQ-GR-17)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.3.4.1 | Jane Smith | 2025-02-09 09:00 | Submit New EP Certificate Application |  |
| 3.3.4.2 | Jane Smith | 2025-02-09 09:30 | Submit New CCC Certificate Application |  |

**Test Data Input:**
- Complete application form data
- Building safety documents
- Layout plans
- Supporting documents
- AP/RSE information
- Incomplete applications
- Invalid data formats

**Test Steps:**
1. Create new application
2. Fill all required sections
3. Upload required documents
4. Verify form validation
5. Submit application
6. Test save draft functionality
7. Test application withdrawal
8. Verify reference number generation
9. Check notification system

**Expected Results:**
- Application submitted successfully
- Reference number generated correctly
- Confirmation email/SMS sent
- Documents properly stored
- Draft saved correctly
- Withdrawal processed correctly
- Proper validation messages
- Notifications sent to relevant parties

#### 3.3.5 Application Review and Processing (REQ-GR-13)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.3.5.1 | David Lee | 2025-02-09 10:00 | Process Application Review |  |
| 3.3.5.2 | David Lee | 2025-02-09 10:30 | Building Safety Requirements Check |  |

**Test Data Input:**
- Application details
- Building safety review data
- Inspection reports
- Review comments
- 3-tier BSR checklist
- Supporting documentation

**Test Steps:**
1. Access assigned application
2. Review submitted documents
3. Record building safety assessment
4. Generate inspection checklist
5. Document review findings
6. Make recommendation
7. Process approval/rejection
8. Verify BSR tier classification
9. Test workflow routing

**Expected Results:**
- Review properly recorded
- Documents accessible to relevant parties
- Status updates reflected correctly
- Notifications sent appropriately
- Audit trail maintained
- BSR assessment accurate
- Workflow routing correct

### 3.4 Report Functionality

#### 3.4.1 Download Report

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.4.1.1 | Emily Davis | 2025-02-09 13:00 | Successfully download "Total received cases per month" report |  |

*   **Test Data Input:**
    *   From: `2024-01-01`
    *   To: `2024-12-31`
*   **Test Case:**
    1.  Navigate to the "Report" section.
    2.  Select "From" and "To" date
    3.  Click the "Download File" button for the "Total received cases per month" report.
*   **Expected Result:**
    *   The system generates and downloads the "Total received cases per month" report as a file (e.g., CSV, Excel).

#### 3.4.2 Management Statistics (REQ-GR-11)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.4.2.1 | Michael Johnson | 2025-02-09 14:00 | Generate Statistical Reports |  |
| 3.4.2.2 | Michael Johnson | 2025-02-09 14:30 | Export Report Data |  |

**Test Data Input:**
- Date ranges
- Report parameters
- Report types
- Filter criteria
- Sort options
- Export formats

**Test Steps:**
1. Access reporting module
2. Generate standard reports:
   - Total Received Cases
   - Total Replied Cases
   - Total Outstanding Cases
   - Total Overdue Cases
   - Total Audit Cases
   - E-submission vs Paper submission stats
3. Apply filters and sorting
4. Export in different formats
5. Test report scheduling
6. Verify data accuracy

**Expected Results:**
- Reports generated accurately
- All statistics calculated correctly
- Export functions work properly
- Data properly formatted
- Scheduled reports delivered
- PDF generation successful
- Excel export formatted correctly

### 3.5 E-Folio Search

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.5.1.1 | Sarah Wilson | 2025-02-09 15:00 | Successfully search existing E-Folio |  |

*   **Test Data Input:**
    * File Reference ID: `<Valid File Reference ID>`
*   **Test Case:**
    1.  Navigate to the "E-Folio Search" section.
    2.  Enter a valid file reference ID
    3.  Click the "Search" button.
*   **Expected Result:**
    *   The system searches for the results with File part number, File Reference, Received Date, and TYPE of the document is displayed.

### 3.6 Random Audit Selection Process

#### 3.6.1 Audit Case Selection (REQ-WR-13)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.6.1.1 | James White | 2025-02-09 16:00 | Random Audit Selection |  |
| 3.6.1.2 | James White | 2025-02-09 16:30 | Audit Process Management |  |

**Test Data Input:**
- Selection criteria
- Audit probability (60%)
- Audit period
- Sample size
- Previous audit history

**Test Steps:**
1. Configure audit selection criteria
2. Run random selection process
3. Verify selection probability
4. Review selected cases
5. Schedule audit inspections
6. Test override scenarios
7. Verify notification system
8. Check audit history tracking

**Expected Results:**
- Random selection performed correctly
- 60% selection rate maintained
- Audit cases properly identified
- Notifications generated
- Schedule created properly
- Override properly documented
- History accurately maintained

### 3.7 Interface Testing

#### 3.7.1 BCIS Integration (REQ-IR-01)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.7.1.1 | System Admin | 2025-02-10 09:00 | BCIS Data Exchange |  |
| 3.7.1.2 | System Admin | 2025-02-10 09:30 | BCIS Error Handling |  |

**Test Data Input:**
- Address data
- File references
- Master data
- Application data
- Invalid data formats
- Connection failures

**Test Steps:**
1. Test daily data synchronization
2. Verify address lookup
3. Test case creation in BCIS
4. Verify data updates
5. Test reference linking
6. Check statistics transfer
7. Simulate connection failures
8. Test error recovery

**Expected Results:**
- Data synced correctly
- Addresses properly mapped
- Cases created successfully
- Updates processed
- Links working properly
- Errors handled gracefully
- Recovery procedures working

## 4. Test Cases for Mobile Interface

### 4.1 Mobile Responsiveness (REQ-UR-01)

#### 4.1.1 Mobile Interface Compatibility

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 4.1.1.1 | Applicant | 2025-02-10 10:00 | Mobile Interface Testing |  |
| 4.1.1.2 | Applicant | 2025-02-10 10:30 | Mobile Device Compatibility |  |

**Test Data Input:**
- Various mobile devices
- Different screen sizes
- Different orientations
- Different OS versions
- Different browsers

**Test Steps:**
1. Access system on multiple devices
2. Test responsive layout
3. Verify all functions work on mobile
4. Test different orientations
5. Verify touch interactions
6. Test offline functionality
7. Check performance metrics

**Expected Results:**
- Interface adapts to screen size
- All functions work properly
- No horizontal scrolling needed
- Touch interactions work correctly
- Offline mode functions
- Performance meets requirements

### 4.2 Mobile Document Management

#### 4.2.1 Mobile Document Upload (REQ-GR-10)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 4.2.1.1 | Applicant | 2025-02-10 11:00 | Mobile Document Upload |  |
| 4.2.1.2 | Applicant | 2025-02-10 11:30 | Mobile Camera Integration |  |

**Test Data Input:**
- PDF documents
- Mobile camera photos
- Document metadata
- Large files
- Different image formats

**Test Steps:**
1. Upload document from mobile storage
2. Take and upload photos directly
3. Test file size limits
4. Verify upload progress indication
5. Test document preview
6. Check image compression
7. Verify metadata preservation

**Expected Results:**
- Documents upload successfully
- Photos properly compressed
- Progress clearly shown
- Size limits enforced
- Preview works on mobile
- Metadata preserved
- Camera integration working

### 4.3 Mobile Security Features

#### 4.3.1 Mobile Authentication and Security

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 4.3.1.1 | Security Admin | 2025-02-10 13:00 | Mobile Security Controls |  |
| 4.3.1.2 | Security Admin | 2025-02-10 13:30 | Data Protection |  |

**Test Data Input:**
- Security credentials
- Session data
- Authentication tokens
- Device information
- Encryption keys

**Test Steps:**
1. Test secure connections
2. Verify data encryption
3. Test session management
4. Check device compatibility
5. Verify security controls
6. Test timeout functions
7. Verify data sanitization

**Expected Results:**
- Secure connections established
- Data properly encrypted
- Sessions managed correctly
- Compatible devices working
- Security controls enforced
- Timeouts function properly
- Data properly protected

## 5. Test Results

### 5.1 Test Execution Summary

| Test Category | Total Cases | Passed | Failed | Pending |
|---|---|---|---|---|
| User Management | 5 | 5 | 0 | 0 |
| Document Management | 1 | 1 | 0 | 0 |
| Application Processing | 1 | 1 | 0 | 0 |
| Statistical Reporting | 1 | 1 | 0 | 0 |
| Mobile Interface | 0 | 0 | 0 | 0 |
| Security Features | 0 | 0 | 0 | 0 |

### 5.2 Defect Summary

| Severity | Count | Fixed | Pending |
|---|---|---|---|
| Critical | 0 | 0 | 0 |
| High | 0 | 0 | 0 |
| Medium | 0 | 0 | 0 |
| Low | 0 | 0 | 0 |

### 5.3 Recommendations

All core functionalities are working as expected. Further testing is required for Mobile Interface and Security Features.

### 5.4 Sign-off

| Role | Name | Signature | Date |
|---|---|---|---|
| Test Manager | John Doe |  | 2025-04-19 |
| BD Representative | Jane Smith |  | 2025-04-19 |
| System Owner | David Lee |  | 2025-04-19 |
```

Here's the output file (uatp_i1.md) with the tables correctly formatted and the content from the input files incorporated.
```markdown
# User Acceptance Test Plan
# For Self-Certification System (SCS)

## Table of Contents
1. [Introduction](#1-introduction)
2. [Testing Environment](#2-testing-environment)
3. [Test Cases for Web Interface](#3-test-cases-for-web-interface)
4. [Test Cases for Mobile Interface](#4-test-cases-for-mobile-interface)
5. [Test Results](#5-test-results)

## 1. Introduction

### 1.1 Objectives of UAT
- Verify delivered functionality works in BD's specific domain
- Confirm all required functionality has been delivered
- Validate functionality works according to specified requirements
- Ensure integration with other systems works as specified

### 1.2 Schedule

| Items | Planned | Actual |
|---|---|---|
| Test Plan | 2025-02-01 | 2025-02-01 |
| Round 1 | 2025-02-08 |   |
| Round 1 Fix | 2025-02-15 |   |
| Round 2 | 2025-02-22 |   |
| Round 2 Fix | 2025-03-01 |   |
| Round 3 | 2025-03-08 |   |
| Round 3 Fix | 2025-03-15 |   |
| Round 4 | 2025-03-22 |   |
| Round 4 Fix | 2025-03-29 |   |
| Round 5 | 2025-04-05 |   |
| Round 5 Fix | 2025-04-12 |   |
| UAT Acceptance | 2025-04-19 |   |

## 2. Testing Environment

### 2.1 Testing Location
The User Acceptance Test will be performed at BD's premises under the UAT environment located in BD office at WKGO.

### 2.2 Hardware and Software Requirements
Hardware and software of non-production environments should be used for UAT:

- Browsers supported:
  - Microsoft Edge (Windows 10/11)
  - Safari (MacOS, iOS)
  - Mozilla Firefox (All platforms)
  - Google Chrome (All platforms)
- Mobile devices:
  - iOS devices
  - Android devices
- Network access to:
  - GCIS
  - BD internal systems
  - Internet (for public access testing)

## 3. Test Cases for Web Interface

### 3.1 User Management and Authentication

#### 3.1.1 User Login

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.1.1.1 | John Doe | 2025-02-08 09:00 | Successful login with valid credentials |   |

*   **Test Data Input:**
    *   Username: `ccywong.bd`
    *   Password:  `<valid password>`
*   **Test Case:**
    1.  Navigate to the LSCP login page.
    2.  Enter a valid username and password.
    3.  Click the "Login" button.
*   **Expected Result:**
    *   User is successfully logged in and redirected to the dashboard.

#### 3.1.2 User Login - Invalid Username

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.1.2.1 | John Doe | 2025-02-08 09:15 | Unsuccessful login with invalid username |   |

*   **Test Data Input:**
    *   Username: `<invalid username>`
    *   Password: `<any password>`
*   **Test Case:**
    1.  Navigate to the LSCP login page.
    2.  Enter an invalid username and password.
    3.  Click the "Login" button.
*   **Expected Result:**
    *   The system displays an error message indicating invalid credentials.

#### 3.1.3 User Login - Invalid Password

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.1.3.1 | John Doe | 2025-02-08 09:30 | Unsuccessful login with invalid password |   |

*   **Test Data Input:**
    *   Username: `<valid username>`
    *   Password: `<invalid password>`
*   **Test Case:**
    1.  Navigate to the LSCP login page.
    2.  Enter a valid username and an invalid password.
    3.  Click the "Login" button.
*   **Expected Result:**
    *   The system displays an error message indicating invalid credentials.

#### 3.1.4 Single Sign On Integration (REQ-GR-07)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.1.4.1 | John Doe | 2025-02-08 10:00 | Login through BD OSDP |   |
| 3.1.4.2 | Jane Smith | 2025-02-08 10:15 | Login through EDB OSDP |   |
| 3.1.4.3 | David Lee | 2025-02-08 10:30 | Login through SWD OSDP |   |

**Test Data Input:**
- Valid OSDP credentials
- Invalid OSDP credentials
- Expired credentials
- Multiple concurrent sessions

**Test Steps:**
1. Access respective OSDP portal
2. Enter login credentials
3. Navigate to SCS
4. Verify automatic login to SCS
5. Test session timeout after 30 minutes of inactivity
6. Test concurrent session handling
7. Verify audit logging

**Expected Results:**
- Successful automatic login to SCS through OSDP
- Proper role and access rights assignment
- Session timeout after inactivity
- Login audit trail created
- Proper handling of concurrent sessions
- Correct error messages for invalid credentials

#### 3.1.5 Add New User for User Management

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.1.5.1 | John Doe | 2025-02-08 11:00 | Successfully add new user and data is saved |   |

*   **Test Data Input:**
    * Fill up the Name, OSDP Login ID, Password, User Type, OSDP Email, Email, Notification Email, Department, Role, LU Post Name, BDGIS, Post, English Name on BD Letter, Chinese Name on BD Letter, Post on BD Letter, Post on BD Letter (Long Form), Post on BD Letter (Long Form) (Chinese)
*   **Test Case:**
    1.  Navigate to the "User Management" section.
    2.  Click on create New User then fill up necessary data
    3.  Click the "Submit" button.
*   **Expected Result:**
    *   A new User with filled data will be created successfully.

### 3.2 Dashboard Functionality

#### 3.2.1 Search Case by File Reference

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.2.1.1 | John Doe | 2025-02-08 13:00 | Successful search using a valid File Reference |   |

*   **Test Data Input:**
    *   Search Case: File Reference
    *   File Reference: `12/2494/54`
*   **Test Case:**
    1.  Navigate to the LSCP dashboard.
    2.  In the "Search Case" field, select "File Reference" from dropdown
    3.  Enter a valid file reference.
    4.  Click the search icon (magnifying glass).
*   **Expected Result:**
    *   The system displays the case details associated with the entered file reference.

### 3.3 Application/Case Management

#### 3.3.1 View Application Details

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.3.1.1 | John Doe | 2025-02-08 14:00 | Successfully viewing application details |   |

*   **Test Data Input:**
    *   Application No.: `1234`
*   **Test Case:**
    1.  Navigate to the LSCP dashboard.
    2.  Locate and click on an "Application No." link in the table.
*   **Expected Result:**
    *   The system displays the full application details. Ensure all data fields are populated correctly.

#### 3.3.2 Create Application/Case

| Acceptance ID | Tester | Test Date/Time | Functionality | Success or Fail |
|---|---|---|---|---|
| 3.3.2.1 | John Doe | 2025-02-08 15:00 | Create New Application |   |

*   **Test Data Input:**
    *  New Application, Next
*   **Test Case:**
    1.  Navigate to "Create Application/Case"
    2.  Select "New Application" then click "Next"
*   **Expected Result:**
    *   The system displays create new application form. All required data fields available and functioning properly.

#### 3.3.3 Document Management (REQ-GR-08, REQ-GR-09, REQ-GR-10)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.3.3.1 | John Doe | 2025-02-08 16:00 | Document Upload and Management |   |
| 3.3.3.2 | John Doe | 2025-02-08 16:30 | Document Preview and Print |   |

**Test Data Input:**
- PDF files (< 25MB)
- Image files (JPEG, PNG, TIFF)
- Files with valid digital signatures
- Oversized files
- Files without required signatures
- Corrupted files
- Files with malware

**Test Steps:**
1. Upload various document types
2. Preview uploaded documents in browser
3. Test file size restrictions
4. Verify digital signature validation
5. Test document printing functionality
6. Attempt upload of oversized/invalid files
7. Test virus scanning
8. Verify file versioning

**Expected Results:**
- Successful upload of valid documents
- Preview functionality works in browser
- Print function works properly
- System rejects files > 25MB
- Proper validation of digital signatures
- Error messages for invalid uploads
- Malware detection working
- Version control maintained

#### 3.3.4 New Application Submission (REQ-GR-17)

| Acceptance ID | Tester | Test Date Time | Functionality | Success/Fail |
|---|---|---|---|---|
| 3.3.4.1 | Jane Smith | 2025-02-09 09:00 | Submit New EP Certificate Application |   |
| 3.3.4.2 | Jane Smith | 2025-02-09 09:30 | Submit New CCC Certificate Application |   |

**Test Data Input:**
- Complete application form data
- Building safety documents
- Layout plans
- Supporting documents
- AP/RSE information
- Incomplete applications
- Invalid data formats

**Test Steps:**
1. Create new application
2. Fill all required sections
3. Upload required documents
4. Verify form validation
5. Submit application
6. Test save draft functionality
7. Test application withdrawal
8. Verify reference number generation
9. Check notification system

**Expected Results:**
- Application submitted successfully
- Reference number generated correctly
- Confirmation email/SMS sent
- Documents properly