# Physical Data Design for Licensing Self-Certification Portal

This document outlines the physical data design for the Licensing Self-Certification Portal (LSCP) project, focusing on the database structure and key considerations for implementation.

## 1. Introduction

This document provides a comprehensive description of the physical data structure and process design for the Licensing Self-Certification Portal (LSCP) Project. This document serves as a blueprint for the implementation of the LSCP database, ensuring a robust and efficient data management system.

The document delves into the detailed relationships between key business entities within the LSCP. A clear and concise diagrammatic representation is provided to visually illustrate the connections between these entities. This section also includes a comprehensive description of each entity, its attributes, and the data types used to represent them. The data relationships are further explained, highlighting the primary keys, foreign keys, and any constraints imposed on the data.

By providing a detailed understanding of the physical data structure, this document serves as a valuable resource for developers, database administrators, and other stakeholders involved in the implementation and maintenance of the LSCP.

## 2. Objectives

The objectives of the proposed Licensing Self-Certification Portal (LSCP) should:

1.  Provide user-friendly and meaningful messages to users.
2.  Store all electronic and paper submissions from applicant and authorized person (AP)/registered structural engineer (RSE) applications of the requisite safety certificates for registration of non-purpose built schools and child care centres, and applications in related to non-purpose non-local higher and professional education courses.
3.  BD departmental portal login for internal users (BD), and provide User ID and password as an alternative.
4.  Support the latest web browsers.
5.  Comply with the standards of the Government System Architecture and government IT security policy.

## 3. Physical Data Structure Specification

This section details the data model, including descriptions of the collections and their fields.

### 3.1. Physical Data Structure

The LSCP system utilizes a multi-database approach, leveraging both MongoDB and Microsoft SQL Server. MongoDB is used for flexible document storage, while SQL Server provides a relational structure for specific data requirements.

**Entity-Relationship Diagram (Conceptual)**

```
[Insert ER Diagram Here - Not provided in the input files, but would be beneficial]
```

**Collections Overview (MongoDB)**

The MongoDB database named `bd` contains the following collections:

*   **tasks**: Stores information about tasks assigned to users.
*   **eminutes**: Stores electronic minutes related to cases.
*   **submissions**: Stores submission data (currently empty).
*   **applications**: Stores application form data.
*   **notifications**: Stores notifications for users.
*   **bsblocks**: Stores building structure block data.
*   **cases**: Stores case-related information.
*   **oauthtokens**: Stores OAuth tokens for authentication.
*   **sysfilerefs**: Stores system file references.
*   **attachments**: Stores file attachments related to applications and cases.
*   **users**: Stores user information.
*   **adrblkfilerefs**: Stores address block file references.

**Table Mapping (Microsoft SQL Server)**

| Table ID | LSCP Name                  | LSCP Entity Description                                                     | Key Nature | Key Data Item                | N/A |----------|----------------------------|-----------------------------------------------------------------------------|------------|----------------------------| N/A |---|---|---|---|---| N/A | T-S-01   | ApplicationCase            | Table to store all the application number                                   | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |---|---|---|---|---| N/A | T-S-02   | SchoolApp\_Infos           | Table to store the latest update of the submitted application data as 1 row | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |---|---|---|---|---| N/A | T-S-03   | SchoolApp\_Submissions     | Table to store the submission of each application                           | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |          | N/A |                                                                             | N/A | SubmissionId                 | N/A |---|---|---|---|---| N/A | T-S-04   | ApplicationFiles           | Table to store all the path of applicant upload files                       | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |          | N/A |                                                                             | N/A | SubmissionId                 | N/A |---|---|---|---|---| N/A | T-S-05   | LSCPMasterTable          | Table to store meta-data or parameter data for frontend                     | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | Code                         | N/A |          | N/A |                                                                             | N/A | Type + Code                  | N/A |---|---|---|---|---| N/A | T-S-06   | GenOtp                     | Table to store generated OTP code and the usage status                      | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo + userId + Otp | N/A |---|---|---|---|---| N/A | T-S-07   | AdrBlk                     | Table to store addresses that import from BCIS                              | PK         | ADR\_BLK\_ID                   | N/A |---|---|---|---|---| N/A | T-S-08   | SYS\_META\_DATA             | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID             | N/A |          | N/A |                                                                             | N/A | REC\_TYPE                     | N/A |          | N/A |                                                                             | N/A | CODE                         | N/A |---|---|---|---|---| N/A | T-S-09   | Aprse                      | Table to store AP / RSE information that import from MWMS 2.0               | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | Name + RegistrationNumber    | N/A |---|---|---|---|---|
### 3.1.1. (GCIS) Frontend - Application Forms Submission

