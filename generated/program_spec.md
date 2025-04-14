# Program Specification: Combined System Development Services for Rates Exemption Information System (REIS)

## Introduction

This document merges information from various sources to provide a comprehensive program specification for the Combined System Development Services of the Rates Exemption Information System (REIS) for the Home Affairs Department (HAD). It includes user requirements, functional and non-functional requirements, technical specifications, and constraints.

## 1. Purpose

This document contains the detailed program specification of all programs used within the implementation of Rates Exemption Information System (REIS) for the HAD.

## 2. Scope

This program specification provides information on the program codes and software modules produced in the Implementation of the REIS.

It covers the following functionalities:

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

## 3. References

| **Reference Document**                        | **Version** |
|-----------------------------------------------|-------------|
| User Requirement Document of REIS for the HAD | v1.0.0      |
| System Specification of REIS for the HAD      | v1.0.0      |
| Process Data Interface                        | v0.1.0      |
| Data Catalogue of REIS for the HAD            | v0.1.0      |
| Physical Data Design of REIS for the HAD      | v0.1.0      |
| Screen Layout                                 | v0.1.0      |

## 4. Definitions and Conventions

### 4.1 Definitions

Nil.

### 4.2 Conventions

#### 1. Validation checking of Data type

To protect data input into the system, validation checking will be performed against input data according to expected data type defined to the field. Only certain range of characters will be accepted by the input function of the system:

| **Data Type**            | **Definition of data filter**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **6** | **<span class="smallcaps">PROGRAM SPECIFICATIONS</span>** |
| --- | --- |

1.  <span class="smallcaps">ACS-001 ? USER LOGIN</span>

| Program ID:   | ACS-001                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode:         | Online                                                                                                                                               |
| Program Name: | User Login                                                                                                                                           |
| Description:  | This program is developed to allow user to input user login information. User authentication is performed based on user login information collected. |

> Program Environment:

| **Program Source**   | **Location**       | **Language / Compiler** |
|----------------------|--------------------|-------------------------|
| login.aspx           | reis\\             | ASP.NET Web Form        |
| login.aspx.vb        | reis\\             | Code Behind VB.NET File |
| UserAccess.vb        | reis\class\ASC\\   | VB.NET Class            |
| RoleDAO.vb           | reis\class\model\\ | DAO VB.NET Class        |
| RolePermissionDAO.vb | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description** |
|-----------------|----------|-----------|-------------|-----------|--------------|
| loginID       | X             | 20                                | \[Alphanumeric]    | Y             | Login ID        |
| password      | X             | 20                                | \[Alphanumeric]    | Y             | Password        |

> Screen Layout:

| 1 - Login |
|-----------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When login button is clicked:</p>
<ul>
<li><p>UserAccess.login() is called with userID and password as
parameters.</p></li>
<li><p>Retrieve user record from REIS_USER, if user record does not
exist or user?s status inactive, error of user account does not exist is
return.</p></li>
<li><p>Encrypt password. password is validated if encrypted passwords
are matched.</p></li>
<li><p>Validate the login ID and password</p></li>
<li><p>If the password is expired, error of invalid password is
return.</p></li>
<li><p>If user password is reset, action ?Change Expired Password? is
triggered.</p></li>
<li><p>If validation success, assign the user role and user access
rights (refer to ACS-007) of the user to session.</p></li>
<li><p>Check user notification of urgent case (refer to
RXA-002).</p></li>
<li><p>The web page of main page is displayed.</p></li>
<li><p>If validation is fail, update REIS_USER.ur_login_fail_count =
ur_login_fail_count + 1.</p></li>
<li><p>Read system parameter for maximum login attempt allowed, if
ur_login_fail_count &gt; parameter, update ur_rec_status to
inactive.</p></li>
</ul>
<p>System menu is displayed based on user right of the user. (refer to
ACS-003)</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">ACS-002 ? USER LOGOUT</span>

