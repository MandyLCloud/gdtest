<img src="media/image2.jpg" style="width:2.03125in;height:1.52083in"
alt="BDlogo" />

**<span class="smallcaps">PHYSICAL DATA DESIGN</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">COMBINED SYSTEM DEVELOPMENT SERVICES</span>**

**<span class="smallcaps">FOR</span>**

**<span class="smallcaps">LICENSING SELF-CERTIFICATION PORTAL</span>**

**<span class="smallcaps">OF THE</span>**

**<span class="smallcaps">BUILDINGS DEPARTMENT</span>**

**Version 0.1**

**Jan 2025**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR.

<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 80%" />
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
|-----------|--------------------|-------------------|-----------|-------------|
| Change Number         | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date       |
| 1                     | 1st draft            | All                                  | 0.1                       | 16/01/2025 |
|                       |                      |                                      |                           |            |
|                       |                      |                                      |                           |            |
|                       |                      |                                      |                           |            |

**TABLE OF CONTENTS**

[1. Introduction 4](#introduction)

[2. Objectives 5](#objectives)

> [3. Physical Data Structure Specification
> 6](#physical-data-structure-specification)
>
> [3.1. Physical Data Structure 6](#physical-data-structure)
>
> [3.1.1. (GCIS) Frontend - Application Forms Submission
> 7](#gcis-frontend---application-forms-submission)
>
> [3.1.2. (GCIS) Frontend - OTP login control
> 8](#gcis-frontend---otp-login-control)
>
> [3.1.3. (BD) Backend - TBC 9](#bd-backend---tbc)

[4. Data Entity Description 10](#data-entity-description)

# Introduction

This Physical Data Design Document provides a comprehensive description
of the physical data structure and process design for the Licensing
Self-Certification Portal (LSCP) Project. This document serves as a
blueprint for the implementation of the LSCP database, ensuring a robust
and efficient data management system.

The document delves into the detailed relationships between key business
entities within the LSCP. A clear and concise diagrammatic
representation is provided to visually illustrate the connections
between these entities. This section also includes a comprehensive
description of each entity, its attributes, and the data types used to
represent them. The data relationships are further explained,
highlighting the primary keys, foreign keys, and any constraints imposed
on the data.

By providing a detailed understanding of the physical data structure,
this document serves as a valuable resource for developers, database
administrators, and other stakeholders involved in the implementation
and maintenance of the LSCP.

#  

# Objectives

The objectives of the proposed Licensing Self-Certification Portal
(LSCP) should:

1.  Provide user-friendly and meaningful messages to users.

2.  Store all electronic and paper submissions from applicant and
    > authorized person (AP)/registered structural engineer (RSE)
    > applications of the requisite safety certificates for registration
    > of non-purpose built schools and child care centres, and
    > applications in related to non-purpose non-local higher and
    > professional education courses.

3.  BD departmental portal login for internal users (BD), and provide
    > User ID and password as an alternative.

4.  Support the latest web browsers.

5.  Comply with the standards of the Government System Architecture and
    > government IT security policy.

## Physical Data Structure Specification

This section documents the data model and its associated descriptions of
the required system.

##  Physical Data Structure

An entity-relationship diagram consists of three basic elements such as
entity, relationship, and attribute. Along with these are more
components based on their main elements like weak entity, multi-valued
attribute, and many more. Notations used to make ERD diagram examples
include cardinality and ordinality to define relationships in numbers.  
  
<img src="media/image1.png" style="width:3.79114in;height:2.47369in"
alt="A screenshot of a white sheet Description automatically generated" />

There are 7 categories of entities in the data model design.

-   (CGIS) Frontend - Application Forms submission

-   (CGIS) Frontend - OTP login control

-   Backend - Users

-   Backend - Workflow of Application Forms submission

### (GCIS) Frontend - Application Forms Submission

<img src="media/image3.jpg" style="width:6.38161in;height:6.68056in" />

> Diagram 3.1-1

### (GCIS) Frontend - OTP login control

Diagram 3.1-2

Pending

### (BD) Backend - TBC

Diagram 3.1-3

Pending

# Data Entity Description

This section states the conversion rules, the assumptions applied for
the physical data design, the names of the physical data tables, the
corresponding required system entities and key details to be stored into
the database.

The database is a physical store of contract related information and
textual data inside a database management system (DBMS). For LSCP,
<span class="mark">Microsoft SQL Server 2019</span> is selected for the
database management system. <span class="mark">All the spatial and
textual entity will be stored into Microsoft SQL Server 2019.</span>

The following tables document how the Logical Data Model (LDM) can be
mapped onto the physical data design.

<span class="mark">(RY Note: following table needs to review its
correctness)</span>

> LSCP Frontend

| Table ID | LSCP Name                                 | LSCP Entity Description                                                     | Key Nature | Key Data Item                |
|--------|--------------|---------------------------|--------|----------------|
| T-S-01   | ApplicationCases                          | Table to store all the application number                                   | PK         | Id                           |
|          |                                           |                                                                             |            | ApplicationNo                |
| T-S-02   | SchoolApp_Infos                           | Table to store the latest update of the submitted application data as 1 row | PK         | Id                           |
|          |                                           |                                                                             |            | ApplicationNo                |
| T-S-03   | SchoolApp_Submissions                     | Table to store the submission of each application                           | PK         | Id                           |
|          |                                           |                                                                             |            | ApplicationNo                |
|          |                                           |                                                                             |            | SubmissionId                 |
| T-S-04   | ApplicationFiles                          | Table to store all the path of applicant upload files                       | PK         | Id                           |
|          |                                           |                                                                             |            | ApplicationNo                |
|          |                                           |                                                                             |            | SubmissionId                 |
| T-S-05   | <span class="mark">LSCPMasterTable</span> | Table to store meta-data or parameter data for frontend                     | PK         | Id                           |
|          |                                           |                                                                             |            | Code                         |
|          |                                           |                                                                             |            | Type + Code                  |
| T-S-06   | GenOtp                                    | Table to store generated OTP code and the usage status                      | PK         | Id                           |
|          |                                           |                                                                             |            | ApplicationNo + userId + Otp |
| T-S-07   | AdrBlk                                    | Table to store addresses that import from BCIS                              | PK         | ADR_BLK_ID                   |
| T-S-08   | SYS_META_DATA                             | Table to store meta data that import from BCIS                              | PK         | SYS_META_DATA_ID             |
|          |                                           |                                                                             |            | REC_TYPE                     |
|          |                                           |                                                                             |            | CODE                         |
| T-S-09   | Aprse                                     | Table to store AP / RSE information that import from MWMS 2.0               | PK         | Id                           |
|          |                                           |                                                                             |            | Name + RegistrationNumber    |

> LSCP Backend

| Table ID | LSCP Name                                 | LSCP Entity Description                                                     | Key Nature | Key Data Item    |
|--------|--------------|---------------------------|--------|----------------|
| T-S-01   | ApplicationCases                          | Table to store all the application number                                   | PK         | Id               |
|          |                                           |                                                                             |            | ApplicationNo    |
| T-S-02   | SchoolApp_Infos                           | Table to store the latest update of the submitted application data as 1 row | PK         | Id               |
|          |                                           |                                                                             |            | ApplicationNo    |
| T-S-03   | SchoolApp_Submissions                     | Table to store the submission of each application                           | PK         | Id               |
|          |                                           |                                                                             |            | ApplicationNo    |
|          |                                           |                                                                             |            | SubmissionId     |
| T-S-04   | ApplicationFiles                          | Table to store all the path of applicant upload files                       | PK         | Id               |
|          |                                           |                                                                             |            | ApplicationNo    |
|          |                                           |                                                                             |            | SubmissionId     |
| T-S-05   | <span class="mark">LSCPMasterTable</span> | Table to store meta-data or parameter data for frontend                     | PK         | Id               |
|          |                                           |                                                                             |            | Code             |
|          |                                           |                                                                             |            | Type + Code      |
| T-S-06   | SYS_META_DATA                             | Table to store meta data that import from BCIS                              | PK         | SYS_META_DATA_ID |
|          |                                           |                                                                             |            | REC_TYPE         |
|          |                                           |                                                                             |            | CODE             |
| T-S-07   | SYS_META_DATA                             | Table to store meta data that import from BCIS                              | PK         | SYS_META_DATA_ID |
|          |                                           |                                                                             |            | REC_TYPE         |
|          |                                           |                                                                             |            | CODE             |

\*\*\* End of document\*\*\*