See the table mapping above for the SQL Server tables. The following sections describe the MongoDB collections.

**Collection: tasks**

*   **Document Count:** 5523
*   **Size:** 0.99 MB
*   **Average Document Size:** 0.18 KB

**Fields:**

| Field Name   | Types             | Occurrences | N/A |--------------|-------------------|-------------| N/A |---|---|---| N/A | \_\_v        | objectId, int     | 1000        | N/A |---|---|---| N/A | \_id         | objectId          | 1000        | N/A |---|---|---| N/A | application  | objectId          | 998         | N/A |---|---|---| N/A | createdAt    | date              | 1000        | N/A |---|---|---| N/A | status       | string            | 1000        | N/A |---|---|---| N/A | submissionCase | objectId          | 998         | N/A |---|---|---| N/A | taskType     | string            | 998         | N/A |---|---|---| N/A | team         | string            | 835         | N/A |---|---|---| N/A | user         | string, objectId  | 713         | N/A |---|---|---|
**Collection: eminutes**

*   **Document Count:** 133
*   **Size:** 0.03 MB
*   **Average Document Size:** 0.24 KB

**Fields:**

| Field Name     | Types             | Occurrences | N/A |----------------|-------------------|-------------| N/A |---|---|---| N/A | \_\_v          | int               | 133         | N/A |---|---|---| N/A | \_id           | objectId          | 133         | N/A |---|---|---| N/A | comment        | string            | 64          | N/A |---|---|---| N/A | content        | string            | 133         | N/A |---|---|---| N/A | createdAt      | date              | 133         | N/A |---|---|---| N/A | efolio         | string            | 100         | N/A |---|---|---| N/A | eminuteId      | string            | 133         | N/A |---|---|---| N/A | from           | objectId, string  | 133         | N/A |---|---|---| N/A | status         | string            | 133         | N/A |---|---|---| N/A | subject        | string            | 133         | N/A |---|---|---| N/A | submissionCase | objectId          | 133         | N/A |---|---|---| N/A | sysFileRefId   | string            | 65          | N/A |---|---|---| N/A | to             | objectId, string  | 129         | N/A |---|---|---|
**Collection: applications**

*   **Document Count:** 381
*   **Size:** 0.36 MB
*   **Average Document Size:** 0.96 KB

**Fields:**