| Program ID:   | ACS-002                                                                   |
|---------------|-------------------------------------------------------------------------|
| Mode:         | Online                                                                    |
| Program Name: | User Logout                                                               |
| Description:  | This program is developed to allow current login user to exit the system. |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| UserAccess.vb      | reis\class\ASC\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description** |
|-----------------|----------|-----------|-------------|-----------|--------------|

> Screen Layout:

| 2 - Main page |
|---------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When Logout is clicked:</p>
<ul>
<li><p>UserAccess.logout() is called to invalidate user current
session.</p></li>
<li><p>Redirect to login page.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">ACS-003 ? DISPLAY SYSTEM MENU</span>

| Program ID:   | ACS-003                                                            |
|---------------|--------------------------------------------------------------------|
| Mode:         | Online                                                             |
| Program Name: | Display System menu                                                |
| Description:  | This program is developed to show system menu after user is login. |

> Program Environment:

| **Program Source** | **Location** | **Language / Compiler** |
|--------------------|--------------|-------------------------|
| menu.ascx          | reis\\       | Web User Control        |
| navigation.ascx    | reis\\       | Web User Control        |
| header.ascx        | reis\\       | Web User Control        |
| footer.ascx        | reis\\       | Web User Control        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

| 2 - Main page |
|---------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>Display of System menu:</u></p>
<p>When user is not log in, system menu will not be displayed.</p>
<p>When user is logged in, system menu will be also displayed
(menu.ascx):</p>
<ul>
<li><p>Based on user access permission stored in the current session,
only permitted function will be displayed (refer to ACS-008 for access
rights checking).</p></li>
</ul>
<p><u>Display of Page Navigation (navigation.ascx):</u></p>
<ul>
<li><p>Current web page address is retrieved from HTTP request
header.</p></li>
<li><p>Based on current web page address, navigation links are created
and displayed.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">ACS-004 ? USER ACCOUNT LISTING</span>

| Program ID:   | ACS-004                                                 |
|---------------|---------------------------------------------------------|
| Mode:         | Online                                                  |
| Program Name: | User Account Listing                                    |
| Description:  | This program is developed to show list of user account. |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| userlist.aspx      | reis\\             | ASP.NET Web Form        |
| userlist.aspx.vb   | reis\\             | Code Behind VB.NET File |
| UserAccessMaint.vb | reis\class\ASC\\   | VB.NET Class            |
| UserDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**                                                                                 |
|-----------------|----------|-----------|-------------|-----------|--------------|
| userID        | N/A           | N/A                               | N/A                 | N/A           | User ID of selected record stored in the hidden form field used for record update and deletion. |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>13.1 - User Account Listing,</p>
<p>13.1.2 - User Account Listing (UserAccount-List.htm)</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>Display of User Account Listing:</u></p>
<ul>
<li><p>Retrieve user accounts and their user role name from REIS_USER
and REIS_ROLE.</p></li>
<li><p>Displays list of user ordered by UR_USERID.</p></li>
</ul>
<p><u>When Add User is clicked:</u></p>
<ul>
<li><p>Redirect to create new user account (refer to ACS-005).</p></li>
</ul>
<p><u>When Update of user account is clicked:</u></p>
<ul>
<li><p>Redirect to update user account (refer to ACS-006) with userID as
parameter.</p></li>
</ul>
<p><u>When Delete of user account is clicked:</u></p>
<ul>
<li><p>UserAccessMaint.deleteUser() is called with userID as
parameter.</p></li>
<li><p>UserDAO.inactivated() is called:</p>
<ul>
<li><blockquote>
<p>Update UR_REC_STATUS = I;</p>
</blockquote></li>
</ul></li>
<li><p>Redirect to User Account Listing, the user account records are
reloaded for displaying updated listing.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">ACS-005 ? CREATE NEW USER ACCOUNT</span>

