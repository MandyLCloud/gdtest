**Program Specification**

**of the**

**Combined System Development Services of the**

**Rates Exemption Information System (REIS)**

**for the**

**Home Affairs Department (HAD)**

Version: 1.0.0

**<u>TABLE OF CONTENTS</u>**

**<span class="smallcaps">1</span>** **<span class="smallcaps">PURPOSE
1-1</span>**

**<span class="smallcaps">2</span>** **<span class="smallcaps">SCOPE
3.1-1</span>**

**<span class="smallcaps">3</span>**
**<span class="smallcaps">REFERENCES 3.1-1</span>**

<span class="smallcaps">3.1</span> <span class="smallcaps">References
3.1-1</span>

**<span class="smallcaps">4</span>**
**<span class="smallcaps">DEFINITIONS AND CONVENTIONS 3.1-1</span>**

<span class="smallcaps">4.1</span> <span class="smallcaps">Definitions
4.1-1</span>

<span class="smallcaps">4.2</span> <span class="smallcaps">Conventions
4.2-1</span>

**<span class="smallcaps">5</span>** **<span class="smallcaps">PROGRAM
LIST 4.2-1</span>**

**<span class="smallcaps">6</span>** **<span class="smallcaps">PROGRAM
SPECIFICATIONS 4.2-1</span>**

<span class="smallcaps">6.1</span> <span class="smallcaps">ACS-001 –
User Login 6.1-1</span>

<span class="smallcaps">6.2</span> <span class="smallcaps">ACS-002 –
User Logout 6.2-2</span>

<span class="smallcaps">6.3</span> <span class="smallcaps">ACS-003 –
Display System menu 6.3-3</span>

<span class="smallcaps">6.4</span> <span class="smallcaps">ACS-004 –
User Account Listing 6.4-4</span>

<span class="smallcaps">6.5</span> <span class="smallcaps">ACS-005 –
Create New User Account 6.5-5</span>

<span class="smallcaps">6.6</span> <span class="smallcaps">ACS-006 –
Update User Account 6.6-7</span>

<span class="smallcaps">6.7</span> <span class="smallcaps">ACS-007 –
Update User Role Permission 6.7-9</span>

<span class="smallcaps">6.8</span> <span class="smallcaps">ACS-008 –
Access rights checking 6.8-10</span>

<span class="smallcaps">6.9</span> <span class="smallcaps">ACS-009 –
Change Password 6.9-12</span>

<span class="smallcaps">6.10</span> <span class="smallcaps">RXA-001 –
Display Sumamry List 6.10-14</span>

<span class="smallcaps">6.11</span> <span class="smallcaps">RXA-002 –
Notification of urgent case 6.11-16</span>

<span class="smallcaps">6.12</span> <span class="smallcaps">RXA-003 –
Open of Rates Exemption Application Record 6.12-18</span>

<span class="smallcaps">6.13</span> <span class="smallcaps">RXA-004 –
Create New Rates Exemption Application Record 6.13-19</span>

<span class="smallcaps">6.14</span> <span class="smallcaps">RXA-005 –
Check duplicate case 6.14-21</span>

<span class="smallcaps">6.15</span> <span class="smallcaps">RXA-006 –
Input Rates Exemption Application – A - Applicant 6.15-23</span>

<span class="smallcaps">6.16</span> <span class="smallcaps">RXA-007 –
Input Rates Exemption Application: B - Village House 6.16-25</span>

<span class="smallcaps">6.17</span> <span class="smallcaps">RXA-008 –
Input Rates Exemption Application: C - Application File 6.17-27</span>

<span class="smallcaps">6.18</span> <span class="smallcaps">RXA-009 –
Input Rates Exemption Application: C - Application File, Upload New File
6.18-29</span>

<span class="smallcaps">6.19</span> <span class="smallcaps">RXA-010 –
Input Rates Exemption Application: C - Application File, Open / Delete
File 6.19-30</span>

