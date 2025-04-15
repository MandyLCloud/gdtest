# Physical Data Design for Licensing Self-Certification Portal (LSCP)

**Version 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

## 1. Introduction

This document provides a comprehensive description of the physical data design for the Licensing Self-Certification Portal (LSCP) project. It serves as a blueprint for implementing the LSCP database, ensuring a robust and efficient data management system.

This document details the physical data structure, relationships between key business entities, and descriptions of each entity, its attributes, and data types. It also outlines the database management system (DBMS) selected for the LSCP.

## 2. Objectives

The objectives of the LSCP include:

1.  Providing user-friendly and meaningful messages to users.
2.  Storing electronic and paper submissions from applicants and authorized persons (AP)/registered structural engineers (RSE).
3.  Providing BD departmental portal login for internal users (BD), and providing User ID and password as an alternative.
4.  Supporting the latest web browsers.
5.  Complying with the standards of the Government System Architecture and government IT security policy.

## 3. Physical Data Structure Specification

This section details the data model and its descriptions.

### 3.1. Physical Data Structure

The entity-relationship diagram illustrates the relationships between entities.

![ER Diagram](media/image1.png)

There are 7 categories of entities in the data model design:

*   (GCIS) Frontend - Application Forms submission
*   (GCIS) Frontend - OTP login control
*   Backend - Users
*   Backend - Workflow of Application Forms submission

#### 3.1.1. (GCIS) Frontend - Application Forms Submission

![Frontend Application Forms Submission](media/image3.jpg)

#### 3.1.2. (GCIS) Frontend - OTP login control

![Frontend OTP Login Control](media/image3.jpg)

#### 3.1.3. (BD) Backend - TBC

![Backend TBC](media/image3.jpg)

## 4. Data Entity Description

This section details the conversion rules, assumptions, physical data table names, corresponding system entities, and key details stored in the database.

**Database Management System (DBMS):** Microsoft SQL Server 2019

All spatial and textual entities will be stored in Microsoft SQL Server 2019.

**Conversion Rules and Assumptions:**

*   Data types are chosen to efficiently store and represent the data.
*   Relationships are enforced using primary and foreign keys.
*   Constraints are implemented to ensure data integrity.

**Table Mapping:**

### LSCP Frontend

| Table ID | LSCP Name           | LSCP Entity Description                                                     | Key Nature | Key Data Item                | N/A |----------|---------------------|-----------------------------------------------------------------------------|------------|-----------------------------------|---|---| N/A | T-S-01   | ApplicationCases    | Table to store all the application number                                   | PK         | Id                           | N/A | N/A | N/A | N/A | N/A | ApplicationNo                ---|---|---| N/A | T-S-02   | SchoolApp\_Infos    | Table to store the latest update of the submitted application data as 1 row | PK         | Id                           | N/A | N/A | N/A | N/A | N/A | ApplicationNo                ---|---|---| N/A | T-S-03   | SchoolApp\_Submissions | Table to store the submission of each application                           | PK         | Id                           | N/A | N/A | N/A | N/A | N/A | ApplicationNo                | N/A | N/A | N/A | N/A | N/A | SubmissionId                 ---|---|---| N/A | T-S-04   | ApplicationFiles    | Table to store all the path of applicant upload files                       | PK         | Id                           | N/A | N/A | N/A | N/A | N/A | ApplicationNo                | N/A | N/A | N/A | N/A | N/A | SubmissionId                 ---|---|---| N/A | T-S-05   | LSCPMasterTable     | Table to store meta-data or parameter data for frontend                     | PK         | Id                           | N/A | N/A | N/A | N/A | N/A | Code                         | N/A | N/A | N/A | N/A | N/A | Type + Code                  ---|---|---| N/A | T-S-06   | GenOtp              | Table to store generated OTP code and the usage status                      | PK         | Id                           | N/A | N/A | N/A | N/A | N/A | ApplicationNo + userId + Otp ---|---|---| N/A | T-S-07   | AdrBlk              | Table to store addresses that import from BCIS                              | PK         | ADR\_BLK\_ID                   ---|---|---| N/A | T-S-08   | SYS\_META\_DATA       | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID             | N/A | N/A | N/A | N/A | N/A | REC\_TYPE         | N/A | N/A | N/A | N/A | N/A | CODE                         ---|---|---| N/A | T-S-09   | Aprse               | Table to store AP / RSE information that import from MWMS 2.0               | PK         | Id                           | N/A | N/A | N/A | N/A | N/A | Name + RegistrationNumber    ---|---|---| N/A |---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
### LSCP Backend

| Table ID | LSCP Name           | LSCP Entity Description                                                     | Key Nature | Key Data Item    | N/A |----------|---------------------|-----------------------------------------------------------------------------|------------|----------------------|---|---| N/A | T-S-01   | ApplicationCases    | Table to store all the application number                                   | PK         | Id               | N/A | N/A | N/A | N/A | N/A | ApplicationNo    ---|---|---| N/A | T-S-02   | SchoolApp\_Infos    | Table to store the latest update of the submitted application data as 1 row | PK         | Id               | N/A | N/A | N/A | N/A | N/A | ApplicationNo    ---|---|---| N/A | T-S-03   | SchoolApp\_Submissions | Table to store the submission of each application                           | PK         | Id               | N/A | N/A | N/A | N/A | N/A | ApplicationNo    | N/A | N/A | N/A | N/A | N/A | SubmissionId     ---|---|---| N/A | T-S-04   | ApplicationFiles    | Table to store all the path of applicant upload files                       | PK         | Id               | N/A | N/A | N/A | N/A | N/A | ApplicationNo    | N/A | N/A | N/A | N/A | N/A | SubmissionId     ---|---|---| N/A | T-S-05   | LSCPMasterTable     | Table to store meta-data or parameter data for frontend                     | PK         | Id               | N/A | N/A | N/A | N/A | N/A | Code             | N/A | N/A | N/A | N/A | N/A | Type + Code      ---|---|---| N/A | T-S-06   | SYS\_META\_DATA       | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID | N/A | N/A | N/A | N/A | N/A | REC\_TYPE         | N/A | N/A | N/A | N/A | N/A | CODE             ---|---|---| N/A | T-S-07   | AdrBlk              | Table to store addresses that import from BCIS                              | PK         | ADR\_BLK\_ID                   ---|---|---| N/A | T-S-08   | SYS\_META\_DATA       | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID | N/A | N/A | N/A | N/A | N/A | REC\_TYPE         | N/A | N/A | N/A | N/A | N/A | CODE             ---|---|---| N/A | T-S-09   | Aprse               | Table to store AP / RSE information that import from MWMS 2.0               | PK         | Id                           | N/A | N/A | N/A | N/A | N/A | Name + RegistrationNumber    ---|---|---| N/A |---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
\*\*\* End of document\*\*\*