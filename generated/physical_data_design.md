# Physical Data Design for Licensing Self-Certification Portal (LSCP)

## Introduction

This document provides a comprehensive description of the physical data design for the Licensing Self-Certification Portal (LSCP) project. It serves as a blueprint for implementing the LSCP database, ensuring a robust and efficient data management system. This document covers the database statistics, collections overview, and field analysis for each collection. It also includes information about the technology stack and data import scripts.

## Objectives

The objectives of the LSCP are to:

1.  Provide user-friendly and meaningful messages to users.
2.  Store all electronic and paper submissions from applicants and authorized persons (AP)/registered structural engineers (RSE) for safety certificates and related applications.
3.  Provide a Buildings Department (BD) departmental portal login for internal users, with User ID and password as an alternative.
4.  Support the latest web browsers.
5.  Comply with the standards of the Government System Architecture and government IT security policy.

## Database Statistics

-   Database Size: 88.10 MB
-   Collections: 12
-   Total Documents: 1278983
-   Total Data Size: 371.24 MB

## Technology Stack

-   **Database Management System (DBMS):** Microsoft SQL Server 2019 (for the original data) and MongoDB (for the new backend)
-   **Backend Language:** JavaScript (Node.js)
-   **Framework:** Express
-   **ORM:** Mongoose (for MongoDB), Sequelize (for SQL Server)

## Collections Overview

| Collection Name   | Document Count | Size (MB) | N/A |-------------------|----------------|-----------| N/A |---|---|---| N/A | tasks             | 5523           | 0.99      | N/A |---|---|---| N/A | eminutes          | 133            | 0.03      | N/A |---|---|---| N/A | submissions       | 0              | 0.00      | N/A |---|---|---| N/A | applications      | 381            | 0.36      | N/A |---|---|---| N/A | notifications     | 1837           | 0.24      | N/A |---|---|---| N/A | bsblocks          | 98397          | 6.40      | N/A |---|---|---| N/A | cases             | 451            | 1.17      | N/A |---|---|---| N/A | oauthtokens       | 3019           | 2.29      | N/A |---|---|---| N/A | sysfilerefs       | 601808         | 204.70    | N/A |---|---|---| N/A | attachments       | 370            | 0.13      | N/A |---|---|---| N/A | users             | 116            | 0.04      | N/A |---|---|---| N/A | adrblkfilerefs    | 566948         | 154.89    | N/A |---|---|---|
## Data Entity Description

This section details the data model, including table names, entities, and key details stored in the database.

### Collection: tasks

| Field          | Types             | Occurrences | N/A |----------------|-------------------|-------------| N/A |---|---|---| N/A | __v            | objectId, int     | 1000        | N/A |---|---|---| N/A | _id            | objectId          | 1000        | N/A |---|---|---| N/A | application    | objectId          | 998         | N/A |---|---|---| N/A | createdAt      | date              | 1000        | N/A |---|---|---| N/A | status         | string            | 1000        | N/A |---|---|---| N/A | submissionCase | objectId          | 998         | N/A |---|---|---| N/A | taskType       | string            | 998         | N/A |---|---|---| N/A | team           | string            | 835         | N/A |---|---|---| N/A | user           | string, objectId  | 713         | N/A |---|---|---|
### Collection: eminutes

| Field          | Types             | Occurrences | N/A |----------------|-------------------|-------------| N/A |---|---|---| N/A | __v            | int               | 133         | N/A |---|---|---| N/A | _id            | objectId          | 133         | N/A |---|---|---| N/A | comment        | string            | 64          | N/A |---|---|---| N/A | content        | string            | 133         | N/A |---|---|---| N/A | createdAt      | date              | 133         | N/A |---|---|---| N/A | efolio         | string            | 100         | N/A |---|---|---| N/A | eminuteId      | string            | 133         | N/A |---|---|---| N/A | from           | objectId, string  | 133         | N/A |---|---|---| N/A | status         | string            | 133         | N/A |---|---|---| N/A | subject        | string            | 133         | N/A |---|---|---| N/A | submissionCase | objectId          | 133         | N/A |---|---|---| N/A | sysFileRefId   | string            | 65          | N/A |---|---|---| N/A | to             | objectId, string  | 129         | N/A |---|---|---|
### Collection: submissions

This collection currently has no documents.

### Collection: applications