<span class="smallcaps">6.20</span> <span class="smallcaps">RXA-011 –
Input Rates Exemption Application: D - Application Submission
6.20-32</span>

<span class="smallcaps">6.21</span> <span class="smallcaps">RXA-012 –
Update Rates Exemption Application: E - Application Update
6.21-33</span>

<span class="smallcaps">6.22</span> <span class="smallcaps">RXA-013 –
Update Rates Exemption Application: F - Generate Case Summary
6.22-35</span>

<span class="smallcaps">6.23</span> <span class="smallcaps">RXA-014 –
Update Rates Exemption Application: F - Display Case Summary
6.23-36</span>

<span class="smallcaps">6.24</span> <span class="smallcaps">RXA-015 –
Update Rates Exemption Application: G - Application Status
6.24-37</span>

<span class="smallcaps">6.25</span> <span class="smallcaps">RXA-016 –
Update Rates Exemption Application: G - Application Status, Generate New
Memo / Letter 6.25-38</span>

<span class="smallcaps">6.26</span> <span class="smallcaps">RXA-017 –
Update Rates Exemption Application: G - Application Status, Input
Response 6.26-40</span>

<span class="smallcaps">6.27</span> <span class="smallcaps">RXA-018 –
Update Rates Exemption Application: Save and Submit 6.27-41</span>

<span class="smallcaps">6.28</span> <span class="smallcaps">RXA-019 –
Amend Rates Exemption Application 6.28-42</span>

<span class="smallcaps">6.29</span> <span class="smallcaps">RXA-020 –
Display Endorsement Summary List 6.29-43</span>

<span class="smallcaps">6.30</span> <span class="smallcaps">RXA-021 –
Generate Endorsement Summary 6.30-44</span>

<span class="smallcaps">6.31</span> <span class="smallcaps">RXA-022 –
Endorsement 6.31-45</span>

<span class="smallcaps">6.32</span> <span class="smallcaps">RXA-023 –
Enquiry of Endorsed Records 6.32-46</span>

<span class="smallcaps">6.33</span> <span class="smallcaps">RXA-024 –
Revoke Endorsement 6.33-48</span>

<span class="smallcaps">6.34</span> <span class="smallcaps">RXA-025 –
Display File Minute 6.34-49</span>

<span class="smallcaps">6.35</span> <span class="smallcaps">RXA-026 –
Generate File Minute 6.35-50</span>

<span class="smallcaps">6.36</span> <span class="smallcaps">RXA-027 –
Record Approval 6.36-51</span>

<span class="smallcaps">6.37</span> <span class="smallcaps">RXA-028 –
Enquiry of Confirmed Approval Records 6.37-52</span>

<span class="smallcaps">6.38</span> <span class="smallcaps">RXA-029 –
Revoke Approval 6.38-53</span>

<span class="smallcaps">6.39</span> <span class="smallcaps">RXA-030 –
Batch Letters Generation 6.39-54</span>

<span class="smallcaps">6.40</span> <span class="smallcaps">RXA-031 –
Checking of outstanding case 6.40-55</span>

<span class="smallcaps">6.41</span> <span class="smallcaps">REV-001 –
Display Matching List 6.41-57</span>

<span class="smallcaps">6.42</span> <span class="smallcaps">REV-002 –
Generate New Matching List 6.42-58</span>

<span class="smallcaps">6.43</span> <span class="smallcaps">REV-003 –
Download Matching List 6.43-59</span>

<span class="smallcaps">6.44</span> <span class="smallcaps">REV-004 –
Enquiry Random Check Case 6.44-60</span>

<span class="smallcaps">6.45</span> <span class="smallcaps">REV-005 –
Generate New Random Check Cases 6.45-61</span>

<span class="smallcaps">6.46</span> <span class="smallcaps">REV-006 –
Print Random Check Cases 6.46-63</span>

<span class="smallcaps">6.47</span> <span class="smallcaps">REV-007 –
New Review of Approved Rates Exemption: Search Currently Approved Rates
Exemption 6.47-64</span>

