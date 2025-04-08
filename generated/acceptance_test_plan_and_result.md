# Acceptance Test Plan and Result

## Codebase Overview

### File Summary

```
Purpose:
--------
This file contains a packed representation of the entire repository's contents.
It is designed to be easily consumable by AI systems for analysis, code review,
or other automated processes.

File Format:
------------
The content is organized as follows:
1. This summary section
2. Repository information
3. Directory structure
4. Multiple file entries, each consisting of:
  a. A separator line (================)
  b. The file path (File: path/to/file)
  c. Another separator line
  d. The full contents of the file
  e. A blank line

Usage Guidelines:
-----------------
- This file should be treated as read-only. Any changes should be made to the
  original repository files, not this packed version.
- When processing this file, use the file path to distinguish
  between different files in the repository.
- Be aware that this file may contain sensitive information. Handle it with
  the same level of security as you would the original repository.

Notes:
------
- Some files may have been excluded based on .gitignore rules and Repomix's
  configuration.
- Binary files are not included in this packed representation. Please refer to
  the Repository Structure section for a complete list of file paths, including
  binary files.

Additional Info:
----------------
```

### Directory Structure

```
bd-scs-backend-backend-main/app.js
bd-scs-backend-backend-main/config/application.js
bd-scs-backend-backend-main/config/cat.js
bd-scs-backend-backend-main/config/collections.js
bd-scs-backend-backend-main/config/letterTemplates.js
bd-scs-backend-backend-main/config/replyDays.js
bd-scs-backend-backend-main/config/task.js
bd-scs-backend-backend-main/config/user.js
bd-scs-backend-backend-main/middlewares/requireUser.js
bd-scs-backend-backend-main/models/AdrBlkFileRef.js
bd-scs-backend-backend-main/models/Application_old.js
bd-scs-backend-backend-main/models/Application.js
bd-scs-backend-backend-main/models/Attachment.js
bd-scs-backend-backend-main/models/BsBlock.js
bd-scs-backend-backend-main/models/Case.js
bd-scs-backend-backend-main/models/Eminute.js
bd-scs-backend-backend-main/models/Notification.js
bd-scs-backend-backend-main/models/OAuthToken.js
bd-scs-backend-backend-main/models/Submission.js
bd-scs-backend-backend-main/models/SysFileRef.js
bd-scs-backend-backend-main/models/Task.js
bd-scs-backend-backend-main/models/User.js
bd-scs-backend-backend-main/public/assets/app-DoNz6BTu.js
bd-scs-backend-backend-main/routes/applications.js
bd-scs-backend-backend-main/routes/attachments.js
bd-scs-backend-backend-main/routes/auth.js
bd-scs-backend-backend-main/routes/cases.js
bd-scs-backend-backend-main/routes/fileReferences.js
bd-scs-backend-backend-main/routes/index.js
bd-scs-backend-backend-main/routes/OAuthModel.js
bd-scs-backend-backend-main/routes/submissions.js
bd-scs-backend-backend-main/routes/tasks.js
bd-scs-backend-backend-main/routes/users.js
bd-scs-backend-backend-main/scripts/assignUserType.js
bd-scs-backend-backend-main/scripts/FixBsBlock.js
bd-scs-backend-backend-main/scripts/importAdrFileRef.js
bd-scs-backend-backend-main/scripts/importBsBlock.js
bd-scs-backend-backend-main/scripts/importFileRef.js
bd-scs-backend-backend-main/scripts/importTeam.js
bd-scs-backend-backend-main/scripts/importUsers.js
bd-scs-backend-backend-main/scripts/migrateGroupAndDepartment.js
bd-scs-backend-backend-main/scripts/setUpDb.js
bd-scs-backend-backend-main/scripts/syncFrontendSubmissions.js
bd-scs-backend-backend-main/utils/application.js
bd-scs-backend-backend-main/utils/hkpostUtils.js
bd-scs-backend-backend-main/utils/letter.js
bd-scs-backend-backend-main/utils/MongoDBHelper.js
bd-scs-backend-backend-main/utils/sendEmail.js
bd-scs-backend-backend-main/utils/SQLDBHelper.js
bd-scs-backend-web-main/src/apis/application.js
bd-scs-backend-web-main/src/apis/auth.js
bd-scs-backend-web-main/src/apis/case.js
bd-scs-backend-web-main/src/apis/letterTemplate.js
bd-scs-backend-web-main/src/apis/task.js
bd-scs-backend-web-main/src/apis/user.js
bd-scs-backend-web-main/src/App.test.js
bd-scs-backend-web-main/src/constants/colors.js
bd-scs-backend-web-main/src/constants/index.js
bd-scs-backend-web-main/src/constants/letters.js
bd-scs-backend-web-main/src/constants/options.js
bd-scs-backend-web-main/src/constants/tasks.js
bd-scs-backend-web-main/src/i18n.js
bd-scs-backend-web-main/src/reportWebVitals.js
bd-scs-backend-web-main/src/setupTests.js
bd-scs-backend-web-main/src/transactions/en/index.js
bd-scs-backend-web-main/src/transactions/zh/index.js
bd-scs-nodejs-frontend-main/src/app.js
bd-scs-nodejs-frontend-main/src/migrations/20241013174558-add_Synced_field.js
bd-scs-nodejs-frontend-main/src/models/AdrBlk.js
bd-scs-nodejs-frontend-main/src/models/ApplicationCase.js
bd-scs-nodejs-frontend-main/src/models/ApplicationFile.js
bd-scs-nodejs-frontend-main/src/models/ApRse.js
bd-scs-nodejs-frontend-main/src/models/Attachment.js
bd-scs-nodejs-frontend-main/src/models/BackendUpdate.js
bd-scs-nodejs-frontend-main/src/models/GenOtp.js
bd-scs-nodejs-frontend-main/src/models/IamSmart.js
bd-scs-nodejs-frontend-main/src/models/LogEvents.js
bd-scs-nodejs-frontend-main/src/models/SchoolAppInfo.js
bd-scs-nodejs-frontend-main/src/models/SchoolAppSubmission.js
bd-scs-nodejs-frontend-main/src/models/ScsMasterTable.js
bd-scs-nodejs-frontend-main/src/models/Staff.js
bd-scs-nodejs-frontend-main/src/models/Sys_Meta_Data.js
bd-scs-nodejs-frontend-main/src/models/Test.js
bd-scs-nodejs-frontend-main/src/routes/ApplicationController.js
bd-scs-nodejs-frontend-main/src/routes/AuthController.js
bd-scs-nodejs-frontend-main/src/routes/ESignController.js
bd-scs-nodejs-frontend-main/src/services/IamSmartServices.js
bd-scs-nodejs-frontend-main/src/tests/initializeDatabase.js
bd-scs-nodejs-frontend-main/src/tests/testAdrBlk.js
bd-scs-nodejs-frontend-main/src/tests/testApplicationCase.js
bd-scs-nodejs-frontend-main/src/tests/testApplicationFile.js
bd-scs-nodejs-frontend-main/src/tests/testApRse.js
bd-scs-nodejs-frontend-main/src/tests/testGenOtp.js
bd-scs-nodejs-frontend-main/src/tests/testLogEvents.js
bd-scs-nodejs-frontend-main/src/tests/testSchoolAppInfo.js
bd-scs-nodejs-frontend-main/src/tests/testSchoolAppSubmission.js
bd-scs-nodejs-frontend-main/src/tests/testScsMasterTable.js
bd-scs-nodejs-frontend-main/src/tests/testSMTP.js
bd-scs-nodejs-frontend-main/src/tests/testStaff.js
bd-scs-nodejs-frontend-main/src/tests/testSysMetaDataModel.js
bd-scs-nodejs-frontend-main/src/tests/testTestModel.js
bd-scs-nodejs-frontend-main/src/utils/aes256gcm.js
bd-scs-nodejs-frontend-main/src/utils/applicationUtils.js
bd-scs-nodejs-frontend-main/src/utils/ExternalSigner.js
bd-scs-nodejs-frontend-main/src/utils/hkpostUtils.js
bd-scs-nodejs-frontend-main/src/utils/iamSmartUtils.js
bd-scs-nodejs-frontend-main/src/utils/loginUtils.js
bd-scs-nodejs-frontend-main/src/utils/on9Dotnet.js
bd-scs-nodejs-frontend-main/src/utils/signConfig.js
bd-scs-nodejs-frontend-main/src/utils/Signer.js
bd-scs-nodejs-frontend-main/src/utils/signUtils.js
bd-scs-react-frontend-frontend-main/.eslintrc.js
bd-scs-react-frontend-frontend-main/.prettierrc.js
bd-scs-react-frontend-frontend-main/.stylelintrc.js
bd-scs-react-frontend-frontend-main/commitlint.config.js
bd-scs-react-frontend-frontend-main/lint-staged.config.js
bd-scs-react-frontend-frontend-main/postcss.config.js
bd-scs-react-frontend-frontend-main/tailwind.config.js
```