| Field                     | Types                  | Occurrences | N/A |---------------------------|------------------------|-------------| N/A |---|---|---| N/A | APP13                     | object, array          | 172         | N/A |---|---|---| N/A | AddressOfPremiseCN        | string                 | 267         | N/A |---|---|---| N/A | AddressOfPremiseCNFloor   | string                 | 147         | N/A |---|---|---| N/A | AddressOfPremiseCNUnit    | string                 | 147         | N/A |---|---|---| N/A | AddressOfPremiseEN        | string                 | 271         | N/A |---|---|---| N/A | AddressOfPremiseENFloor   | string                 | 155         | N/A |---|---|---| N/A | AddressOfPremiseENUnit    | string                 | 154         | N/A |---|---|---| N/A | AgeOfStudent              | null, string           | 328         | N/A |---|---|---| N/A | ApplicantAddress          | string                 | 335         | N/A |---|---|---| N/A | ApplicantEmail            | string                 | 289         | N/A |---|---|---| N/A | ApplicantFax              | string                 | 21          | N/A |---|---|---| N/A | ApplicantMobile           | string                 | 288         | N/A |---|---|---| N/A | ApplicantName             | string                 | 189         | N/A |---|---|---| N/A | ApplicantNameCN           | string                 | 28          | N/A |---|---|---| N/A | ApplicantNameEN           | null, string           | 148         | N/A |---|---|---| N/A | ApplicantTel              | null, string           | 307         | N/A |---|---|---| N/A | ApplicationNo             | null, string           | 381         | N/A |---|---|---| N/A | ApplicationType           | string                 | 356         | N/A |---|---|---| N/A | Area                      | string                 | 28          | N/A |---|---|---| N/A | BlockID                   | string                 | 178         | N/A |---|---|---| N/A | ContactPerson             | string                 | 95          | N/A |---|---|---| N/A | ContactPersonCN           | string                 | 6           | N/A |---|---|---| N/A | ContactPersonEN           | string                 | 6           | N/A |---|---|---| N/A | ContactPersonEmail        | string                 | 6           | N/A |---|---|---| N/A | ContactPersonTel          | string                 | 6           | N/A |---|---|---| N/A | DescriptionOfSchool       | string, null           | 329         | N/A |---|---|---| N/A | District                  | string                 | 33          | N/A |---|---|---| N/A | EstimatedNoOfStudent      | int, null              | 328         | N/A |---|---|---| N/A | FileReference             | string                 | 35          | N/A |---|---|---| N/A | NameOfSchoolCN            | string                 | 323         | N/A |---|---|---| N/A | NameOfSchoolEN            | string                 | 350         | N/A |---|---|---| N/A | Region                    | string                 | 29          | N/A |---|---|---| N/A | RelatedPremise            | string                 | 62          | N/A |---|---|---| N/A | RelatedPremises           | array                  | 381         | N/A |---|---|---| N/A | SelfCertification         | object, null           | 65          | N/A |---|---|---| N/A | StructuralCalculation     | object                 | 18          | N/A |---|---|---| N/A | SubmissionType            | string                 | 187         | N/A |---|---|---| N/A | __v                       | int                    | 381         | N/A |---|---|---| N/A | _id                       | objectId               | 381         | N/A |---|---|---| N/A | address                   | object                 | 69          | N/A |---|---|---| N/A | assignedBS                | objectId, string, null | 364         | N/A |---|---|---| N/A | assignedGR                | objectId, null         | 64          | N/A |---|---|---| N/A | assignedSBS               | string, null           | 53          | N/A |---|---|---| N/A | createdAt                 | date                   | 381         | N/A |---|---|---| N/A | updatedAt                 | date                   | 194         | N/A |---|---|---|
### Collection: notifications

| Field            | Types      | Occurrences | N/A |------------------|------------|-------------| N/A |---|---|---| N/A | __v              | int        | 1000        | N/A |---|---|---| N/A | _id              | objectId   | 1000        | N/A |---|---|---| N/A | createdAt        | date       | 1000        | N/A |---|---|---| N/A | eminute          | objectId   | 58          | N/A |---|---|---| N/A | notificationType | string     | 1000        | N/A |---|---|---| N/A | requireSendEmail | bool       | 1000        | N/A |---|---|---| N/A | task             | objectId   | 942         | N/A |---|---|---| N/A | user             | string     | 991         | N/A |---|---|---|
### Collection: bsblocks