| Program ID:   | ACS-005                                              |
|---------------|------------------------------------------------------|
| Mode:         | Online                                               |
| Program Name: | Create New User Account                              |
| Description:  | This program is developed to create new user account |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| usermaint.aspx     | reis\\             | ASP.NET Web Form        |
| usermaint.aspx.vb  | reis\\             | Code Behind VB.NET File |
| UserAccessMaint.vb | reis\class\ASC\\   | VB.NET Class            |
| UserDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |
| RoleDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 12%" />
<col style="width: 14%" />
<col style="width: 20%" />
<col style="width: 14%" />
<col style="width: 15%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Data Type</strong></th>
<th><strong>Maximum Length of input field</strong></th>
<th><strong>Validation Rule</strong></th>
<th><strong>Mandatory</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>userID</th>
<th>X</th>
<th>20</th>
<th><p>1.[Alphanumeric]</p>
<p>2.userID of new user account should not already exist in the
system.</p></th>
<th>Y</th>
<th></th>
</tr>
<tr class="header">
<th>userName</th>
<th>X</th>
<th>50</th>
<th>[Text]</th>
<th>Y</th>
<th></th>
</tr>
<tr class="odd">
<th>password</th>
<th>X</th>
<th>20</th>
<th>[Alphanumeric]</th>
<th>Y</th>
<th></th>
</tr>
<tr class="header">
<th>confirmPassword</th>
<th>X</th>
<th>20</th>
<th><p>1.[Alphanumeric]</p>
<p>2.password should be matched with password.</p>
<p>3. password of new user should follow password format according to
SYS_PARAM.</p></th>
<th>Y</th>
<th></th>
</tr>
<tr class="odd">
<th>userRole</th>
<th>[Selection: RE_ROLE]</th>
<th>N/A</th>
<th>N/A</th>
<th>Y</th>
<th></th>
</tr>
<tr class="header">
<th>userStatus</th>
<th>[Selection: Action | Inactive]</th>
<th>N/A</th>
<th>N/A</th>
<th>Y</th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 13.1.1 - New User Account (UserAccount-New.htm) |
|-------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When save button is clicked:</u></p>
<ul>
<li><p>Method UserAccessMaint.addUser() is called.</p>
<ul>
<li><blockquote>
<p>Validate the uniqueness of login ID</p>
</blockquote></li>
<li><blockquote>
<p>Check password format.</p>
</blockquote></li>
<li><blockquote>
<p>Encrypt user password.</p>
</blockquote></li>
<li><blockquote>
<p>Call UserDAO.add() for creation of use account.</p>
</blockquote></li>
</ul></li>
<li><p>Redirect to User Account Listing, the user account records are
reloaded for displaying updated listing.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RPT-005 ? RF0005-STATISTICAL REPORT</span>

| Program ID:   | RPT-005                                                                |
|---------------|-------------------------------------------------------------------------|
| Mode:         | Online                                                                 |
| Program Name: | RF0005-Statistical Report                                              |
| Description:  | This program is developed to generate report RF0005-Statistical Report |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| rpt0005.aspx       | reis\\           | ASP.NET Web Form        |
| rpt0005.aspx.vb    | reis\\           | Code Behind VB.NET File |
| RPT0005.vb         | reis\class\RPT\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description** |
|---------------|------------|-----------------|
|               |            |                 |

> Screen Layout:

| 12.7 - RF0005 - Statistical Reports (RF0005-StatisticalReports.htm) |
|---------------------------------------------------------------------|

> Processing Logic:
>
> RF0005A Statistical report on processing time

> RF0005B Statistical report of application? Received

> RF0005C Statistical report of application? Processed

> RF0005D Statistical report of application? Backlog

> RF0005E Statistical report of application? Cancelled

1.  <span class="smallcaps">RPT-006 ? RF0006-EXCEPTION REPORT</span>