### Files

```
================
File: bd-scs-backend-backend-main/app.js
================
var createError = require("http-errors");
var express = require("express");
var path = require("path");
var cookieParser = require("cookie-parser");
var logger = require("morgan");
var cors = require("cors");

var indexRouter = require("./routes/index");
var authRouter = require("./routes/auth");
var usersRouter = require("./routes/users");
var tasksRouter = require("./routes/tasks");
var casesRouter = require("./routes/cases");
var applicationsRouter = require("./routes/applications");
var submissionsRouter = require("./routes/submissions");
var attachmentsRouter = require("./routes/attachments");
const fileReferencesRouter = require("./routes/fileReferences");
var app = express();

// const { importBsBlock } = require("./scripts/importBsBlock");
// importBsBlock("./scripts/LU1_StructID (BDGIS v20240425).xlsx");
// view engine setup
app.set("views", path.join(__dirname, "views"));
app.set("view engine", "jade");

app.use(logger("dev"));
app.use(cors());
app.use(express.json());
app.use(express.urlencoded({ extended: false }));
app.use(cookieParser());
app.use(express.static(path.join(__dirname, "public")));

app.use("/", indexRouter);
app.use("/auth", authRouter);
app.use("/users", usersRouter);
app.use("/tasks", tasksRouter);
app.use("/cases", casesRouter);
app.use("/applications", applicationsRouter);
app.use("/submissions", submissionsRouter);
app.use("/attachments", attachmentsRouter);
app.use("/file-references", fileReferencesRouter);

// catch 404 and forward to error handler
app.use(function (req, res, next) {
  next(createError(404));
});

// error handler
app.use(function (err, req, res, next) {
  console.log(err);
  // set locals, only providing error in development
  res.locals.message = err.message;
  res.locals.error = req.app.get("env") === "development" ? err : {};

  // render the error page
  res.status(err.status || 500).send({ error: err.message });
  // res.render("error");
});

// Schedule tasks
const { sync } = require("./scripts/syncFrontendSubmissions");
setInterval(sync, 60000);

module.exports = app;
```