<span class="smallcaps">6.48</span> <span class="smallcaps">REV-008 –
Input Review Record: H - Review of Granted Rates Exemption
6.48-66</span>

<span class="smallcaps">6.49</span> <span class="smallcaps">REV-009 –
Input Review Record: I - Review Status 6.49-67</span>

<span class="smallcaps">6.50</span> <span class="smallcaps">REV-010 –
Input Review Record: I - Input Response 6.50-68</span>

<span class="smallcaps">6.51</span> <span class="smallcaps">REV-011 –
Input Review Record: I - Generate New Memo / letter 6.51-69</span>

<span class="smallcaps">6.52</span> <span class="smallcaps">REV-012 –
Input Review Record: I - Input Random Check Results 6.52-71</span>

<span class="smallcaps">6.53</span> <span class="smallcaps">REV-013 –
Input Review Record: I - Input Matching Check Results 6.53-73</span>

<span class="smallcaps">6.54</span> <span class="smallcaps">REV-014 –
Input Review Record: I - Memo from Other Depts / Confirmation letter
from applicant 6.54-74</span>

<span class="smallcaps">6.55</span> <span class="smallcaps">REV-015 –
Input Review Record: J - Historical Rates Exemption Applications and
Granted Cases 6.55-76</span>

<span class="smallcaps">6.56</span> <span class="smallcaps">REV-016 –
Input Review Record: Save and Submission 6.56-77</span>

<span class="smallcaps">6.57</span> <span class="smallcaps">ENQ-001 –
Rates Exemption Record Enquiry 6.57-78</span>

<span class="smallcaps">6.58</span> <span class="smallcaps">ENQ-002 –
Audit Log Enquiry 6.58-81</span>

<span class="smallcaps">6.59</span> <span class="smallcaps">ENQ-003 –
Ad-hoc Report 6.59-82</span>

<span class="smallcaps">6.60</span> <span class="smallcaps">GEN-001 –
System Parameter 6.60-84</span>

<span class="smallcaps">6.61</span> <span class="smallcaps">GEN-002 –
Type of Breach 6.61-85</span>

<span class="smallcaps">6.62</span> <span class="smallcaps">GEN-003 –
District 6.62-86</span>

<span class="smallcaps">6.63</span> <span class="smallcaps">COM-001 –
Insertion new audit log 6.63-87</span>

<span class="smallcaps">6.64</span> <span class="smallcaps">RPT-001 –
RF0001- Application Listing 6.64-1</span>

<span class="smallcaps">6.65</span> <span class="smallcaps">RPT-002 –
RF0002-Outstanding Case Report 6.65-10</span>

<span class="smallcaps">6.66</span> <span class="smallcaps">RPT-003 –
RF0003-Approved cases/ Rejected cases/ Cancelled cases Report
6.66-16</span>

<span class="smallcaps">6.67</span> <span class="smallcaps">RPT-004 –
RF0004-Monthly Report 6.67-19</span>

<span class="smallcaps">6.68</span> <span class="smallcaps">RPT-005 –
RF0005-Statistical Report 6.68-23</span>

<span class="smallcaps">6.69</span> <span class="smallcaps">RPT-006 –
RF0006-Exception Report 6.69-34</span>

<span class="smallcaps">6.70</span> <span class="smallcaps">RPT-007 –
RF0007-Performance Pledge Report 6.70-36</span>

1.  **<span class="smallcaps">PURPOSE</span>**

> This document contains the detailed program specification of all
> programs used within the implementation of Rates Exemption Information
> System (REIS) for the HAD.

1.  **<span class="smallcaps">SCOPE</span>**

> This program specification provides information on the program codes
> and software modules produced in the Implementation of the REIS.

-   Capture of Rates Exemptions Application

-   Update and amend of Rates Exemption Application

-   Uploading of application file

-   Notification of urgent case of application and review

-   Checking and notification of outstanding case of application and
    > review

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