| Program ID:   | RPT-006                                                              |
|---------------|-----------------------------------------------------------------------|
| Mode:         | Online                                                               |
| Program Name: | RF0006-Exception Report                                              |
| Description:  | This program is developed to generate report RF0006-Exception Report |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| rpt0006.aspx       | reis\\           | ASP.NET Web Form        |
| rpt0006.aspx.vb    | reis\\           | Code Behind VB.NET File |
| RPT0006.vb         | reis\class\RPT\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> Screen Layout:

| 12.8 - RF0006 - Exception Reports (RF0006-ExceptionReports.htm) |
|-----------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 75%" />
</colgroup>
<thead>
<tr class="header">
<th>Data Source:</th>
<th><p>Rate Exemption Case File</p>
<p>Rate Exemption Case</p>
<p>Applicant/ Grantee</p>
<p>Rate Exemption Case Applicant/ Grantee</p>
<p>Rate Exemption Case Subject Officer</p></th>
</tr>
<tr class="odd">
<th>Orientation:</th>
<th>A4, Landscape</th>
</tr>
<tr class="header">
<th>Searching Criteria :</th>
<th><p>User can specify the following searching criteria:</p>
<p>Application receipt date range or reply date range.</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th>Sort on district code, ?name of subject officer?, application date,
LM No.</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The output is grouped by district code. Within each application
approval status group, it is further grouped by ?name of subject
officer?.</p>
<p>Each district code group will have a district total, and each ?name
of subject officer? group inside a district code group will have an
officer total. At the end of the report, there will have ?totals? which
is the number of records printed out in this report.</p>
<p>Exception records are records which the status cannot be determined.
For an application record, if there are one or more floors which have
non-empty approval status and those non-empty approval status are not
all consistent with each other, then the application approval status is
undetermined, and it is marked as exception.</p>
<p>The records shown in this table only includes records which the
application approval status cannot be determined.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RPT-007 ? RF0007-PERFORMANCE PLEDGE
    REPORT</span>

| Program ID:   | RPT-007                                                                       |
|---------------|-------------------------------------------------------------------------------|
| Mode:         | Online                                                                        |
| Program Name: | RF0007-Performance Pledge Report                                              |
| Description:  | This program is developed to generate report RF0007-Performance Pledge Report |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| rpt0007.aspx       | reis\\           | ASP.NET Web Form        |
| rpt0007.aspx.vb    | reis\\           | Code Behind VB.NET File |
| RPT0007.vb         | reis\class\RPT\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> Screen Layout:

| 12.9 - RF0007 - Performance pledge report (RF0007-PerformancePledgeReport.htm) |
|------------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 75%" />
</colgroup>
<thead>
<tr class="header">
<th>Data Source:</th>
<th><p>Rate Exemption Case File</p>
<p>Rate Exemption Case</p></th>
</tr>
<tr class="odd">
<th>Orientation:</th>
<th>A4, Landscape</th>
</tr>
<tr class="header">
<th>Searching Criteria :</th>
<th><p>User can specify the following searching criteria:</p>
<p>Application receipt range</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th>N/A</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The program will first sort out all applications in rate
exemption case which the receipt date is within the searching
period.</p>
<p>Processing time of each selected application record is counted and
number of month of process more than performance pledge setting are
highlighted.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 7. User Requirements

This section outlines the user requirements for the Self-Certification System (SCS).

### 7.1 Proposed System Overview

The proposed Self-Certification System (SCS) aims to enable Buildings Department (BD) users to efficiently manage applications for certificates and notices required under the Education Ordinance (Cap.279) and the Child Care Services Ordinance (Cap. 243). It also supports building safety comments for Education Bureau applications under NLHPE(R) Rules (Cap.493B). The system will facilitate electronic submissions from applicants, APs, and RSEs, and serve as a centralized repository for all application-related documents.

### 7.2 Functional Requirements

#### 7.2.1 General Requirements

| Req. ID | Requirement Name | Target Users | Priority |
|---|---|---|---|
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