---

## User Acceptance Test Plan

### 1. Introduction

This document is the User Acceptance Test Plan (UATP) for Combined
System Development Services for Licensing Self-Certification Portal
(LSCP) of the Buildings Department.

### 1.1 Objectives of the UAT

It is helpful to know the definition of UAT and the purpose of it.
Therefore, the objectives of the User Acceptance Test should be agreed
upon in advance. The objectives of the UAT are

-   Checking that the delivered functionality works in BD?s specific
    domain.

-   Checking that all functionality required has been delivered.

-   Checking that the delivered functionality works according to
    specified and approved scope and requirements.

### 1.2 Schedule

| Items                               | Planned     |             | Actual      |             |
| :---------------------------------- | :---------- | :---------- | :---------- | :---------- |
| Test Plan                           | 17 Mar 2023 | 7 Apr 2023  | 17 Mar 2023 | 7 Apr 2023  |
| Round 1                             | 17 Apr 2023 | 28 Apr 2023 | 17 Apr 2023 | 28 Apr 2023 |
| Round 1 Fix                         | 1 May 2023  | 6 Jun 2023  | 1 May 2023  | 6 Jun 2023  |
| Round 2                             | 7 Jun 2023 | 23 Jun 2023 | 7 Jun 2023  | 23 Jun 2023 |
| Round2 Fix                          | 26 Jun 2023 | 3 Jul 2023  | 26 Jun 2023 | 3 Jul 2023  |
| Round 3                             | 5 Jul 2023  | 28 Jul 2023 | 5 Jul 2023  | 28 Jul 2023 |
| Round 3 Fix                         | 31 Jul 2023 | 4 Aug 2023  | 31 Jul 2023 | 4 Aug 2023  |
| Round 4                             | 7 Aug 2023  | 25 Aug 2023 | 7 Aug 2023  | 25 Aug 2023 |
| Round 4 Fix                         | 28 Aug 2023 | 22 Sep 2023 | 28 Aug 2023 | 22 Sep 2023 |
| Round 5                             | 25 Sep 2023 | 13 Oct 2023 | 25 Sep 2023 | 30 Oct 2023 |
| Round 5 Fix                         | 16 Oct 2023 | 25 Oct 2023 | 1 Nov 2023  | 7 Nov 2023  |
| Presentation to Senior Management | 17 Oct 2023 | 17 Oct 2023 | 17 Oct 2023 | 17 Oct 2023 |
| UAT Acceptance                      | 26 Oct 2023 | 30 Oct 2023 | 8 Nov 2023  | 6 Dec 2023  |

