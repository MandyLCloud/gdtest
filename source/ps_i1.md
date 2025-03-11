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

1.  <span class="smallcaps">ACS-006 – UPDATE USER ACCOUNT</span>

| Program ID:   | ACS-006                                           |
|---------------|---------------------------------------------------|
| Mode:         | Online                                            |
| Program Name: | Update User Account                               |
| Description:  | This program is developed to update user account. |

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
<th>N/A</th>
<th>N/A</th>
<th>N/A</th>
<th></th>
<th>userID is read-only in update mode.</th>
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
<p>2.password should be matched with password</p>
<p>3.password when altered, should follow password format according to
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

| 13.1.3 - User Account Update (UserAccount-Update.htm) |
|-------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Retrieve user account based on parameter userID.</p></li>
<li><p>Display user account information in the page.</p></li>
</ul>
<p><u>When save button is clicked:</u></p>
<ul>
<li><p>Method UserAccessMaint.updateUser() is called.</p>
<ul>
<li><blockquote>
<p>Validate the uniqueness of login ID</p>
</blockquote></li>
<li><blockquote>
<p>Encrypt user password.</p>
</blockquote></li>
<li><blockquote>
<p>If password is altered (i.e. match password &lt;&gt; password stored
in the database), check user password format.</p>
</blockquote></li>
<li><blockquote>
<p>Call UserDAO.update() for updating of use account.</p>
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

1.   <span class="smallcaps">ACS-007 – UPDATE USER ROLE
    PERMISSION</span>

| Program ID:   | ACS-007                                                                                   |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                    |
| Program Name: | Update User Role Permission                                                               |
| Description:  | This program is developed to show list of role and update access permission of user role. |

> Program Environment:

| **Program Source**   | **Location**       | **Language / Compiler** |
|----------------------|--------------------|-------------------------|
| rolemaint.aspx       | reis\\             | ASP.NET Web Form        |
| rolemaint.aspx.vb    | reis\\             | Code Behind VB.NET File |
| UserAccessMaint.vb   | reis\class\ASC\\   | VB.NET Class            |
| RoleDAO.vb           | reis\class\model\\ | DAO VB.NET Class        |
| RolePermissionDAO.vb | reis\class\model\\ | DAO VB.NET Class        |
| FunctionDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter**      | **Data Type**            | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**            |
|-----------------|----------|-----------|---------------|-----------|------------|
| roleID             | \[Selection: REIS_ROLE\] | N/A                               | N/A                 |               | selection of existing role |
| assignedPermission | \[Selection: function\]  |                                   |                     |               | selection of               |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>13.2 - User Role Listing</p>
<p>13.2.1 - User Role Update (UserRole-Update.htm)</p></th>
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
<th><p><u>Display role permission listing when page is opened:</u></p>
<ul>
<li><p>UserAccessMaint.displayRoleMaint() is called.</p></li>
<li><p>(RoleDAO, RolePermissionDAO): Retrieve existing information of
role and corresponding role permission assigned from REIS_ROLE and
REIS_PERMISSION.</p></li>
<li><p>(FunctionDAO): Retrieve all function records for permission
available.</p></li>
</ul>
<p><u>When User role is change:</u></p>
<ul>
<li><p>(rolemaint.aspx.vb): display of role and related role permission
based on selected role.</p></li>
</ul>
<p><u>When Save is clicked:</u></p>
<ul>
<li><p>UserAccessMaint.saveRolePermission() is called.</p></li>
<li><p>(RolePermissionDAO): Update records of permission assigned for
the role to REIS_PERMISSION.</p></li>
<li><p>Redirect to role permission listing, updated records are
displayed.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">ACS-008 – ACCESS RIGHTS CHECKING</span>

| Program ID:   | ACS-008                                                                                         |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                          |
| Program Name: | Access rights checking                                                                          |
| Description:  | This program is developed to perform access control whenever user attempt to access a function. |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| UserAccess.vb      | reis\class\ASC\\ | VB.NET Class            |
| UserAccessMaint.vb | reis\class\ASC\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter**       | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**                                   |
|-----------------|----------|-----------|---------------|-----------|------------|
| requestedFunctionID | X             | 10                                | N/A                 | Y             | Function ID provided from function access request |

> Screen Layout:

| N/A |
|-----|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When login is success:</u></p>
<ul>
<li><p>UserAccessMaint.getUserAccessPermission() is called:</p>
<ul>
<li><blockquote>
<p>based on roleID of login user, collect role access permission from
REIS_PERMISSION.</p>
</blockquote></li>
<li><blockquote>
<p>Created a string array permittedFunction which contain all function
ID permitted by the role.</p>
</blockquote></li>
<li><blockquote>
<p>user role (session variable userRole), permittedFunction (session
variable permittedFunc) are set into current session.</p>
</blockquote></li>
</ul></li>
</ul>
<p><u>When request of access a function is received:</u></p>
<ul>
<li><p>UserAccessMaint.checkAccess () with parameters user session,
requestedFunctionID is called:</p>
<ul>
<li><blockquote>
<p>Return false if requestedFunctionID not contain in permittedFunc of
the session. Otherwise true is return.</p>
</blockquote></li>
<li><blockquote>
<p>If false is return, error message for user does not have access right
granted for the function is displayed. Access of the function will be
denied.</p>
</blockquote></li>
</ul></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">ACS-009 – CHANGE PASSWORD</span>

| Program ID:   | ACS-009                                                                |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                 |
| Program Name: | Change Password                                                        |
| Description:  | This program is developed to allow users to change their own password. |

> Program Environment:

| **Program Source**  | **Location**       | **Language / Compiler** |
|---------------------|--------------------|-------------------------|
| chgpassword.aspx    | reis\\             | ASP.NET Web Form        |
| chgpassword.aspx.vb | reis\\             | Code Behind VB.NET File |
| UserAccess.vb       | reis\class\ASC\\   | VB.NET Class            |
| UserDAO.vb          | reis\class\model\\ | DAO VB.NET Class        |

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
<th>oldpassword</th>
<th>X</th>
<th>20</th>
<th><p>1.[alphanumeric],</p>
<p>2.oldpassword should be correct.</p></th>
<th>Y</th>
<th>Old Password</th>
</tr>
<tr class="header">
<th>newPassword</th>
<th>X</th>
<th>20</th>
<th><p>1.[alphanumeric],</p>
<p>2.newPassword should be follow password based on SYS_PARAM</p></th>
<th>Y</th>
<th>New Password</th>
</tr>
<tr class="odd">
<th>newPasswordR</th>
<th>X</th>
<th>20</th>
<th><p>1.[alphanumeric],</p>
<p>2.newPassowrdR should match with newPassword.</p></th>
<th>Y</th>
<th>Confirm New Password</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:
>
> <img src="media/image17.png" style="width:6.00139in;height:3.44931in" />
>
> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When Save is clicked:</u></p>
<ul>
<li><p>UserAccess.changePasswordCheck() is called:</p>
<ul>
<li><blockquote>
<p>User old password is checked (refer to ACS-001 – user login for user
identification and user password checking).</p>
</blockquote></li>
<li><blockquote>
<p>When new password and confirm new password is validated, save user
new password by calling UserDAO.changePassword().</p>
</blockquote></li>
<li><blockquote>
<p>UserDAO.changePassword():</p>
</blockquote>
<ul>
<li><blockquote>
<p>Encrypt new password.</p>
</blockquote></li>
<li><blockquote>
<p>Update REIS_USER.UR_PASSWORD with encrypted password.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Redirect to user main page (RXA-001).</p>
</blockquote></li>
</ul></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-001 – DISPLAY SUMAMRY LIST</span>