1.  **<span class="smallcaps">REFERENCES</span>**

1.  <span class="smallcaps">REFERENCES</span>

| **Reference Document**                        | **Version** |
|-----------------------------------------------|-------------|
| User Requirement Document of REIS for the HAD | v1.0.0      |
| System Specification of REIS for the HAD      | v1.0.0      |
| Process Data Interface                        | v0.1.0      |
| Data Catalogue of REIS for the HAD            | v0.1.0      |
| Physical Data Design of REIS for the HAD      | v0.1.0      |
| Screen Layout                                 | v0.1.0      |

1.  **<span class="smallcaps">DEFINITIONS AND CONVENTIONS</span>**

1.  <span class="smallcaps">DEFINITIONS</span>

> Nil.

1.  <span class="smallcaps">CONVENTIONS</span>

<!-- -->

1.  **Validation checking of Data type**

> To protect data input into the system, validation checking will be
> performed against input data according to expected data type defined
> to the field. Only certain range of characters will be accepted by the
> input function of the system:

<table>
<colgroup>
<col style="width: 32%" />
<col style="width: 67%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Data Type</strong></th>
<th><strong>Definition of data filter</strong></th>
</tr>
<tr class="odd">
<th>[Alphanumeric]</th>
<th>Only characters in range [0-9a-zA-Z] are allowed.</th>
</tr>
<tr class="header">
<th>[numeric]</th>
<th>Only characters in range [0-9] are allowed.</th>
</tr>
<tr class="odd">
<th>[Alphabetic]</th>
<th>Only characters in range [a-zA-Z] are allowed.</th>
</tr>
<tr class="header">
<th>[Text]</th>
<th>For input of English / Chinese characters (e.g. address, and
personal name), only Unicode characters are allowed.</th>
</tr>
<tr class="odd">
<th>[Date]</th>
<th>Valid calendar date in dd/mm/yyyy format.</th>
</tr>
<tr class="header">
<th>[DateRangte]</th>
<th><p>Date range with Start date and End date.</p>
<p>Both start date and end date, when not empty, should be a valid
calendar date.</p>
<p>Additionally, when end date is not null:</p>
<ul>
<li><p>start date must not empty; and</p></li>
<li><p>end date must not earlier than start date.</p></li>
</ul></th>
</tr>
<tr class="odd">
<th><p>[,-]</p>
<p>[space]</p></th>
<th><p>Other specific character allow in the field.</p>
<p>For example, [alphanumeric]+[,-]+[space] means only characters in
range [0-9a-zA-Z] and comma (,) and hyphen (-) and space are
allowed.</p></th>
</tr>
<tr class="header">
<th>[Selection: Table]</th>
<th><p>Input data must match item of table.</p>
<p>For example, [Selection: DISTRICT] means only district in the
district table is accepted.</p></th>
</tr>
<tr class="odd">
<th>[Selection: Yes | No]</th>
<th><p>Input data must match item in the option.</p>
<p>For example, [Selection: Yes | No] means only option Yes or No is
accepted.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  **<span class="smallcaps">PROGRAM LIST</span>**

> **User Account Management**

| **Program ID** | **Program Name**        |
|----------------|-------------------------|
| ACS-001        | User Login              |
| ACS-002        | User Logout             |
| ACS-003        | Display System menu     |
| ACS-004        | User Account Listing    |
| ACS-005        | Create New User Account |
| ACS-006        | Update User Account     |
| ACS-007        | Update User Role        |
| ACS-008        | Access rights checking  |
| ACS-009        | Change Password         |

> **Processing Rates Exemption Application**