### 2. Testing Environment

#### 2.1 Testing Location

The User Acceptance Test will be performed at BD?s premises under the
UAT environment located in BD office at WKGO.

#### 2.2 Hardware and Software Requirement

Hardware and software of non-production environments should be used for
UAT.

### 3. Test Case for Web

#### 3.1 User Management

##### 3.1.1 Public User registration

| Acceptance ID | Tester | Test Date Time | Functionality                                                                   | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------------------------------------------------ | :-------------- |
| 3.1.1.1       |        |                | successful case for registering new account                                     | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Tester clicks the ?Register? button on the system login page.                                                           |                 |

##### Expected Result

Tester registered the new account successfully

#### 3.1.2 Public login

| Acceptance ID | Tester | Test Date Time | Functionality                                                              | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------------------------------------------- | :-------------- |
| 3.1.2.1       | TCP    |                | System generates a one-time password when the user accesses the system.     | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  In reference to the account registered in acceptance ID 3.1.1.1                                                       |                 |
| 2.  TCP inputs peter.chan@hotmail.com in the Email field                                                                  |                 |
| 3.  TCP inputs Aa@123456 in Password field                                                                               |                 |
| 4.  TCP presses Login button                                                                                               |                 |

##### Expected Result

TCP should receive a one-time password (OTP) in his registered email
address generated by the system

| Acceptance ID | Tester | Test Date Time | Functionality                                    | Success or Fail |
| :------------ | :----- | :------------- | :----------------------------------------------- | :-------------- |
| 3.1.2.4       | TCP    |                | User use one time password to login into system | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  In reference to acceptance ID 3.1.1.10                                                                                 |                 |
| 2.  TCP inputs the one-time password received from his registered email address into One-Time Password field              |                 |
| 3.  TCP presses Login button                                                                                               |                 |

##### Expected Result

User login into system successfully

| Acceptance ID | Tester | Test Date Time | Functionality                               | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------------ | :-------------- |
| 3.1.2.5       | TCP    |                | System allow user to reset password         | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  TCP presses Forget Password link on the login page (picture 1)                                                         |                 |
| 2.  TCP inputs his registered email address into the email field (picture 2)                                               |                 |
| 3.  System prompts out notification message (picture 3)                                                                    |                 |

##### Expected Result

User receives an email with reset password link from his registered
email address

| Acceptance ID | Tester | Test Date Time | Functionality                                                              | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------------------------------------------- | :-------------- |
| 3.1.2.6       | AP, RSE, RGE and AS    |                | System only allows each user to have one single user session on the server | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  User log into system successfully as in Acceptance ID 3.1.1.1                                                         |                 |
| 2.  User then log into system again but using another device                                                              |                 |

##### Expected Result

The device for the initial login is redirected back to the login screen

### 3.1.3 User Management - Others

