<img src="media/image1.jpg" style="width:2.03125in;height:1.52083in"
alt="BDlogo" />

**<span class="smallcaps">SYSTEM TEST PLAN, SPECIFICATION AND</span>**

**<span class="smallcaps">RESULTS</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">COMBINED SYSTEM DEVELOPMENT SERVICES
FOR</span>**

**<span class="smallcaps">PILOT PROJECT OF</span>**

**<span class="smallcaps">COMMON DIGITAL PLATFORM FOR SITE
SUPERVISION</span>**

**<span class="smallcaps">OF THE</span>**

**<span class="smallcaps">BUILDINGS DEPARTMENT</span>**

Version : 1.0

**Apr 2024**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR

| **Distribution** |                             |
|------------------|-----------------------------|
| Copy No.         | Holder                      |
| 1                | Buildings Department (BD)   |
| 2                | Master Concept Limited (MC) |

| **Amendment History** |                      |                                      |                           |           |                    |
|----------|-----------------------|-------------|----------|---------|----------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date      | Approval Reference |
| 1.0                   | Baseline             |                                      | 1.0                       | 17-Apr-24 |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |
|                       |                      |                                      |                           |           |                    |

**<u>Table of Contents</u>**

[1.](#overview) Overview 3

[1.1](#introduction) Introduction 3

[1.2](#purpose-of-document) Purpose of Document 3

[1.3](#document-of-organization) Document of Organization 3

[2.](#purpose) Purpose 3

[3.](#scope) Scope 4

[4.](#test-plan) Test Plan 4

[4.1 Test Schedule 5](#test-schedule)

[4.2](#role-and-responsibilities) Role and Responsibilities 5

[4.3](#acceptance-criteria) Acceptance Criteria 5

[5.](#test-specification) Test Specification 6

[5.1](#test-control-procedures) Test Control Procedures 6

[5.3](#cases-summary) Cases Summary 7

[5.4](#test-scope) Test scope 10

[6.](#test-cases-result) Test Cases Result 11

# Overview

## Introduction

This document is the System Integration Test Plan for the Combined
System Development Services for Pilot Project of CDPSS of the Buildings
Department. It provides a detailed description and result of the System
Integration Test.

## Purpose of Document

This document describes the scope, methodology, procedures, control,
responsible parties, schedule, and other necessary arrangements for the
SIT of CDPSS. This plan and specification provide the baseline for the
SIT to prove that the System is able to meet the functional
specifications and data migration specifications as specified in the
Project Specifications of the Tender.

## Document of Organization

This document consists of the following sections-

1.  The ‘Overview’ section is to explain the contents and purposes of
    this document;

2.  The ‘Test Plan’ section refers to the testing approach adopted for
    the SIT and identify the role and responsibilities of the relevant
    parties;

3.  The ‘Test Specification’ section describes the control procedures,
    test entry and termination criteria and the necessary arrangements
    for setting up the testing environment, test data and database, and
    the test cases for the SIT; and

4.  The ‘Test Report’ section describes the content of functional test
    reports for the SIT, A description of the test cases, including the
    description, involved role, result, actual date and system
    environment

# Purpose

The purposes of this System Test Plan are:

-   To define the types of tests to be carried out on the system

-   To define the requirements for test data to be used

-   To establish the test data which will enable the system as a whole
    > to be tested according to the Plan and Specification

-   To show the outcome of the system tests, including re-testing
    > carried out after any necessary corrective has been taken.

# Scope

The tests are focused on the functional, non-functional and technical
features of the new Information Framework system.

1.  Function Test of

    1.  Information Framework Web Site

    2.  Institution Web-Site

    3.  Administration Module

2.  System Integration Test

    1.  System backup, Fall-back and Recovery Test

    2.  Performance , Stress and Load Test

-   **Function Test**

The objective of the function test is to measure the effectiveness and
efficiency of the system in compliance with the User Requirements and
System Design. The Function Test is based on the Function Test Plan,
which contains itinerary and procedures to cover the test cases based
upon user requirements.

-   **System Backup, Fall-back and Recovery Test**

The backup and recovery test is to test that the system are protected
from various types of failure and be able to recover to a consistent
state after failure.

-   **Performance, Stress and Load Test**

The objective of performance test is to determine the amount of
execution time spent on various parts of the program. Many programs have
specific performance or efficiency objectives, such as response times
and throughput rates under certain workload and configuration
conditions. Performance testing should attempt to show that the system
does not satisfy its performance objectives.

# Test Plan

This test plan is divided into two parts - function tests and system
integration tests.

In the function tests, the following functional areas will be tested:

1.  User Management

2.  Form and Record

3.  Report and Alert

The system integration test will be taken after all the components have
been fully tested and integrated.

1.  System backup, Fallback and Recovery Test

2.  Performance, Stress and Load Test

## 4.1 Test Schedule

|     | **Test Tasks**                                  | **Estimated Effort** | **Start Date** | **End Date** | **Responsible by** |
|-----|--------------------------|----------|-----------|----------|------------|
| 1   | Prepare and review SIT test plan and test cases | 60 days              | Sep 2022       | Nov 2023     | MC and ITU         |
| 2   | Functional Test for non-production servers      | 11 months            | Nov 10, 2022   | Oct 30, 2023 | MC                 |
| 3   | System Tests on non-production servers          | 11 months            | Nov 10, 2022   | Oct 30, 2023 | MC                 |
| 4   | Functional Test for pre-production servers      | 2 days               | Dec 18, 2023   | Dec 20, 2023 | MC                 |
| 5   | System Tests for pre-production servers         | 2 days               | Dec 18, 2023   | Dec 20, 2023 | MC                 |

## 4.2 Role and Responsibilities

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 66%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Team / Role</strong></th>
<th><strong>Responsibilities</strong></th>
</tr>
<tr class="odd">
<th>BD ITU</th>
<th><ul>
<li><p>Liaise with CPDSS Contractor and other related parties for the
setup of SIT environments.</p></li>
<li><p>Arrange necessary testing facilities and equipment for
SIT.</p></li>
<li><p>Perform tests according to the predefined test cases.</p></li>
</ul></th>
</tr>
<tr class="header">
<th>MC – Project Team</th>
<th><ul>
<li><p>Develop detailed work plan and build test cases.</p></li>
<li><p>Perform tests according to the predefined test cases.</p></li>
<li><p>Compile SIT Report</p></li>
<li><p>Analyse and rectify problems related to the CDPSS System reported
in SIT Report.</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 4.3 Acceptance Criteria

At the end of each batch of the System Integration Test, all outstanding
incidents should be cleared.

The acceptance criteria include the following conditions:

-   No bugs in severe category is outstanding, and

-   No problem of severe nature which makes application program not
    executable, e.g. system crash, showstoppers or cumulative defects
    prevent the workflow from continuing

No problem leads to erroneous data or loss of data.

# Test Specification

## 5.1 Test Control Procedures

System Integration Test testers have to follow the testing schedule to
execute all System Integration test cases in the System Integration Test
Specification. They should execute the testing by referencing the test
cases provided by MC. The System Integration Test tester should verify
the actual result against the expected result.

5.2 TESTING ENVIRONMENT

5.2.1 Testing Location

The System Integration Test will be performed in DR and Pre-production
environments.

5.2.2 System Integration Test Equipment

**Desktop Operating System:**

Windows 10  
MacOS 14 Sonoma

**Mobile Operating System:**

Android: 11, 14  
IOS: 14, 17

**Browsers:**

**MS Edge (Version 119)**

[<u>https://www.microsoft.com/en-us/edge/download?form=MA13FJ</u>](https://www.microsoft.com/en-us/edge/download?form=MA13FJ)

or you can install the latest MS Edge Browsers through the Windows
Update.

**Mozilla Firefox (Version 120)**

[<u>https://www.mozilla.org/en-US/firefox/download/</u>](https://www.mozilla.org/en-US/firefox/download/)

**Chrome (Version 120)**

[<u>https://www.google.com/chrome/</u>](https://www.google.com/chrome/)

## 5.3 Cases Summary

The following is a summary of all test cases which is for easy reference
during the test.

<table>
<colgroup>
<col style="width: 70%" />
<col style="width: 29%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Test Case Description</strong></th>
<th><strong>Relevant Functions</strong></th>
</tr>
<tr class="odd">
<th>To test the APIs related with register process on website</th>
<th><p>REQ-WEB-1-1-1<br />
REQ-WEB-1-1-3</p>
<p>REQ-WEB-1-2-1</p>
<p>REQ-WEB-1-2-2</p>
<p>REQ-WEB-2-1-9</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with register process on mobile app</th>
<th><p>REQ-MOB-2-2-1</p>
<p>REQ-MOB-2-2-2</p>
<p>REQ-MOB-2-2-4</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with login process on website</th>
<th><p>REQ-WEB-1-1-2</p>
<p>REQ-WEB-1-1-2</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with login process on mobile app</th>
<th><p>REQ-MOB-2-1-1</p>
<p>REQ-MOB-2-1-2</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with login process with iAM Smart</th>
<th>REQ-WEB-1-1-3REQ-MOB-2-1-3</th>
</tr>
<tr class="header">
<th>To test the APIs related with change password function</th>
<th><p>REQ-WEB-1-1-4</p>
<p>REQ-WEB-1-2-5</p>
<p>REQ-MOB-2-1-4</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with forget password process</th>
<th><p>REQ-WEB-1-1-4</p>
<p>REQ-WEB-1-2-5</p>
<p>REQ-MOB-2-1-4</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with change user general information</th>
<th><p>REQ-WEB-1-2-3</p>
<p>REQ-WEB-1-2-4</p>
<p>REQ-WEB-4-1-1</p></th>
</tr>
<tr class="odd">
<th>To test the assignment TCP function</th>
<th>REQ-WEB-1-2-6</th>
</tr>
<tr class="header">
<th>To test the APIs related with creation of site project</th>
<th><p>REQ-WEB-2-1-3</p>
<p>REQ-WEB-2-1-5</p>
<p>REQ-WEB-2-1-8</p>
<p>REQ-WEB-2-1-9</p>
<p>REQ-MOB-3-1-3</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with update of site project</th>
<th><p>REQ-WEB-2-1-4</p>
<p>REQ-MOB-3-1-4</p>
<p>REQ-MOB-3-1-6</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with supervision plan management
function</th>
<th><p>REQ-WEB-2-1-1</p>
<p>REQ-WEB-2-1-7</p>
<p>REQ-MOB-3-1-7</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with creation of Form A Template</th>
<th><p>REQ-WEB-2-1-12</p>
<p>REQ-MOB-3-1-9</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with assignment of Form A Template</th>
<th><p>REQ-WEB-2-1-12</p>
<p>REQ-MOB-3-1-9</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with creation of the Form A Record</th>
<th><p>REQ-WEB-2-1-12</p>
<p>REQ-MOB-3-1-9</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with update of Form A Record</th>
<th><p>REQ-WEB-2-1-12</p>
<p>REQ-MOB-3-1-9</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with draft of Form A Record</th>
<th><p>REQ-WEB-2-1-12</p>
<p>REQ-MOB-3-1-9</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with filing of Form A Record</th>
<th><p>REQ-WEB-2-1-12</p>
<p>REQ-MOB-3-1-9</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with upload of Form A Attachment</th>
<th><p>REQ-WEB-2-1-11</p>
<p>REQ-WEB-2-1-12</p>
<p>REQ-MOB-3-1-8</p>
<p>REQ-MOB-3-1-9</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with export of Form A Record</th>
<th><p>REQ-WEB-2-1-10</p>
<p>REQ-WEB-2-1-12</p>
<p>REQ-MOB-3-1-9</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with import of Form A Record</th>
<th><p>REQ-WEB-2-1-10</p>
<p>REQ-WEB-2-1-12</p>
<p>REQ-MOB-3-1-9</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with creation of Form B</th>
<th><p>REQ-WEB-2-1-13</p>
<p>REQ-MOB-3-1-10</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with upload of Form B Attachment</th>
<th><p>REQ-WEB-2-1-11</p>
<p>REQ-WEB-2-1-13</p>
<p>REQ-MOB-3-1-10</p>
<p>REQ-MOB-3-1-8</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with creation of Form APP-158 Template</th>
<th><p>REQ-WEB-2-1-14</p>
<p>REQ-MOB-3-1-11</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with assignment of Form APP-158
Template</th>
<th><p>REQ-WEB-2-1-14</p>
<p>REQ-MOB-3-1-11</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with creation of the Form APP-158
Record</th>
<th><p>REQ-WEB-2-1-14</p>
<p>REQ-MOB-3-1-11</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with update of Form APP-158 Record</th>
<th><p>REQ-WEB-2-1-14</p>
<p>REQ-MOB-3-1-11</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with draft of Form APP-158 Record</th>
<th><p>REQ-WEB-2-1-14</p>
<p>REQ-MOB-3-1-11</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with filing of Form APP-158 Record</th>
<th><p>REQ-WEB-2-1-14</p>
<p>REQ-MOB-3-1-11</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with upload of Form APP-158 Attachment</th>
<th><p>REQ-WEB-2-1-11</p>
<p>REQ-WEB-2-1-14</p>
<p>REQ-MOB-3-1-8</p>
<p>REQ-MOB-3-1-11</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with export of Form APP-158 Record</th>
<th><p>REQ-WEB-2-1-10</p>
<p>REQ-WEB-2-1-14</p></th>
</tr>
<tr class="header">
<th>To test the APIs related with import of Form APP-158 Record</th>
<th><p>REQ-WEB-2-1-10</p>
<p>REQ-WEB-2-1-14</p></th>
</tr>
<tr class="odd">
<th>To test the APIs related with notification of assign TCP</th>
<th><p>REQ-WEB-3-1-1</p>
<p>REQ-WEB-3-1-3</p></th>
</tr>
<tr class="header">
<th>Access to CDPSS website</th>
<th></th>
</tr>
<tr class="odd">
<th>Perform a test to ensure the load balancer works if one or two of
the application servers</th>
<th>Test performed and load balancer working correctly</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 5.4 Test scope

The System Integration Test will be conducted in 2 batches, the
followings are the description and the conducting period of the System
Integration Test batch.

1.  **System Integration Test for non-production environment**

**Description**:

System Integration Testing (SIT) in a non-production environment
involves verifying the interactions between different modules of a
software system in an integrated hardware and software setting. It aims
to evaluate the system's compliance with specified requirements and
ensure proper communication between modules. This testing is conducted
in a test environment that closely replicates the production environment
but without affecting real users, allowing for the detection and fixing
of errors before deployment

**Period**:

**Environment:** DR and Intranet UAT

1.  **System Integration Test for pre-production environment**

**Description**:

Some hardware are running in dual nodes, other than functional test,
system level components resilience tests are expected:

System Integration Testing (SIT) in a pre-production environment
involves validating the interactions between different software modules
in a setting that closely mirrors the production environment. The goal
is to ensure the system's compliance with specified requirements and
proper communication between modules. This testing is performed in a
controlled environment that doesn't impact real users, allowing for the
identification and resolution of issues before deployment

**Period**:

**Environment:** Pre-production of Intranet and Internet

# Test Cases Result

Below are test cases initial from mobile, it means we create the record/
initial start the scenario with mobile, but after that, we may double
check with desktop browser.

<table>
<colgroup>
<col style="width: 7%" />
<col style="width: 11%" />
<col style="width: 9%" />
<col style="width: 44%" />
<col style="width: 9%" />
<col style="width: 8%" />
<col style="width: 9%" />
</colgroup>
<thead>
<tr class="header">
<th>Acceptance ID</th>
<th>Tester</th>
<th>Test Date</th>
<th>Functionality</th>
<th>Web</th>
<th>Mobile</th>
<th>Result</th>
</tr>
<tr class="odd">
<th>1</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Successful case for registering new account</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>2</th>
<th>AP</th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for register new account – wrong username (English)</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>3</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for register new account – wrong password</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>4</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for register new account – value in confirm password field
does not consist with password field</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>5</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for register new account – wrong AP registration number</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>6</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>System generates a one-time password when the user accesses the
system.</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>7</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for system to generate one time password when user access
into system - wrong email address</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>8</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for system to generate one time password when user access
into system - wrong password</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>9</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>User use one time password to login into system</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>10</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>System allow user to reset password</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>11</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Successful case for user to change password</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>12</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for user to change password - retype new password does not
consist with new password</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>13</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for user to change password - new password does not meet
requirement of minimum length</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>14</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for user to change password - new password does not meet
the requirement of mixed-case alphabetic character</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>15</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Fail case for user to change password - new password does not meet
the requirement of having at least one special characters</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>16</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Successful case for updating personal information in “Update Account
Info” page</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>17</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Successful case for Head of Stream searches for site project, which
they are responsible for - single search result</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>18</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Successful case for creating Site Project from the submitted
Supervision plan</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>19</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Successful case for editing and updating site project detail</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>20</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>AP/RSE/RGE/AS create a supervision plan under a site project</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>21</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>AP/RSE/RGE/AS views the supervision plan detail of the project</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>22</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Create Form A template</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>23</th>
<th>TCP</th>
<th>May 2023</th>
<th><blockquote>
<p>Create Form A</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>24</th>
<th>AP / RSE / RGE / AS</th>
<th>May 2023</th>
<th><blockquote>
<p>File a draft Form A record</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>25</th>
<th><blockquote>
<p>TCP</p>
</blockquote></th>
<th>June 2023</th>
<th><blockquote>
<p>Successful case for creating new Form B</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>26</th>
<th><blockquote>
<p>TCP</p>
</blockquote></th>
<th>June 2023</th>
<th><blockquote>
<p>Successful case for saving Form B Part 1 as draft</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>27</th>
<th>TCP</th>
<th>June 2023</th>
<th>Successful case for uploading attachment when Form B Part 1 is saved
as draft</th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>28</th>
<th>TCP</th>
<th>June 2023</th>
<th>Successful case for completing Form B Part 1</th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>29</th>
<th>AP, TCP</th>
<th>June 2023</th>
<th>Successful case for uploading attachments when Form B part 1 is
completed</th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>30</th>
<th>AP, TCP</th>
<th>June 2023</th>
<th>Successful case for saving response to Form B part 1 as draft</th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>31</th>
<th>AP, TCP</th>
<th>June 2023</th>
<th>Successful case for completing response to Form B Part 1</th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>32</th>
<th>AP, BD Officer</th>
<th>June 2023</th>
<th>Successful case for reporting imminent danger to BD in Form B part
1</th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>33</th>
<th>TCP Representative, TCP</th>
<th>June 2023</th>
<th>Successful case for saving Form B part 2 as draft</th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>34</th>
<th>BD Officer, AP</th>
<th>June 2023</th>
<th>Successful case for reporting material concern to BD</th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>35</th>
<th>TCP Rep</th>
<th>June 2023</th>
<th>Successful case for uploading attachment when Form B Part 2 is Saved
as Draft</th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>36</th>
<th>AP</th>
<th>June 2023</th>
<th>Successful case for completing Form B Part 2</th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>37</th>
<th>AP, TCP Rep, TCP</th>
<th>June 2023</th>
<th>Successful case for saving response to Form B part 2 as draft</th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>38</th>
<th>AP</th>
<th>June 2023</th>
<th>Successful case for completing response to Form B Part 2</th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>39</th>
<th>AP</th>
<th>June 2023</th>
<th>Successful case for reporting imminent danger to BD in Form B part
2</th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>40</th>
<th>AP</th>
<th>June 2023</th>
<th>Successful case for creating PNAP APP-158 template</th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>41</th>
<th>TCP</th>
<th>June 2023</th>
<th>Successful case for creating PNAP APP-158 draft</th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>42</th>
<th>AP</th>
<th>June 2023</th>
<th>Successful case for filing PNAP APP-158</th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>43</th>
<th>TCP, AP</th>
<th>June 2023</th>
<th>Successful case for uploading PNG on drafted PNAP APP-158
record</th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>44</th>
<th>AP, TCP</th>
<th>June 2023</th>
<th>Successful case for viewing PNAP APP-158 Results and History</th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>45</th>
<th><blockquote>
<p>AS</p>
</blockquote></th>
<th>Aug 2023</th>
<th>Successful case for creating new site-monitoring scheme</th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>46</th>
<th><blockquote>
<p>AS</p>
</blockquote></th>
<th>Aug 2023</th>
<th><blockquote>
<p>Successful case for editing 3A level</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>47</th>
<th>AS</th>
<th>Aug 2023</th>
<th>Successful case for adding monitoring point</th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>48</th>
<th>AS</th>
<th>Aug 2023</th>
<th>Successful case for editing monitoring point</th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>49</th>
<th>RC TCP</th>
<th>Aug 2023</th>
<th>Successful case for TCP to save measurement records as draft</th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>50</th>
<th>AS, RC TCP</th>
<th>Aug 2023</th>
<th>Successful case for file/amend measurement records</th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>51</th>
<th>TCP Representative, Head of Stream</th>
<th>Aug 202Aug 20233</th>
<th>Successful case for viewing measurement record results</th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>52</th>
<th>TCP Representative, Head of Stream</th>
<th>Aug 2023</th>
<th>Successful case for filtering measurement record results</th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>53</th>
<th>TCP Representative, Head of Stream</th>
<th>Aug 2023</th>
<th>Successful case for viewing measurement record history</th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>54</th>
<th>BD Internal User</th>
<th>Aug 2023</th>
<th>Successful case for BD Internal User to login with Time-based One
Time Password</th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>55</th>
<th>Public user with iAM Smart account</th>
<th>Aug 2023</th>
<th>Successful case for linkup and login via iAM Smart</th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>56</th>
<th><blockquote>
<p>All users</p>
</blockquote></th>
<th>Sep 2023</th>
<th>Successful case for viewing the notification list</th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>57</th>
<th><blockquote>
<p>All users</p>
</blockquote></th>
<th>Sep 2023</th>
<th><blockquote>
<p>Successful case for viewing the notification details</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>58</th>
<th><blockquote>
<p>All users</p>
</blockquote></th>
<th>Sep 2023</th>
<th><blockquote>
<p>Successful case for redirecting to another page by clicking on the
clink in notification</p>
</blockquote></th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>59</th>
<th><blockquote>
<p>Hos, Rep, AP</p>
</blockquote></th>
<th>Sep 2023</th>
<th><blockquote>
<p>Successful case for opt-out the email notification</p>
</blockquote></th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>60</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for list of Heads of Stream
and their responsible sites</th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>61</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for List of TCPs and assigned
sites/supervision plans</th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>62</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for List of non-conformities
(Form B)</th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>63</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for List of inspection records
of Form APP-158</th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>64</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for List of inspection records
of Form A</th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>65</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for List of Supervision Plans
(SP)</th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>66</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for List of Sites</th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>67</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for Monitoring Point</th>
<th>Mac + Safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>68</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for 3A level changes</th>
<th>Win 10 + Chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>69</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for List of site-monitoring
activities</th>
<th>Mac + Safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>70</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for List of inspection item
checklist changes</th>
<th>Win 10 + Chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>71</th>
<th>BD Officer</th>
<th>Sep 2023</th>
<th>Successful case for generating report for List of site
activities</th>
<th>Mac + Safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>72</th>
<th>TCP, HOS</th>
<th>Sep 2023</th>
<th>Successful case for Unfiled Record Reminder for Level 5 Frequency of
Inspection</th>
<th>Win 10 + Chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Below are test cases initial from desktop browser, it means we create
the record/ initial start the scenario with desktop browser, but after
that, we may double check mobile browser, but not a must as some of the
function available in desktop browser only

<table>
<colgroup>
<col style="width: 7%" />
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 44%" />
<col style="width: 9%" />
<col style="width: 8%" />
<col style="width: 8%" />
</colgroup>
<thead>
<tr class="header">
<th>Case ID</th>
<th>Involved role</th>
<th>Test Date</th>
<th>Functionality</th>
<th>Web</th>
<th>Mobile</th>
<th>Result</th>
</tr>
<tr class="odd">
<th>1</th>
<th><blockquote>
<p>TCP</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>successful case for registering new account</p>
</blockquote></th>
<th>Win 11 + edge</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>2</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>System generates a one-time password when the user accesses the
system.</p>
</blockquote></th>
<th>Win 10 + firefox</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>3</th>
<th><blockquote>
<p>TCP</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>User use one time password to login into system</p>
</blockquote></th>
<th>Win 11 + chrome</th>
<th>Android + firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>4</th>
<th><blockquote>
<p>TCP</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>System allow user to reset password</p>
</blockquote></th>
<th>Mac OS + safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>5</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>System only allows each user to have one single user session on the
server</p>
</blockquote></th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>6</th>
<th><blockquote>
<p>TCP</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>Successful case for user to change password</p>
</blockquote></th>
<th>Win 10 + firefox</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>7</th>
<th><blockquote>
<p>TCP</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>Successful case for updating personal information in “Update Account
Info” page</p>
</blockquote></th>
<th>Win 11 + chrome</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>8</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>Successful case for Head of Stream searches for site project, which
they are responsible for</p>
</blockquote></th>
<th>Mac OS + safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>9</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>Successful case for creating new Site Project</p>
</blockquote></th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>10</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>Successful case for editing and updating site project detail</p>
</blockquote></th>
<th>Win 10 + firefox</th>
<th><blockquote>
<p>views the supervision plan</p>
</blockquote></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>11</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>AP/RSE/RGE/AS views the site project details</p>
</blockquote></th>
<th>Win 11 + chrome</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>12</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>AP/RSE/RGE/AS views the supervision plan details in the site
project</p>
</blockquote></th>
<th>Mac OS + safari</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>13</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>Successful case for AP/RSE/RGE/AS to edit the supervision plan detail
of the project</p>
</blockquote></th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>14</th>
<th>AP, RSE, RGE and AS</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Search TCP by Name</p>
</blockquote></th>
<th>Win 10 + firefox</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>15</th>
<th>AP, RSE, RGE and AS</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Add TCP into project</p>
</blockquote></th>
<th>Win 11 + chrome</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>16</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Accept “Assign TCP” Request</p>
</blockquote></th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>17</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Reject “Assign TCP” Request</p>
</blockquote></th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>18</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Unassign the assigned TCPs from project</p>
</blockquote></th>
<th>Win 10 + firefox</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>19</th>
<th>AP, RSE, RGE and AS</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Temporary replacement of TCP</p>
</blockquote></th>
<th>Win 11 + chrome</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>20</th>
<th>AP, RSE, RGE and AS</th>
<th>Mar 2023</th>
<th>Acceptance of being temporary TCP</th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>21</th>
<th><blockquote>
<p>AP/RSE/RGE/AS</p>
</blockquote></th>
<th>Mar 2023</th>
<th><blockquote>
<p>Create Form A template</p>
</blockquote></th>
<th>Win 11 + edge</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>22</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Create Form A</p>
</blockquote></th>
<th>Win 10 + firefox</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>23</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Select or amend different tasks item status</p>
</blockquote></th>
<th>Win 11 + chrome</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>24</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Review previous updated history</p>
</blockquote></th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>25</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Import inspection record files</p>
</blockquote></th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>26</th>
<th>TCP</th>
<th>Mar 2023</th>
<th>Review the imported file records</th>
<th>Win 10 + firefox</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>27</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Upload PDF, PNG on Form A and Quality Supervision Form ("Form
APP-158”)</p>
</blockquote></th>
<th>Win 11 + chrome</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>28</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>View Form A Result and History</p>
</blockquote></th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>29</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Download Form A Site Inspection Import Template</p>
</blockquote></th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>30</th>
<th>TCP</th>
<th>Mar 2023</th>
<th><blockquote>
<p>Import Form A Site Inspection Records by Excel</p>
</blockquote></th>
<th>Win 10 + firefox</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>31</th>
<th><blockquote>
<p>TCP</p>
</blockquote></th>
<th>Apr 2023</th>
<th><blockquote>
<p>Successful case for creating new Form B</p>
</blockquote></th>
<th>Win 11 + chrome</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>32</th>
<th><blockquote>
<p>TCP</p>
</blockquote></th>
<th>Apr 2023</th>
<th><blockquote>
<p>Successful case for saving Form B Part 1 as draft</p>
</blockquote></th>
<th>Mac OS + safari</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>33</th>
<th>TCP</th>
<th>Apr 2023</th>
<th>Successful case for uploading attachment when Form B Part 1 is saved
as draft</th>
<th>Win 11 + edge</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>34</th>
<th>TCP</th>
<th>Apr 2023</th>
<th>Successful case for completing Form B Part 1</th>
<th>Win 10 + firefox</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>35</th>
<th>AP, TCP</th>
<th>Apr 2023</th>
<th>Successful case for uploading attachments when Form B part 1 is
completed</th>
<th>Win 11 + chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>36</th>
<th>AP, TCP</th>
<th>Apr 2023</th>
<th>Successful case for saving response to Form B part 1 as draft</th>
<th>Mac OS + safari</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>37</th>
<th>AP, TCP</th>
<th>Apr 2023</th>
<th>Successful case for completing response to Form B Part 1</th>
<th>Win 11 + edge</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>38</th>
<th>AP, BD Officer</th>
<th>Apr 2023</th>
<th>Successful case for reporting imminent danger to BD in Form B part
1</th>
<th>Win 10 + firefox</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>39</th>
<th>TCP Representative, TCP</th>
<th>Apr 2023</th>
<th>Successful case for saving Form B part 2 as draft</th>
<th>Win 11 + chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>40</th>
<th>BD Officer, AP</th>
<th>Apr 2023</th>
<th>Successful case for reporting material concern to BD</th>
<th>Mac OS + safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>41</th>
<th>TCP Rep</th>
<th>Apr 2023</th>
<th>Successful case for uploading attachment when Form B Part 2 is Saved
as Draft</th>
<th>Win 11 + edge</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>42</th>
<th>AP</th>
<th>Apr 2023</th>
<th>Successful case for completing Form B Part 2</th>
<th>Win 10 + firefox</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>43</th>
<th>AP, TCP Rep, TCP</th>
<th>Apr 2023</th>
<th>Successful case for saving response to Form B part 2 as draft</th>
<th>Win 11 + chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>44</th>
<th>AP</th>
<th>Apr 2023</th>
<th>Successful case for completing response to Form B Part 2</th>
<th>Mac OS + safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>45</th>
<th>AP</th>
<th>Apr 2023</th>
<th>Successful case for reporting imminent danger to BD in Form B part
2</th>
<th>Win 11 + edge</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>46</th>
<th>AP</th>
<th>Apr 2023</th>
<th>Successful case for creating PNAP APP-158 template</th>
<th>Win 10 + firefox</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>47</th>
<th>TCP</th>
<th>Apr 2023</th>
<th>Successful case for creating PNAP APP-158 draft</th>
<th>Win 11 + chrome</th>
<th>IOS + Firefox</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>48</th>
<th>AP</th>
<th>Apr 2023</th>
<th>Successful case for filing PNAP APP-158</th>
<th>Mac OS + safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>49</th>
<th>TCP, AP</th>
<th>Apr 2023</th>
<th>Successful case for uploading PNG on drafted PNAP APP-158
record</th>
<th>Win 11 + edge</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>50</th>
<th>AP, TCP</th>
<th>Apr 2023</th>
<th>Successful case for viewing PNAP APP-158 Results and History</th>
<th>Win 10 + firefox</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>51</th>
<th>TCP</th>
<th>Apr 2023</th>
<th>Successful case for downloading PNAP APP-158 Import Template</th>
<th>Win 11 + chrome</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>52</th>
<th>TCP</th>
<th>Apr 2023</th>
<th>Successful case for importing PNAP APP-158 record from template</th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>53</th>
<th>BD admin</th>
<th>Apr 2023</th>
<th>Successful case for BD admin to view Public Users</th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>54</th>
<th>BD admin</th>
<th>Apr 2023</th>
<th>Successful case for BD admin to edit Public Users</th>
<th>Win 10 + firefox</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>55</th>
<th>BD admin</th>
<th>Apr 2023</th>
<th>Successful case for BD admin to inactivate Public Users</th>
<th>Win 11 + chrome</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>56</th>
<th>BD admin</th>
<th>Apr 2023</th>
<th>Successful case for BD admin to activate Public Users</th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>57</th>
<th>BD admin</th>
<th>Apr 2023</th>
<th>Successful case for BD admin to view Public User’s responsible site
project</th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>58</th>
<th>BD admin</th>
<th>Apr 2023</th>
<th>Successful case for BD admin to remove Head of Stream from site
project</th>
<th>Win 10 + firefox</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>59</th>
<th><blockquote>
<p>AS</p>
</blockquote></th>
<th>May 2023</th>
<th>Successful case for creating new site-monitoring scheme</th>
<th>Win 11 + chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>60</th>
<th><blockquote>
<p>AS</p>
</blockquote></th>
<th>May 2023</th>
<th><blockquote>
<p>Successful case for editing 3A level</p>
</blockquote></th>
<th>Mac OS + safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>61</th>
<th>AS</th>
<th>May 2023</th>
<th>Successful case for adding monitoring point</th>
<th>Win 11 + edge</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>62</th>
<th>AS</th>
<th>May 2023</th>
<th>Successful case for editing monitoring point</th>
<th>Win 10 + firefox</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>63</th>
<th>RC TCP</th>
<th>May 2023</th>
<th>Successful case for TCP to save measurement records as draft</th>
<th>Win 11 + chrome</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>64</th>
<th>RC TCP</th>
<th>May 2023</th>
<th>Successful case for RC TCP to download import measurement
template</th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>65</th>
<th>RC TCP</th>
<th>May 2023</th>
<th>Successful case for importing site-monitoring measurement
records</th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>66</th>
<th>AS, RC TCP</th>
<th>May 2023</th>
<th>Successful case for file/amend measurement records</th>
<th>Win 10 + firefox</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>67</th>
<th>TCP Representative, Head of Stream</th>
<th>May 2023</th>
<th>Successful case for viewing measurement record results</th>
<th>Win 11 + chrome</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>68</th>
<th>TCP Representative, Head of Stream</th>
<th>May 2023</th>
<th>Successful case for filtering measurement record results</th>
<th>Mac OS + safari</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>69</th>
<th>TCP Representative, Head of Stream</th>
<th>May 2023</th>
<th>Successful case for viewing measurement record history</th>
<th>Win 11 + edge</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>70</th>
<th>BD Internal User</th>
<th>May 2023</th>
<th>Successful case for BD Internal User to login via Departmental
Portal</th>
<th>Win 10 + firefox</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>71</th>
<th>BD Internal User</th>
<th>May 2023</th>
<th>Successful case for BD Internal User to update personal and post
details</th>
<th>Win 11 + chrome</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>72</th>
<th>BD admin</th>
<th>May 2023</th>
<th>Successful case for BD admin to view BD Internal Users</th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>73</th>
<th>BD admin</th>
<th>May 2023</th>
<th>Successful case for BD admin to create BD Internal Users</th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>74</th>
<th>BD admin</th>
<th>May 2023</th>
<th>Successful case for BD admin to edit BD Internal Users</th>
<th>Win 10 + firefox</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>75</th>
<th>Public user with iAM Smart account</th>
<th>May 2023</th>
<th>Successful case for linkup and login via iAM Smart</th>
<th>Win 11 + chrome</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>76</th>
<th><blockquote>
<p>All users</p>
</blockquote></th>
<th>June 2023</th>
<th>Successful case for viewing the notification list</th>
<th>Mac OS + safari</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>77</th>
<th><blockquote>
<p>All users</p>
</blockquote></th>
<th>June 2023</th>
<th><blockquote>
<p>Successful case for viewing the notification details</p>
</blockquote></th>
<th>Win 11 + edge</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>78</th>
<th><blockquote>
<p>All users</p>
</blockquote></th>
<th>June 2023</th>
<th><blockquote>
<p>Successful case for redirecting to another page by clicking on the
clink in notification</p>
</blockquote></th>
<th>Win 10 + firefox</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>79</th>
<th><blockquote>
<p>Hos, Rep, AP</p>
</blockquote></th>
<th>June 2023</th>
<th><blockquote>
<p>Successful case for opt-out the email notification</p>
</blockquote></th>
<th>Win 11 + chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>80</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for list of Heads of Stream
and their responsible sites</th>
<th>Mac OS + safari</th>
<th>Android + Chrome</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>81</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of TCPs and assigned
sites/supervision plans</th>
<th>Win 11 + edge</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>82</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of non-conformities
(Form B)</th>
<th>Win 10 + firefox</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>83</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of inspection records
of Form APP-158</th>
<th>Win 11 + chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>84</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of inspection records
of Form A</th>
<th>Mac OS + safari</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>85</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of Supervision Plans
(SP)</th>
<th>Win 11 + edge</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>86</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of Sites</th>
<th>Win 10 + firefox</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>87</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for Monitoring Point</th>
<th>Win 11 + chrome</th>
<th>huawei harmony + huawei global</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>88</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for 3A level changes</th>
<th>Mac OS + safari</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>89</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of site-monitoring
activities</th>
<th>Win 11 + edge</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>90</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of inspection item
checklist changes</th>
<th>Win 10 + firefox</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>91</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of site
activities</th>
<th>Win 11 + chrome</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="header">
<th>92</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for list of site inspection
notifications</th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>93</th>
<th>BD Officer</th>
<th>June 2023</th>
<th>Successful case for generating report for List of site-monitoring
alerts</th>
<th>Mac OS + safari</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>94</th>
<th>TCP, HOS</th>
<th>June 2023</th>
<th>Successful case for Unfiled Record Reminder for Level 5 Frequency of
Inspection</th>
<th>Win 11 + edge</th>
<th>IOS + Safari</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>95</th>
<th>RC TCP, AS HOS</th>
<th>June 2023</th>
<th>Successful case for Batch file for site monitoring records</th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="header">
<th>96</th>
<th><blockquote>
<p>BD Officer</p>
</blockquote></th>
<th>July 2023</th>
<th>Successful case for create, update and remove BD Officer from Site
Project</th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
<tr class="odd">
<th>97</th>
<th><blockquote>
<p>AS</p>
</blockquote></th>
<th>July 2023</th>
<th>Successful case for creating new type of monitoring for site
monitoring</th>
<th>Win 11 + edge</th>
<th></th>
<th>Pass</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

**System backup, Fall-back and Recovery Test**

Test date : 12 Apr 2023

<table>
<colgroup>
<col style="width: 9%" />
<col style="width: 51%" />
<col style="width: 20%" />
<col style="width: 18%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>No.</strong></th>
<th><strong>Task</strong></th>
<th><strong>Results for Site Recovery</strong></th>
<th><strong>Results for Site Fall-back</strong></th>
</tr>
<tr class="odd">
<th colspan="4"><strong>General</strong></th>
</tr>
<tr class="header">
<th><ol type="1">
<li></li>
</ol></th>
<th><p>Access homepage of CDPSS site </p>
<p>DR Site: <a
href="https://cdpssdr.bd.gov.hk/login"><u>https://cdpssdr.bd.gov.hk/login</u></a> </p></th>
<th>Pass</th>
<th>NA</th>
</tr>
<tr class="odd">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Check forget password function and the forget password email is sent
by CDPSS by administrator login</th>
<th>Pass</th>
<th>NA</th>
</tr>
<tr class="header">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Login CDPSS by administrator login</th>
<th>Pass</th>
<th>NA</th>
</tr>
<tr class="odd">
<th colspan="4"><strong>Function for Health Check Purpose</strong></th>
</tr>
<tr class="header">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Public user registration</th>
<th>Pass</th>
<th>NA</th>
</tr>
<tr class="odd">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Form A</th>
<th>Pass</th>
<th>NA</th>
</tr>
<tr class="header">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Site monitor form</th>
<th>Pass</th>
<th>NA</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Test date : 22 Nov 2023

<table>
<colgroup>
<col style="width: 6%" />
<col style="width: 57%" />
<col style="width: 18%" />
<col style="width: 17%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>No.</strong></th>
<th><strong>Task</strong></th>
<th><strong>Results for Site Recovery</strong></th>
<th><strong>Results for Site Fall- back</strong></th>
</tr>
<tr class="odd">
<th colspan="4"><strong>General</strong></th>
</tr>
<tr class="header">
<th><ol type="1">
<li></li>
</ol></th>
<th><p>Access homepage of CDPSS site </p>
<p>Production Site: <a
href="https://cdpss.bd.gov.hk/login"><u>https://cdpss.bd.gov.hk/login</u></a> </p></th>
<th>NA</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Check forget password function and the forget password email is sent
by CDPSS by administrator login</th>
<th>NA</th>
<th>Pass</th>
</tr>
<tr class="header">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Login CDPSS by administrator login</th>
<th>NA</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th colspan="4"><strong>Function for Health Check Purpose</strong></th>
</tr>
<tr class="header">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Public user registration</th>
<th>NA</th>
<th>Pass</th>
</tr>
<tr class="odd">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Form A</th>
<th>NA</th>
<th>Pass</th>
</tr>
<tr class="header">
<th><ol start="0" type="1">
<li></li>
</ol></th>
<th>Site monitor form</th>
<th>NA</th>
<th>Pass</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

**Performance, Stress and Load Test Result**

Test date : 12 Apr 2023 to 14 Apr 2023

| **Function**                                                                                     | **Expected Response Time in CDPSS** |                          | **Actual average response time in CDPSS with 100 concurrent users** | **Actual response time of existing system \> expected response time(Y/N)** | **CDPSS expected to meet the expected time in (\*) (Y/N)** |
|--------------|---------|---------|--------------|--------------|--------------|
|                                                                                                  | **Single User**                     | **100 Concurrent Users** | **(S)**                                                             |                                                                            |                                                            |
| **Stage 1**                                                                                      |                                     |                          |                                                                     |                                                                            |                                                            |
|                                                                                                  |                                     |                          |                                                                     |                                                                            |                                                            |
| Stage 1 - Visit the platform                                                                     | \< 1s                               | \< 3s                    | 2.870                                                               | N                                                                          | Y                                                          |
| Stage 1 - Public User create/register an account                                                 | \< 1s                               | \< 3s                    | 0.620                                                               | N                                                                          | Y                                                          |
| Stage 1 - Public User Authentication with Password                                               | \< 1s                               | \< 3s                    | 2.889                                                               | N                                                                          | Y                                                          |
| Stage 1 - Create a Site Project from submitted Supervision plan                                  | \< 2s                               | \< 4s                    | 1.480                                                               | N                                                                          | Y                                                          |
| Stage 1 – Edit and update Site Project Detail                                                    | \< 1s                               | \< 3s                    | 2.764                                                               | N                                                                          | Y                                                          |
| Stage 1 – List out Site Project                                                                  | \< 1s                               | \< 3s                    | 2.825                                                               | N                                                                          | Y                                                          |
| Stage 1 – Site Project Detail View                                                               | \< 1s                               | \< 3s                    | 2.809                                                               | N                                                                          | Y                                                          |
| Stage 1 - Supervision Plan Detail View                                                           | \< 2s                               | \< 4s                    | 2.789                                                               | N                                                                          | Y                                                          |
| Stage 1 – Supervision Plan Detail Management                                                     | \< 2s                               | \< 4s                    | 2.859                                                               | N                                                                          | Y                                                          |
| Stage 1 – Assign TCPs                                                                            | \< 1s                               | \< 3s                    | 2.875                                                               | N                                                                          | Y                                                          |
| Stage 1 – List of TCPs                                                                           | \< 2s                               | \< 4s                    | 2.754                                                               | N                                                                          | Y                                                          |
| Stage 1 – Create Template of Form A                                                              | \< 1s                               | \< 3s                    | 2.800                                                               | N                                                                          | Y                                                          |
| Stage 1 - Create Form A                                                                          | \< 1s                               | \< 3s                    | 2.815                                                               | N                                                                          | Y                                                          |
| Stage 1 – Draft Form A                                                                           | \< 1s                               | \< 3s                    | 2.791                                                               | N                                                                          | Y                                                          |
| Stage 1 – File Form A                                                                            | \< 2s                               | \< 4s                    | 3.614                                                               | N                                                                          | Y                                                          |
| Stage 1 – View Form A Result and History                                                         | \< 1s                               | \< 3s                    | 2.792                                                               | N                                                                          | Y                                                          |
| Stage 1 - Create Form B                                                                          | \< 1s                               | \< 3s                    | 2.768                                                               | N                                                                          | Y                                                          |
| Stage 1 - Draft Part 1 of Form B                                                                 | \< 1s                               | \< 3s                    | 2.854                                                               | N                                                                          | Y                                                          |
| Stage 1 - Complete Form B Part 1                                                                 | \< 1s                               | \< 3s                    | 2.860                                                               | N                                                                          | Y                                                          |
| Stage 1 - Submit Form B Part 1 to BD                                                             | \< 1s                               | \< 3s                    | 2.858                                                               | N                                                                          | Y                                                          |
| Stage 1 – Draft Part 2 of Form B                                                                 | \< 1s                               | \< 3s                    | 2.779                                                               | N                                                                          | Y                                                          |
| Stage 1 – Complete Form B Part 2                                                                 | \< 1s                               | \< 3s                    | 2.783                                                               | N                                                                          | Y                                                          |
| Stage 1 – Submit Form B to BD                                                                    | \< 1s                               | \< 3s                    | 2.891                                                               | N                                                                          | Y                                                          |
| **Stage 2**                                                                                      |                                     |                          |                                                                     |                                                                            |                                                            |
| Stage 2 – View Form B Result and History                                                         | \< 1s                               | \< 3s                    | 2.766                                                               | N                                                                          | Y                                                          |
| Stage 2 – Create Template of Quality Supervision Form (PNAP APP-158 Appendix B) (“Form APP-158”) | \< 1s                               | \< 3s                    | 2.829                                                               | N                                                                          | Y                                                          |
| Stage 2 – Create Form APP-158                                                                    | \< 1s                               | \< 3s                    | 2.898                                                               | N                                                                          | Y                                                          |
| Stage 2 – Draft Form APP-158                                                                     | \< 1s                               | \< 3s                    | 2.889                                                               | N                                                                          | Y                                                          |
| Stage 2 – File PNAP APP-158                                                                      | \< 2s                               | \< 4s                    | 2.980                                                               | N                                                                          | Y                                                          |
| Stage 2 – View PNAP APP-158 Result and History                                                   | \< 2s                               | \< 4s                    | 2.882                                                               | N                                                                          | Y                                                          |
| Stage 2 – Create site-monitoring scheme                                                          | \< 1s                               | \< 3s                    | 0.163                                                               | N                                                                          | Y                                                          |
| Stage 2 – View site-monitoring measurement record results                                        | \< 2s                               | \< 4s                    | 3.942                                                               | N                                                                          | Y                                                          |
| Stage 2 – Listing out responsible Inspection Form                                                | \< 2s                               | \< 4s                    | 2.848                                                               | N                                                                          | Y                                                          |
| Stage 2 – Listing out responsible Site-Monitoring Schemes                                        | \< 2s                               | \< 4s                    | 3.497                                                               | N                                                                          | Y                                                          |
| Stage 2 – Public Users create/register an account                                                | \< 1s                               | \< 3s                    | 2.796                                                               | N                                                                          | Y                                                          |
| Stage 2 – View Public User                                                                       | \< 1s                               | \< 3s                    | 2.785                                                               | N                                                                          | Y                                                          |
| Stage 2 – Edit Public User                                                                       | \< 1s                               | \< 3s                    | 2.944                                                               | N                                                                          | Y                                                          |
| Stage 2 – Activate Public User                                                                   | \< 1s                               | \< 3s                    | 2.792                                                               | N                                                                          | Y                                                          |