| Program ID:   | RXA-001                                                               |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                |
| Program Name: | Display Sumamry List                                                  |
| Description:  | This program is developed to show summary list in the user main page. |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| main.aspx          | reis\\             | ASP.NET Web Form        |
| main.aspx.vb       | reis\\             | Code Behind VB.NET File |
| AppSummary.vb      | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb  | reis\class\model\\ | DAO VB.NET Class        |
| RevSummary.vb      | reis\class\REV\\   | VB.NET Class            |
| ReviewDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |
| UrgSummary.vb      | reis\class\RXA\\   | VB.NET Class            |
| UrgentCaseDAO.vb   | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**                     |
|-----------------|----------|-----------|---------------|-----------|------------|
| listName      | N/A           | N/A                               | N/A                 | Y             | Summary list name selected by user. |
| pageNo        | N/A           | N/A                               | N/A                 | Y             | Page number requested.              |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>2 - Main page</p>
<p>2.1 - Rates Exemption Application</p>
<p>2.2 - Approved Rates Exemption Case Review</p>
<p>2.3 - Urgent Case(Application)</p>
<p>2.4 - Urgent Case(Review</p></th>
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
<th><p>The summary page should be implemented as default page (and as
address of “Home” of the navigation bar) after user is successfully
login.</p>
<p><u>When page is loaded:</u></p>
<ul>
<li><p>AppSummary.getSummaryList() with pageNo = 1 is called:</p>
<ul>
<li><blockquote>
<p>Retrieve Application records (RXA_APPL) assigned to where</p>
</blockquote>
<ul>
<li><blockquote>
<p>Record status is active,</p>
</blockquote></li>
<li><blockquote>
<p>Application status is not completed (i.e. not (17) Result letter by
RxS and not (18) NFA);</p>
</blockquote></li>
<li><blockquote>
<p>Range of record no based on page no.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Retrieve Rates Exemption File (RX_FILE) of related application
where</p>
</blockquote>
<ul>
<li><blockquote>
<p>Record status is active.</p>
</blockquote></li>
</ul></li>
</ul></li>
</ul>
<p><u>When Rates Exemption Application tab is clicked:</u></p>
<p>Refer to “When page is loaded” with pageNo based on current user
selection.</p>
<p><u>When Approved Rates Exemption Case Review tab is clicked:</u></p>
<ul>
<li><p>RevSummary.getSummaryList() with pageNo = 1 is called:</p>
<ul>
<li><blockquote>
<p>Review records (RXV_CASE) assigned to where</p>
</blockquote>
<ul>
<li><blockquote>
<p>Record status is active,</p>
</blockquote></li>
<li><blockquote>
<p>Application status is not completed (i.e. not (17) Result letter by
RxS and not (18) NFA);</p>
</blockquote></li>
<li><blockquote>
<p>record no based on page no.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Retrieve Rates Exemption File (RX_FILE) of related application
where</p>
</blockquote>
<ul>
<li><blockquote>
<p>Record status is active.</p>
</blockquote></li>
</ul></li>
</ul></li>
</ul>
<p><u>When Urgent Case (Application) tab is clicked:</u></p>
<ul>
<li><p>Refer to selection criteria of Rates Exemption Application tab
with addition selection criteria:</p>
<ul>
<li><blockquote>
<p>Join with urgent case records (URGENT_CASE) on URG_TYPE = “A” and
URG_FILENO = RX_FILE.RX_FILENO and record status is active;</p>
</blockquote></li>
</ul></li>
</ul>
<p><u>When Urgent Case (Review) tab is clicked:</u></p>
<ul>
<li><p>Refer to selection criteria of Approved Rates Exemption Case
Review tab with addition selection criteria:</p>
<ul>
<li><blockquote>
<p>Join with urgent case records (URGENT_CASE) on URG_TYPE = “R” and
URG_FILENO = RX_FILE.RX_FILENO and record status is active;</p>
</blockquote></li>
</ul></li>
</ul>
<p><u>main.aspx.vb:</u></p>
<ul>
<li><p>Display summary listing based on records retrieved.</p></li>
<li><p>Display no. of total records of all searching results next to the
tab title.</p></li>
<li><p>Generate page number navigation based on total records of all
searching results and maximum no. of record to be displayed stored in
the SYS_PARAM.</p></li>
</ul>
<p><u>When hyperlink open of specific record is clicked:</u></p>
<ul>
<li><p>Call open record function (refer to RXA-003 and
REV-008).</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-002 – NOTIFICATION OF URGENT CASE</span>

| Program ID:   | RXA-002                                                        |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                         |
| Program Name: | Notification of urgent case                                    |
| Description:  | This program is developed to show notification of urgent case. |

> Program Environment:

| **Program Source**    | **Location**       | **Language / Compiler** |
|-----------------------|--------------------|-------------------------|
| notifypopup.aspx      | reis\\             | ASP.NET Web Form        |
| notifypopup.aspx.vb   | reis\\             | Code Behind VB.NET File |
| UrgentNotification.vb | reis\class\RXA\\   | VB.NET Class            |
| UrgentCaseDAO.vb      | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**                                         |
|-----------------|----------|-----------|---------------|-----------|------------|
| userID        | N/A           | N/A                               | N/A                 | N/A           | User ID of login user internally stored in the session. |

> Screen Layout:
>
> <img src="media/image8.png" style="width:3.33333in;height:2.22222in" />
>
> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When user is login successfully:</u></p>
<ul>
<li><p>UrgentNotification.createNotificationList(): All urgent cases
assigned to user are retrieved and stored in session variable
urgCases:</p>
<ul>
<li><blockquote>
<p>(UrgentCaseDAO) Retrieve urgent case records where:</p>
</blockquote>
<ul>
<li><blockquote>
<p>notification status = Y; and</p>
</blockquote></li>
<li><blockquote>
<p>record status is active;</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Join with Application (RXA_APPL) on</p>
</blockquote>
<ul>
<li><blockquote>
<p>URG_TYPE = A; and</p>
</blockquote></li>
<li><blockquote>
<p>URG_FILENO = RXA_FILENO; and</p>
</blockquote></li>
<li><blockquote>
<p>RXA_OFFICER_USERID = current user ID collected from the session.</p>
</blockquote></li>
<li><blockquote>
<p>record status is active;</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Join with Reveiw (RXV_CASE) on</p>
</blockquote>
<ul>
<li><blockquote>
<p>URG_TYPE = R; and</p>
</blockquote></li>
<li><blockquote>
<p>URG_FILENO = REV_FILENO; and</p>
</blockquote></li>
<li><blockquote>
<p>REV_OFFICER_USERID = current user ID collected from the session.</p>
</blockquote></li>
<li><blockquote>
<p>record status is active;</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Sorting order = LM No.</p>
</blockquote></li>
</ul></li>
</ul>
<p><u>When user is access any function (notifypopup.aspx):</u></p>
<ul>
<li><p>urgCase is collected from the session.</p></li>
<li><p>If urgCase is null, re-created urgCase.</p></li>
<li><p>If urgCase is not null and urgCase is empty, pop-up window will
not be created. Otherwise, display notification in pop-up window (window
name = notifyWin, status bar, menu bar are disabled, scroll bar is
enabled)</p></li>
</ul>
<p><u>When LM No in the notification pop-up window is clicked:</u></p>
<p>Open corresponding record (application / review) in the main windows.
(Refer to RXA-003and REV-008)</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-003 – OPEN OF RATES EXEMPTION
    APPLICATION RECORD</span>

| Program ID:   | RXA-003                                                               |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                |
| Program Name: | Open of Rates Exemption Application Record                            |
| Description:  | This program is developed to open rates exemption application record. |

> Program Environment:

| **Program Source**  | **Location**       | **Language / Compiler** |
|---------------------|--------------------|-------------------------|
| application.aspx    | reis\\             | ASP.NET Web Form        |
| application.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb          | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb   | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**                              |
|-----------------|----------|-----------|---------------|-----------|------------|
| appID         | N/A           | N/A                               | N/A                 | N/A           | Application ID password from other function. |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.3 - Application Case (oldvth-ApplicationCase.htm)</p>
<p>3.2.2 - Application case (newvth-ApplicationCase.htm)</p></th>
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
<th><p>When page is loaded:</p>
<p>Retrieved application record based on appID:</p>
<table>
<colgroup>
<col style="width: 27%" />
<col style="width: 72%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Major table</strong></th>
<th><strong>Application information</strong></th>
</tr>
<tr class="odd">
<th>RX_FILE</th>
<th>Village House</th>
</tr>
<tr class="header">
<th>RXA_APPL</th>
<th>Application Case information,<br />
Application Submission</th>
</tr>
<tr class="odd">
<th>RXA_AG</th>
<th>Applicant information</th>
</tr>
<tr class="header">
<th>RXA_FLOOR</th>
<th>Village House - Floor(s),<br />
Application Update: update information of floor(s).</th>
</tr>
<tr class="odd">
<th>RXA_DOC</th>
<th>Application File - Supplement Document</th>
</tr>
<tr class="header">
<th>RXA_MIS_INFO</th>
<th>Application File - Missing Information in the Application Form</th>
</tr>
<tr class="odd">
<th>RXA_FILE</th>
<th>Application File - Uploaded File</th>
</tr>
<tr class="header">
<th>RXA_UBW</th>
<th>Application Update: Reason Code (CRV), Reason (DLO)</th>
</tr>
<tr class="odd">
<th>RXA_PENDING</th>
<th>Application Status</th>
</tr>
<tr class="header">
<th>APR_CASE</th>
<th>Case Summary - Approved Case</th>
</tr>
<tr class="odd">
<th>CAN_CASE</th>
<th>Case summary: Cancelled Case</th>
</tr>
<tr class="header">
<th>REJ_CASE</th>
<th>Case summary: Rejected Case</th>
</tr>
</thead>
<tbody>
</tbody>
</table></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-004 – CREATE NEW RATES EXEMPTION
    APPLICATION RECORD</span>

| Program ID:   | RXA-004                                                                     |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                      |
| Program Name: | Create New Rates Exemption Application Record                               |
| Description:  | This program is developed to create new rates exemption application record. |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| appNewStart.aspx   | reis\\             | ASP.NET Web Form        |
| appNew.aspx        | reis\\             | ASP.NET Web Form        |
| appNew.aspx.vb     | reis\\             | Code Behind VB.NET File |
| AppForm.vb         | reis\class\RXA\\   | VB.NET Class            |
| RXFileDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |
| ApplicationDAO.vb  | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:
>
> appNewStart.aspx

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
<th>appType</th>
<th>X</th>
<th>1</th>
<th><p>O - Old VTH</p>
<p>N - New VTH</p></th>
<th>Y</th>
<th>Type of application to be created.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> appNew.aspx (Old VTH & New VTH)

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
<th>hkid_id</th>
<th>X</th>
<th>8</th>
<th>[alphanumeric]</th>
<th>Y</th>
<th>HKID: Identifier</th>
</tr>
<tr class="header">
<th>hkid_cd</th>
<th>X</th>
<th>1</th>
<th>[alphanumeric]</th>
<th>Y</th>
<th>HKID: Check digit</th>
</tr>
<tr class="odd">
<th>sureNameEn</th>
<th>X</th>
<th>50</th>
<th>[text]</th>
<th>Y</th>
<th>Name : Surname (English)</th>
</tr>
<tr class="header">
<th>givenNameEn</th>
<th>X</th>
<th>50</th>
<th>[text]</th>
<th>Y</th>
<th>Name : Given name (English)</th>
</tr>
<tr class="odd">
<th>sureNameCn</th>
<th>X</th>
<th>20</th>
<th>[text]</th>
<th>Y</th>
<th>Name : Surname (Chinese)</th>
</tr>
<tr class="header">
<th>givenNameCn</th>
<th>X</th>
<th>20</th>
<th>[text]</th>
<th>Y</th>
<th>Name : Given name (Chinese)</th>
</tr>
<tr class="odd">
<th>sex</th>
<th>X</th>
<th>1</th>
<th><p>M –Male;</p>
<p>F-Female</p></th>
<th>Y</th>
<th>Sex</th>
</tr>
<tr class="header">
<th>lmNo</th>
<th>9</th>
<th>8,0</th>
<th>[numeric]</th>
<th>Y</th>
<th>LM No.</th>
</tr>
<tr class="odd">
<th>dd</th>
<th>X</th>
<th>20</th>
<th>[alphanumeric]</th>
<th></th>
<th>DD</th>
</tr>
<tr class="header">
<th>lotno</th>
<th>X</th>
<th>20</th>
<th>[alphanumeric]</th>
<th></th>
<th>Lot</th>
</tr>
<tr class="odd">
<th>dist</th>
<th>[Selection:DISTRICT]</th>
<th>N/A</th>
<th>N/A</th>
<th>Y</th>
<th>District code</th>
</tr>
<tr class="header">
<th>stt</th>
<th>X</th>
<th>20</th>
<th>[alphanumeric]</th>
<th></th>
<th>STT</th>
</tr>
<tr class="odd">
<th>cll</th>
<th>X</th>
<th>20</th>
<th>[alphanumeric]</th>
<th></th>
<th>CLL</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> appNew.aspx (New VTH only)

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**                           |
|-----------------|----------|-----------|---------------|-----------|------------|
| ceIssueDate   | Date          | N/A                               | \[Date\]            |               | Date of acknowledge letter issued by DLO: |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.1 - Input Old VTH Applicants (oldvth.htm)</p>
<p>3.2.1 - Input New VTH Applicants (newvth.htm)</p></th>
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
<th><p><u>When Add button is clicked:</u></p>
<ul>
<li><p>Validation check of Applicant(s) data input.</p></li>
<li><p>display one more row of applicant for user input</p></li>
</ul>
<p><u>When Delete button is clicked:</u></p>
<ul>
<li><p>If no checkbox is selected, display error message.</p></li>
<li><p>remove select row(s) of applicant</p></li>
</ul>
<p><u>When Next button is clicked:</u></p>
<ul>
<li><p>Collect application file information to perform duplication check
(refer to RXA-005).</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-005 – CHECK DUPLICATE CASE</span>

| Program ID:   | RXA-005                                                                                                                                   |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                                                    |
| Program Name: | Check duplicate case                                                                                                                      |
| Description:  | This program is developed to capture address and applicant information from the application and check if duplicated record already exist. |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| appDupList.aspx    | reis\\             | ASP.NET Web Form        |
| appDupList.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb         | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb  | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters (pass from RXA-004):

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**             |
|-----------------|----------|-----------|---------------|-----------|------------|
| hkid_id       | N/A           | N/A                               | N/A                 | N/A           | HKID: Identifier            |
| hkid_cd       | N/A           | N/A                               | N/A                 | N/A           | HKID: Check digit           |
| sureNameEn    | N/A           | N/A                               | N/A                 | N/A           | Name : Surname (English)    |
| givenNameEn   | N/A           | N/A                               | N/A                 | N/A           | Name : Given name (English) |
| sureNameCn    | N/A           | N/A                               | N/A                 | N/A           | Name : Surname (Chinese)    |
| givenNameCn   | N/A           | N/A                               | N/A                 | N/A           | Name : Given name (Chinese) |
| sex           | N/A           | N/A                               | N/A                 | N/A           | Sex                         |
| lmNo          | N/A           | N/A                               | N/A                 | N/A           | LM No.                      |
| dd            | N/A           | N/A                               | N/A                 | N/A           | DD                          |
| lotno         | N/A           | N/A                               | N/A                 | N/A           | Lot                         |
| dist          | N/A           | N/A                               | N/A                 | N/A           | District code               |
| stt           | N/A           | N/A                               | N/A                 | N/A           | STT                         |
| cll           | N/A           | N/A                               | N/A                 | N/A           | CLL                         |

> Screen Layout:

| 3.1.2 - Application Case Listing (oldvth-ApplicationCasesListing.htm) |
|-----------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Duplication File checking:</p>
<p>(1)Duplicated Address</p>
<p>Search for records of Rates exemption file (RX_FILE) with same lmNo
(RX_LMNO):</p>
<p>Join with application record (RXA_APPL) on same FileID</p>
<p>(2) Duplicated applicant</p>
<p>Any applicant in the list of applicant(s) are checked:</p>
<p>Search for records of Application Applicant / Grantee (RXA_AG inner
join with RXA_AG with same PERSON_ID)</p>
<p>Join with Application (RXA_APPL) on same APPID.</p>
<p>Jon with Rates exemption file (RX_FILE) on same FILEID.</p>
<p>Exclude file found in (1) (i.e. both address and applicants is
duplicated already searched in (1) ).</p>
<p>When record is searched in (1) and (2), display list of duplicated
record.</p>
<p>If application is not duplicated, create new RX_FILE, RXA_AG and
RXA_APPL record and redirect to RXA-006.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-006 – INPUT RATES EXEMPTION APPLICATION
    – A - APPLICANT</span>

| Program ID:   | RXA-006                                                                                       |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                        |
| Program Name: | Input Rates Exemption Application – A - Applicant                                             |
| Description:  | This program is developed to capture of rates exemption application information A - Applicant |

> Program Environment:

| **Program Source**        | **Location**       | **Language / Compiler** |
|---------------------------|--------------------|-------------------------|
| appMaintApplicant.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintApplicant.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb                | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:
>
> (For both Old VTH and New VTH)

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
<th>comAddrEn (1..5)</th>
<th>X</th>
<th>40</th>
<th><p>1.[Text]+[/,.-]</p>
<p>2.Either English or Chinese address must be entered</p></th>
<th>See Validation rule</th>
<th>Communication address (line 1 to line 5) English</th>
</tr>
<tr class="header">
<th>comAddrCn (1..5)</th>
<th>X</th>
<th>40</th>
<th>[Text]+[/,.-]</th>
<th>See Validation rule</th>
<th>Communication address (line 1 to line 5) English</th>
</tr>
<tr class="odd">
<th>phone1</th>
<th>X</th>
<th>20</th>
<th>[alphanumeric]</th>
<th>Y</th>
<th>day time phone 1</th>
</tr>
<tr class="header">
<th>phone2</th>
<th>X</th>
<th>20</th>
<th>[alphanumeric]</th>
<th></th>
<th>day time phone 2</th>
</tr>
<tr class="odd">
<th>isOwner</th>
<th>[Selection Y | N]</th>
<th>N/A</th>
<th>N/A</th>
<th>Y</th>
<th>Is applicant owner of the village house</th>
</tr>
<tr class="header">
<th>isIndigenous</th>
<th>[Selection Y | N]</th>
<th>N/A</th>
<th>N/A</th>
<th>Y</th>
<th>Indigenous status</th>
</tr>
<tr class="odd">
<th>relationship</th>
<th>[Selection RXA_RELATE]</th>
<th>N/A</th>
<th>Mandatory when isIndigenous = N</th>
<th>See validation rule</th>
<th>Relationship between applicant and person who have indigenous
status</th>
</tr>
<tr class="header">
<th>otherRelation</th>
<th>X</th>
<th>20</th>
<th><p>[Text]</p>
<p>Mandatory when relationship = other</p></th>
<th>See validation rule</th>
<th>Other relationship.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 3.1.3.1 - A – Applicant(s) |
|----------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When Change button of Applicant is clicked, redirect to input
applicant page (RXA-004).</p>
<p>When save the record:</p>
<p>Validation checking of application form.</p>
<p>Update applicant information in RXA_AG.</p>
<p>Update other information in RXA_APPL.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-007 – INPUT RATES EXEMPTION APPLICATION:
    B - VILLAGE HOUSE</span>

| Program ID:   | RXA-007                                                                                           |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                            |
| Program Name: | Input Rates Exemption Application: B - Village House                                              |
| Description:  | This program is developed to capture of rates exemption application information B - Village House |

> Program Environment:

| **Program Source**           | **Location**       | **Language / Compiler** |
|-----------------------------|-------------------|-------------------------|
| appMaintVillageHouse.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintVillageHouse.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb                   | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb            | reis\class\model\\ | DAO VB.NET Class        |
| ApplicationFloorDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:
>
> (For both Old VTH and New VTH)

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
<th>AddrEn (1..5)</th>
<th>X</th>
<th>40</th>
<th><p>1.[Text]+[/,.-]</p>
<p>2.Either English or Chinese address must be entered</p></th>
<th>See Validation rule</th>
<th>Address (line 1 to line 5) English</th>
</tr>
<tr class="header">
<th>AddrCn (1..5)</th>
<th>X</th>
<th>40</th>
<th>[Text]+[/,.-]</th>
<th>See Validation rule</th>
<th>Address (line 1 to line 5) English</th>
</tr>
<tr class="odd">
<th>floor</th>
<th>See program logic</th>
<th>N/A</th>
<th>Selected floor does not duplicate with other row.</th>
<th>Y</th>
<th>day time phone 1</th>
</tr>
<tr class="header">
<th>isApply</th>
<th>[Selection Y | N]</th>
<th>N/A</th>
<th></th>
<th>Y</th>
<th>day time phone 2</th>
</tr>
<tr class="odd">
<th>purpose</th>
<th>[Selection RAF_ FORM_PURPOSE]</th>
<th>N/A</th>
<th><p>Purpose:</p>
<p>1 - Self Residential</p>
<p>2 - Rental</p>
<p>3 - Other</p>
<p>N - N/A. will be automatic selected if isApply = N</p></th>
<th>Y</th>
<th>Is applicant owner of the village house</th>
</tr>
<tr class="header">
<th>otherPurpose</th>
<th>X</th>
<th>300</th>
<th><p>[Text]</p>
<p>Mandatory when purpose = other.</p></th>
<th>See validation rule</th>
<th>Indigenous status</th>
</tr>
<tr class="odd">
<th>startDate</th>
<th>[Selection]</th>
<th>N/A</th>
<th>[DateRange]</th>
<th></th>
<th>Start Date</th>
</tr>
<tr class="header">
<th>endDate</th>
<th>X</th>
<th>20</th>
<th><p>[DateRange]</p>
<p>When endDate is not empty, isNow should not be selected.</p></th>
<th></th>
<th>End Date</th>
</tr>
<tr class="odd">
<th>isNow</th>
<th></th>
<th></th>
<th>When selected, endDate will be automatically clear.</th>
<th></th>
<th>Now</th>
</tr>
<tr class="header">
<th>isUnit</th>
<th>[Selection Y | N]</th>
<th></th>
<th></th>
<th></th>
<th><p>Independent</p>
<p>unit?</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> (For New VTH Only)

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**               |
|-----------------|----------|-----------|---------------|-----------|------------|
| ccDate        | Date          | N/A                               | \[Date\]            |               | Application Date of CC / NOTO |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.3.2 - B – Village House</p>
<p>3.2.2.2 - B – Village House</p></th>
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
<th><p>When Change button of Applicant is clicked, redirect to input
applicant page (RXA-004).</p>
<p><u>Selection of Floor:</u></p>
<ul>
<li><p>Retrieve maximum floor no. from SYS_PARAM.</p></li>
<li><p>Options of selection = G/F + (1/F .. Maximum Floor No) +
Roof</p></li>
</ul>
<p><u>When save the record:</u></p>
<ul>
<li><p>Validation checking of application form.</p></li>
<li><p>Update Address information in RX_FILE.</p></li>
<li><p>Update Floor information in RXA_AF.</p></li>
<li><p>Update other application information in RXA_APPL.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-008 – INPUT RATES EXEMPTION APPLICATION:
    C - APPLICATION FILE</span>

| Program ID:   | RXA-008                                                                                              |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                               |
| Program Name: | Input Rates Exemption Application: C - Application File                                              |
| Description:  | This program is developed to capture of rates exemption application information C - Application File |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| appMaintAppFile.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintAppFile.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb              | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |

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
<th>supDoc</th>
<th>[Selection: Submitted | Not Submitted | N/A]</th>
<th>N/A</th>
<th><p>Submission of document:</p>
<p>0 - Submitted</p>
<p>1 - Not Submitted</p>
<p>2 - Not Required</p></th>
<th>Y</th>
<th>Supplement Documents</th>
</tr>
<tr class="header">
<th>misInfo</th>
<th>[Selection Y | N]</th>
<th></th>
<th><p>Is Missing:</p>
<p>Y - Yes;</p>
<p>N - No.</p></th>
<th>Y</th>
<th>Missing Information in the Application Form</th>
</tr>
<tr class="odd">
<th>isReturn</th>
<th>[Selection Y | N]</th>
<th></th>
<th><p>Is Application form return:</p>
<p>Y - Yes;</p>
<p>N - No.</p></th>
<th>Y</th>
<th>Application Fom is returned?</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.3.3 - C – Application File</p>
<p>3.2.2.3 - C – Application File</p></th>
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
<th><p><u>Selection of supplement documents:</u></p>
<ul>
<li><p>Retrieve type of supplement documents from DOC_PARAM where
application type (old VTH (O) or New VTH (N)) = SDP_APP_TYPE.</p></li>
</ul>
<p><u>Selection of missing information:</u></p>
<ul>
<li><p>Retrieve type of missing information from MIS_INFO_PARAM where
application type (old VTH (O) or New VTH (N)) = MIP_APP_TYPE.</p></li>
</ul>
<p><u>When save the record:</u></p>
<ul>
<li><p>Validation checking of application form.</p></li>
<li><p>Update Supplement document information in RXA_DOC.</p></li>
<li><p>Update missing information in RXA_MIS_INFO.</p></li>
<li><p>Update other application information in RXA_APPL.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-009 – INPUT RATES EXEMPTION APPLICATION:
    C - APPLICATION FILE, UPLOAD NEW FILE</span>

| Program ID:   | RXA-009                                                                                                               |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                                |
| Program Name: | Input Rates Exemption Application: C - Application File, Upload New File                                              |
| Description:  | This program is developed to capture of rates exemption application information C - Application File, Upload New File |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| appMaintAppFile.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintAppFile.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb              | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule**                                             | **Mandatory** | **Description**      |
|-----------------|----------|-----------|---------------|-----------|------------|
| filename      | X             | 100                               | File size not over maximum file size allow defined in SYS_PARAM | Y             | Supplement Documents |
| fileDesc      | X             | 100                               | \[Text\]                                                        | Y             | File description     |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.3.3 - C – Application File</p>
<p>3.2.2.3 - C – Application File</p></th>
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
<th><p>On clicking “Upload New File” button, the “Add New File” page
will be displayed in the new window.</p>
<p><u>When upload button in the upload file window is clicked:</u></p>
<ul>
<li><p>The file name is retrieved. It should check if file with same
file name already exist for the same web content in the storage. It
should return exception for alert user same file already existed for the
web content.</p></li>
<li><p>The file format should be determined by file extension
name</p></li>
<li><p>The new RXA_FILE record is record is created.</p></li>
<li><p>After new record is saved, upload the file into the storage
location defined by the system parameter.</p></li>
<li><p>For any exception, return the error message and display in the
Add file window.</p></li>
<li><p>After file upload is success, return to the main window and
display update file attachment listing.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-010 – INPUT RATES EXEMPTION APPLICATION:
    C - APPLICATION FILE, OPEN / DELETE FILE</span>

| Program ID:   | RXA-010                                                                                                                  |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                                   |
| Program Name: | Input Rates Exemption Application: C - Application File, Open / Delete File                                              |
| Description:  | This program is developed to capture of rates exemption application information C - Application File, Open / Delete File |

> Program Environment:

| **Program Source**    | **Location**       | **Language / Compiler** |
|-----------------------|--------------------|-------------------------|
| viewer.aspx           | reis\\             | ASP.NET Web Form        |
| viewer.aspx.vb        | reis\\             | Code Behind VB.NET File |
| UploadFile.vb         | reis\class\RXA\\   | VB.NET Class            |
| ApplicationFileDAO.vb | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type** | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**                              |
|-----------------|----------|-----------|---------------|-----------|------------|
| fileName      | X             | 100                               |                     |               | File to be opened/deleted specified by user. |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.3.3 - C – Application File</p>
<p>3.2.2.3 - C – Application File</p></th>
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
<th><p><u>When Delete button is clicked:</u></p>
<p>User confirmation dialog box will be displayed. Input form will be
submitted when user confirmation is acquired.</p>
<p>UploadFile.deleteFile() is called to search for file physical
location from RXA_FILE. When record is searched, file is deleted based
on the file address.</p>
<p>Update RXA_FILE set REC_STATUS as inactive.</p>
<p><u>When Open button is clicked:</u></p>
<p>UploadFile.openFile() is called to search for file physical location
from RXA_FILE. When record is searched, file is opened based on the file
address.</p>
<p>A new windows is created.</p>
<p>The file stream is opened in the window.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-011 – INPUT RATES EXEMPTION APPLICATION:
    D - APPLICATION SUBMISSION</span>

| Program ID:   | RXA-011                                                                                                    |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                     |
| Program Name: | Input Rates Exemption Application: D - Application Submission                                              |
| Description:  | This program is developed to capture of rates exemption application information D - Application Submission |

> Program Environment:

| **Program Source**         | **Location**       | **Language / Compiler** |
|----------------------------|--------------------|-------------------------|
| appMaintSubmission.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintSubmission.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb                 | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb          | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type**            | **Maximum Length of input field** | **Validation Rule** | **Mandatory** | **Description**              |
|-----------------|----------|-----------|---------------|-----------|------------|
| submittDate   | Date                     | N/A                               | \[Date\]            |               | Application Submission Date  |
| receptDate    | Date                     | N/A                               | \[Date\]            | Y             | Application Receipt Date     |
| ackDate       | Date                     | N/A                               | \[Date\]            | Y             | Application Acknowledge Date |
| submitTo      | \[Selection: RXS \| DO\] | N/A                               | N/A                 | Y             | Submitted to                 |
| officer       | See Process Logic        | N/A                               | N/A                 | Y             | Subject officer              |
| isUrgent      | \[checkbox\]             | N/A                               | N/A                 |               | Urgent case                  |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.3.4 - D – Application Submission</p>
<p>3.2.2.4 - D – Application Submission</p></th>
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
<th><p><u>When save the record:</u></p>
<ul>
<li><p>Validation checking of application form.</p></li>
<li><p>Update application information in RXA_APPL.</p></li>
<li><p>Redirect to summary list page.</p></li>
</ul>
<p><u>When save &amp; submit the record:</u></p>
<ul>
<li><p>Perform save the record.</p></li>
<li><p>Change application status to (1) Acknowledgement by HAD (RxS or
DO)</p></li>
<li><p>Create Acknowledgement Letter generation record in PRN_INFO:</p>
<ul>
<li><blockquote>
<p>Select TemplateID based on status of missing information and
supplement document.</p>
</blockquote></li>
<li><blockquote>
<p>Event = 6 – Application Acknowledgement</p>
</blockquote></li>
</ul></li>
<li><p>Redirect to summary list page.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-012 – UPDATE RATES EXEMPTION
    APPLICATION: E - APPLICATION UPDATE</span>

| Program ID:   | RXA-012                                                                                                 |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                  |
| Program Name: | Update Rates Exemption Application: E - Application Update                                              |
| Description:  | This program is developed to allow user to update of rates exemption application E - Application Update |

> Program Environment:

| **Program Source**     | **Location**       | **Language / Compiler** |
|------------------------|--------------------|-------------------------|
| appMaintUpdate.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintUpdate.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb             | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb      | reis\class\model\\ | DAO VB.NET Class        |

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
<col style="width: 40%" />
<col style="width: 25%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>Floor(s): (Rates Assessment, Indigenous Status, Occupied for
domestic purpose, Exemption not granted for another NT property)</th>
<th><p>Assessment No,</p>
<p>Assessment Date,</p>
<p>The indigenous villager is the applicant or close relative</p>
<p>Occupied for domestic purposes</p>
<p>Exemption from rates payment not granted for another NT
property</p></th>
<th>Floor(s): (Rates Assessment, Indigenous Status, Occupied for
domestic purpose, Exemption not granted for another NT property)</th>
</tr>
<tr class="header">
<th>Floor(s): Proper size, Structure Tolerated</th>
<th><p>Proper size (Recommended</p>
<p>Approval by CRV),</p>
<p>Structure tolerated by DLO,</p>
<p>Covered by Survey Number</p>
<p>Whether DLO recommended that UBW has been rectified</p></th>
<th>Floor(s): Proper size, Structure Tolerated</th>
</tr>
<tr class="odd">
<th>Reason Code (CRV)</th>
<th><p>Floor(s),</p>
<p>UBW,</p>
<p>Description</p></th>
<th>Reason Code (CRV)</th>
</tr>
<tr class="header">
<th>Reason Code (DLO)</th>
<th><p>Floor(s),</p>
<p>UBW,</p>
<p>Description</p></th>
<th>Reason Code (DLO)</th>
</tr>
<tr class="odd">
<th>Results</th>
<th><p>Results,</p>
<p>NFA Reason,</p>
<p>Remark</p></th>
<th>Results</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.4.5 - E – Application Update</p>
<p>3.2.3.5 - E – Application Update</p></th>
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
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Floor(s) of each table is based on floor(s) applied to the
application.</p></li>
</ul>
<p><u>For saving of records:</u></p>
<ul>
<li><p>Floor(s): (Rates Assessment, Indigenous Status, Occupied for
domestic purpose, Exemption not granted for another NT property) is
saved in table RXA_FLOOR and RXA_APPL.</p></li>
<li><p>Floor(s): Proper size, Structure Tolerated is saved in table
RXA_FLOOR</p></li>
<li><p>Reason Code (CVR or DLO) is saved in table RXA_UBW and
RXA_UBW_FLOOR</p></li>
<li><p>Results is saved in RXA_FLOOR</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-013 – UPDATE RATES EXEMPTION
    APPLICATION: F - GENERATE CASE SUMMARY</span>