| Acceptance ID | Tester | Test Date Time | Functionality                                                     | Success or Fail |
| :------------ | :----- | :------------- | :---------------------------------------------------------------- | :-------------- |
| 3.1.3.1       | TCP    |                | Successful case for user to change password                       | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  TCP enters into account detail page after successful login as in Acceptance ID 3.1.1.1                                 |                 |
| 2.  TCP input Aa@123456 into ?Current Password? field                                                                      |                 |
| 3.  TCP input aA173173@ into ?New Password? field                                                                         |                 |
| 4.  TCP input aA173173@ into ?Confirm your new password? field                                                             |                 |
| 5.  TCP press ?Submit? button                                                                                               |                 |

##### Expected Result

System displays successful message and TCP has changed the password

| Acceptance ID | Tester | Test Date Time | Functionality                                                              | Success or Fail |
| :------------ | :----- | :------------- | :-------------------------------------------------------------------------- | :-------------- |
| 3.1.3.6       | TCP    |                | Successful case for updating personal information in ?Update Account Info? page | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  In reference to Acceptance ID 5.1.1, user enters into ?Account Detail? page                                           |                 |
| 2.  TCP inputs below information to the relevant fields                                                                    |                 |

*   User Given Name (English) ? Chi Keung

*   Chinese Full Name ? ???

*   Phone Number ? 61236123

3.  User press ?Submit? button

##### Expected Result

User changes his name and phone number successfully

## 3.2 Site Projects and Supervision Plan Management

### 3.2.1 Search Responsible Site Project

| Acceptance ID | Tester | Test Date Time | Functionality                                                              | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------------------------------------------- | :-------------- |
| 3.2.2.1       | AP/RSE/RGE/AS    |                | Successful case for Head of Stream searches for site project, which they are responsible for | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Head of Stream input the BD reference of the site project that he is responsible for in ?Search by Site Project BD Reference? field |                 |

##### Expected Result

System lists out the site project(s) that matches with the BD reference
and is responsible by the Head of Stream

### 3.2.2 Create new Site Project

| Acceptance ID | Tester | Test Date Time | Functionality                                | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------------- | :-------------- |
| 3.2.3.1       | AP/RSE/RGE/AS    |                | Successful case for creating new Site Project | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Tester press ?Create Site Project? button on ?Site Projects? page (Picture 1)                                          |                 |
| 2.  Tester inputs assigned BD Reference in ?Search by Site Project BD Reference? field (Picture 3)                         |                 |
| 3.  Tester press ?Create? button under the ?Action? column (Picture 3)                                                     |                 |
| 4.  Tester inputs below information in ?Create Site Project? page (Picture 4)                                              |                 |

*   Site Address

*   Lot No.

*   Site Address

*   Select Responsible Stream

5.  Tester press ?Submit? button

##### Expected Result

The new project is created successfully

### 3.2.3 Edit and update Site Project Detail

| Acceptance ID | Tester | Test Date Time | Functionality                                               | Success or Fail |
| :------------ | :----- | :------------- | :---------------------------------------------------------- | :-------------- |
| 3.2.4.1       | AP/RSE/RGE/AS    |                | Successful case for editing and updating site project detail | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Tester presses ?Edit? button on ?Site Projects? page                                                                   |                 |
| 2.  Tester edits and update information in below field                                                                     |                 |

*   Site Address

*   Lot No.

*   Tentative Commencement Date

##### Expected Result

The site project information has been edited successfully

### 3.2.4 List out Site Project

### 3.2.5 View Site Project Detail

| Acceptance ID | Tester | Test Date Time | Functionality                                 | Success or Fail |
| :------------ | :----- | :------------- | :-------------------------------------------- | :-------------- |
| 3.2.6.1       | AP/RSE/RGE/AS    |                | AP/RSE/RGE/AS views the site project details | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  On ?Site Projects? page, Tester clicks ?View? button for the site project that he wants to view                         |                 |

##### Expected Result

Tester can view the site project details such as the stream of site
project, site address, tentative commencement date etc.

### 3.2.6 Supervision Plan Detail View