| **Program ID** | **Program Name**                                                                       |
|--------------------|----------------------------------------------------|
| RXA-001        | Display Summary List                                                                   |
| RXA-002        | Notification of urgent case                                                            |
| RXA-003        | Open of Rates Exemption Application Record                                             |
| RXA-004        | Create New Rates Exemption Application Record                                          |
| RXA-005        | Check duplicate case                                                                   |
| RXA-006        | Input Rates Exemption Application – A - Applicant                                      |
| RXA-007        | Input Rates Exemption Application: B - Village House                                   |
| RXA-008        | Input Rates Exemption Application: C - Application File                                |
| RXA-009        | Input Rates Exemption Application: C - Application File, Upload New File               |
| RXA-010        | Input Rates Exemption Application: C - Application File, Open / Delete File            |
| RXA-011        | Input Rates Exemption Application: D - Application Submission                          |
| RXA-012        | Update Rates Exemption Application: E - Application Update                             |
| RXA-013        | Update Rates Exemption Application: F - Generate Case Summary                          |
| RXA-014        | Update Rates Exemption Application: F - Display Case Summary                           |
| RXA-015        | Update Rates Exemption Application: G - Application Status                             |
| RXA-016        | Update Rates Exemption Application: G - Application Status, Generate New Memo / Letter |
| RXA-017        | Update Rates Exemption Application: G - Application Status, Input Response             |
| RXA-018        | Update Rates Exemption Application: Save and Submit                                    |
| RXA-019        | Amend Rates Exemption Application                                                      |
| RXA-020        | Display Endorsement Summary List                                                       |
| RXA-021        | Generate Endorsement Summary                                                           |
| RXA-022        | Endorsement                                                                            |
| RXA-023        | Enquiry of Endorsed Records                                                            |
| RXA-024        | Revoke Endorsement                                                                     |
| RXA-025        | Display File Minute                                                                    |
| RXA-026        | Generate File Minute                                                                   |
| RXA-027        | Record Approval                                                                        |
| RXA-028        | Enquiry of Confirmed Approval Records                                                  |
| RXA-029        | Revoke Approval                                                                        |
| RXA-030        | Batch Letters Generation                                                               |
| RXA-031        | Checking of outstanding case                                                           |

> **Review and Cancellation of Approved Rates Exemption Cases**

| **Program ID** | **Program Name**                                                                    |
|--------------------|----------------------------------------------------|
| REV-001        | Display Matching List                                                               |
| REV-002        | Generate New Matching List                                                          |
| REV-003        | Download Matching List                                                              |
| REV-004        | Enquiry Random Check Case                                                           |
| REV-005        | Generate New Random Check Cases                                                     |
| REV-006        | Print Random Check Cases                                                            |
| REV-007        | New Review of Approved Rates Exemption: Search Currently Approved Rates Exemption   |
| REV-008        | Input Review Record: H - Review of Granted Rates Exemption                          |
| REV-009        | Input Review Record: I - Review Status                                              |
| REV-010        | Input Review Record: I - Input Response                                             |
| REV-011        | Input Review Record: I - Generate New Memo / letter                                 |
| REV-012        | Input Review Record: I - Input Random Check Results                                 |
| REV-013        | Input Review Record: I - Input Matching Check Results                               |
| REV-014        | Input Review Record: I - Memo from Other Depts / Confirmation letter from applicant |
| REV-015        | Input Review Record: J - Historical Rates Exemption Applications and Granted Cases  |
| REV-016        | Input Review Record: Save and Submission                                            |

> **Record Enquiry and Report Generation**

| **Program ID** | **Program Name**               |
|----------------|--------------------------------|
| ENQ-001        | Rates Exemption Record Enquiry |
| ENQ-002        | Audit Log Enquiry              |
| ENQ-003        | Ad-hoc Report                  |

> **System Administration**

| **Program ID** | **Program Name** |
|----------------|------------------|
| GEN-001        | System Parameter |
| GEN-002        | Type of Breach   |
| GEN-003        | District         |

> **Common Module**

| **Program ID** | **Program Name**        |
|----------------|-------------------------|
| COM-001        | Insertion new audit log |

> **Report**