| Field     | Types  | Occurrences | N/A |-----------|--------|-------------| N/A |---|---|---| N/A | __v       | int    | 1000        | N/A |---|---|---| N/A | _id       | objectId | 1000        | N/A |---|---|---| N/A | bdgis     | string | 1000        | N/A |---|---|---| N/A | blockId   | string | 1000        | N/A |---|---|---|
### Collection: cases

| Field                       | Types          | Occurrences | N/A |-----------------------------|----------------|-------------| N/A |---|---|---| N/A | ActualReplyDate             | null, date     | 39          | N/A |---|---|---| N/A | Area                        | string         | 26          | N/A |---|---|---| N/A | AuditResult                 | string         | 11          | N/A |---|---|---| N/A | CaseOfficer                 | string         | 108         | N/A |---|---|---| N/A | Category                    | string         | 384         | N/A |---|---|---| N/A | District                    | string         | 37          | N/A |---|---|---| N/A | FileReference               | string         | 60          | N/A |---|---|---| N/A | LAFileReference             | object         | 17          | N/A |---|---|---| N/A | Nature                      | null, string   | 382         | N/A |---|---|---| N/A | ObjectiontoLR               | string         | 12          | N/A |---|---|---| N/A | ReceivedDate                | date, null     | 375         | N/A |---|---|---| N/A | Referrer                    | object         | 43          | N/A |---|---|---| N/A | Region                      | string         | 32          | N/A |---|---|---| N/A | Remarks                     | string         | 7           | N/A |---|---|---| N/A | Reminders                   | array          | 55          | N/A |---|---|---| N/A | SubmissionType              | string         | 8           | N/A |---|---|---| N/A | SubstantialReplyDate        | null, date     | 42          | N/A |---|---|---| N/A | TargetReplyDate             | date, null     | 111         | N/A |---|---|---| N/A | ThreeTierReqt               | string         | 12          | N/A |---|---|---| N/A | ViaSCS                      | bool           | 17          | N/A |---|---|---| N/A | __v                         | int            | 451         | N/A |---|---|---| N/A | _id                         | objectId       | 451         | N/A |---|---|---| N/A | application                 | objectId       | 450         | N/A |---|---|---| N/A | assignedBS                  | objectId       | 274         | N/A |---|---|---| N/A | assignedGR                  | objectId       | 137         | N/A |---|---|---| N/A | building_information        | object         | 14          | N/A |---|---|---| N/A | caseDescription             | object         | 9           | N/A |---|---|---| N/A | caseOfficerReceive          | string         | 172         | N/A |---|---|---| N/A | caseOfficerReply            | string         | 72          | N/A |---|---|---| N/A | createdAt                   | date           | 451         | N/A |---|---|---| N/A | deck_study                  | object         | 451         | N/A |---|---|---| N/A | documentChecklist           | object         | 2           | N/A |---|---|---| N/A | dv                          | object         | 197         | N/A |---|---|---| N/A | frc                         | object         | 451         | N/A |---|---|---| N/A | misc                        | object         | 451         | N/A |---|---|---| N/A | moe                         | object         | 451         | N/A |---|---|---| N/A | seniorCaseOfficerReceive    | string         | 54          | N/A |---|---|---| N/A | seniorCaseOfficerReply      | string         | 41          | N/A |---|---|---| N/A | site_inspection             | object         | 7           | N/A |---|---|---| N/A | structural_ccc_bs           | object         | 451         | N/A |---|---|---| N/A | structural_schnlh           | object         | 152         | N/A |---|---|---| N/A | structural_schnlhkinds      | object         | 301         | N/A |---|---|---| N/A | team                        | string         | 374         | N/A |---|---|---| N/A | ubw                         | object         | 451         | N/A |---|---|---| N/A | updatedAt                   | date           | 16          | N/A |---|---|---|
### Collection: oauthtokens

| Field                 | Types      | Occurrences | N/A |-----------------------|------------|-------------| N/A |---|---|---| N/A | __v                   | int        | 1000        | N/A |---|---|---| N/A | _id                   | objectId   | 1000        | N/A |---|---|---| N/A | accessToken           | string     | 1000        | N/A |---|---|---| N/A | accessTokenExpiresAt  | date       | 1000        | N/A |---|---|---| N/A | client                | object     | 1000        | N/A |---|---|---| N/A | refreshToken          | string     | 1000        | N/A |---|---|---| N/A | refreshTokenExpiresAt | date       | 1000        | N/A |---|---|---| N/A | user                  | objectId   | 1000        | N/A |---|---|---|
### Collection: sysfilerefs