| Program ID:   | RXA-013                                                                                                    |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                     |
| Program Name: | Update Rates Exemption Application: F - Generate Case Summary                                              |
| Description:  | This program is developed to allow user to update of rates exemption application F - Generate Case Summary |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| appMaintSummary.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintSummary.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb              | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |
| RXCaseDAO.vb            | reis\class\model\\ | DAO VB.NET Class        |

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
| Criteria Meet | N/A        | Criteria Meet   |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.4.6 - F – Case Summary</p>
<p>3.2.3.6 - F –Case Summary</p></th>
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
<th><p><u>When Update Case Summary is clicked:</u></p>
<ul>
<li><p>Based on results in RXA_FLOOR, floor(s) and assessment no. which
have been selected as approved / rejected / NFA are retrieved.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-014 – UPDATE RATES EXEMPTION
    APPLICATION: F - DISPLAY CASE SUMMARY</span>

| Program ID:   | RXA-014                                                                                                   |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                    |
| Program Name: | Update Rates Exemption Application: F - Display Case Summary                                              |
| Description:  | This program is developed to allow user to update of rates exemption application F - Display Case Summary |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| appMaintSummary.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintSummary.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb              | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |
| RXCaseDAO.vb            | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.4.6 - F – Case Summary</p>
<p>3.2.3.6 - F –Case Summary</p></th>
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
<th><p>Retrieve approved / rejected /NFA case information:</p>
<ul>
<li><p>Case records for approved case from APR_CASE, APR_FLOOR and
APR_CRITERIA</p></li>
<li><p>Case records for rejected case from REJ_CASE, REJ_FLOOR and
REJ_CRITERIA</p></li>
</ul>
<p>Displayed case summary table of Approved cases / Rejected cases / NFA
cases.</p>
<p>When approval letter issue date is input, the date since application
acknowledgement date issue date is calculated and shown on the
page.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-015 – UPDATE RATES EXEMPTION
    APPLICATION: G - APPLICATION STATUS</span>

| Program ID:   | RXA-015                                                                                                 |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                  |
| Program Name: | Update Rates Exemption Application: G - Application Status                                              |
| Description:  | This program is developed to allow user to update of rates exemption application G - Application Status |

> Program Environment:

| **Program Source**       | **Location**       | **Language / Compiler** |
|--------------------------|--------------------|-------------------------|
| appMaintStatus.aspx.vb   | reis\\             | Code Behind VB.NET File |
| AppForm.vb               | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb        | reis\class\model\\ | DAO VB.NET Class        |
| ApplicationPendingDAO.vb | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter**  | **Format**                             | **Description**                                                   |
|-----------------------|----------------|----------------------------------|
| Current status | \[Selection: RXA_APPL.RXA_APP_STATUS\] | Selection of application status. (Please refer processing logic). |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.4.7 - G – Application Status</p>
<p>3.2.3.7 - G – Application Status</p></th>
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
<th><p>When page is loaded, display current application status based on
RXA_APPL.RXA_APP_STATUS.</p>
<p><u>Selection of application status:</u></p>
<ul>
<li><p>When current status is &gt;= 14 (i.e. application has been
endorsed or final approved), the input of status will be disabled (i.e
the application status is read-only.)</p></li>
<li><p>Similarly, manually switch application status to 0 (receive
application) or ≥ 14 is not allowed.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-016 – UPDATE RATES EXEMPTION
    APPLICATION: G - APPLICATION STATUS, GENERATE NEW MEMO /
    LETTER</span>

| Program ID:   | RXA-016                                                                                                                             |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                                              |
| Program Name: | Update Rates Exemption Application: G - Application Status, Generate New Memo / Letter                                              |
| Description:  | This program is developed to allow user to update of rates exemption application G - Application Status, Generate New Memo / Letter |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| appMaintGenMemo.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintGenMemo.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb              | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |
| MemoLetterDAO.vb        | reis\class\model\\ | DAO VB.NET Class        |

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
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 8%" />
<col style="width: 15%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Length</strong></th>
<th><strong>Mandatory</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>Issue Date</th>
<th>[Date]</th>
<th></th>
<th>Y</th>
<th>Issue Date</th>
</tr>
<tr class="header">
<th>Encl:</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Encl:</th>
</tr>
<tr class="odd">
<th>Memo/ letter type – To</th>
<th><p>1 - Applicant;</p>
<p>2 - DO;</p>
<p>3 - RVD;</p>
<p>4 - DLO or M/SC</p></th>
<th></th>
<th>Y</th>
<th>Memo/ letter type – To</th>
</tr>
<tr class="header">
<th>Memo / Letter Type – Template</th>
<th>Template of report / memo</th>
<th></th>
<th>Y</th>
<th>Template of letter / memo to be generated</th>
</tr>
<tr class="odd">
<th>Sender From</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Sender From</th>
</tr>
<tr class="header">
<th>Sender Ref</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Sender Ref</th>
</tr>
<tr class="odd">
<th>Sender Tel</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Sender Tel</th>
</tr>
<tr class="header">
<th>Sender Fax</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Sender Fax</th>
</tr>
<tr class="odd">
<th>Receiver To / Applicants name</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver To / Applicants name</th>
</tr>
<tr class="header">
<th>Receiver Attn</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Attn</th>
</tr>
<tr class="odd">
<th>Receiver Your ref.</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Your ref.</th>
</tr>
<tr class="header">
<th>Receiver Dated</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Dated</th>
</tr>
<tr class="odd">
<th>Receiver Fax No.</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Fax No.</th>
</tr>
<tr class="header">
<th>Receiver Total Pages</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Total Pages</th>
</tr>
<tr class="odd">
<th>CC</th>
<th><p>CVD/LandD/Land Registry, HAD</p>
<p>District</p>
<p>Note</p></th>
<th></th>
<th></th>
<th>CC list.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 3.1.4.7.1 - Generate New Memo/Letter to Applicant (oldvth-GenerateMemoLetter.htm) |
|------------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Default value of sender information (sender tel., sender from,
sender fax, sender ref) is retrieved from SYS_PARM.</p></li>
</ul>
<p><u>When Print button is clicked:</u></p>
<ul>
<li><p>Based on template selected, application pending record
(RXA_PENDING) is created. The issue date will be served as pending start
date of the record.</p></li>
<li><p>Record of memo &amp; letter (PRN_INFO, PRN_CC) is
created.</p></li>
<li><p>Open the corresponding report template to generate report in PDF
format.</p></li>
<li><p>The generated memo /letter is displayed in new windows.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-017 – UPDATE RATES EXEMPTION
    APPLICATION: G - APPLICATION STATUS, INPUT RESPONSE</span>

| Program ID:   | RXA-017                                                                                                                 |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                                  |
| Program Name: | Update Rates Exemption Application: G - Application Status, Input Response                                              |
| Description:  | This program is developed to allow user to update of rates exemption application G - Application Status, Input Response |

> Program Environment:

| **Program Source**       | **Location**       | **Language / Compiler** |
|--------------------------|--------------------|-------------------------|
| appMaintResponse.aspx    | reis\\             | ASP.NET Web Form        |
| appMaintResponse.aspx.vb | reis\\             | Code Behind VB.NET File |
| AppForm.vb               | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb        | reis\class\model\\ | DAO VB.NET Class        |
| MemoLetterDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |
| ApplicationPendingDAO.vb | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format**  | **Length** | **Mandatory** | **Description** |
|---------------|-------------|------------|---------------|-----------------|
| Response Date | \[Date\]    |            | Y             | Response Date   |
| Remark        | X, \[Text\] | 100        |               | Remark          |

> Screen Layout:

| 3.1.4.7.2 - Input Response (oldvth-InputMemo.htm) |
|---------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When Save button is clicked:</u></p>
<ul>
<li><p>The related application pending record (RXA_PENDING) is opened
and updated. The response date will be served as pending end date of the
record.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-018 – UPDATE RATES EXEMPTION
    APPLICATION: SAVE AND SUBMIT</span>

| Program ID:   | RXA-018                                                        |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                         |
| Program Name: | Update Rates Exemption Application: Save and Submit            |
| Description:  | This program is developed to save and submi application record |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| AppForm.vb         | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb  | reis\class\model\\ | DAO VB.NET Class        |
| RXCaseDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |
| MemoLetterDAO.vb   | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>3.1.4.6 - F – Case Summary</p>
<p>3.2.3.6 - F –Case Summary</p></th>
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
<th><p><u>When Save button is clicked:</u></p>
<ul>
<li><p>Case records for approved case are created in APR_CASE, APR_FLOOR
and APR_CRITERIA</p></li>
<li><p>Case records for rejected case are created in REJ_CASE, REJ_FLOOR
and REJ_CRITERIA</p></li>
<li><p>Redirect to summary list.</p></li>
</ul>
<p><u>When Save and submit button is clicked:</u></p>
<ul>
<li><p>Perform save action.</p></li>
<li><p>Application status (RXA_APPL.RXA_APP_STATUS) is updated to (13)
Submitted to endorsement officer.</p></li>
<li><p>For NFA case, memo / letter record for NFA letters will be
created. the memo/letter ID is also updated to the REJ_CASE
record.</p></li>
<li><p>Redirect to summary list.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-019 – AMEND RATES EXEMPTION
    APPLICATION</span>

