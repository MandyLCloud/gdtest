# Physical Data Design for Licensing Self-Certification Portal (LSCP)

**Version 0.1**

**Jan 2025**

## 1. Introduction

This document provides a comprehensive description of the physical data structure and process design for the Licensing Self-Certification Portal (LSCP) Project. It serves as a blueprint for the implementation of the LSCP database, ensuring a robust and efficient data management system.

The document details the relationships between key business entities within the LSCP, including a diagrammatic representation and comprehensive descriptions of each entity, its attributes, and data types. Data relationships are further explained, highlighting primary keys, foreign keys, and constraints.

This document serves as a valuable resource for developers, database administrators, and other stakeholders involved in the implementation and maintenance of the LSCP.

## 2. Objectives

The objectives of the LSCP are:

1.  Provide user-friendly and meaningful messages to users.
2.  Store all electronic and paper submissions from applicant and authorized person (AP)/registered structural engineer (RSE) applications of the requisite safety certificates for registration of non-purpose built schools and child care centres, and applications in related to non-purpose non-local higher and professional education courses.
3.  Provide BD departmental portal login for internal users (BD), and provide User ID and password as an alternative.
4.  Support the latest web browsers.
5.  Comply with the standards of the Government System Architecture and government IT security policy.

## 3. Physical Data Structure Specification

This section documents the data model and its associated descriptions of the required system.

### 3.1. Physical Data Structure

An entity-relationship diagram consists of three basic elements such as entity, relationship, and attribute. Along with these are more components based on their main elements like weak entity, multi-valued attribute, and many more. Notations used to make ERD diagram examples include cardinality and ordinality to define relationships in numbers.

**Entity-Relationship Diagram:**

(Diagram image is not possible to render in markdown. Refer to the original document for the visual representation.)

**Categories of Entities:**

*   (GCIS) Frontend - Application Forms submission
*   (GCIS) Frontend - OTP login control
*   (BD) Backend - Users
*   Backend - Workflow of Application Forms submission

#### 3.1.1. (GCIS) Frontend - Application Forms Submission

(Diagram image is not possible to render in markdown. Refer to the original document for the visual representation.)

#### 3.1.2. (GCIS) Frontend - OTP login control

(Diagram image is not possible to render in markdown. Refer to the original document for the visual representation.)

#### 3.1.3. (BD) Backend - TBC

(Diagram image is not possible to render in markdown. Refer to the original document for the visual representation.)

## 4. Data Entity Description

This section states the conversion rules, the assumptions applied for the physical data design, the names of the physical data tables, the corresponding required system entities and key details to be stored into the database.

The database is a physical store of contract related information and textual data inside a database management system (DBMS). For LSCP, Microsoft SQL Server 2019 is selected for the database management system. All the spatial and textual entity will be stored into Microsoft SQL Server 2019.

The following tables document how the Logical Data Model (LDM) can be mapped onto the physical data design.

**LSCP Frontend**

| Table ID | LSCP Name           | LSCP Entity Description                                                     | Key Nature | Key Data Item                | N/A | :------- | :------------------ | :-------------------------------------------------------------------------- | :--------- | :--------------------------- | N/A |---|---|---|---|---| N/A | T-S-01   | ApplicationCases    | Table to store all the application number                                   | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |---|---|---|---|---| N/A | T-S-02   | SchoolApp\_Infos    | Table to store the latest update of the submitted application data as 1 row | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |---|---|---|---|---| N/A | T-S-03   | SchoolApp\_Submissions | Table to store the submission of each application                           | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |          | N/A |                                                                             | N/A | SubmissionId                 | N/A |---|---|---|---|---| N/A | T-S-04   | ApplicationFiles    | Table to store all the path of applicant upload files                       | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |          | N/A |                                                                             | N/A | SubmissionId                 | N/A |---|---|---|---|---| N/A | T-S-05   | LSCPMasterTable     | Table to store meta-data or parameter data for frontend                     | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | Code                         | N/A |          | N/A |                                                                             | N/A | Type + Code                  | N/A |---|---|---|---|---| N/A | T-S-06   | GenOtp              | Table to store generated OTP code and the usage status                      | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo + userId + Otp | N/A |---|---|---|---|---| N/A | T-S-07   | AdrBlk              | Table to store addresses that import from BCIS                              | PK         | ADR\_BLK\_ID                   | N/A |---|---|---|---|---| N/A | T-S-08   | SYS\_META\_DATA     | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID             | N/A |          | N/A |                                                                             | N/A | REC\_TYPE                     | N/A |          | N/A |                                                                             | N/A | CODE                         | N/A |---|---|---|---|---| N/A | T-S-09   | Aprse               | Table to store AP / RSE information that import from MWMS 2.0               | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | Name + RegistrationNumber    | N/A |---|---|---|---|---|
**LSCP Backend**

| Table ID | LSCP Name           | LSCP Entity Description                                                     | Key Nature | Key Data Item    | N/A | :------- | :------------------ | :-------------------------------------------------------------------------- | :--------- | :----------------- | N/A |---|---|---|---|---| N/A | T-S-01   | ApplicationCases    | Table to store all the application number                                   | PK         | Id               | N/A |          | N/A |                                                                             | N/A | ApplicationNo    | N/A |---|---|---|---|---| N/A | T-S-02   | SchoolApp\_Infos    | Table to store the latest update of the submitted application data as 1 row | PK         | Id               | N/A |          | N/A |                                                                             | N/A | ApplicationNo    | N/A |---|---|---|---|---| N/A | T-S-03   | SchoolApp\_Submissions | Table to store the submission of each application                           | PK         | Id               | N/A |          | N/A |                                                                             | N/A | ApplicationNo    | N/A |          | N/A |                                                                             | N/A | SubmissionId     | N/A |---|---|---|---|---| N/A | T-S-04   | ApplicationFiles    | Table to store all the path of applicant upload files                       | PK         | Id               | N/A |          | N/A |                                                                             | N/A | ApplicationNo    | N/A |          | N/A |                                                                             | N/A | SubmissionId     | N/A |---|---|---|---|---| N/A | T-S-05   | LSCPMasterTable     | Table to store meta-data or parameter data for frontend                     | PK         | Id               | N/A |          | N/A |                                                                             | N/A | Code             | N/A |          | N/A |                                                                             | N/A | Type + Code      | N/A |---|---|---|---|---| N/A | T-S-06   | SYS\_META\_DATA     | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID | N/A |          | N/A |                                                                             | N/A | REC\_TYPE         | N/A |          | N/A |                                                                             | N/A | CODE             | N/A |---|---|---|---|---| N/A | T-S-07   | SYS\_META\_DATA     | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID | N/A |          | N/A |                                                                             | N/A | REC\_TYPE         | N/A |          | N/A |                                                                             | N/A | CODE             | N/A |---|---|---|---|---|
\*\*\* End of document\*\*\*
