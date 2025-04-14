# Physical Data Design for Licensing Self-Certification Portal

**Version 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

## 1. Introduction

This document provides a comprehensive description of the physical data structure and process design for the Licensing Self-Certification Portal (LSCP) Project. It serves as a blueprint for the implementation of the LSCP database, ensuring a robust and efficient data management system.

## 2. Objectives

The objectives of the LSCP are to:

1.  Provide user-friendly and meaningful messages to users.
2.  Store all electronic and paper submissions from applicants and authorized persons (AP)/registered structural engineers (RSE).
3.  Provide BD departmental portal login for internal users (BD), and offer User ID and password as an alternative.
4.  Support the latest web browsers.
5.  Comply with the standards of the Government System Architecture and government IT security policy.

## 3. Physical Data Structure Specification

This section documents the data model and its associated descriptions of the required system.

### 3.1. Physical Data Structure

The LSCP uses a database with the following key characteristics:

*   **Database Management System (DBMS):** Microsoft SQL Server 2019
*   **Data Storage:** Both spatial and textual data are stored within the SQL Server.

The database schema is implemented using Mongoose with MongoDB on the backend, and Sequelize with Microsoft SQL Server on the Node.js frontend. The data is synchronized between the two databases.

#### 3.1.1. (GCIS) Frontend - Application Forms Submission

The frontend utilizes Sequelize models connected to a Microsoft SQL Server database.

Key tables include:

*   `SchoolApp_Submissions`: Stores submission data.
*   `SchoolApp_Infos`: Stores application information.
*   `ApplicationFiles`: Stores file attachments.
*   `ScsMasterTable`: Stores meta-data.
*   `AdrBlk`: Stores address information.
*   `ApRse`: Stores AP/RSE information.
*   `GenOtp`: Stores OTP codes for login verification.

#### 3.1.2. (GCIS) Frontend - OTP login control

This section manages user authentication through One-Time Passwords (OTPs).

#### 3.1.3. (BD) Backend

The backend utilizes Mongoose models connected to a MongoDB database.

Key collections include:

*   `Application`: Stores application data.
*   `Submission`: Stores submission data.
*   `Attachment`: Stores file attachments.
*   `BsBlock`: Stores block ID and BDGIS code mappings.
*   `Task`: Stores workflow tasks.
*   `Case`: Stores case details.
*   `Eminute`: Stores e-minute details.
*   `OAuthToken`: Stores OAuth tokens for authentication.
*   `User`: Stores user information.
*   `Notification`: Stores notifications.
*   `SysFileRef`: Stores system file reference information.
*   `AdrBlkFileRef`: Stores address block file reference information.

## 4. Data Entity Description

This section details the conversion rules, assumptions, table names, entities, and key data items stored in the database.

**LSCP Frontend (Microsoft SQL Server)**

| Table ID | LSCP Name                  | LSCP Entity Description                                  | Key Nature | Key Data Item                               |
| :------- | :------------------------- | :------------------------------------------------------- | :--------- | :------------------------------------------ |
| T-S-01   | ApplicationCase            | Stores application case data                             | PK         | Id                                          |
|          |                            |                                                          |            | ApplicationNo                               |
| T-S-02   | SchoolApp_Infos            | Stores application information (latest update)           | PK         | Id                                          |
|          |                            |                                                          |            | ApplicationNo                               |
| T-S-03   | SchoolApp_Submissions      | Stores application submissions                           | PK         | Id                                          |
|          |                            |                                                          |            | ApplicationNo                               |
|          |                            |                                                          |            | SubmissionId                                |
| T-S-04   | ApplicationFiles           | Stores file attachments                                  | PK         | Id                                          |
|          |                            |                                                          |            | ApplicationNo                               |
|          |                            |                                                          |            | SubmissionId                                |
| T-S-05   | LSCPMasterTable            | Stores meta-data for the frontend                        | PK         | Id                                          |
|          |                            |                                                          |            | Code                                        |
|          |                            |                                                          |            | Type + Code                                 |
| T-S-06   | GenOtp                     | Stores OTP codes and usage status                        | PK         | Id                                          |
|          |                            |                                                          |            | ApplicationNo + userId + Otp                |
| T-S-07   | AdrBlk                     | Stores addresses imported from BCIS                       | PK         | ADR_BLK_ID                                  |
| T-S-08   | SYS_META_DATA              | Stores meta-data imported from BCIS                       | PK         | SYS_META_DATA_ID                            |
|          |                            |                                                          |            | REC_TYPE                                    |
|          |                            |                                                          |            | CODE                                        |
| T-S-09   | Aprse                      | Stores AP/RSE information imported from MWMS 2.0          | PK         | Id                                          |
|          |                            |                                                          |            | Name + RegistrationNumber                   |

**LSCP Backend (MongoDB)**

| Table ID | LSCP Name                  | LSCP Entity Description                                  | Key Nature | Key Data Item    |
| :------- | :------------------------- | :------------------------------------------------------- | :--------- | :----------------- |
| T-S-01   | Application                | Stores application data                                  | PK         | \_id               |
|          |                            |                                                          |            | ApplicationNo    |
| T-S-02   | Submission                 | Stores submission data                                   | PK         | \_id               |
|          |                            |                                                          |            | Application        |
| T-S-03   | Attachment                 | Stores file attachments                                  | PK         | \_id               |
|          |                            |                                                          |            | Application        |
|          |                            |                                                          |            | SubmissionCase     |
| T-S-04   | BsBlock                    | Stores block ID and BDGIS code mappings                  | PK         | \_id               |
|          |                            |                                                          |            | blockId            |
| T-S-05   | Task                       | Stores workflow tasks                                    | PK         | \_id               |
|          |                            |                                                          |            | application        |
|          |                            |                                                          |            | submissionCase     |
| T-S-06   | Case                       | Stores case details                                      | PK         | \_id               |
|          |                            |                                                          |            | application        |
| T-S-07   | Eminute                    | Stores e-minute details                                  | PK         | \_id               |
|          |                            |                                                          |            | submissionCase     |
| T-S-08   | OAuthToken                 | Stores OAuth tokens for authentication                   | PK         | \_id               |
|          |                            |                                                          |            | accessToken        |
| T-S-09   | User                       | Stores user information                                  | PK         | \_id               |
|          |                            |                                                          |            | osdpLoginId        |
| T-S-10   | Notification               | Stores notifications                                     | PK         | \_id               |
|          |                            |                                                          |            | user               |
| T-S-11   | SysFileRef                 | Stores system file reference information                 | PK         | \_id               |
|          |                            |                                                          |            | sysFileRefId       |
| T-S-12   | AdrBlkFileRef              | Stores address block file reference information          | PK         | \_id               |
|          |                            |                                                          |            | adrBlkFileRefId    |

\*\*\* End of document\*\*\*