| Field Name                  | Types                      | Occurrences | N/A |-----------------------------|----------------------------|-------------| N/A |---|---|---| N/A | APP13                       | object, array              | 172         | N/A |---|---|---| N/A | AddressOfPremiseCN          | string                     | 267         | N/A |---|---|---| N/A | AddressOfPremiseCNFloor     | string                     | 147         | N/A |---|---|---| N/A | AddressOfPremiseCNUnit      | string                     | 147         | N/A |---|---|---| N/A | AddressOfPremiseEN          | string                     | 271         | N/A |---|---|---| N/A | AddressOfPremiseENFloor     | string                     | 155         | N/A |---|---|---| N/A | AddressOfPremiseENUnit      | string                     | 154         | N/A |---|---|---| N/A | AgeOfStudent                | null, string               | 328         | N/A |---|---|---| N/A | ApplicantAddress            | string                     | 335         | N/A |---|---|---| N/A | ApplicantEmail              | string                     | 289         | N/A |---|---|---| N/A | ApplicantFax                | string                     | 21          | N/A |---|---|---| N/A | ApplicantMobile             | string                     | 288         | N/A |---|---|---| N/A | ApplicantName               | string                     | 189         | N/A |---|---|---| N/A | ApplicantNameCN             | string                     | 28          | N/A |---|---|---| N/A | ApplicantNameEN             | null, string               | 148         | N/A |---|---|---| N/A | ApplicantTel                | null, string               | 307         | N/A |---|---|---| N/A | ApplicationNo               | null, string               | 381         | N/A |---|---|---| N/A | ApplicationType             | string                     | 356         | N/A |---|---|---| N/A | Area                        | string                     | 28          | N/A |---|---|---| N/A | BlockID                     | string                     | 178         | N/A |---|---|---| N/A | ContactPerson               | string                     | 95          | N/A |---|---|---| N/A | ContactPersonCN             | string                     | 6           | N/A |---|---|---| N/A | ContactPersonEN             | string                     | 6           | N/A |---|---|---| N/A | ContactPersonEmail          | string                     | 6           | N/A |---|---|---| N/A | ContactPersonTel            | string                     | 6           | N/A |---|---|---| N/A | DescriptionOfSchool         | string, null               | 329         | N/A |---|---|---| N/A | District                    | string                     | 33          | N/A |---|---|---| N/A | EstimatedNoOfStudent        | int, null                  | 328         | N/A |---|---|---| N/A | FileReference               | string                     | 35          | N/A |---|---|---| N/A | NameOfSchoolCN              | string                     | 323         | N/A |---|---|---| N/A | NameOfSchoolEN              | string                     | 350         | N/A |---|---|---| N/A | Region                      | string                     | 29          | N/A |---|---|---| N/A | RelatedPremise              | string                     | 62          | N/A |---|---|---| N/A | RelatedPremises             | array                      | 381         | N/A |---|---|---| N/A | SelfCertification          | object, null               | 65          | N/A |---|---|---| N/A | StructuralCalculation       | object                     | 18          | N/A |---|---|---| N/A | SubmissionType              | string                     | 187         | N/A |---|---|---| N/A | \_\_v                       | int                        | 381         | N/A |---|---|---| N/A | \_id                        | objectId                   | 381         | N/A |---|---|---| N/A | address                     | object                     | 69          | N/A |---|---|---| N/A | assignedBS                  | objectId, string, null     | 364         | N/A |---|---|---| N/A | assignedGR                  | objectId, null             | 64          | N/A |---|---|---| N/A | assignedSBS                 | string, null               | 53          | N/A |---|---|---| N/A | createdAt                   | date                       | 381         | N/A |---|---|---| N/A | updatedAt                   | date                       | 194         | N/A |---|---|---|
**Collection: notifications**

*   **Document Count:** 1837
*   **Size:** 0.24 MB
*   **Average Document Size:** 0.13 KB

**Fields:**

| Field Name       | Types      | Occurrences | N/A |------------------|------------|-------------| N/A |---|---|---| N/A | \_\_v            | int        | 1000        | N/A |---|---|---| N/A | \_id             | objectId   | 1000        | N/A |---|---|---| N/A | createdAt        | date       | 1000        | N/A |---|---|---| N/A | eminute          | objectId   | 58          | N/A |---|---|---| N/A | notificationType | string     | 1000        | N/A |---|---|---| N/A | requireSendEmail | bool       | 1000        | N/A |---|---|---| N/A | task             | objectId   | 942         | N/A |---|---|---| N/A | user             | string     | 991         | N/A |---|---|---|
**Collection: bsblocks**

*   **Document Count:** 98397
*   **Size:** 6.40 MB
*   **Average Document Size:** 0.07 KB

**Fields:**

