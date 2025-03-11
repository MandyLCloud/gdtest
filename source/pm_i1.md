<img src="media/image1.jpg" style="width:1.30903in;height:1.30903in" />

**PROGRAM MANUAL**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**OF THE**

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
|----------|-------------------------|------------|------------|--------------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date       |
| 1                     | 1st draft            | All                                  | 0.1                       | 16/01/2025 |
|                       |                      |                                      |                           |            |
|                       |                      |                                      |                           |            |

**TABLE OF CONTENTS**

[1. Purpose 4](#purpose)

[2. Scope 5](#scope)

> [2.1 Development Tools and Platform
> 6](#development-tools-and-platform)

[3. Reference 7](#reference)

> [4.1 Definition 8](#definition)
>
> [4.2 Conventions 9](#conventions)

[5. Program List 10](#program-list)

> [5.1 Web Application 11](#web-application)

[6. Program Specification 12](#program-specification)

> [6.1 Public User Authentication with Password
> 12](#public-user-authentication-with-password)

#  

# 1. Purpose

The objective of this document is to provide an overview of the system
by listing out in brief the programs, data files, etc. Reader interested
in specific area may refer to the corresponding manuals (Data Manual,
Program Specifications, etc.).

The major readers of Program Manual are the staff responsible for
maintaining the application system.

#  

# 2. Scope 

The Program Manual serves as a comprehensive guide to understanding the
intricacies of the software utilized within the Licensing
Self-Certification Portal (LSCP). It encompasses detailed program
specifications for each program integrated into the system.

Throughout the Implementation Phase, the program specifications are
meticulously prepared by system analysts. These specifications play a
pivotal role in guiding programmers during the coding phase, ensuring
that the software is developed according to the predetermined
requirements and standards. Moreover, the program specifications act as
a valuable resource for future maintenance endeavors, facilitating the
identification and resolution of potential issues or enhancements.

It's imperative for the project team to customize the Program Manual to
encapsulate any unique characteristics or nuances inherent within the
software development environment. This could entail elaborating on
specific methodologies employed, such as event handling mechanisms or
message passing protocols, to provide a comprehensive understanding for
all stakeholders involved.

However, it's important to note that if there are no new programs being
developed for the application system, the preparation of a Program
Manual may not be necessary. In such instances, the project team can
focus their efforts on other pertinent tasks, thereby optimizing
resource allocation and streamlining the development process.

##  

## 2.1 Development Tools and Platform 

Web Administration

Applications were developed with the following software:

#  

# 3. Reference

Systems Analysis and Design Report: This report serves as the foundation
for the design and development of the system. It includes detailed
analysis of the system requirements, user needs, and business processes.
The report outlines the system architecture, data models, and functional
specifications, providing a comprehensive understanding of the system's
design and objectives.

System Manual: The System Manual contains detailed documentation on the
system's architecture, functionality, and usage guidelines. It serves as
a comprehensive reference guide for users, administrators, and
developers involved in the system's operation and maintenance. The
manual includes information on installation procedures, system
configuration, troubleshooting tips, and best practices for utilizing
the system effectively.

**4. Defintions and Conventions**

## 4.1 Definition

NIL

##  

## 4.2 Conventions 

| Term                          | Definitions                                                        |
|-----------------|-------------------------------------------------------|
| iAM Smart                     | <span class="mark">Internet Access by Mobile in a Smart Way</span> |
| <span class="mark">BD </span> | Buildings Department                                               |
| JWT                           | JSON Web Tokens                                                    |

#  

# 5. Program List

This part provides a list of program specifications contained in the
program manual. The program specifications may be grouped under
following function groups.

## 5.1 Web Application

The following table shows the list of functions mapping of the desktop
and mobile version.

| Model Name | Program ID | Program Name                             | Type        |
|-----------------|--------------|------------------------------|------------|
| Login      | PRO-SYS-01 | Public User Authentication with Password | Web, Mobile |
|            |            |                                          |             |
|            |            |                                          |             |
|            |            |                                          |             |
|            |            |                                          |             |
|            |            |                                          |             |

# 

#  

# 6. Program Specification

# 

## 6.1 Public User Authentication with Password

| Program ID           |                      | PRO-SYS-01                               |                 | Mode: |     |      |
|---------------------|---------|-----------------------|---|-------|-----|------|
| Program Name         |                      | Public User Authentication with Password |                 |       |     |      |
| Description          |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
| Program Environment: |                      |                                          |                 |       |     |      |
| Program Source       |                      |                                          |                 |       |     |      |
| Language Compiler    |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
| Amendment History:   |                      |                                          |                 |       |     |      |
| Change Number        | Revision Description |                                          | Revision Number |       |     | Date |
|                      |                      |                                          |                 |       |     |      |
| Table/File Usage:    |                      |                                          |                 |       |     |      |
| Table/File           |                      | Usage                                    |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |
|                      |                      |                                          |                 |       |     |      |

Processing Logic

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 20%" />
<col style="width: 24%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr class="header">
<th>Pre-submit Validity Check</th>
<th colspan="3"><p>1 Validate the user input at client side.</p>
<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 32%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th>Input</th>
<th>Validation</th>
<th>Remarks</th>
</tr>
<tr class="odd">
<th>Email</th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>Password</th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<p>2</p>
<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 32%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th>Input</th>
<th>Validation</th>
<th>Remarks</th>
</tr>
<tr class="odd">
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table></th>
</tr>
<tr class="odd">
<th colspan="4">Event</th>
</tr>
<tr class="header">
<th></th>
<th colspan="3"></th>
</tr>
<tr class="odd">
<th></th>
<th colspan="3"></th>
</tr>
<tr class="header">
<th colspan="4">Window Navigation</th>
</tr>
<tr class="odd">
<th colspan="2">From Screen</th>
<th colspan="2">To Screen</th>
</tr>
<tr class="header">
<th colspan="2">Screen</th>
<th>Event</th>
<th>Screen</th>
</tr>
<tr class="odd">
<th colspan="2"></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th colspan="2"></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>Arithmetic computation and logical manipulation</th>
<th colspan="3"><p>Event EV01: Login Button Clicked (Section Username,
Password)</p>
<ol type="1">
<li></li>
<li></li>
<li></li>
</ol></th>
</tr>
<tr class="header">
<th>Additional Requirements</th>
<th colspan="3"><ol type="1">
<li></li>
<li></li>
</ol></th>
</tr>
<tr class="odd">
<th>External Reference</th>
<th colspan="3">Nil</th>
</tr>
<tr class="header">
<th>Program Limits</th>
<th colspan="3">Nil</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Dialogue Design

| ID                         | Name         | Data Item | I/O | Processing Remarks |
|-----|---------------|--------------------------------|-------|---------------|
| Section Username, Password |              |           |     |                    |
|                            | Email        |           |     |                    |
|                            | Password     |           |     |                    |
|                            | Login Button |           |     |                    |
| Section OTP                |              |           |     |                    |
|                            | OTP token    |           |     |                    |
|                            | Login Button |           |     |                    |

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 28%" />
<col style="width: 24%" />
<col style="width: 22%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th colspan="3"></th>
</tr>
<tr class="odd">
<th colspan="4"></th>
</tr>
<tr class="header">
<th></th>
<th colspan="3"></th>
</tr>
<tr class="odd">
<th colspan="4"></th>
</tr>
<tr class="header">
<th colspan="2"></th>
<th colspan="2"></th>
</tr>
<tr class="odd">
<th colspan="2"></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th colspan="2"></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th></th>
<th colspan="3"><ol type="1">
<li></li>
</ol></th>
</tr>
<tr class="header">
<th></th>
<th colspan="3"></th>
</tr>
<tr class="odd">
<th></th>
<th colspan="3"></th>
</tr>
<tr class="header">
<th></th>
<th colspan="3"></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Dialogue Design

| ID  | Name            | Data Item | I/O | Processing Remarks |
|-----|-----------------|-----------|-----|--------------------|
| 1   | App158 Template |           |     |                    |
| 2   | Record Date     |           |     |                    |
| 3   | Draft DateTime  |           |     |                    |
| 4   | Draft By User   |           |     |                    |

\<\<End of Document\>\>