| Field               | Types          | Occurrences | N/A |---------------------|----------------|-------------| N/A |---|---|---| N/A | __v                 | int            | 1000        | N/A |---|---|---| N/A | _id                 | objectId       | 1000        | N/A |---|---|---| N/A | createdDt           | date           | 1000        | N/A |---|---|---| N/A | createdName         | null, string   | 1000        | N/A |---|---|---| N/A | createdPost         | null, string   | 1000        | N/A |---|---|---| N/A | createdSection      | null, string   | 1000        | N/A |---|---|---| N/A | display             | string         | 1000        | N/A |---|---|---| N/A | dvExceed            | null, string   | 1000        | N/A |---|---|---| N/A | dvStatusDt          | null, date     | 1000        | N/A |---|---|---| N/A | frefPref            | string, null   | 1000        | N/A |---|---|---| N/A | frefSeq             | null, string   | 1000        | N/A |---|---|---| N/A | frefSuf             | null, string   | 1000        | N/A |---|---|---| N/A | frefYr              | null, string   | 1000        | N/A |---|---|---| N/A | lastModifiedDt      | date           | 1000        | N/A |---|---|---| N/A | lastModifiedName    | null, string   | 1000        | N/A |---|---|---| N/A | lastModifiedPost    | null, string   | 1000        | N/A |---|---|---| N/A | lastModifiedSection | null           | 1000        | N/A |---|---|---| N/A | sysFileRefId        | string         | 1000        | N/A |---|---|---|
### Collection: attachments

| Field          | Types          | Occurrences | N/A |----------------|----------------|-------------| N/A |---|---|---| N/A | __v            | int            | 370         | N/A |---|---|---| N/A | _id            | objectId       | 370         | N/A |---|---|---| N/A | application    | objectId       | 364         | N/A |---|---|---| N/A | createdAt      | date           | 370         | N/A |---|---|---| N/A | efolio         | null, string   | 351         | N/A |---|---|---| N/A | file           | object, string | 247         | N/A |---|---|---| N/A | filePartNo     | string         | 216         | N/A |---|---|---| N/A | receivedDate   | date           | 352         | N/A |---|---|---| N/A | remarks        | string         | 216         | N/A |---|---|---| N/A | subType        | string         | 203         | N/A |---|---|---| N/A | submissionCase | objectId       | 350         | N/A |---|---|---| N/A | sysFileRefId   | string         | 67          | N/A |---|---|---| N/A | type           | string         | 348         | N/A |---|---|---| N/A | updatedAt      | date           | 3           | N/A |---|---|---|
### Collection: users

| Field                | Types  | Occurrences | N/A |----------------------|--------|-------------| N/A |---|---|---| N/A | __v                  | int    | 116         | N/A |---|---|---| N/A | _id                  | objectId | 116         | N/A |---|---|---| N/A | bdgis                | string | 29          | N/A |---|---|---| N/A | begis                | string | 1           | N/A |---|---|---| N/A | delegateTo           | string | 8           | N/A |---|---|---| N/A | department           | string | 116         | N/A |---|---|---| N/A | email                | string | 109         | N/A |---|---|---| N/A | group                | string | 17          | N/A |---|---|---| N/A | lastLoginAt          | date   | 41          | N/A |---|---|---| N/A | letterLongPosition   | string | 11          | N/A |---|---|---| N/A | letterLongPositionCn | string | 12          | N/A |---|---|---| N/A | letterName           | string | 76          | N/A |---|---|---| N/A | letterNameCn         | string | 75          | N/A |---|---|---| N/A | letterPosition       | string | 79          | N/A |---|---|---| N/A | letterPositionCn     | string | 1           | N/A |---|---|---| N/A | lock                 | bool   | 116         | N/A |---|---|---| N/A | luPostName           | string | 78          | N/A |---|---|---| N/A | name                 | string | 80          | N/A |---|---|---| N/A | notificationEmail    | string | 23          | N/A |---|---|---| N/A | osdpEmail            | string | 62          | N/A |---|---|---| N/A | osdpLoginId          | string | 102         | N/A |---|---|---| N/A | password             | string | 108         | N/A |---|---|---| N/A | phoneNumber          | string | 65          | N/A |---|---|---| N/A | position             | string | 85          | N/A |---|---|---| N/A | role                 | string | 112         | N/A |---|---|---| N/A | team                 | string | 52          | N/A |---|---|---| N/A | userType             | string | 116         | N/A |---|---|---|
### Collection: adrblkfilerefs