| Field Name | Types  | Occurrences | N/A |------------|--------|-------------| N/A |---|---|---| N/A | \_\_v      | int    | 1000        | N/A |---|---|---| N/A | \_id       | objectId | 1000        | N/A |---|---|---| N/A | bdgis      | string | 1000        | N/A |---|---|---| N/A | blockId    | string | 1000        | N/A |---|---|---|
**Collection: cases**

*   **Document Count:** 451
*   **Size:** 1.17 MB
*   **Average Document Size:** 2.65 KB

**Fields:**

| Field Name                  | Types          | Occurrences | N/A |-----------------------------|----------------|-------------| N/A |---|---|---| N/A | ActualReplyDate             | null, date     | 39          | N/A |---|---|---| N/A | Area                        | string         | 26          | N/A |---|---|---| N/A | AuditResult                 | string         | 11          | N/A |---|---|---| N/A | CaseOfficer                 | string         | 108         | N/A |---|---|---| N/A | Category                    | string         | 384         | N/A |---|---|---| N/A | District                    | string         | 37          | N/A |---|---|---| N/A | FileReference               | string         | 60          | N/A |---|---|---| N/A | LAFileReference             | object         | 17          | N/A |---|---|---| N/A | Nature                      | null, string   | 382         | N/A |---|---|---| N/A | ObjectiontoLR               | string         | 12          | N/A |---|---|---| N/A | ReceivedDate                | date, null     | 375         | N/A |---|---|---| N/A | Referrer                    | object         | 43          | N/A |---|---|---| N/A | Region                      | string         | 32          | N/A |---|---|---| N/A | Remarks                     | string         | 7           | N/A |---|---|---| N/A | Reminders                   | array          | 55          | N/A |---|---|---| N/A | SubmissionType              | string         | 8           | N/A |---|---|---| N/A | SubstantialReplyDate        | null, date     | 42          | N/A |---|---|---| N/A | TargetReplyDate             | date, null     | 111         | N/A |---|---|---| N/A | ThreeTierReqt               | string         | 12          | N/A |---|---|---| N/A | ViaSCS                      | bool           | 17          | N/A |---|---|---| N/A | \_\_v                       | int            | 451         | N/A |---|---|---| N/A | \_id                        | objectId       | 451         | N/A |---|---|---| N/A | application                 | objectId       | 450         | N/A |---|---|---| N/A | assignedBS                  | objectId       | 274         | N/A |---|---|---| N/A | assignedGR                  | objectId       | 137         | N/A |---|---|---| N/A | building\_information       | object         | 14          | N/A |---|---|---| N/A | caseDescription             | object         | 9           | N/A |---|---|---| N/A | caseOfficerReceive          | string         | 172         | N/A |---|---|---| N/A | caseOfficerReply            | string         | 72          | N/A |---|---|---| N/A | createdAt                   | date           | 451         | N/A |---|---|---| N/A | deck\_study                 | object         | 451         | N/A |---|---|---| N/A | documentChecklist           | object         | 2           | N/A |---|---|---| N/A | dv                          | object         | 197         | N/A |---|---|---| N/A | frc                         | object         | 451         | N/A |---|---|---| N/A | misc                        | object         | 451         | N/A |---|---|---| N/A | moe                         | object         | 451         | N/A |---|---|---| N/A | seniorCaseOfficerReceive    | string         | 54          | N/A |---|---|---| N/A | seniorCaseOfficerReply      | string         | 41          | N/A |---|---|---| N/A | site\_inspection            | object         | 7           | N/A |---|---|---| N/A | structural\_ccc\_bs          | object         | 451         | N/A |---|---|---| N/A | structural\_schnlh          | object         | 152         | N/A |---|---|---| N/A | structural\_schnlhkinds     | object         | 301         | N/A |---|---|---| N/A | team                        | string         | 374         | N/A |---|---|---| N/A | ubw                         | object         | 451         | N/A |---|---|---| N/A | updatedAt                   | date           | 16          | N/A |---|---|---|
**Collection: oauthtokens**