| **Program ID** | **Program Name**                                              |
|--------------------|----------------------------------------------------|
| RPT-001        | RF0001- Application Listing                                   |
| RPT-002        | RF0002-Outstanding Case Report                                |
| RPT-003        | RF0003-Approved cases/ Rejected cases/ Cancelled cases Report |
| RPT-004        | RF0004-Monthly Report                                         |
| RPT-005        | RF0005-Statistical Report                                     |
| RPT-006        | RF0006-Exception Report                                       |
| RPT-007        | RF0007-Performance Pledge Report                              |

1.  **<span class="smallcaps">PROGRAM SPECIFICATIONS</span>**

1.  <span class="smallcaps">ACS-001 – USER LOGIN</span>

| Program ID:   | ACS-001                                                                                                                                              |
|-------------------|-----------------------------------------------------|
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
| loginID       | X             | 20                                | \[Alphanumeric\]    | Y             | Login ID        |
| password      | X             | 20                                | \[Alphanumeric\]    | Y             | Password        |

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
exist or user’s status inactive, error of user account does not exist is
return.</p></li>
<li><p>Encrypt password. password is validated if encrypted passwords
are matched.</p></li>
<li><p>Validate the login ID and password</p></li>
<li><p>If the password is expired, error of invalid password is
return.</p></li>
<li><p>If user password is reset, action “Change Expired Password” is
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

1.  <span class="smallcaps">ACS-002 – USER LOGOUT</span>

| Program ID:   | ACS-002                                                                   |
|-------------------|-----------------------------------------------------|
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

1.  <span class="smallcaps">ACS-003 – DISPLAY SYSTEM MENU</span>

| Program ID:   | ACS-003                                                            |
|-------------------|-----------------------------------------------------|
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

1.  <span class="smallcaps">ACS-004 – USER ACCOUNT LISTING</span>

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

1.  <span class="smallcaps">ACS-005 – CREATE NEW USER ACCOUNT</span>

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

1.  <span class="smallcaps">RPT-005 – RF0005-STATISTICAL REPORT</span>

| Program ID:   | RPT-005                                                                |
|-------------------|-----------------------------------------------------|
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

<img src="media/image10.png" style="width:5.61111in;height:6.04236in" />

<img src="media/image1.png" style="width:5.88472in;height:2.81597in" />

<img src="media/image5.png" style="width:5.24583in;height:4.31319in" />

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
<p>Reply date range</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th><p>For part A, B and C, it has no sorting.</p>
<p>For part D, it is sorted on LM No.</p></th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The program will first sort out all applications in rate
exemption case which the reply date is within the searching period.</p>
<p>Processing time is counted by the reply date minus by the application
date.</p>
<p>For a case, first check out the range of its processing time,
afterwards,</p>
<p>If the approval status of either one of its floor is “A”, then the
case is approved,</p>
<p>Else if the approval status of either one of its floor is “R”, then
the case is rejected.</p>
<p>Else if the approval status of either one of its floor is “N”, then
the case is no further action.</p>
<p>Part B is Average Processing Time, group by different statuses.</p>
<p>Part C is Average Processing Time (excluding those exceptional cases
which took over one year to be completed), group by different
statuses.</p>
<p>In Part D, only cases which processing time is over one year will be
selected. It is grouped by different application approval status
(approved, rejected or NFA) of cases. Therefore rejected cases, approved
cases and NFA cases are the 3 groups. For each group, the LM No. of
those cases are printed out.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0005B Statistical report of application– Received

<img src="media/image14.png" style="width:9.69444in;height:1.25208in" />

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
<p>Rate Exemption Case Subject Officer</p></th>
</tr>
<tr class="odd">
<th>Orientation:</th>
<th>A4, Landscape</th>
</tr>
<tr class="header">
<th>Searching Criteria :</th>
<th><p>User can specify the following searching criteria:</p>
<p>Application receipt date range</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th>Sort on ‘name of subject officer’</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The output is grouped by ‘name of subject officer’.</p>
<p>The application approval status of the application selected should be
Approved, NFA, Rejected--Others or Rejected—UBW. The cancelled
applications should not be included in the report. The date of
application/reconsideration of the application must be within the
specified period of the user.</p>
<p>Within each ‘name of subject officer’ group, the name (i.e. ‘name of
subject officer’) of the processing officer will be shown and the
counters are used for counting number of records processed by that
officer in each district.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0005C Statistical report of application– Processed