| Field               | Types          | Occurrences | N/A |---------------------|----------------|-------------| N/A |---|---|---| N/A | __v                 | int            | 1000        | N/A |---|---|---| N/A | _id                 | objectId       | 1000        | N/A |---|---|---| N/A | adrBlkFileRefId     | string         | 1000        | N/A |---|---|---| N/A | adrBlkId            | string         | 1000        | N/A |---|---|---| N/A | createdDt           | date           | 1000        | N/A |---|---|---| N/A | createdName         | null, string   | 1000        | N/A |---|---|---| N/A | createdPost         | string         | 1000        | N/A |---|---|---| N/A | createdSection      | null, string   | 1000        | N/A |---|---|---| N/A | lastModifiedDt      | date           | 1000        | N/A |---|---|---| N/A | lastModifiedName    | null, string   | 1000        | N/A |---|---|---| N/A | lastModifiedPost    | string         | 1000        | N/A |---|---|---| N/A | lastModifiedSection | string, null   | 1000        | N/A |---|---|---| N/A | sysFileRefId        | string         | 1000        | N/A |---|---|---|
## Data Import Scripts

The following scripts are used to import data into the MongoDB database:

-   `importBsBlock.js`: Imports building structure data from an Excel file (`LU1.xlsx`) into the `bsblocks` collection.
-   `importFileRef.js`: Imports system file reference data from a CSV file (`sys_file_ref.csv`) into the `sysfilerefs` collection.
-   `importAdrFileRef.js`: Imports address block file reference data from a CSV file (`adr_blk_fileref.csv`) into the `adrblkfilerefs` collection.
-   `importUsers.js`: Imports user data from an Excel file (`UserList.xlsx`) into the `users` collection.
-   `importTeam.js`: Assigns teams to users based on their positions, using the `BS_TEAM_MAPPINGS` configuration.

## Scripts for Data Management

-   `FixBsBlock.js`: Cleans and standardizes the `bdgis` field in the `bsblocks` collection by removing whitespace and converting to uppercase.
-   `migrateGroupAndDepartment.js`: Migrates data from the `group` field to the `role` field in the `users` collection and sets the `department` field to "BD".
-   `syncFrontendSubmissions.js`: Synchronizes submissions from the frontend to the backend database.

## API Endpoints

The backend provides the following API endpoints for data access and manipulation:

-   `/applications`: Manages application-related operations.
-   `/auth`: Handles authentication and token management.
-   `/users`: Manages user-related operations.
-   `/tasks`: Manages tasks related to applications and cases.
-   `/cases`: Manages cases related to applications.
-   `/attachments`: Manages file attachments for applications and cases.
-   `/file-references`: Provides access to system file references.

## Models

The backend uses the following Mongoose and Sequelize models to represent data entities:

**Mongoose Models:**

-   `Application.js`: Represents application data.
-   `Submission.js`: Represents submission data.
-   `Attachment.js`: Represents file attachments.
-   `BsBlock.js`: Represents building structure block data.
-   `Task.js`: Represents tasks in the workflow.
-   `Case.js`: Represents cases related to applications.
-   `Eminute.js`: Represents electronic minutes.
-   `OAuthToken.js`: Represents OAuth tokens for authentication.
-   `User.js`: Represents user data.
-   `Notification.js`: Represents notifications.
-   `SysFileRef.js`: Represents system file references.
-   `AdrBlkFileRef.js`: Represents address block file references.

**Sequelize Models:**

-   `AdrBlk.js`: Represents address block data.
-   `ApplicationCase.js`: Represents application case data.
-   `ApplicationFile.js`: Represents application file data.
-   `ApRse.js`: Represents AP/RSE data.
-   `BackendUpdate.js`: Represents backend updates.
-   `GenOtp.js`: Represents generated OTP data.
-   `IamSmart.js`: Represents IAM Smart data.
-   `LogEvents.js`: Represents log events.
-   `SchoolAppInfo.js`: Represents school application information.
-   `SchoolAppSubmission.js`: Represents school application submissions.
-   `ScsMasterTable.js`: Represents SCS master table data.
-   `Staff.js`: Represents staff data.
-   `Sys_Meta_Data.js`: Represents system metadata.
-   `Test.js`: Represents test data.