| Program ID:   | RXA-019                                                                             |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                              |
| Program Name: | Amend Rates Exemption Application                                                   |
| Description:  | This program is developed to allow user to amend rates exmption application record. |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| AppForm.vb         | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb  | reis\class\model\\ | DAO VB.NET Class        |
| RXCaseDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

| Refer to RXA-006 to RXA-018 |
|-----------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When application that application status is not completed is
amended, the saving of record is refer to RXA-018.</p>
<p><u>When application that application status is completed is
amended:</u></p>
<ul>
<li><p>Record of pending for amend will be created for saving of new
image of application.</p></li>
<li><p>When amendment is approved, the changes in the new image record
will be updated to the application record.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-020 – DISPLAY ENDORSEMENT SUMMARY
    LIST</span>

| Program ID:   | RXA-020                                                    |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                     |
| Program Name: | Display Endorsement Summary List                           |
| Description:  | This program is developed to show endorsement summary list |

> Program Environment:

| **Program Source**     | **Location**       | **Language / Compiler** |
|------------------------|--------------------|-------------------------|
| endorseSummary.aspx    | reis\\             | ASP.NET Web Form        |
| endorseSummary.aspx.vb | reis\\             | Code Behind VB.NET File |
| EndorseSummary.vb      | reis\class\RXA\\   | VB.NET Class            |
| RXCaseDAO.vb           | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

| 5.1 - Endorsement Summary Generation (EndorsementSummaryGeneration.htm) |
|------------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Approved Case (APR_CASE), Rejected Case (REJ_CASE), Cancelled
case (CAN_CASE) with RXA_APPL_STATUS = (13) Submitted to endorsement
officer will be retrieved.</p></li>
<li><p>By default, all records with endorsement list print date = null
will be selected (i.e. checkbox selected).</p></li>
<li><p>When checkbox is checked / unchecked, the counting of total
recommended case will be updated and displayed.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-021 – GENERATE ENDORSEMENT
    SUMMARY</span>

| Program ID:   | RXA-021                                                   |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                    |
| Program Name: | Generate Endorsement Summary                              |
| Description:  | This program is developed to generate endorsement summary |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| EndorseSummary.vb  | reis\class\RXA\\   | VB.NET Class            |
| RXCaseDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description**                                   |
|-----------------------|----------------|----------------------------------|
| LMNo.         | Checkbox   | LM No. selected for generate endorsement summary. |

> Screen Layout:

| 5.1 - Endorsement Summary Generation (EndorsementSummaryGeneration.htm) |
|------------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When print button is clicked, endorsement summary for selected LM
No. will be generated.</p>
<p>The report generated will be displayed in the new windows in PDF
format.</p>
<p>The endorsement list print date time will be updated in the Approved
Case (APR_CASE), Rejected Case (REJ_CASE), Cancelled case (CAN_CASE)
record.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-022 – ENDORSEMENT</span>

| Program ID:   | RXA-022                                                                          |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                           |
| Program Name: | Endorsement                                                                      |
| Description:  | This program is developed to endorse recommended approved / rejected / cancelled |

> Program Environment:

| **Program Source**     | **Location**       | **Language / Compiler** |
|------------------------|--------------------|-------------------------|
| endorseSummary.aspx    | reis\\             | ASP.NET Web Form        |
| endorseSummary.aspx.vb | reis\\             | Code Behind VB.NET File |
| Endorse.vb             | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb      | reis\class\model\\ | DAO VB.NET Class        |
| RXReviewDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |

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
<col style="width: 31%" />
<col style="width: 20%" />
<col style="width: 47%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>LMNo.</th>
<th>Checkbox</th>
<th>LM No. selected for endorsement.</th>
</tr>
<tr class="header">
<th>Endorsement Date</th>
<th>[Date]</th>
<th><p>Endorsement Date.</p>
<p>The endorsement date should not earlier than application
acknowledgement date or application receipt date.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 5.2 - Endorsement (Endorsement.htm) |
|-------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Approved Case (APR_CASE), Rejected Case (REJ_CASE), Cancelled
case (CAN_CASE) with RXA_APPL_STATUS = (13) Submitted to endorsement
officer will be retrieved.</p></li>
<li><p>By default, all records with endorsement list print date &lt;&gt;
null will be selected (i.e. checkbox selected).</p></li>
<li><p>When checkbox is checked / unchecked, the counting of total
recommended case will be updated and displayed.</p></li>
</ul>
<p><u>When Confirm Endorsement button is clicked:</u></p>
<ul>
<li><p>Endorsement date and endorsement by (as current user ID in the
session) is updated to Approved Case (APR_CASE), Rejected Case
(REJ_CASE), Cancelled case (CAN_CASE)</p></li>
<li><p>The RXA_APPL_STATUS of related application record is updated to
(14) Endorsed by endorsement officer.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-023 – ENQUIRY OF ENDORSED RECORDS</span>

| Program ID:   | RXA-023                                                           |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                            |
| Program Name: | Enquiry of Endorsed Records                                       |
| Description:  | This program is developed to retrieve endorse records for revoke. |

> Program Environment:

| **Program Source**        | **Location**       | **Language / Compiler** |
|---------------------------|--------------------|-------------------------|
| endorseRevokeList.aspx    | reis\\             | ASP.NET Web Form        |
| endorseRevokeList.aspx.vb | reis\\             | Code Behind VB.NET File |
| EndorseRevoke.vb          | reis\class\RXA\\   | VB.NET Class            |
| RXCaseDAO.vb              | reis\class\model\\ | DAO VB.NET Class        |

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
<col style="width: 31%" />
<col style="width: 20%" />
<col style="width: 47%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>Endorsement Date</th>
<th>[Date]</th>
<th><p>Endorsement Date for searching of endorsed record.</p>
<p>User must enter a date for clicking Search button.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 5.3 - Revoke Endorsement (EndorsementRevoke.htm) |
|--------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When search button is clicked:</u></p>
<ul>
<li><p>Approved Case (APR_CASE), Rejected Case (REJ_CASE), Cancelled
case (CAN_CASE) with RXA_APPL_STATUS = (14) Endorsed by endorsement
officer will be retrieved.</p></li>
<li><p>By default, all records will not be selected (i.e. checkbox not
selected).</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-024 – REVOKE ENDORSEMENT</span>

| Program ID:   | RXA-024                                               |
|---------------|-------------------------------------------------------|
| Mode:         | Online                                                |
| Program Name: | Revoke Endorsement                                    |
| Description:  | This program is developed to revoke endorsed records. |

> Program Environment:

| **Program Source**        | **Location**       | **Language / Compiler** |
|---------------------------|--------------------|-------------------------|
| endorseRevokeList.aspx    | reis\\             | ASP.NET Web Form        |
| endorseRevokeList.aspx.vb | reis\\             | Code Behind VB.NET File |
| EndorseRevoke.vb          | reis\class\RXA\\   | VB.NET Class            |
| RXCaseDAO.vb              | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description**                         |
|---------------|------------|-----------------------------------------|
| LMNo.         | Checkbox   | LM No. selected for revoke endorsement. |

> Screen Layout:

| 5.3 - Revoke Endorsement (EndorsementRevoke.htm) |
|--------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When Confirm Revoke Endorsement button is clicked:</u></p>
<ul>
<li><p>Confirmation dialog box is displayed.</p></li>
<li><p>When confirmation is acquired, Endorsement date and endorsement
by is updated as null to Approved Case (APR_CASE), Rejected Case
(REJ_CASE), Cancelled case (CAN_CASE)</p></li>
<li><p>The RXA_APPL_STATUS of related application record is updated to
(13) Submitted to endorsement officer.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-025 – DISPLAY FILE MINUTE</span>

| Program ID:   | RXA-025                                                   |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                    |
| Program Name: | Display File Minute                                       |
| Description:  | This program is developed to show file minute information |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| approvalSummary.aspx    | reis\\             | ASP.NET Web Form        |
| approvalSummary.aspx.vb | reis\\             | Code Behind VB.NET File |
| ApprovalSummary.vb      | reis\class\RXA\\   | VB.NET Class            |
| RXCaseDAO.vb            | reis\class\model\\ | DAO VB.NET Class        |

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

| 6.1 - File Minute Generation (ApprovalFileMinuteGeneration.htm) |
|-----------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Approved Case (APR_CASE), Rejected Case (REJ_CASE), Cancelled
case (CAN_CASE) with RXA_APPL_STATUS = (14) Endorsed by endorsement
officer will be retrieved.</p></li>
<li><p>By default, all records with file minute print date = null will
be selected (i.e. checkbox selected).</p></li>
<li><p>When checkbox is checked / unchecked, the counting of total
recommended case will be updated and displayed.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-026 – GENERATE FILE MINUTE</span>

| Program ID:   | RXA-026                                            |
|---------------|----------------------------------------------------|
| Mode:         | Online                                             |
| Program Name: | Generate File Minute                               |
| Description:  | This program is developed to generate file minute. |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| ApprovalSummary.vb | reis\class\RXA\\   | VB.NET Class            |
| RXCaseDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description**                           |
|---------------|------------|-------------------------------------------|
| LMNo.         | Checkbox   | LM No. selected for generate file minute. |

> Screen Layout:

| 6.1 - File Minute Generation (ApprovalFileMinuteGeneration.htm) |
|-----------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When print button is clicked, file minute for selected LM No.
will be generated.</p>
<p>The report generated will be displayed in the new windows in PDF
format.</p>
<p>The file minute print date time will be updated in the Approved Case
(APR_CASE), Rejected Case (REJ_CASE), Cancelled case (CAN_CASE)
record.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-027 – RECORD APPROVAL</span>

| Program ID:   | RXA-027                                                                                            |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                             |
| Program Name: | Record Approval                                                                                    |
| Description:  | This program is developed to confirm the endorsed approved / rejected / cancelled / amended cases. |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| approvalSummary.aspx    | reis\\             | ASP.NET Web Form        |
| approvalSummary.aspx.vb | reis\\             | Code Behind VB.NET File |
| Approval.vb             | reis\class\RXA\\   | VB.NET Class            |
| ApplicationDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |
| RXReviewDAO.vb          | reis\class\model\\ | DAO VB.NET Class        |

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
<col style="width: 31%" />
<col style="width: 20%" />
<col style="width: 47%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>LMNo.</th>
<th>Checkbox</th>
<th>LM No. selected for approval.</th>
</tr>
<tr class="header">
<th>Approval Date</th>
<th>[Date]</th>
<th><p>Approval Date.</p>
<p>The Approval date should not earlier than endorsement date.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 6.2 - Approval (Approval.htm) |
|-------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Approved Case (APR_CASE), Rejected Case (REJ_CASE), Cancelled
case (CAN_CASE) with RXA_APPL_STATUS = (14) Endorsed by endorsement
officer will be retrieved.</p></li>
<li><p>By default, all records with file minute print date &lt;&gt; null
will be selected (i.e. checkbox selected).</p></li>
<li><p>When checkbox is checked / unchecked, the counting of total
recommended case will be updated and displayed.</p></li>
</ul>
<p><u>When Confirm Approval button is clicked:</u></p>
<ul>
<li><p>Approval date and Approved by (as current user ID in the session)
is updated to Approved Case (APR_CASE), Rejected Case (REJ_CASE),
Cancelled case (CAN_CASE)</p></li>
<li><p>The RXA_APPL_STATUS of related application record is updated to
(16) Return from DHA.</p></li>
<li><p>Memo/letter record for approval letter / rejection letter /
cancellation letter will be created. The memo/letter ID is also updated
to the APV_CASE / REJ_CASE / CAN_CASE record.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-028 – ENQUIRY OF CONFIRMED APPROVAL
    RECORDS</span>

| Program ID:   | RXA-028                                                            |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                             |
| Program Name: | Enquiry of Confirmed Approval Records                              |
| Description:  | This program is developed to retrieve confirmed record for revoke. |

> Program Environment:

| **Program Source**         | **Location**       | **Language / Compiler** |
|----------------------------|--------------------|-------------------------|
| approvalRevokeList.aspx    | reis\\             | ASP.NET Web Form        |
| approvalRevokeList.aspx.vb | reis\\             | Code Behind VB.NET File |
| ApprovalRevoke.vb          | reis\class\RXA\\   | VB.NET Class            |
| RXCaseDAO.vb               | reis\class\model\\ | DAO VB.NET Class        |

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
<col style="width: 31%" />
<col style="width: 20%" />
<col style="width: 47%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>Approval Date</th>
<th>[Date Range]</th>
<th><p>Endorsement Date range for searching of approved record.</p>
<p>User must enter a date for clicking Search button.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 6.3 - Revoke Approval (ApprovaRevokel.htm) |
|--------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When search button is clicked:</u></p>
<ul>
<li><p>Approved Case (APR_CASE), Rejected Case (REJ_CASE), Cancelled
case (CAN_CASE) with RXA_APPL_STATUS = (16) Return from DHA or (17)
Result letter by RxS.</p></li>
<li><p>By default, all records will not be selected (i.e. checkbox not
selected).</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-029 – REVOKE APPROVAL</span>

| Program ID:   | RXA-029                                               |
|---------------|-------------------------------------------------------|
| Mode:         | Online                                                |
| Program Name: | Revoke Approval                                       |
| Description:  | This program is developed to revoke confirmed record. |

> Program Environment:

| **Program Source**         | **Location**       | **Language / Compiler** |
|----------------------------|--------------------|-------------------------|
| approvalRevokeList.aspx    | reis\\             | ASP.NET Web Form        |
| approvalRevokeList.aspx.vb | reis\\             | Code Behind VB.NET File |
| ApprovalRevoke.vb          | reis\class\RXA\\   | VB.NET Class            |
| RXCaseDAO.vb               | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description**                      |
|---------------|------------|--------------------------------------|
| LMNo.         | Checkbox   | LM No. selected for revoke approval. |

> Screen Layout:

| 6.3 - Revoke Approval (ApprovaRevokel.htm) |
|--------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When Confirm Revoke Endorsement button is clicked:</u></p>
<ul>
<li><p>Confirmation dialog box is displayed.</p></li>
<li><p>When confirmation is acquired, approval date and approval by is
updated as null to Approved Case (APR_CASE), Rejected Case (REJ_CASE),
Cancelled case (CAN_CASE)</p></li>
<li><p>The RXA_APPL_STATUS of related application record is updated to
(14) Endorsed by endorsement officer.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-030 – BATCH LETTERS GENERATION</span>

| Program ID:   | RXA-030                                              |
|---------------|------------------------------------------------------|
| Mode:         | Online                                               |
| Program Name: | Batch Letters Generation                             |
| Description:  | This program is developed to generate batch letters. |

> Program Environment:

| **Program Source**  | **Location**     | **Language / Compiler** |
|---------------------|------------------|-------------------------|
| batchLetter.aspx    | reis\\           | ASP.NET Web Form        |
| batchLetter.aspx.vb | reis\\           | Code Behind VB.NET File |
| BatchLetter.vb      | reis\class\RXA\\ | VB.NET Class            |

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

| 7 - Case for Letter Generation Listing (CaseforLetterGenerationListing.htm) |
|------------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Records of memo/letter where print date time is null is
retrieved.</p></li>
<li><p>The records is grouped by type of event (application
acknowledgement letter / approval letter / rejection letters /
no-further action letters).</p></li>
<li><p>When checkbox is checked / unchecked, the counting of total case
will be updated and displayed.</p></li>
</ul>
<p><u>When print button is clicked:</u></p>
<ul>
<li><p>Letters for selected LM No. will be generated.</p></li>
<li><p>The report generated will be displayed in the new windows in PDF
format.</p></li>
<li><p>The letter print date time will be updated in the memo/letter
record.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RXA-031 – CHECKING OF OUTSTANDING
    CASE</span>

| Program ID:   | RXA-031                                                                                                     |
|-------------------|-----------------------------------------------------|
| Mode:         | Batch                                                                                                       |
| Program Name: | Checking of outstanding case                                                                                |
| Description:  | This program is developed to perform checking of outstanding case of rates exemption application and review |

> Program Environment:

| **Program Source**           | **Location** | **Language / Compiler** |
|------------------------------|--------------|-------------------------|
| sp_outstandingcase_check.sql | Database     | MS SQL Stored Procedure |
| sp_effectivecase_check.sql   | Database     | MS SQL Stored Procedure |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