*   **Document Count:** 3019
*   **Size:** 2.29 MB
*   **Average Document Size:** 0.78 KB

**Fields:**

| Field Name            | Types  | Occurrences | N/A |-----------------------|--------|-------------| N/A |---|---|---| N/A | \_\_v                 | int    | 1000        | N/A |---|---|---| N/A | \_id                  | objectId | 1000        | N/A |---|---|---| N/A | accessToken           | string | 1000        | N/A |---|---|---| N/A | accessTokenExpiresAt  | date   | 1000        | N/A |---|---|---| N/A | client                | object | 1000        | N/A |---|---|---| N/A | refreshToken          | string | 1000        | N/A |---|---|---| N/A | refreshTokenExpiresAt | date   | 1000        | N/A |---|---|---| N/A | user                  | objectId | 1000        | N/A |---|---|---|
**Collection: sysfilerefs**

*   **Document Count:** 601808
*   **Size:** 204.70 MB
*   **Average Document Size:** 0.35 KB

**Fields:**

| Field Name          | Types        | Occurrences | N/A |---------------------|--------------|-------------| N/A |---|---|---| N/A | \_\_v               | int          | 1000        | N/A |---|---|---| N/A | \_id                | objectId     | 1000        | N/A |---|---|---| N/A | createdDt           | date         | 1000        | N/A |---|---|---| N/A | createdName         | null, string | 1000        | N/A |---|---|---| N/A | createdPost         | null, string | 1000        | N/A |---|---|---| N/A | createdSection      | null, string | 1000        | N/A |---|---|---| N/A | display             | string       | 1000        | N/A |---|---|---| N/A | dvExceed            | null, string | 1000        | N/A |---|---|---| N/A | dvStatusDt          | null, date   | 1000        | N/A |---|---|---| N/A | frefPref            | string, null | 1000        | N/A |---|---|---| N/A | frefSeq             | null, string | 1000        | N/A |---|---|---| N/A | frefSuf             | null, string | 1000        | N/A |---|---|---| N/A | frefYr              | null, string | 1000        | N/A |---|---|---| N/A | lastModifiedDt      | date         | 1000        | N/A |---|---|---| N/A | lastModifiedName    | null, string | 1000        | N/A |---|---|---| N/A | lastModifiedPost    | null, string | 1000        | N/A |---|---|---| N/A | lastModifiedSection | null         | 1000        | N/A |---|---|---| N/A | sysFileRefId        | string       | 1000        | N/A |---|---|---|
**Collection: attachments**

*   **Document Count:** 370
*   **Size:** 0.13 MB
*   **Average Document Size:** 0.37 KB

**Fields:**

| Field Name     | Types             | Occurrences | N/A |----------------|-------------------|-------------| N/A |---|---|---| N/A | \_\_v          | int               | 370         | N/A |---|---|---| N/A | \_id           | objectId          | 370         | N/A |---|---|---| N/A | application    | objectId          | 364         | N/A |---|---|---| N/A | createdAt      | date              | 370         | N/A |---|---|---| N/A | efolio         | null, string      | 351         | N/A |---|---|---| N/A | file           | object, string    | 247         | N/A |---|---|---| N/A | filePartNo     | string            | 216         | N/A |---|---|---| N/A | receivedDate   | date              | 352         | N/A |---|---|---| N/A | remarks        | string            | 216         | N/A |---|---|---| N/A | subType        | string            | 203         | N/A |---|---|---| N/A | submissionCase | objectId          | 350         | N/A |---|---|---| N/A | sysFileRefId   | string            | 67          | N/A |---|---|---| N/A | type           | string            | 348         | N/A |---|---|---| N/A | updatedAt      | date              | 3           | N/A |---|---|---|
**Collection: users**

*   **Document Count:** 116
*   **Size:** 0.04 MB
*   **Average Document Size:** 0.39 KB

**Fields:**