<img src="media/image6.png" style="width:9.69097in;height:1.66111in" />

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
<p>Rate Exemption Subject Officer</p></th>
</tr>
<tr class="odd">
<th>Orientation:</th>
<th>A4, Landscape</th>
</tr>
<tr class="header">
<th>Searching Criteria :</th>
<th><p>User can specify the following searching criteria:</p>
<p>Application receipt date range or reply date range</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th>Sort on application approval status, ‘name of subject officer’</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The output is grouped by application approval status. Within each
application approval status group, it is further grouped by ‘name of
subject officer’.</p>
<p>The application approval status shown in this table includes
Approved, NFA, Rejected—Others and Rejected—UBW. The cancelled
applications should not be included in the table. The reply date of the
applications selected must be non-empty, which means they must not be
outstanding cases.</p>
<p>There are 4 application approval status groups, which are Approved,
NFA, Rejected—Others and Rejected—UBW. Within each ‘name of subject
officer’ group which is inside a application approval status group, the
name (i.e. ‘name of subject officer’) of the processing officer will be
shown and the counters are used for counting number of records processed
by that officer in each district.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0005D Statistical report of application– Backlog

<img src="media/image20.png" style="width:9.68681in;height:1.59931in" />

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
<p>Rate Exemption Case Subject Officer</p></th>
</tr>
<tr class="odd">
<th>Orientation:</th>
<th>A4, Landscape</th>
</tr>
<tr class="header">
<th>Searching Criteria :</th>
<th><p>User can specify the following searching criteria:</p>
<p>Outstanding as at</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th>Sort on ‘name of subject officer’</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The output is grouped by ‘name of subject officer’.</p>
<p>If the date of application/reconsideration of the record is before
the specified input date, and the reply date of the record is either
empty or after the specified input date, then the record satisfy the
searching criteria, and it will be included in the output.</p>
<p>Within each ‘name of subject officer’ group, the name (i.e. ‘name of
subject officer’) of the processing officer will be shown and the
counters are used for counting number of records processed by that
officer in each district.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0005E Statistical report of application– Cancelled

<img src="media/image19.png" style="width:9.68542in;height:1.61667in" />

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
<th>Sort on application approval status, ‘name of subject officer’</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The output is grouped by application approval status. Within each
application approval status group, it is further grouped by ‘name of
subject officer’.</p>
<p>The application approval status shown in this table includes
Cancelled--Others and Cancelled—UBW. Only cancelled applications are
included in the table.</p>
<p>There are 2 application approval status groups, which are
Cancelled--Others and Cancelled—UBW. Within each ‘name of subject
officer’ group which is inside a application approval status group, the
name (i.e. ‘name of subject officer’) of the processing officer will be
shown and the counters are used for counting number of records processed
by that officer in each district.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RPT-006 – RF0006-EXCEPTION REPORT</span>

| Program ID:   | RPT-006                                                              |
|-------------------|-----------------------------------------------------|
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

<img src="media/image7.png" style="width:9.69028in;height:3.37986in" />

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
<th>Sort on district code, ‘name of subject officer’, application date,
LM No.</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The output is grouped by district code. Within each application
approval status group, it is further grouped by ‘name of subject
officer’.</p>
<p>Each district code group will have a district total, and each ‘name
of subject officer’ group inside a district code group will have an
officer total. At the end of the report, there will have ‘totals’ which
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

1.  <span class="smallcaps">RPT-007 – RF0007-PERFORMANCE PLEDGE
    REPORT</span>

| Program ID:   | RPT-007                                                                       |
|-------------------|-----------------------------------------------------|
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