| N/A |
|-----|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>This procedure perform following tasks:</p>
<p>(Task 1, sp_outstandingcase_check.sql) Checking of long outstanding
cases:</p>
<table>
<colgroup>
<col style="width: 28%" />
<col style="width: 71%" />
</colgroup>
<thead>
<tr class="header">
<th>(1) - acknowledge receipt of new application</th>
<th><p>For application (RXA_APP) which application status &lt; (1)
Acknowledgement by HAD (RxS or DO):</p>
<p>If (application receipt date + no. of month allow from SYS_PARAM)
&lt; current system date, then outstanding status = 1.</p></th>
</tr>
<tr class="odd">
<th><p>(2) - Response from RVD,</p>
<p>(3) - Response from LandsD</p></th>
<th><p>For application (RXA_APP) which application status &lt; (16)
Return from DHA (i.e. not yet completed):</p>
<p>If there is a pending record (RXA_PENDING) which:</p>
<ul>
<li><p>Pending status in</p>
<ul>
<li><blockquote>
<p>(3) Pending advice from RVD; or</p>
</blockquote></li>
<li><blockquote>
<p>(4) Pending advice from DLO; or</p>
</blockquote></li>
<li><blockquote>
<p>(5) Pending advice from M/SC; or</p>
</blockquote></li>
<li><blockquote>
<p>(6) Pending advice from DLO and M/SC; and</p>
</blockquote></li>
</ul></li>
<li><p>(Pending start date + no. of month allow from SYS_PARAM) &lt;
current system date, then outstanding status = 2 (when pending status =
3) or 3 (when pending status = 4 to 6).</p></li>
</ul></th>
</tr>
<tr class="header">
<th>(4) - Completion of rates exemption application process</th>
<th><p>For application (RXA_APP) which:</p>
<ul>
<li><p>application status ≥ (1) Acknowledgement by HAD; and (RxS or
DO)</p></li>
<li><p>application status &lt; (16) Return from DHA (i.e. not yet
completed); and</p></li>
<li><p>If (application acknowledgment date + no. of month allow from
SYS_PARAM) &lt; current system date, then outstanding status =
4.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<p>For each of outstanding case found:</p>
<ul>
<li><p>An Outstanding record (OS_CASE) will be created.</p></li>
</ul>
<p>(Task 2, sp_effectivecase_check.sql) Checking Effective Date of
Approved Case / Cancelled Case</p>
<ul>
<li><p>Since end date of effective period can be specified to approved
case or cancelled, to enhanced performance of searching of rates
exemption cases which is currently being approved or cancelled, a batch
function is implemented to check each of approved and cancelled
case.</p></li>
<li><p>Checking of all approved (APV_CASE) cases where effective end
date is not null, approval is no longer effective when:</p>
<ul>
<li><blockquote>
<p>Current APR_STATUS = “A”</p>
</blockquote></li>
<li><blockquote>
<p>Effective end date &gt; current system date; and</p>
</blockquote></li>
<li><blockquote>
<p>The related application have final approval (i.e. RXA_APP.APP_STATUS
&gt; 16 and APR_A_APPROVAL_DATE is not null), then</p>
</blockquote></li>
</ul></li>
</ul>
<blockquote>
<p>Update APR_STATUS to “C”.</p>
</blockquote>
<ul>
<li><p>Checking of all cancelled (CAN_CASE) cases where effective end
date is not null, cancellation is no longer effective when:</p>
<ul>
<li><blockquote>
<p>Current CAN_STATUS = “C”</p>
</blockquote></li>
<li><blockquote>
<p>Effective end date &gt; current system date; and</p>
</blockquote></li>
<li><blockquote>
<p>The related application have final approval (i.e. RXA_APP.APP_STATUS
&gt; 16 and CAN_C_APPROVAL_DATE is not null), then</p>
</blockquote></li>
</ul></li>
</ul>
<blockquote>
<p>Update CAN_STATUS to “A”.</p>
</blockquote></th>
</tr>
<tr class="odd">
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-001 – DISPLAY MATCHING LIST</span>

| Program ID:   | REV-001                                                                   |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                    |
| Program Name: | Display Matching List                                                     |
| Description:  | This program is developed to show web page of generation of matching list |

> Program Environment:

| **Program Source**    | **Location**       | **Language / Compiler** |
|-----------------------|--------------------|-------------------------|
| matchingList.aspx     | reis\\             | ASP.NET Web Form        |
| matchingList.aspx.vb  | reis\\             | Code Behind VB.NET File |
| MatchingList.vb       | reis\class\REV\\   | VB.NET Class            |
| MatchingListDAO.vb    | reis\class\model\\ | DAO VB.NET Class        |
| SystemParameterDAO.vb | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

| 8 - Matching List (MatchingList.htm) |
|--------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When page is loaded:</p>
<p>The previous Matching Listing has been generated date time is
retrieved from SYS_PARAM.</p>
<p>In case of previous matching listing has been generated, the message
and the downloaded will not be displayed.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-002 – GENERATE NEW MATCHING LIST</span>

| Program ID:   | REV-002                                                            |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                             |
| Program Name: | Generate New Matching List                                         |
| Description:  | This program is developed to generate matching list interface file |

> Program Environment:

| **Program Source**    | **Location**       | **Language / Compiler** |
|-----------------------|--------------------|-------------------------|
| matchingList.aspx     | reis\\             | ASP.NET Web Form        |
| matchingList.aspx.vb  | reis\\             | Code Behind VB.NET File |
| MatchingList.vb       | reis\class\REV\\   | VB.NET Class            |
| MatchingListDAO.vb    | reis\class\model\\ | DAO VB.NET Class        |
| SystemParameterDAO.vb | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description**                           |
|---------------|------------|-------------------------------------------|
| Password      | X(20)      | Password for generation of matching file. |

> Screen Layout:

| 8 - Matching List (MatchingList.htm) |
|--------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When Generate New Matching List button is clicked:</p>
<ul>
<li><p>All approved cases (APV_CASE) which is still effective based
effective date (i.e Either effective end date = null or effective end
date ≥ current system date) are retrieved.</p></li>
<li><p>The case information are retrieved for generation of text
file.</p></li>
<li><p>The text file is saved in the matching list file directory
(defined in system config file).</p></li>
<li><p>The text file is renamed as “matching_list” + YYYYMMDDHHMI +
“.txt”. (whereYYYYMMDDHHMI stand for generation date time).</p></li>
<li><p>The text file is then zipped with encryption using password
provided by user.</p></li>
<li><p>The zip file should have file name = text file’s file name +
“.zip”.</p></li>
<li><p>After zip file is created, the original plain text file and
previous generated file are deleted.</p></li>
<li><p>Update matching list file generation date time (same date time
used for filename creation) to the SYS_PARAM.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-003 – DOWNLOAD MATCHING LIST</span>

| Program ID:   | REV-003                                                                  |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                   |
| Program Name: | Download Matching List                                                   |
| Description:  | This program is developed to download genreated matching interface file. |

> Program Environment:

| **Program Source**   | **Location**     | **Language / Compiler** |
|----------------------|------------------|-------------------------|
| matchingList.aspx    | reis\\           | ASP.NET Web Form        |
| matchingList.aspx.vb | reis\\           | Code Behind VB.NET File |
| MatchingList.vb      | reis\class\REV\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

| 8 - Matching List (MatchingList.htm) |
|--------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When Download button is clicked:</p>
<ul>
<li><p>The zip file with file name =“matching_list” + YYYYMMDDHHMI +
“.txt.zip”. (where YYYYMMDDHHMI stand for generation date time from
SYS_PARAM) is collected from the matching list file directory (defined
in system config file).</p></li>
<li><p>The zip file is then downloaded by to user.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-004 – ENQUIRY RANDOM CHECK CASE</span>

| Program ID:   | REV-004                                               |
|---------------|-------------------------------------------------------|
| Mode:         | Online                                                |
| Program Name: | Enquiry Random Check Case                             |
| Description:  | This program is developed to search random check case |

> Program Environment:

| **Program Source**  | **Location**       | **Language / Compiler** |
|---------------------|--------------------|-------------------------|
| randomCheck.aspx    | reis\\             | ASP.NET Web Form        |
| randomCheck.aspx.vb | reis\\             | Code Behind VB.NET File |
| RandomCheck.vb      | reis\class\REV\\   | VB.NET Class            |
| RandomCheckDAO.vb   | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description**                                          |
|-----------------------|----------------|----------------------------------|
| Year          | N/A        | Selection of year for searching of random check records. |

> Screen Layout:

| 9 - Random Check Cases Generation (RandomCheckCasesGeneration.htm) |
|--------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>(randomCheck.aspx.vb) the selection of years from (current year –
10) to (current year +1) is created. Current year is selected as default
selection.</p></li>
</ul>
<p><u>When search button is clicked:</u></p>
<ul>
<li><p>Random check records (RAN_HDR) of the selected year is
retrieved.</p></li>
<li><p>The approved case file record (RAN_RX_FILE) selected in the
random check is retrieved.</p></li>
<li><p>Join with rates exemption file (RX_FILE on same FILENO) and
related approved cases (APR_CASE on same FILENO, APR_FLOOR on same
CASEID, RXA_AG on same APPID), to get address, approved floor(s) and
grantee information</p></li>
<li><p>Retrieved records are grouped by district and displayed in the
list.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-005 – GENERATE NEW RANDOM CHECK
    CASES</span>

| Program ID:   | REV-005                                                       |
|-------------------|-----------------------------------------------------|
| Mode:         | Batch                                                         |
| Program Name: | Generate New Random Check Cases                               |
| Description:  | This program is developed to generate new random check cases. |

> Program Environment:

| **Program Source**  | **Location**       | **Language / Compiler** |
|---------------------|--------------------|-------------------------|
| randomCheck.aspx    | reis\\             | ASP.NET Web Form        |
| randomCheck.aspx.vb | reis\\             | Code Behind VB.NET File |
| RandomCheck.vb      | reis\class\REV\\   | VB.NET Class            |
| RandomCheckDAO.vb   | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description**                                       |
|-----------------------|----------------|----------------------------------|
| Year          | N/A        | Selection of year for generation of new random check. |

> Screen Layout:

| 9 - Random Check Cases Generation (RandomCheckCasesGeneration.htm) |
|--------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When Generate New Random Check Case button is clicked:</u></p>
<ul>
<li><p>New Random check records (RAN_HDR) of the selected year is
created.</p></li>
<li><p>Since previous picked LM No. (FILENO) should not be picked in
current selection, RCD_FILENO of previous latest random check are
retrieved.</p></li>
<li><p>Based on number of random selection case retrieved from
SYS_PARAM, a number of random case files are selected by each active
district.</p></li>
<li><p>The random selected RX_FILE records must have approved rates
exemption case, that is:</p>
<ul>
<li><blockquote>
<p>RX_REC_STATUS is active; and</p>
</blockquote></li>
<li><blockquote>
<p>Join with application (RXA_APP on same FILENO) which join with
approved case (APR_CASE on same APPID); and</p>
</blockquote></li>
<li><blockquote>
<p>The approved case should have effective approval status, that is:</p>
</blockquote>
<ul>
<li><blockquote>
<p>APR_STATUS = A (approved);</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>The RX_FILENO should not contain in RCD_FILENO of previous latest
random check.</p>
</blockquote></li>
</ul></li>
<li><p>Based random selected RX_FILE and district, records of
RAN_RX_FILE are created.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-006 – PRINT RANDOM CHECK CASES</span>

| Program ID:   | REV-006                                               |
|---------------|-------------------------------------------------------|
| Mode:         | Online                                                |
| Program Name: | Print Random Check Cases                              |
| Description:  | This program is developed to print random check case. |

> Program Environment:

| **Program Source**  | **Location**       | **Language / Compiler** |
|---------------------|--------------------|-------------------------|
| randomCheck.aspx    | reis\\             | ASP.NET Web Form        |
| randomCheck.aspx.vb | reis\\             | Code Behind VB.NET File |
| RandomCheck.vb      | reis\class\REV\\   | VB.NET Class            |
| RandomCheckDAO.vb   | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description**                                          |
|-----------------------|----------------|----------------------------------|
| Year          | N/A        | Selection of year for searching of random check records. |

> Screen Layout:

| 9 - Random Check Cases Generation (RandomCheckCasesGeneration.htm) |
|--------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When Print button is clicked, the random check cases of selected
random check is printed.</p>
<p>The generated report in PDF format is opened in a new
window.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-007 – NEW REVIEW OF APPROVED RATES
    EXEMPTION: SEARCH CURRENTLY APPROVED RATES EXEMPTION</span>