| Field Name           | Types  | Occurrences | N/A |----------------------|--------|-------------| N/A |---|---|---| N/A | \_\_v                | int    | 116         | N/A |---|---|---| N/A | \_id                 | objectId | 116         | N/A |---|---|---| N/A | bdgis                | string | 29          | N/A |---|---|---| N/A | begis                | string | 1           | N/A |---|---|---| N/A | delegateTo           | string | 8           | N/A |---|---|---| N/A | department           | string | 116         | N/A |---|---|---| N/A | email                | string | 109         | N/A |---|---|---| N/A | group                | string | 17          | N/A |---|---|---| N/A | lastLoginAt          | date   | 41          | N/A |---|---|---| N/A | letterLongPosition   | string | 11          | N/A |---|---|---| N/A | letterLongPositionCn | string | 12          | N/A |---|---|---| N/A | letterName           | string | 76          | N/A |---|---|---| N/A | letterNameCn         | string | 75          | N/A |---|---|---| N/A | letterPosition       | string | 79          | N/A |---|---|---| N/A | letterPositionCn     | string | 1           | N/A |---|---|---| N/A | lock                 | bool   | 116         | N/A |---|---|---| N/A | luPostName           | string | 78          | N/A |---|---|---| N/A | name                 | string | 80          | N/A |---|---|---| N/A | notificationEmail    | string | 23          | N/A |---|---|---| N/A | osdpEmail            | string | 62          | N/A |---|---|---| N/A | osdpLoginId          | string | 102         | N/A |---|---|---| N/A | password             | string | 108         | N/A |---|---|---| N/A | phoneNumber          | string | 65          | N/A |---|---|---| N/A | position             | string | 85          | N/A |---|---|---| N/A | role                 | string | 112         | N/A |---|---|---| N/A | team                 | string | 52          | N/A |---|---|---| N/A | userType             | string | 116         | N/A |---|---|---|
**Collection: adrblkfilerefs**

*   **Document Count:** 566948
*   **Size:** 154.89 MB
*   **Average Document Size:** 0.28 KB

**Fields:**

| Field Name          | Types        | Occurrences | N/A |---------------------|--------------|-------------| N/A |---|---|---| N/A | \_\_v               | int          | 1000        | N/A |---|---|---| N/A | \_id                | objectId     | 1000        | N/A |---|---|---| N/A | adrBlkFileRefId     | string       | 1000        | N/A |---|---|---| N/A | adrBlkId            | string       | 1000        | N/A |---|---|---| N/A | createdDt           | date         | 1000        | N/A |---|---|---| N/A | createdName         | null, string | 1000        | N/A |---|---|---| N/A | createdPost         | string       | 1000        | N/A |---|---|---| N/A | createdSection      | null, string | 1000        | N/A |---|---|---| N/A | lastModifiedDt      | date         | 1000        | N/A |---|---|---| N/A | lastModifiedName    | null, string | 1000        | N/A |---|---|---| N/A | lastModifiedPost    | string       | 1000        | N/A |---|---|---| N/A | lastModifiedSection | string, null | 1000        | N/A |---|---|---| N/A | sysFileRefId        | string       | 1000        | N/A |---|---|---|
## 4. Data Entity Description

This section states the conversion rules, the assumptions applied for the physical data design, the names of the physical data tables, the corresponding required system entities and key details to be stored into the database.

The database is a physical store of contract related information and textual data inside a database management system (DBMS). For LSCP, Microsoft SQL Server 2019 is selected for the database management system. All the spatial and textual entity will be stored into Microsoft SQL Server 2019.

The following tables document how the Logical Data Model (LDM) can be mapped onto the physical data design.

**LSCP Frontend**