| Acceptance ID | Tester | Test Date Time | Functionality                                           | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------------------------ | :-------------- |
| 3.2.7.1       | AP/RSE/RGE/AS    |                | AP/RSE/RGE/AS views the supervision plan detail | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  On ?Site Project Detail? page, Tester clicks ?View? button on the supervision plan that he wants to view              |                 |

##### Expected Result

Tester can view the supervision plan details

### 3.2.7 Supervision Plan Detail Management

| Acceptance ID | Tester | Test Date Time | Functionality                                                              | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------------------------------------------- | :-------------- |
| 3.2.8.1       | AP/RSE/RGE/AS    |                | Successful case for AP/RSE/RGE/AS to edit the supervision plan detail | successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  On ?Site Project Detail? page, Tester clicks ?Edit? button on the supervision plan that he wants to Edit             |                 |
| 2.  Tester change value of fields as below                                                                                 |                 |

*   Type of building works and street works ? Ground Investigation field
    works

*   Specific type of building works and street works ? GIFW

*   T1 - T4 Grade of TCP ? Suggested TCP assigned number ? 2

3.  Tester clicks ?Submit? button

##### Expected Result

Tester changed supervision plan details successfully

## 3.3 TCP management

### 3.3.1 Assign TCPs

| Acceptance ID | Tester | Test Date Time | Functionality                   | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------ | :-------------- |
| 3.3.1.1       | AP, RSE, RGE and AS    |                | Search TCP by Name                | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Go to ?List of TCPs? page                                                                                               |                 |
| 2.  Input the Name of TCP in ?Search Name? field                                                                           |                 |

##### Expected Result

All the matched TCPs will be Shown

| Acceptance ID | Tester | Test Date Time | Functionality         | Success or Fail |
| :------------ | :----- | :------------- | :-------------------- | :-------------- |
| 3.3.1.4       | AP, RSE, RGE and AS    |                | Add TCP into project     | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Go to ?List of TCPs? page                                                                                               |                 |
| 2.  Click ?Assign TCP? button                                                                                              |                 |
| 3.  Input the username that you want to assign as TCP in ?Search by Name? field                                            |                 |
| 4.  Add ?Add? button                                                                                                       |                 |
| 5.  Select ?Grade of TCP?                                                                                                  |                 |
| 6.  Click ?I confirm the personal above is qualified for his/her grade of TCP as declared.?                               |                 |
| 7.  The Page shown message shown the TCP adding request sent to TCP and awaiting TCP accept                               |                 |
| 8.  Tester switch the role and use TCP account to login into system again                                                 |                 |
| 9.  Tester accepts TCP invitation                                                                                          |                 |

##### Expected Result

HOS assign TCP successfully

### 3.3.2 Request TCP acceptance

| Acceptance ID | Tester | Test Date Time | Functionality                 | Success or Fail |
| :------------ | :----- | :------------- | :---------------------------- | :-------------- |
| 3.3.2.1       | TCP    |                | Accept ?Assign TCP? Request   | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  After completing Acceptance ID 3.3.1.4, TCP receives an assignment request email generated from the system.           |                 |
| 2.  TCP clicks on the accept link to accept being TCP in the assignment request email.                                     |                 |

##### Expected Result

The user should be redirected to the notification page, notifying him he
has been assigned as TCP of the project

| Acceptance ID | Tester | Test Date Time | Functionality                 | Success or Fail |
| :------------ | :----- | :------------- | :---------------------------- | :-------------- |
| 3.3.2.2       | TCP    |                | Reject ?Assign TCP? Request   | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  After completing Acceptance ID 3.3.1.4, TCP receives an assignment request email generated from the system.           |                 |
| 2.  TCP clicks on the reject link to reject being TCP in the assignment request email.                                     |                 |

##### Expected Result

The user should be redirected to the notification page, notifying him he
has rejected to be TCP of the project

### 3.3.3 Unassign TCPs

| Acceptance ID | Tester | Test Date Time | Functionality                       | Success or Fail |
| :------------ | :----- | :------------- | :---------------------------------- | :-------------- |
| 3.3.3.1       | TCP    |                | Unassign the assigned TCPs from project | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Go to ?List of TCPs? page                                                                                               |                 |
| 2.  Input ?Tai Man? in the first name field and ?Chan? in the last name field                                              |                 |
| 3.  Press ?Search? button                                                                                                   |                 |
| 4.  Click the row of ?Chan Tai Man? in the display result and then press ?Remove? button                                    |                 |