| Program ID:   | REV-007                                                                           |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                            |
| Program Name: | New Review of Approved Rates Exemption: Search Currently Approved Rates Exemption |
| Description:  | This program is developed to search currently approved rates exemption record     |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| revNew.aspx        | reis\\             | ASP.NET Web Form        |
| revNew.aspx.vb     | reis\\             | Code Behind VB.NET File |
| ReviewMaint.vb     | reis\class\REV\\   | VB.NET Class            |
| RXCaseDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |
| RXReviewDAO.vb     | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Data Type**         | **Maximum Length of input field** | **Validation Rule**    | **Mandatory** | **Description**                                         |
|-----------------|----------|-----------|-------------|-----------|--------------|
| lmNo          | 9                     | 8                                 | \[numeric\]            |               | LM No                                                   |
| lotNo         | X                     | 20                                | \[alphanumeric\]       |               | Lot No                                                  |
| cll           | X                     | 20                                | \[alphanumeric\]       |               | CLL                                                     |
| dd            | X                     | 20                                | \[alphanumeric\]       |               | DD                                                      |
| address       | X                     | 200                               | \[text\]               |               | Address of village house with rates exemption approved. |
| name          | X                     | 100                               | \[text\]               |               | Full name (surename + “ “ + given name) of grantee      |
| hkID          | X                     | 12                                | \[alphanumeric\]       |               | HKID (identifier +”(“ check digit + “)”                 |
| distcode      | \[Selection:DISTICT\] | N/A                               | N/A                    |               | Selection of district                                   |
| assessmentNo  | X                     | 14                                | \[alphanumeric\]+\[-\] |               | Assessment No.                                          |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>4.1 - Review Search (review-search.htm)</p>
<p>4.2 - Search Results (review-searchResults.htm)</p>
<p>4.3 - Review Record (review-record.htm)</p></th>
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
<th><p><u>When search button is clicked:</u></p>
<ul>
<li><p>Currently approved rates exemption (i.e. APR_CASE where
APR_STATUS = “A”) are searched using searching criteria
submitted.</p></li>
<li><p>Address line 1 to line 5 are concatenated with space character
separating each line is used for matching with address provided by user.
“Like” operator is used in the string matching operation.</p></li>
<li><p>Surename and given name are concatenated with space character
separating is used for matching with name provided by user. English or
Chinese name of any grantee of approved case matched will be
retrieved.</p></li>
<li><p>Identifier (HKID_ID) and check digit (HKID_CD) of HKID are
combined as HKID_ID(HKID_CD) for matching with hkID provided by
user.</p></li>
<li><p>When multiple searching criteria are provided, criteria are
joined with “AND” operator for the searching.</p></li>
<li><p>The search results is return and displayed to user. Page
navigation based on maximum no. of row per page defined in SYS_PARAM is
implemented.</p></li>
</ul>
<p><u>When an approved rates exemption file is opened:</u></p>
<ul>
<li><p>All existing review (REV_CASE on same FILEID) records of selected
file are searched and listed out. The list is displayed in descending
order of review creation date.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-008 – INPUT REVIEW RECORD: H - REVIEW OF
    GRANTED RATES EXEMPTION</span>

| Program ID:   | REV-008                                                                                                                  |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                                   |
| Program Name: | Input Review Record: H - Review of Granted Rates Exemption                                                               |
| Description:  | This program is developed to capture review of granted rates exemption information H - Review of Granted Rates Exemption |

> Program Environment:

| **Program Source**     | **Location**       | **Language / Compiler** |
|------------------------|--------------------|-------------------------|
| revMaintUpdate.aspx    | reis\\             | ASP.NET Web Form        |
| revMaintUpdate.aspx.vb | reis\\             | Code Behind VB.NET File |
| ReviewMaint.vb         | reis\class\REV\\   | VB.NET Class            |
| RXReviewDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |

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
<col style="width: 31%" />
<col style="width: 30%" />
<col style="width: 37%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>Floor(s) for Approved Rates Exemption Review</th>
<th>Selection of floor(s)</th>
<th>Floor(s) for Review</th>
</tr>
<tr class="header">
<th>Consideration</th>
<th><p>Reason,</p>
<p>UBW,</p>
<p>Ref/ Remarks</p></th>
<th>Consideration</th>
</tr>
<tr class="odd">
<th>Case Review Submission</th>
<th><p>Review Creation Date,</p>
<p>Urgent case,</p>
<p>Subject officer</p></th>
<th>Case Review Submission</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 4.4.1 - H - Review of Granted Rates Exemption |
|-----------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Floor(s) for Approved Rates Exemption Review is/are based on
floor(s) applied to the approved case (APR_FLOOR).</p></li>
<li><p>List of consideration reason options are based on type of breach
(SYS_BREACH).</p></li>
</ul>
<p><u>For saving of records:</u></p>
<ul>
<li><p>New cancellation case (CAN_CASE) record is created. Cancellation
submission information is updated to that record.</p></li>
<li><p>Floor(s) for Approved Rates Exemption Review is/are saved in
table RXV_FLOOR.</p></li>
<li><p>Consideration is saved in table RXV_BREACH.</p></li>
<li><p>UBW is saved in table RXV_UBW and RXV_UBW_FLOOR.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-009 – INPUT REVIEW RECORD: I - REVIEW
    STATUS</span>

| Program ID:   | REV-009                                                                                              |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                               |
| Program Name: | Input Review Record: I - Review Status                                                               |
| Description:  | This program is developed to capture review of granted rates exemption information I - Review Status |

> Program Environment:

| **Program Source**     | **Location**       | **Language / Compiler** |
|------------------------|--------------------|-------------------------|
| revMaintStatus.aspx    | reis\\             | ASP.NET Web Form        |
| revMaintStatus.aspx.vb | reis\\             | Code Behind VB.NET File |
| ReviewMaint.vb         | reis\class\REV\\   | VB.NET Class            |
| RXReviewDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |
| ReviewPendingDAO.vb    | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter**  | **Format**                             | **Description**                                                      |
|-----------------------|----------------|----------------------------------|
| Current status | \[Selection: RXV_CASE.REV_APP_STATUS\] | Selection of review process status. (Please refer processing logic). |

> Screen Layout:

| 4.4.2 - I - Review Status |
|---------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When page is loaded, display current application status based on
RXV_REVIEW.REV_APP_STATUS.</p>
<p><u>Selection of application status:</u></p>
<ul>
<li><p>When current status is &gt;= 14 (i.e. application has been
endorsed or final approved), the input of status will be disabled (i.e
the application status is read-only.)</p></li>
<li><p>Similarly, manually switch application status to 0 (receive
application) or ≥ 14 is not allowed.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-010 – INPUT REVIEW RECORD: I - INPUT
    RESPONSE</span>

| Program ID:   | REV-010                                                                                               |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                |
| Program Name: | Input Review Record: I - Input Response                                                               |
| Description:  | This program is developed to capture review of granted rates exemption information I - Input Response |

> Program Environment:

| **Program Source**       | **Location**       | **Language / Compiler** |
|--------------------------|--------------------|-------------------------|
| revMaintResponse.aspx    | reis\\             | ASP.NET Web Form        |
| revMaintResponse.aspx.vb | reis\\             | Code Behind VB.NET File |
| ReviewMaint.vb           | reis\class\REV\\   | VB.NET Class            |
| RXReviewDAO.vb           | reis\class\model\\ | DAO VB.NET Class        |
| MemoLetterDAO.vb         | reis\class\model\\ | DAO VB.NET Class        |
| ApplicationPendingDAO.vb | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format**  | **Length** | **Mandatory** | **Description** |
|---------------|-------------|------------|---------------|-----------------|
| Response Date | \[Date\]    |            | Y             | Response Date   |
| Remark        | X, \[Text\] | 100        |               | Remark          |

> Screen Layout:

| 3.1.4.7.2 - Input Response (oldvth-InputMemo.htm) |
|---------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When Save button is clicked:</u></p>
<ul>
<li><p>The related review pending record (RXV_PENDING) is opened and
updated. The response date will be served as pending end date of the
record.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-011 – INPUT REVIEW RECORD: I - GENERATE
    NEW MEMO / LETTER</span>

| Program ID:   | REV-011                                                                                                           |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                            |
| Program Name: | Input Review Record: I - Generate New Memo / letter                                                               |
| Description:  | This program is developed to capture review of granted rates exemption information I - Generate New Memo / letter |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| revMaintGenMemo.aspx    | reis\\             | ASP.NET Web Form        |
| revMaintGenMemo.aspx.vb | reis\\             | Code Behind VB.NET File |
| ReviewMaint.vb          | reis\class\REV\\   | VB.NET Class            |
| RXReviewDAO.vb          | reis\class\model\\ | DAO VB.NET Class        |
| MemoLetterDAO.vb        | reis\class\model\\ | DAO VB.NET Class        |

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
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 8%" />
<col style="width: 15%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Length</strong></th>
<th><strong>Mandatory</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>Issue Date</th>
<th>[Date]</th>
<th></th>
<th>Y</th>
<th>Issue Date</th>
</tr>
<tr class="header">
<th>Encl:</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Encl:</th>
</tr>
<tr class="odd">
<th>Memo/ letter type – To</th>
<th><p>1 - Applicant;</p>
<p>2 - DO;</p>
<p>3 - RVD;</p>
<p>4 - DLO or M/SC</p></th>
<th></th>
<th>Y</th>
<th>Memo/ letter type – To</th>
</tr>
<tr class="header">
<th>Memo / Letter Type – Template</th>
<th>Template of report / memo</th>
<th></th>
<th>Y</th>
<th>Template of letter / memo to be generated</th>
</tr>
<tr class="odd">
<th>Sender From</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Sender From</th>
</tr>
<tr class="header">
<th>Sender Ref</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Sender Ref</th>
</tr>
<tr class="odd">
<th>Sender Tel</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Sender Tel</th>
</tr>
<tr class="header">
<th>Sender Fax</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Sender Fax</th>
</tr>
<tr class="odd">
<th>Receiver To / Applicants name</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver To / Applicants name</th>
</tr>
<tr class="header">
<th>Receiver Attn</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Attn</th>
</tr>
<tr class="odd">
<th>Receiver Your ref.</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Your ref.</th>
</tr>
<tr class="header">
<th>Receiver Dated</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Dated</th>
</tr>
<tr class="odd">
<th>Receiver Fax No.</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Fax No.</th>
</tr>
<tr class="header">
<th>Receiver Total Pages</th>
<th>X, [alphanumeric]</th>
<th>40</th>
<th></th>
<th>Receiver Total Pages</th>
</tr>
<tr class="odd">
<th>CC</th>
<th><p>CVD/LandD/Land Registry, HAD</p>
<p>District</p>
<p>Note</p></th>
<th></th>
<th></th>
<th>CC list.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 3.1.4.7.2 - Input Response (oldvth-InputMemo.htm) |
|---------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When page is loaded:</u></p>
<ul>
<li><p>Default value of sender information (sender tel., sender from,
sender fax, sender ref) is retrieved from SYS_PARM.</p></li>
</ul>
<p><u>When Print button is clicked:</u></p>
<ul>
<li><p>Based on template selected, review pending record (RXV_PENDING)
is created. The issue date will be served as pending start date of the
record.</p></li>
<li><p>Record of memo &amp; letter (PRN_INFO, PRN_CC) is
created.</p></li>
<li><p>Open the corresponding report template to generate report in PDF
format.</p></li>
<li><p>The generated memo /letter is displayed in new windows.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-012 – INPUT REVIEW RECORD: I - INPUT
    RANDOM CHECK RESULTS</span>

| Program ID:   | REV-012                                                                                                           |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                            |
| Program Name: | Input Review Record: I - Input Random Check Results                                                               |
| Description:  | This program is developed to capture review of granted rates exemption information I - Input Random Check Results |

> Program Environment:

| **Program Source**           | **Location**       | **Language / Compiler** |
|-----------------------------|-------------------|-------------------------|
| revRandomCheckReults.aspx    | reis\\             | ASP.NET Web Form        |
| revRandomCheckReults.aspx.vb | reis\\             | Code Behind VB.NET File |
| RandomCheckResults.vb        | reis\class\REV\\   | VB.NET Class            |
| RXReviewDAO.vb               | reis\class\model\\ | DAO VB.NET Class        |
| RandomCheckDAO.vb            | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter**                                                                         | **Format**              | **Description**                                                                       |
|-----------------------|----------------|----------------------------------|
| Date of Inspection                                                                    | \[Date\]                | Date of Inspection                                                                    |
| Is the building larger than the permitted size                                        | \[Select: Yes \| No\]   | Is the building larger than the permitted size                                        |
| Any additional storey                                                                 | \[Select: Yes \| No\]   | Any additional storey                                                                 |
| Any rooftop structures exceeding the tolerated limits                                 | \[Select: Yes \| No\]   | Any rooftop structures exceeding the tolerated limits                                 |
| UBW                                                                                   | \[Selection: Floor(s)\] | Any unauthorized extension/addition found at floor(s)                                 |
| Description of Irregularities                                                         | X(100), \[Text\]        | Description of Irregularities                                                         |
| Is the building shared by a joint/communal staircase                                  | \[Select: Yes \| No\]   | Is the building shared by a joint/communal staircase                                  |
| Is resite valiage house with its official notification issued on or before 20.7.1992. | \[Select: Yes \| No\]   | Is resite valiage house with its official notification issued on or before 20.7.1992. |
| Receive date                                                                          | \[Date\]                | Receive date                                                                          |
| Encl                                                                                  | X(3), \[Alphanumeric\]  | Encl                                                                                  |

> Screen Layout:

| 4.4.2.1 - Input Random Check Results (review-InputRandomCheckResults.htm) |
|------------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When save button is clicked:</u></p>
<ul>
<li><p>Results are saved into random check case file table
(RAN_RX_FILE). the REVIEWID and response input date (RCD_RES_UPDDATE,
saved as record creation timestamp) is also saved into the record for
reference.</p></li>
<li><p>Any unauthorized extension/addition found at floor(s) selected
will be saved into random check floor result table
(RAN_RX_FLOOR).</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-013 – INPUT REVIEW RECORD: I - INPUT
    MATCHING CHECK RESULTS</span>

| Program ID:   | REV-013                                                                                                             |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                              |
| Program Name: | Input Review Record: I - Input Matching Check Results                                                               |
| Description:  | This program is developed to capture review of granted rates exemption information I - Input Matching Check Results |

> Program Environment:

| **Program Source**              | **Location**       | **Language / Compiler** |
|-----------------------------|-------------------|-------------------------|
| revMatchingCheckResults.aspx    | reis\\             | ASP.NET Web Form        |
| revMatchingCheckResults.aspx.vb | reis\\             | Code Behind VB.NET File |
| MatchingCheckResults.vb         | reis\class\REV\\   | VB.NET Class            |
| RXReviewDAO.vb                  | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter**                                  | **Format**              | **Description**                                |
|-----------------------|----------------|----------------------------------|
| Location                                       | X(100), \[Text\]        | Location description                           |
| Matched cases                                  | \[Selection: Floor(s)\] | Any matched case (selection of floor(s))       |
| File reference                                 | X(100), \[Text\]        | File reference                                 |
| Details of breach as at the date of inspection | X(100), \[Text\]        | Details of breach as at the date of inspection |
| Encl                                           | X(3), \[Alphanumeric\]  | Encl                                           |
| Date of Inspection                             | \[Date\]                | Date of Inspection                             |

> Screen Layout:

| 4.4.2.2 - Input Matching Check Results (review-InputMatchingCheckResults.htm) |
|------------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When save button is clicked:</u></p>
<ul>
<li><p>Results are saved into Approved Case Matching List Results table
(APR_MATCH_TEST).</p></li>
<li><p>Any matched case(s) will be saved into Matched case table
(APR_MATCH_CASE).</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-014 – INPUT REVIEW RECORD: I - MEMO FROM
    OTHER DEPTS / CONFIRMATION LETTER FROM APPLICANT</span>

| Program ID:   | REV-014                                                                                                                                           |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                                                            |
| Program Name: | Input Review Record: I - Memo from Other Depts / Confirmation letter from applicant                                                               |
| Description:  | This program is developed to capture review of granted rates exemption information I - Memo from Other Depts / Confirmation letter from applicant |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| revMaintExtMemo.aspx    | reis\\             | ASP.NET Web Form        |
| revMaintExtMemo.aspx.vb | reis\\             | Code Behind VB.NET File |
| ExtMemo.vb              | reis\class\REV\\   | VB.NET Class            |
| ExtMemoDAO.vb           | reis\class\model\\ | DAO VB.NET Class        |

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
<col style="width: 31%" />
<col style="width: 20%" />
<col style="width: 47%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>Memo / Letter Type – To</th>
<th><p>[Selection:</p>
<p>AP - Applicant;</p>
<p>DO - DO;</p>
<p>RV- RVD;</p>
<p>LD - DLO / M/SC]</p></th>
<th>Memo / Letter Type – To</th>
</tr>
<tr class="header">
<th>Date of memo received by HAD</th>
<th>[Date]</th>
<th>Date of memo received by HAD</th>
</tr>
<tr class="odd">
<th>remark</th>
<th>X(100), [Text]</th>
<th>remark</th>
</tr>
<tr class="header">
<th>Details of breach as at the date of inspection</th>
<th>X(100), [Text]</th>
<th>Details of breach as at the date of inspection</th>
</tr>
<tr class="odd">
<th>Encl</th>
<th>X(3), [Alphanumeric]</th>
<th>Encl</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 4.4.2.3 - Input Memo / Letter from Other Depts/Applicant |
|----------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When save button is clicked:</u></p>
<ul>
<li><p>Results are saved into Review memo received table
(RXV_EXT_MEMO).</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-015 – INPUT REVIEW RECORD: J -
    HISTORICAL RATES EXEMPTION APPLICATIONS AND GRANTED CASES</span>

| Program ID:   | REV-015                                                                                                                                          |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                                                           |
| Program Name: | Input Review Record: J - Historical Rates Exemption Applications and Granted Cases                                                               |
| Description:  | This program is developed to capture review of granted rates exemption information J - Historical Rates Exemption Applications and Granted Cases |

> Program Environment:

| **Program Source**    | **Location**       | **Language / Compiler** |
|-----------------------|--------------------|-------------------------|
| rxfileHistory.aspx    | reis\\             | ASP.NET Web Form        |
| rxfileHistory.aspx.vb | reis\\             | Code Behind VB.NET File |
| RXFileHistory.vb      | reis\class\REV\\   | VB.NET Class            |
| RXFileHistoryDAO.vb   | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter** | **Format** | **Description**       |
|---------------|------------|-----------------------|
| fileID        | N/A        | File ID of case file. |

> Screen Layout:

| 4.4.3 - J- Historical Rates Exemption Applications and Granted Cases |
|----------------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When page is loaded:</p>
<ul>
<li><p>All active records under same case file:</p>
<ul>
<li><blockquote>
<p>Exiting application being processed;</p>
</blockquote></li>
<li><blockquote>
<p>Completed application with approved case;</p>
</blockquote></li>
<li><blockquote>
<p>Completed application with rejected case;</p>
</blockquote></li>
<li><blockquote>
<p>Completed application with approved case and then cancelled are
selected</p>
</blockquote></li>
</ul></li>
</ul>
<blockquote>
<p><u>Note:</u></p>
<p>Same case which was approved and subsequently cancelled will be
presented in 2 rows for approval and cancellation.</p>
</blockquote>
<ul>
<li><p>The list is displayed in descending order of date:</p>
<ul>
<li><blockquote>
<p>For application, application receipt date is used for sorting</p>
</blockquote></li>
<li><blockquote>
<p>For approved / rejected / cancelled case, reply date (REPLY_DATE) is
used for sorting.</p>
</blockquote></li>
</ul></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">REV-016 – INPUT REVIEW RECORD: SAVE AND
    SUBMISSION</span>

| Program ID:   | REV-016                                                    |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                     |
| Program Name: | Input Review Record: Save and Submission                   |
| Description:  | This program is developed to save and submit review record |

> Program Environment:

| **Program Source** | **Location**       | **Language / Compiler** |
|--------------------|--------------------|-------------------------|
| ReviewMaint.vb     | reis\class\RXA\\   | VB.NET Class            |
| RXReviewDAO.vb     | reis\class\model\\ | DAO VB.NET Class        |
| RXCaseDAO.vb       | reis\class\model\\ | DAO VB.NET Class        |
| MemoLetterDAO.vb   | reis\class\model\\ | DAO VB.NET Class        |

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

| 4.4.1 - H - Review of Granted Rates Exemption |
|-----------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When Save button is clicked:</u></p>
<ul>
<li><p>Case records for cancellation case are created in CAN_CASE and
APR_FLOOR.</p></li>
<li><p>Redirect to summary list.</p></li>
</ul>
<p><u>When Save and submit button is clicked:</u></p>
<ul>
<li><p>Perform save action.</p></li>
<li><p>Review status (RXV_REVIEW.RXV_APP_STATUS) is updated to (13)
Submitted to endorsement officer.</p></li>
<li><p>For NFA case, memo / letter record for NFA letters will be
created. the memo/letter ID is also updated to the REJ_CASE
record.</p></li>
<li><p>Redirect to summary list.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">ENQ-001 – RATES EXEMPTION RECORD
    ENQUIRY</span>

| Program ID:   | ENQ-001                                                    |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                     |
| Program Name: | Rates Exemption Record Enquiry                             |
| Description:  | This program is developed to search rates exemption record |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| rxenquiry.aspx     | reis\\           | ASP.NET Web Form        |
| rxenquiry.aspx.vb  | reis\\           | Code Behind VB.NET File |
| RXEnquiry.vb       | reis\class\ENQ\\ | VB.NET Class            |

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
<col style="width: 31%" />
<col style="width: 43%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>Applicant name (English, Chinese)</th>
<th><p>X(100),</p>
<p>[Text]+[space]+[,]</p></th>
<th>Applicant name (English, Chinese)</th>
</tr>
<tr class="header">
<th>Applicant HKID</th>
<th>X(100), [Alphanumeric]+[space]+[,]=[()]</th>
<th>Applicant HKID</th>
</tr>
<tr class="odd">
<th>District</th>
<th>[Selection: DISTRICT]</th>
<th>District</th>
</tr>
<tr class="header">
<th>LM NO</th>
<th><p>X(50),</p>
<p>[numeric]+[space]+[,]</p></th>
<th>LM NO</th>
</tr>
<tr class="odd">
<th>DD</th>
<th><p>X(50),</p>
<p>[Alphanumeric]+[space]+[,]</p></th>
<th>DD</th>
</tr>
<tr class="header">
<th>Lot</th>
<th><p>X(50),</p>
<p>[Alphanumeric]+[space]+[,]</p></th>
<th>Lot</th>
</tr>
<tr class="odd">
<th>Address (English, Chinese)</th>
<th><p>X(200),</p>
<p>[Text]+[space]+[,]</p></th>
<th>Address (English, Chinese)</th>
</tr>
<tr class="header">
<th>CLL</th>
<th><p>X(50),</p>
<p>[Alphanumeric]+[space]+[,]</p></th>
<th>CLL</th>
</tr>
<tr class="odd">
<th>Rates assessment No.(s)</th>
<th><p>X(50),</p>
<p>[Alphanumeric]+[space]+[,]</p></th>
<th>Rates assessment No.(s)</th>
</tr>
<tr class="header">
<th>Application status (s)</th>
<th>[Selection: Application status]</th>
<th>Application status (s)</th>
</tr>
<tr class="odd">
<th>Long outstanding status(s)</th>
<th>[Selection: Long outstanding status]</th>
<th>Long outstanding status(s)</th>
</tr>
<tr class="header">
<th>urgent case</th>
<th>[checkbox: Yes | No]</th>
<th>urgent case</th>
</tr>
<tr class="odd">
<th>Record type</th>
<th><p>[Selection:</p>
<p>All |</p>
<p>Rates Exemption Record |</p>
<p>Approved Rates Exemption Case Review Record</p></th>
<th>Record type</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>10 - Enquiry – Rates Exemption Record Enquiry
(EnquiryRatesExemptionRecord.htm)</p>
<p>10.1 - Search Criteria</p>
<p>10.2 - Search Result (EnquiryRatesExemptionRecordResult.htm)</p></th>
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
<th><p><u>When search button is clicked:</u></p>
<ul>
<li><p>Address line 1 to line 5 are concatenated with space character
separating each line is used for matching with address provided by user.
“Like” operator is used in the string matching operation.</p></li>
<li><p>Surename and given name are concatenated with space character
separating is used for matching with name provided by user. English or
Chinese name of any grantee of approved case matched will be
retrieved.</p></li>
<li><p>Identifier (HKID_ID) and check digit (HKID_CD) of HKID are
combined as HKID_ID(HKID_CD) for matching with hkID provided by
user.</p></li>
<li><p>Following searching criteria allow multiple input with comma
character (,) as separator between each parameter:</p>
<ul>
<li><blockquote>
<p>Applicant name (English, Chinese);</p>
</blockquote></li>
<li><blockquote>
<p>Applicants’ ID;</p>
</blockquote></li>
<li><blockquote>
<p>LM No.;</p>
</blockquote></li>
<li><blockquote>
<p>Lot;</p>
</blockquote></li>
<li><blockquote>
<p>CLL;</p>
</blockquote></li>
<li><blockquote>
<p>Rates assessment no;</p>
</blockquote></li>
</ul></li>
<li><p>For record type selection:</p>
<ul>
<li><blockquote>
<p>When “ALL” is selected, the searching results contain 2 listing:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Listing 1: contain records of rates exemption application,
(approved/rejected/cancelled) cases</p>
</blockquote></li>
<li><blockquote>
<p>Listing 2: contain records of approved case review.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>When “Rates Exemption Record only” is selected, only Listing 1 will
be searched and displayed.</p>
</blockquote></li>
<li><blockquote>
<p>When “Approved Rates Exemption Review Record only” is selected, only
Listing 2 will be searched and displayed.</p>
</blockquote></li>
</ul></li>
<li><p>When multiple searching criteria are provided, criteria are
joined with “AND” operator for the searching.</p></li>
</ul>
<p>The search results are return and displayed to user.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">ENQ-002 – AUDIT LOG ENQUIRY</span>

| Program ID:   | ENQ-002                                                                            |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                             |
| Program Name: | Audit Log Enquiry                                                                  |
| Description:  | This program is developed to enquire audit log and dowload results into text file. |

> Program Environment:

| **Program Source**      | **Location**     | **Language / Compiler** |
|-------------------------|------------------|-------------------------|
| auditLogEnquiry.aspx    | reis\\           | ASP.NET Web Form        |
| auditLogEnquiry.aspx.vb | reis\\           | Code Behind VB.NET File |
| AuditLogEnquiry.vb      | reis\class\ENQ\\ | VB.NET Class            |

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
<col style="width: 31%" />
<col style="width: 20%" />
<col style="width: 47%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Parameter</strong></th>
<th><strong>Format</strong></th>
<th><strong>Description</strong></th>
</tr>
<tr class="odd">
<th>Audit log type</th>
<th><p>[Selection:</p>
<p>Audit log type]</p></th>
<th>Audit log type</th>
</tr>
<tr class="header">
<th>Audit log period</th>
<th>[Date range]</th>
<th>Audit log period</th>
</tr>
<tr class="odd">
<th>Password</th>
<th><p>X(20),</p>
<p>[Alphanumeric]</p></th>
<th>Password</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> Screen Layout:

| 11 - Audit Log Enquiry (EnquiryAuditLog.htm) |
|----------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>When Generate button is clicked:</p>
<ul>
<li><p>According to audit log type, date period, related audit tables
are retrieved and written into CSV format.</p></li>
<li><p>The text file is saved in the audit log file directory (defined
in system config file).</p></li>
<li><p>The text file is renamed as “audit_log” + USERID + YYYYMMDDHHMISS
+ “.csv”. (whereYYYYMMDDHHMISS stand for generation date time).</p></li>
<li><p>The text file is then zipped with encryption using password
provided by user.</p></li>
<li><p>The zip file should have file name = text file’s file name +
“.zip”.</p></li>
<li><p>After zip file is created, the original plain text file and
previous generated file are deleted.</p></li>
<li><p>The generated zip file is return and downloaded by user.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">ENQ-003 – AD-HOC REPORT</span>

| Program ID:   | ENQ-003                                                      |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                       |
| Program Name: | Ad-hoc Report                                                |
| Description:  | This program is developed to user to generate ad-hoc report. |

> Program Environment:

| **Program Source**  | **Location**     | **Language / Compiler** |
|---------------------|------------------|-------------------------|
| rxahenquiry.aspx    | reis\\           | ASP.NET Web Form        |
| rxahenquiry.aspx.vb | reis\\           | Code Behind VB.NET File |
| AdHocEnquiry.vb     | reis\class\ENQ\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Input Parameters:

| **Parameter**                  | **Format** | **Description** |
|--------------------------------|------------|-----------------|
| Please refer to Screen layout. |            |                 |

> Screen Layout:

| 12.2 - Ad-hoc (Ad-hoc.htm) |
|----------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><u>When search button is clicked:</u></p>
<ul>
<li><p>(communication address &amp; village house address) Address line
1 to line 5 are concatenated with space character separating each line
is used for matching with address provided by user. “Like” operator is
used in the string matching operation.</p></li>
<li><p>Surename and given name are concatenated with space character
separating is used for matching with name provided by user. English or
Chinese name of any grantee of approved case matched will be
retrieved.</p></li>
<li><p>Identifier (HKID_ID) and check digit (HKID_CD) of HKID are
combined as HKID_ID(HKID_CD) for matching with hkID provided by
user.</p></li>
<li><p>Following searching criteria allow multiple input with comma
character (,) as separator between each parameter:</p>
<ul>
<li><blockquote>
<p>Applicant name (English, Chinese);</p>
</blockquote></li>
<li><blockquote>
<p>Applicants’ ID;</p>
</blockquote></li>
<li><blockquote>
<p>LM No.;</p>
</blockquote></li>
<li><blockquote>
<p>Lot;</p>
</blockquote></li>
<li><blockquote>
<p>CLL;</p>
</blockquote></li>
<li><blockquote>
<p>Rates assessment no;</p>
</blockquote></li>
</ul></li>
<li><p>For record type selection:</p>
<ul>
<li><blockquote>
<p>When “ALL” is selected, the searching results contain 2 listing:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Listing 1: contain records of rates exemption application,
(approved/rejected/cancelled) cases</p>
</blockquote></li>
<li><blockquote>
<p>Listing 2: contain records of approved case review.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>When “Rates Exemption Record only” is selected, only Listing 1 will
be searched and displayed.</p>
</blockquote></li>
<li><blockquote>
<p>When “Approved Rates Exemption Review Record only” is selected, only
Listing 2 will be searched and displayed.</p>
</blockquote></li>
</ul></li>
<li><p>When multiple searching criteria are provided, criteria are
joined with “AND” operator for the searching.</p></li>
</ul>
<p>When output format = screen, the search results are return and
displayed to user.</p>
<p>When output format = Excel/CSV file:</p>
<ul>
<li><p>The search results are retrieved and written into CSV
format.</p></li>
<li><p>The text file is saved in the ad-hoc report file directory
(defined in system config file).</p></li>
<li><p>The text file is renamed as “ad-hoc” + USERID + YYYYMMDDHHMISS +
“.CSV”. (where YYYYMMDDHHMISS stand for generation date time).</p></li>
<li><p>The text file is then zipped with encryption using password
provided by user.</p></li>
<li><p>The zip file should have file name = text file’s file name +
“.zip”.</p></li>
<li><p>After zip file is created, the original plain text file and
previous generated file are deleted.</p></li>
<li><p>The generated zip file is return and downloaded by user.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">GEN-001 – SYSTEM PARAMETER</span>

| Program ID:   | GEN-001                                                         |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                          |
| Program Name: | System Parameter                                                |
| Description:  | This program is developed to user to maintain system parameter. |

> Program Environment:

| **Program Source**           | **Location**       | **Language / Compiler** |
|-----------------------------|-------------------|-------------------------|
| maintSystemParameter.aspx    | reis\\             | ASP.NET Web Form        |
| maintSystemParameter.aspx.vb | reis\\             | Code Behind VB.NET File |
| SystemParameter.vb           | reis\class\GEN\\   | VB.NET Class            |
| SystemParameterDAO.vb        | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

| 13.3 - System Parameters (SystemParameters.htm) |
|-------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>On load of System Parameter input form:</p>
<ul>
<li><p>The system parameter is retrieved and displayed in the input form
page</p></li>
</ul>
<p>On clicking of "Save" button:</p>
<ul>
<li><p>The updated system parameter is saved in the database.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">GEN-002 – TYPE OF BREACH</span>

| Program ID:   | GEN-002                                                                           |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                            |
| Program Name: | Type of Breach                                                                    |
| Description:  | This program is developed to user to maintain system code table of Type of Breach |

> Program Environment:

| **Program Source**      | **Location**       | **Language / Compiler** |
|-------------------------|--------------------|-------------------------|
| maintBreachType.aspx    | reis\\             | ASP.NET Web Form        |
| maintBreachType.aspx.vb | reis\\             | Code Behind VB.NET File |
| SystemParameter.vb      | reis\class\GEN\\   | VB.NET Class            |
| BreachTypeDAO.vb        | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>13.4.1 - Type of Breach</p>
<p>13.4.1.1 - New Type of Breach (BreachTypeAdd.htm)</p>
<p>13.4.1.2 - Type of Breach List (BreachTypeList.htm)</p>
<p>13.4.1.3 - Type of Breach Update (BreachTypeEdit.htm)</p>
<p>13.4.1.4 - UBW Add(UBWAdd.htm)</p>
<p>13.4.1.5 - UBW Update(UBWEdit.htm)</p></th>
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
<th><p>On load of the page:</p>
<ul>
<li><p>The list of type of breach and UBW are retrieved and displayed in
the input form page</p></li>
</ul>
<p>On Add New button of Type of breach / UBW:</p>
<ul>
<li><p>The input form is displayed for creation of new record.</p></li>
<li><p>Validation checking including duplicate system code should be
performed.</p></li>
</ul>
<p>On Edit button of Type of breach / UBW:</p>
<ul>
<li><p>The selected record is retrieved from the corresponding system
code table.</p></li>
<li><p>The input form is displayed for editing of the record.</p></li>
<li><p>The system code (i.e. Type of Breach code and UBW code) is unique
identifier of the record, therefore editing of these fields should not
be allowed in the update function.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">GEN-003 – DISTRICT</span>

| Program ID:   | GEN-003                                                                     |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                      |
| Program Name: | District                                                                    |
| Description:  | This program is developed to user to maintain system code table of District |

> Program Environment:

| **Program Source**    | **Location**       | **Language / Compiler** |
|-----------------------|--------------------|-------------------------|
| maintDistrict.aspx    | reis\\             | ASP.NET Web Form        |
| maintDistrict.aspx.vb | reis\\             | Code Behind VB.NET File |
| District.vb           | reis\class\GEN\\   | VB.NET Class            |
| DistrictDAO.vb        | reis\class\model\\ | DAO VB.NET Class        |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

| 13.4.2 - District |
|-------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>On load of the page:</p>
<ul>
<li><p>The list of district are retrieved and displayed in the input
form page</p></li>
</ul>
<p>On Add New button of district:</p>
<ul>
<li><p>The input form is displayed for creation of new record.</p></li>
<li><p>Validation checking including duplicate system code should be
performed.</p></li>
</ul>
<p>On Edit button of district:</p>
<ul>
<li><p>The selected record is retrieved from the corresponding system
code table.</p></li>
<li><p>The input form is displayed for editing of the record.</p></li>
<li><p>The district code is unique identifier of the record, therefore
editing of district code should not be allowed in the update
function.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">COM-001 – INSERTION NEW AUDIT LOG</span>

| Program ID:   | COM-001                                                     |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                      |
| Program Name: | Insertion new audit log                                     |
| Description:  | This common module is developed to insert audit log record. |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| AuditLogInsert.vb  | reis\class\GEN\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> File Usage:

| **File/Table Name**            | **Location** | **Usage** | **Access Mean** |
|--------------------------------|--------------|-----------|-----------------|
| Please refer to Program logic. |              |           |                 |

> Screen Layout:

| N/A |
|-----|

> Processing Logic:

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><ol type="1">
<li><p>Following type of audit log tables will be maintained in the
system:</p></li>
</ol>
<table>
<colgroup>
<col style="width: 6%" />
<col style="width: 28%" />
<col style="width: 15%" />
<col style="width: 22%" />
<col style="width: 27%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Type of Audit Log Database Table</strong></th>
<th><strong>Table name</strong></th>
<th><strong>Audit Log Record</strong></th>
<th><strong>Scope</strong></th>
</tr>
<tr class="odd">
<th>1</th>
<th>User Login Attempt</th>
<th>LOG_LOGIN</th>
<th>Audit Log for user login and failure login attempts</th>
<th>Login ID, Login date time, login results, error message</th>
</tr>
<tr class="header">
<th>2</th>
<th>User access</th>
<th>LOG_ACCESS</th>
<th>Audit Log for User access function</th>
<th>Login ID, access function, access results, error message</th>
</tr>
<tr class="odd">
<th rowspan="7">3</th>
<th rowspan="7">Record transaction(New / Update / Delete)</th>
<th rowspan="7">LOG_&lt;Table name&gt;</th>
<th>Audit Log for User change password</th>
<th>PASSWD_HIST</th>
</tr>
<tr class="header">
<th>Audit Log for Transaction of creation / amendment of rates exemption
file</th>
<th>RX_FILE</th>
</tr>
<tr class="odd">
<th>Audit Log for Transaction of creation / amendment of rates exemption
case</th>
<th>RXA_APP, APR_CASE, REJ_CASE, CAN_CASE and all their child
tables</th>
</tr>
<tr class="header">
<th>Audit Log for Transaction of creation / amendment of case
review</th>
<th>RXV_CASE and all its child tables.</th>
</tr>
<tr class="odd">
<th>Audit Log for generation of random check selection</th>
<th>RAN_HDR and all its child tables</th>
</tr>
<tr class="header">
<th>Audit Log for change in User account</th>
<th>REIS_USER</th>
</tr>
<tr class="odd">
<th>Audit Log for change in user role access permission</th>
<th>REIS_PERMISSION</th>
</tr>
<tr class="header">
<th>4</th>
<th>change application status</th>
<th>LOG_APP_STATUS</th>
<th>Audit Log for change of application status</th>
<th>LM No. Application ID, Appliation status</th>
</tr>
<tr class="odd">
<th>5</th>
<th>change review status</th>
<th>LOG_REV_STATUS</th>
<th>Audit Log for change of review status</th>
<th>LM No. Approved Case ID, Review ID, Review status</th>
</tr>
<tr class="header">
<th>6</th>
<th>endorsement</th>
<th>LOG_ENDORSEMENT</th>
<th>Audit Log for endorsement of rates exemption case</th>
<th>LM No. Application ID, Review ID, Case ID, Endorsed Approved /
Rejected / Cancelled,</th>
</tr>
<tr class="odd">
<th>7</th>
<th>Approval</th>
<th>LOG_APPROVAL</th>
<th>Audit Log for approval of rates exemption case</th>
<th>LM No. Application ID, Review ID, Case ID, Approval of Approved /
Rejected / Cancelled,</th>
</tr>
<tr class="header">
<th>8</th>
<th>memo generation</th>
<th>LOG_MEMO</th>
<th>Audit Log for generation of memo</th>
<th>LM No. Memo to, Template, Generation date time</th>
</tr>
<tr class="odd">
<th>9</th>
<th>letter generation</th>
<th>LOG_LETTER</th>
<th>Audit Log for generation of letter</th>
<th>LM No. Letter send to, Template, Generation date time</th>
</tr>
<tr class="header">
<th>10</th>
<th>Enquiry</th>
<th>LOG_ENQUIRY</th>
<th>Audit Log for record enquiry</th>
<th>Search function name, Search criteria used (key=field name |
value=user input, …)</th>
</tr>
<tr class="odd">
<th rowspan="2">11</th>
<th rowspan="2">Report generation</th>
<th rowspan="2">LOG_REPORT</th>
<th>Audit Log for generating report</th>
<th>Report ID , Genration criteria used (key=field name | value=user
input, …)</th>
</tr>
<tr class="header">
<th>Audit Log for generation of export of outstanding report</th>
<th>Report ID , Genration criteria used (key=field name | value=user
input, …)</th>
</tr>
<tr class="odd">
<th>12</th>
<th>matching list generation</th>
<th>LOG_MATCHLIST</th>
<th>Audit Log for generation of matching list</th>
<th>Generation date time</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<ol start="2" type="1">
<li><p>For all audit log table, following fields will be served as log
header:</p></li>
</ol>
<ul>
<li><p>Log date time;</p></li>
<li><p>User ID;</p></li>
<li><p>Audit log record type</p></li>
<li><p>Action (New / Update / Delete)</p></li>
<li><p>Image type (Old / New)</p></li>
</ul>
<ol start="3" type="1">
<li><p>For audit log table (3) - Record transaction(New / Update /
Delete):</p></li>
</ol>
<ul>
<li><p>Since records of different table type (e.g. Application table
have child table of application’s applicants etc) could be involved in
one transaction, additional header fields are required:</p>
<ul>
<li><blockquote>
<p>Log date time;</p>
</blockquote></li>
<li><blockquote>
<p>User ID;</p>
</blockquote></li>
<li><blockquote>
<p>Audit log record type</p>
</blockquote></li>
<li><blockquote>
<p>Action (New / Update / Delete)</p>
</blockquote></li>
<li><blockquote>
<p>Transaction timestamp (in yyyymmddhhmissms format, same timestamp
should be used by all tables involved in the same transaction)</p>
</blockquote></li>
<li><blockquote>
<p>Image type (Old / New)</p>
</blockquote></li>
</ul></li>
</ul>
<p>after header fields, details fields contain all columns of
corresponding table.</p>
<ol start="4" type="1">
<li><p>For audit log table (10) – Enquiry and (11) Report
Generation:</p></li>
</ol>
<ul>
<li><p>Searching criteria submitted by user is saved in one text field
with format of (key=field name | value=user input, …)</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RPT-001 – RF0001- APPLICATION LISTING</span>

| Program ID:   | RPT-001                                                                  |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                   |
| Program Name: | RF0001- Application Listing                                              |
| Description:  | This program is developed to generate report RF0001- Application Listing |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| rpt0001.aspx       | reis\\           | ASP.NET Web Form        |
| rpt0001.aspx.vb    | reis\\           | Code Behind VB.NET File |
| RPT0001.vb         | reis\class\RPT\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> Screen Layout:

| 12.3 - RF0001 - Application List (RF0001-ApplicationList.htm) |
|---------------------------------------------------------------|

> Processing Logic:

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 54%" />
<col style="width: 29%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>No.</strong></th>
<th><strong>Description</strong></th>
<th><strong>Purpose</strong></th>
</tr>
<tr class="odd">
<th>RF0001</th>
<th>Application Listing</th>
<th rowspan="5">List out the information of different types of rates
exemptions application records.</th>
</tr>
<tr class="header">
<th>RF0001A</th>
<th><blockquote>
<p>Application Listing - Received</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>RF0001B</th>
<th><blockquote>
<p>Application Listing - Processed</p>
</blockquote></th>
</tr>
<tr class="header">
<th>RF0001C</th>
<th><blockquote>
<p>Application Listing - Backlog</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>RF0001D</th>
<th><blockquote>
<p>Application Listing - Cancelled</p>
</blockquote></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0001A Application Listing – Received

<img src="media/image15.png" style="width:9.68472in;height:3.87569in" />

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
<p>Application receipt date range</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th>Sort on district code, ‘name of subject officer’, Application date,
LM No.</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The output is grouped by district code. Within each district code
group, it is further grouped by ‘name of subject officer’.</p>
<p>Each district code group will have a district total, and each ‘name
of subject officer’ group inside a district code group will have an
officer total. At the end of the report, there will have ‘totals’ which
is the number of records printed out in this report.</p>
<p>The application approval status should be A--Approved, N--NFA,
Rejected--Others or Rejected—UBW. The cancelled applications should not
be included in the table. The date of application/reconsideration of the
application must be within the specified period of the user.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0001B Application Listing – Processed

<img src="media/image4.png" style="width:9.69306in;height:4.01111in" />

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
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
<p>Application receipt date range or reply date range</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th>Sort on district code, application approval status, ‘name of subject
officer’, application date, LM No.</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The output is grouped by district code. Within each district code
group, it is further grouped by application approval status. Within each
application approval status group, it is further grouped by ‘name of
subject officer’.</p>
<p>Each district code group will have a district total, and each
application approval status group inside a district code group will have
an application approval status total. Each ‘name of subject officer’
group in an application approval status group which is in a district
code group will have an officer total. At the end of the report, there
will have ‘totals’ which is the number of records printed out in this
report.</p>
<p>The application approval status shown in this table includes
Approved, NFA, Rejected—Others and Rejected—UBW. The cancelled
applications should not be included in the table. The reply date of the
applications selected must be non-empty, which means they must not be
outstanding cases.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0001C Application Listing – Backlog

<img src="media/image16.png" style="width:9.69236in;height:4.00972in" />

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
<p>Outstanding as at</p></th>
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
<th><p>The output is grouped by district code. Within each district code
group, it is further grouped by ‘name of subject officer’.</p>
<p>Each district code group will have a district total, and each ‘name
of subject officer’ group inside a district code group will have an
officer total. At the end of the report, there will have ‘totals’ which
is the number of records printed out in this report.</p>
<p>If the date of application/reconsideration of the record is before
the specified input date, and the reply date of the record is either
empty or after the specified input date, then the record satisfy the
searching criteria, and it will be included in the output.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0001D Application Listing – Cancelled

<img src="media/image12.png" style="width:9.68819in;height:3.84097in" />

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
<th>Sort on district code, application approval status, ‘name of subject
officer’, application date, LM No.</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The output is grouped by district code. Within each district code
group, it is further grouped by application approval status. Within each
application approval status group, it is further grouped by ‘name of
subject officer’.</p>
<p>Each district code group will have a district total, and each
application approval status group inside a district code group will have
an application approval status total. Each ‘name of subject officer’
group in an application approval status group which is in a district
code group will have an officer total. At the end of the report, there
will have ‘totals’ which is the number of records printed out in this
report.</p>
<p>The application approval status shown in this table includes
Cancelled--Others and Cancelled—UBW. Only cancelled applications are
included in the table.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RPT-002 – RF0002-OUTSTANDING CASE
    REPORT</span>

| Program ID:   | RPT-002                                                                     |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                      |
| Program Name: | RF0002-Outstanding Case Report                                              |
| Description:  | This program is developed to generate report RF0002-Outstanding Case Report |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| rpt0002.aspx       | reis\\           | ASP.NET Web Form        |
| rpt0002.aspx.vb    | reis\\           | Code Behind VB.NET File |
| RPT0002.vb         | reis\class\RPT\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> Screen Layout:

| 12.4 - RF0002 - Outstanding Case Report (RF0002-OutstandingCaseReport.htm ) |
|------------------------------------------------------------------------|

> Processing Logic:
>
> RF0002A Outstanding cases received by date range

<img src="media/image13.png" style="width:9.69097in;height:1.86944in" />

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
<p>Rate Exemption Case Applicant/ Grantee</p></th>
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
<th>Sort on district code, LM No.</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>In Rates Exemption Case, if reply date is empty, It can be
regarded as cases that are outstanding. If the application date of these
cases is within the specified period, they will be print out.</p>
<p>The output is grouped by district code.</p>
<p>Each district code group will have a district total. At the end of
the report, there will have ‘grand total’ which is the number of records
printed out in this report.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0002B Outstanding cases received before a date

<img src="media/image3.png" style="width:4.35486in;height:5.96319in" />

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
<p>Date range</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th>Sort on LM No., application date.</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th>In Rates Exemption Case, if reply date is empty, It can be regarded
as cases that are outstanding. If the application date of the
outstanding cases are before the specified input date, these cases will
be print out.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

> RF0002C All outstanding cases

<img src="media/image9.png" style="width:7.69931in;height:5.77569in" />

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
<p>Rate Exemption Case Applicant/ Grantee</p></th>
</tr>
<tr class="odd">
<th>Orientation:</th>
<th>A4, Landscape</th>
</tr>
<tr class="header">
<th>Searching Criteria :</th>
<th>Nil</th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th>Sort on district code, LM No.</th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>In Rates Exemption Case, if reply date is empty, It can be
regarded as cases that are outstanding. These cases will be print
out.</p>
<p>The output is grouped by district code.</p>
<p>Each district code group will have a district total. At the end of
the report, there will have ‘grand total’ which is the number of records
printed out in this report.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RPT-003 – RF0003-APPROVED CASES/ REJECTED
    CASES/ CANCELLED CASES REPORT</span>

| Program ID:   | RPT-003                                                                                                    |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                                                                     |
| Program Name: | RF0003-Approved cases/ Rejected cases/ Cancelled cases Report                                              |
| Description:  | This program is developed to generate report RF0003-Approved cases/ Rejected cases/ Cancelled cases Report |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| rpt0003.aspx       | reis\\           | ASP.NET Web Form        |
| rpt0003.aspx.vb    | reis\\           | Code Behind VB.NET File |
| RPT0003.vb         | reis\class\RPT\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> Screen Layout:

| 12.5 - RF0003 - Approved cases/ Rejected cases/ Cancelled cases report (RF0003-CasesReport.htm) |
|------------------------------------------------------------------------|

> Processing Logic:

<img src="media/image18.png" style="width:9.68403in;height:4.50486in" />

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
<p>Rate Exemption Case Applicant/ Grantee</p></th>
</tr>
<tr class="odd">
<th>Orientation:</th>
<th>A4, Landscape</th>
</tr>
<tr class="header">
<th>Searching Criteria :</th>
<th><p>User can specify the following searching criteria:</p>
<p>Application status (approved, rejected or cancelled).</p>
<p>After that user have 2 options to choose. Option 1 is to print all
cases with the same approval status in name sequence. Option 2 is to
print all cases with the same approval status in Id no.
sequence.</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th><p>When option 1 (i.e. in name sequence) is selected, it does
sorting on name.</p>
<p>When option 2 (i.e. in ID. No. sequence) is selected, it does sorting
on HKID No.</p></th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Ad hoc</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>Depends on which status (i.e. approved, rejected or cancelled) is
selected, it will print all cases with the same approval status.</p>
<p>At the end of the report, there will have a ‘total’ which is the
total number of records printed out.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  <span class="smallcaps">RPT-004 – RF0004-MONTHLY REPORT</span>

| Program ID:   | RPT-004                                                            |
|-------------------|-----------------------------------------------------|
| Mode:         | Online                                                             |
| Program Name: | RF0004-Monthly Report                                              |
| Description:  | This program is developed to generate report RF0004-Monthly Report |

> Program Environment:

| **Program Source** | **Location**     | **Language / Compiler** |
|--------------------|------------------|-------------------------|
| rpt0004.aspx       | reis\\           | ASP.NET Web Form        |
| rpt0004.aspx.vb    | reis\\           | Code Behind VB.NET File |
| RPT0004.vb         | reis\class\RPT\\ | VB.NET Class            |

> Amendment History:

| **Change Number** | **Revision Description** | **Revision Number** | **Date** |
|-----------------------|--------------------|--------------------|----------|

> Screen Layout:

| 12.6 - RF0004 - Monthly Reports (RF0004-MonthlyReports.htm) |
|-------------------------------------------------------------|

> Processing Logic:

<img src="media/image11.png" style="width:5.67778in;height:5.90694in" />

<img src="media/image2.png" style="width:6.20764in;height:2.59097in" />

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
<p>Rate Exemption Case Review</p></th>
</tr>
<tr class="odd">
<th>Orientation:</th>
<th>A4, Landscape</th>
</tr>
<tr class="header">
<th>Searching Criteria :</th>
<th><p>User can specify the following searching criteria:</p>
<p>Month and year</p></th>
</tr>
<tr class="odd">
<th>Sorting Sequence :</th>
<th><p>For the first part, sort on LM No.</p>
<p>For the second part, sorting is not required.</p></th>
</tr>
<tr class="header">
<th>Frequency :</th>
<th>Monthly</th>
</tr>
<tr class="odd">
<th>Logic:</th>
<th><p>The report is divided into two parts.</p>
<p><strong>Description of the first part</strong>:</p>
<p>For the first part, the report is group by different types of cases.
The groups includes approved, rejected, NFA, new and reopen cases. The
reply dates of the applications selected have to be within the input
year and month of the user. For the applications that meet the criteria,
the LM No. together with the district code is printed out, grouped by
types of cases.</p>
<p>Description of different types of cases:</p>
<p>If the approval status of either one of its floor is “A”, then the
case is approved,</p>
<p>Else if the approval status of either one of its floor is “R”, then
the case is rejected.</p>
<p>Else if the approval status of either one of its floor is “N”, then
the case is no further action.</p>
<p>If the record exists in the Rate Exemption Case table, then it is a
new case.</p>
<p>If the record exists in the Rates Exemption Case Review table, then
it is a reopen case.</p>
<p><strong>Description of the second part</strong>:</p>
<p>The second part is a summary which summarize the number of different
types of cases occurs in different district. There are seven types of
cases, which include B/F case, new case, reopen case, approved case,
rejected case, NFA case and C/F case. Numbers shown in part B is counted
by different counters.</p>
<p>Description of different types of cases:</p>
<p>B/F case is the case which the date of application/reconsideration is
earlier than the input month and year. Moreover, date of reply have to
be empty, equal or later than the input month and year.</p>
<p>For new case, reopen case, approved case, rejected case and NFA case,
the definition is the same as that described in part one.</p>
<p>For number of C/F case in a district, it is equal to:</p>
<p>Number of B/F case in that district + number of new case in that
district + number of reopen case in that district – number of approved
case in that district – number of rejected case in that district –
number of NFA case in that district.</p></th>
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