| Table ID | LSCP Name                                 | LSCP Entity Description                                                     | Key Nature | Key Data Item                | N/A |--------|--------------|---------------------------|--------|----------------| N/A |---|---|---|---|---| N/A | T-S-01   | ApplicationCases                          | Table to store all the application number                                   | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |---|---|---|---|---| N/A | T-S-02   | SchoolApp\_Infos                           | Table to store the latest update of the submitted application data as 1 row | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |---|---|---|---|---| N/A | T-S-03   | SchoolApp\_Submissions                     | Table to store the submission of each application                           | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |          | N/A |                                                                             | N/A | SubmissionId                 | N/A |---|---|---|---|---| N/A | T-S-04   | ApplicationFiles                          | Table to store all the path of applicant upload files                       | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo                | N/A |          | N/A |                                                                             | N/A | SubmissionId                 | N/A |---|---|---|---|---| N/A | T-S-05   | LSCPMasterTable          | Table to store meta-data or parameter data for frontend                     | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | Code                         | N/A |          | N/A |                                                                             | N/A | Type + Code                  | N/A |---|---|---|---|---| N/A | T-S-06   | GenOtp                     | Table to store generated OTP code and the usage status                      | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | ApplicationNo + userId + Otp | N/A |---|---|---|---|---| N/A | T-S-07   | AdrBlk                     | Table to store addresses that import from BCIS                              | PK         | ADR\_BLK\_ID                   | N/A |---|---|---|---|---| N/A | T-S-08   | SYS\_META\_DATA             | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID             | N/A |          | N/A |                                                                             | N/A | REC\_TYPE                     | N/A |          | N/A |                                                                             | N/A | CODE                         | N/A |---|---|---|---|---| N/A | T-S-09   | Aprse                      | Table to store AP / RSE information that import from MWMS 2.0               | PK         | Id                           | N/A |          | N/A |                                                                             | N/A | Name + RegistrationNumber    | N/A |---|---|---|---|---|
**LSCP Backend**

| Table ID | LSCP Name                                 | LSCP Entity Description                                                     | Key Nature | Key Data Item    | N/A |----------|----------------------------|-----------------------------------------------------------------------------|------------|----------------| N/A |---|---|---|---|---| N/A | T-S-01   | ApplicationCase            | Table to store all the application number                                   | PK         | Id               | N/A |          | N/A |                                                                             | N/A | ApplicationNo    | N/A |---|---|---|---|---| N/A | T-S-02   | SchoolApp\_Infos           | Table to store the latest update of the submitted application data as 1 row | PK         | Id               | N/A |          | N/A |                                                                             | N/A | ApplicationNo    | N/A |---|---|---|---|---| N/A | T-S-03   | SchoolApp\_Submissions     | Table to store the submission of each application                           | PK         | Id               | N/A |          | N/A |                                                                             | N/A | ApplicationNo    | N/A |          | N/A |                                                                             | N/A | SubmissionId     | N/A |---|---|---|---|---| N/A | T-S-04   | ApplicationFiles           | Table to store all the path of applicant upload files                       | PK         | Id               | N/A |          | N/A |                                                                             | N/A | ApplicationNo    | N/A |          | N/A |                                                                             | N/A | SubmissionId     | N/A |---|---|---|---|---| N/A | T-S-05   | LSCPMasterTable          | Table to store meta-data or parameter data for frontend                     | PK         | Id               | N/A |          | N/A |                                                                             | N/A | Code             | N/A |          | N/A |                                                                             | N/A | Type + Code      | N/A |---|---|---|---|---| N/A | T-S-06   | SYS\_META\_DATA             | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID | N/A |          | N/A |                                                                             | N/A | REC\_TYPE         | N/A |          | N/A |                                                                             | N/A | CODE             | N/A |---|---|---|---|---| N/A | T-S-07   | SYS\_META\_DATA             | Table to store meta data that import from BCIS                              | PK         | SYS\_META\_DATA\_ID | N/A |          | N/A |                                                                             | N/A | REC\_TYPE         | N/A |          | N/A |                                                                             | N/A | CODE             | N/A |---|---|---|---|---|
\*\*\* End of document\*\*\*