##### Expected Result

TCP ?Chan Tai Man? should be unassigned as TCP role

### 3.3.4 Temporary replacement of TCP

| Acceptance ID | Tester | Test Date Time | Functionality                        | Success or Fail |
| :------------ | :----- | :------------- | :----------------------------------- | :-------------- |
| 3.3.4.1       | AP, RSE, RGE and AS    |                | Temporary replacement of TCP | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Go to ?List of TCPs? page                                                                                               |                 |
| 2.  Input ?Siu Ming? in the first name field and ?Chan? in the last name field                                             |                 |
| 3.  Press ?Search? button                                                                                                   |                 |
| 4.  Click the row of ?Chan Siu Ming? in the display result and then press ?Temporary Replacement? button                   |                 |
| 5.  Search ?Wong Hoi Yen? name and then press ?Replace? button                                                             |                 |
| 6.  Set effective start date and end date of the replacement period                                                        |                 |

##### Expected Result

Wong Hoi Yen should receive invitation email for being temporary TCP

| Acceptance ID | Tester | Test Date Time | Functionality                               | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------------ | :-------------- |
| 3.3.4.2       | AP, RSE, RGE and AS    |                | Accept Temporary TCP Request | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Continue from Acceptance ID 5.3.4.1, Wong Hoi Yen clicks the link for acceptance of being temporary TCP received from her email |                 |

##### Expected Result

Wong Hoi Yen becomes temporary TCP

## 3.4 Form A

### 3.4.1 Create Form A template

| Acceptance ID | Tester | Test Date Time | Functionality             | Success or Fail |
| :------------ | :----- | :------------- | :------------------------ | :-------------- |
| 3.4.1.1       | AP    |                | Create Form A template    | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Tester clicks ?Create Form A template? button                                                                          |                 |
| 2.  Tester selects ?Chan Tai Man? in the ?Name? field                                                                      |                 |
| 3.  Tester inputs project start date and estimate project end date in the respective fields                               |                 |
| 4.  Tester clicks on ?A1 to A6? checkboxes                                                                                 |                 |
| 5.  Tester clicks ?Save? button                                                                                             |                 |

##### Expected Result

An new Form A template is created

### 3.4.2 Create Form A

| Acceptance ID | Tester | Test Date Time | Functionality         | Success or Fail |
| :------------ | :----- | :------------- | :-------------------- | :-------------- |
| 3.4.2.1       | TCP    |                | Create Form A         | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  TCP chooses a Form A template they are responsible for (Picture 1).                                                    |                 |
| 2.  TCP setup the frequency and the start date of the Form A (Picture 2).                                                  |                 |

##### Expected Result

An new Form A is created

### 3.4.3 Fill Form A

| Acceptance ID | Tester | Test Date Time | Functionality                          | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------------- | :-------------- |
| 3.4.3.1       | TCP    |                | Select or amend different tasks item status | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Users select all ?S? or ?N/A? status                                                                                    |                 |
| 2.  Users don?t select one of the item status                                                                               |                 |
| 3.  Users press ?amend? to correct the wrong status after save as draft                                                     |                 |

##### Expected Result

User can review the updated item status

| Acceptance ID | Tester | Test Date Time | Functionality             | Success or Fail |
| :------------ | :----- | :------------- | :------------------------ | :-------------- |
| 3.4.3.2       | TCP    |                | Review previous updated history | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                                                                                         |                 |
| **Test Case**                                                                                                               |                 |
| 1.  Tester open the draft created in Acceptance ID 5.4.3.1                                                                 |                 |
| 2.  Tester amend the value of the filled item                                                                              |                 |

##### Expected Result

Tester is able to review the revision history of the drafted Form A

| Acceptance ID | Tester | Test Date Time | Functionality                   | Success or Fail |
| :------------ | :----- | :------------- | :------------------------------ | :-------------- |
| 3.4.3.3       | TCP    |                | Import inspection record files | Successful      |
| **Test Data Input**                                                                                                        |                 |
| N/A                                                              