<img src="media/image1.jpg" style="width:1.30903in;height:1.30903in" />

**APPLICATION OPERATION MANUAL**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**

**L<span class="smallcaps">ICENSING SELF-CERTIFICATION PORTAL</span>**

**OF**

**BUILDINGS DEPARTMENT**

**Version: 0.1**

**Jan 2025**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR.

<table>
<colgroup>
<col style="width: 17%" />
<col style="width: 82%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Distribution</strong></th>
</tr>
<tr class="odd">
<th>Copy No.</th>
<th>Holder</th>
</tr>
<tr class="header">
<th>1</th>
<th><blockquote>
<p>Buildings Department (BD)</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>2</th>
<th><blockquote>
<p>Master Concept (Hong Kong) Limited (MC)</p>
</blockquote></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

| **Amendment History** |                      |                                      |                           |            |
|-----------|-----------------------|--------------|--------------|------------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date       |
| 1                     | 1st draft            | N/A                                  | 0.1                       | 16/01/2025 |
|                       |                      |                                      |                           |            |
|                       |                      |                                      |                           |            |
|                       |                      |                                      |                           |            |
|                       |                      |                                      |                           |            |
|                       |                      |                                      |                           |            |
|                       |                      |                                      |                           |            |

**TABLE OF CONTENTS**

[1. Purpose 4](#purpose)

[2. Scope 5](#scope)

[3. Reference 6](#reference)

[4. Definitions and Conventions 7](#definitions-and-conventions)

[5. System Description 8](#system-description)

> [5.1 System Description 8](#system-description-1)
>
> [5.2 Job Identification/ Description
> 8](#job-identification-description)
>
> [5.3 Scheduled Batch Job 8](#scheduled-batch-job)
>
> [5.3.1 INT-MWMS2-01 Data Import from MWMS2
> 8](#int-mwms2-01-data-import-from-mwms2-ry-note-reference-only.-needs-to-update)

[6. System Media Input and Output 10](#system-media-input-and-output)

> [6.1 Input Tapes/ Discs 10](#input-tapes-discs)

[7. System output reports 11](#system-output-reports)

> [7.1 Daily Reports 11](#daily-reports)

[8. Operations Description 12](#operations-description)

> [8.1 Online Schedule 12](#online-schedule)
>
> [8.1.1 LSCP Web Service 12](#lscp-web-service)

[9. Run Job Specifications 13](#run-job-specifications)

> [9.1 Data Import from MWMS
> 13](#data-import-from-mwms-ry-note-not-sure-if-its-true)
>
> [9.1.1 Functions 13](#functions)

[10. Error Handling 14](#error-handling)

> [10.1 Critical Error Handling 14](#critical-error-handling)

# 

# **1. Purpose**

This Application Operation Manual (AOM) is used for providing relevant
information to the application operation staff of the system being
implemented. It documents in detail the instruction of all the work to
be performed when running the application system which include job
submission, report checking and dispatching.

# **2. Scope**

Describe relevant information to the application operation staff.

# **3. Reference**

-   System Analysis and Design Report

-   System Manual (T351)

-   Program Manual (T321)

-   Computer Operation Procedure Manual (T356)

# **4. Definitions and Conventions **

Nil.

# **5. System Description** 

## 5.1 System Description

The entire LSCP system is composed of two sub systems: LSCP Web and LSCP
Mobile.

## 5.2 Job Identification/ Description

The batch job names and their corresponding locations are listed in
following table:  
<span class="mark">\[RY Note: following is for reference only. Content
is incorrect\]</span>

|     | Job Name                            | Job Description/ File Location                                                     | Running Location   | Automatic / Manual Trigger |
|------|---------------|-------------------------|---------------|-------------|
| 1   | INT-MWMS2-01 Data Import from MWMS2 | Import AP/RSE/RGE/RC Basic Information into LSCP database                          | Application Server | Automatic                  |
| 2   | UF-WEB-010-15 App-158 Notification  | Notify representatives & TCP(s) of outstanding un-filed Form APP-158               | Application Server | Automatic                  |
| 3   | UF-WEB-010-10 Form A Notification   | Notify representatives & TCP(s) of outstanding un-filed Form APP-A                 | Application Server | Automatic                  |
| 4   | Import SMIS Excel into LSCP         | Import data from SMIS allowing users to create site projects and supervision plans | Application Server | Manual                     |
| 5   | Production backup                   |                                                                                    | Veeam backup       | Automatic                  |

## 5.3 Scheduled Batch Job

### 5.3.1 INT-MWMS2-01 Data Import from MWMS2 <span class="mark">\[RY Note: reference only. needs to update\]</span>

| **ID/ Name**  |     |
|---------------|-----|
| **Hostname**  |     |
| **IP**        |     |
| **Task**      |     |
| **Frequency** |     |
| **Files**     |     |

# **6. System Media Input and Output**

## 6.1 Input Tapes/ Discs

LSCP application use Veeam for backup and restore (Refer to Computer
Operation Manual)

# **7. System output reports**

## 7.1 Daily Reports

# **8. Operations Description**

## 8.1 Online Schedule

## 

### 8.1.1 LSCP Web Service

| **Day**          | **Time**      |
|------------------|---------------|
| Monday to Friday | 00:00 – 23:59 |
| Saturday         | 00:00 – 23:59 |
| Sunday           | 00:00 – 23:59 |
| Public Holiday   | 00:00 – 23:59 |

# 

# **9. Run Job Specifications**

## 9.1 Data Import from MWMS <span class="mark">\[RY Note: not sure if it’s true\]</span>

### 

### 9.1.1 Functions

The contractors’ information can be imported from MWMS through the Batch
job.

# **10. Error Handling**

## 10.1 Critical Error Handling

Try to access the BD Common Home from FrontEnd Server.

If it still fails, please try to restart frontend server. Make sure the
necessary service is running after restart.

Please refer to section 6.1 (shut down) and 7.10 (start up) of Computer
Operation Procedure Manual

If not, please restart the load balancer. Please refer to section 6.10.1
(shut down) and 7.1.1 (start-up) of Computer Operation Procedure Manual.

\<End of document\>
