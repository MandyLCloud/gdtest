# Physical Data Design for Licensing Self-Certification Portal

## Introduction

This document provides a comprehensive description of the physical data design for the Licensing Self-Certification Portal (LSCP) project. It outlines the database structure, including tables, columns, data types, and relationships, based on the provided database schema analysis and code snippets. This document serves as a blueprint for implementing and maintaining the LSCP database.

## Database Overview

The LSCP database is designed to manage application forms, user data, workflow tasks, and related information. The database statistics indicate the following:

- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1278983
- Total Data Size: 371.24 MB

The database utilizes MongoDB for the backend data storage, as evidenced by the use of Mongoose schemas in the code. The frontend data is managed using a SQL database, likely Microsoft SQL Server 2019, as indicated in the code.

## Data Model

The data model encompasses several key entities, each represented by a collection in MongoDB and a table in the SQL database. The relationships between these entities are crucial for the system's functionality.

### MongoDB Collections

The following collections are used in the MongoDB database:

- **tasks**: Stores workflow tasks associated with applications.
- **eminutes**: Stores electronic minutes related to cases.
- **submissions**:  *(Currently Empty)* Potentially intended to store submission data.
- **applications**: Stores application data.
- **notifications**: Stores notifications for users.
- **bsblocks**: Stores block IDs and their corresponding BDGIS codes.
- **cases**: Stores case details related to applications.
- **oauthtokens**: Stores OAuth tokens for authentication.
- **sysfilerefs**: Stores system file references.
- **attachments**: Stores attachments related to applications and cases.
- **users**: Stores user information.
- **adrblkfilerefs**: Stores address block file references.

### SQL Database Tables

The following tables are used in the SQL database:

- **SchoolApp_Submissions**: Stores submission data from the frontend.
- **SchoolApp_Infos**: Stores application information.
- **ScsMasterTable**: Stores master data used by the frontend.
- **ApRse**: Stores information about Authorized Persons (AP) and Registered Structural Engineers (RSE).
- **AdrBlk**: Stores address block information imported from BCIS.
- **Sys_Meta_Data**: Stores system metadata imported from BCIS.
- **LogEvents**: Stores log events for auditing.
- **Staff**: Stores staff information.
- **Test**: A test table.
- **ApplicationCase**: Stores application case information.
- **ApplicationFiles**: Stores application file information.
- **BackendUpdate**: Stores backend update information.
- **GenOtp**: Stores OTP information for login verification.

## Data Entity Descriptions

### MongoDB Collections

#### Collection: `tasks`

- **Description**: Stores workflow tasks associated with applications.
- **Statistics**:
  - Document Count: 5523
  - Size: 0.99 MB
  - Average Document Size: 0.18 KB
- **Fields**:
  - `_id` (objectId): Unique identifier for the task.
  - `__v` (objectId, int): Version key.
  - `application` (objectId): Reference to the associated application.
  - `createdAt` (date): Timestamp of task creation.
  - `status` (string): Current status of the task.
  - `submissionCase` (objectId): Reference to the associated case.
  - `taskType` (string): Type of the task (e.g., DESK_STUDY, INITIAL_SITE_INSPECTION).
  - `team` (string): Team responsible for the task.
  - `user` (string, objectId): User assigned to the task.

#### Collection: `eminutes`

- **Description**: Stores electronic minutes related to cases.
- **Statistics**:
  - Document Count: 133
  - Size: 0.03 MB
  - Average Document Size: 0.24 KB
- **Fields**:
  - `_id` (objectId): Unique identifier for the e-minute.
  - `__v` (int): Version key.
  - `comment` (string): Comments related to the e-minute.
  - `content` (string): Content of the e-minute.
  - `createdAt` (date): Timestamp of e-minute creation.
  - `efolio` (string): E-folio number.
  - `eminuteId` (string): E-minute identifier.
  - `from` (objectId, string): User who created the e-minute.
  - `status` (string): Status of the e-minute.
  - `subject` (string): Subject of the e-minute.
  - `submissionCase` (objectId): Reference to the associated case.
  - `sysFileRefId` (string): Reference to the associated system file.
  - `to` (objectId, string): User to whom the e-minute is addressed.

#### Collection: `submissions`

- **Description**: *Currently Empty*. Potentially intended to store submission data.
- **Statistics**:
  - Document Count: 0
  - Size: 0.00 MB
  - Average Document Size: 0.00 KB
- **Fields**:
  - *No fields listed in the provided schema.*

#### Collection: `applications`

- **Description**: Stores application data.
- **Statistics**:
  - Document Count: 381
  - Size: 0.36 MB
  - Average Document Size: 0.96 KB
- **Fields**:
  - `APP13` (object, array): AP13 data.
  - `AddressOfPremiseCN` (string): Address of premise in Chinese.
  - `AddressOfPremiseCNFloor` (string): Floor of premise in Chinese.
  - `AddressOfPremiseCNUnit` (string): Unit of premise in Chinese.
  - `AddressOfPremiseEN` (string): Address of premise in English.
  - `AddressOfPremiseENFloor` (string): Floor of premise in English.
  - `AddressOfPremiseENUnit` (string): Unit of premise in English.
  - `AgeOfStudent` (null, string): Age of student.
  - `ApplicantAddress` (string): Applicant address.
  - `ApplicantEmail` (string): Applicant email.
  - `ApplicantFax` (string): Applicant fax.
  - `ApplicantMobile` (string): Applicant mobile.
  - `ApplicantName` (string): Applicant name.
  - `ApplicantNameCN` (string): Applicant name in Chinese.
  - `ApplicantNameEN` (null, string): Applicant name in English.
  - `ApplicantTel` (null, string): Applicant telephone.
  - `ApplicationNo` (null, string): Application number.
  - `ApplicationType` (string): Type of application.
  - `Area` (string): Area.
  - `BlockID` (string): Block ID.
  - `ContactPerson` (string): Contact person.
  - `ContactPersonCN` (string): Contact person in Chinese.
  - `ContactPersonEN` (string): Contact person in English.
  - `ContactPersonEmail` (string): Contact person email.
  - `ContactPersonTel` (string): Contact person telephone.
  - `DescriptionOfSchool` (string, null): Description of school.
  - `District` (string): District.
  - `EstimatedNoOfStudent` (int, null): Estimated number of students.
  - `FileReference` (string): File reference.
  - `NameOfSchoolCN` (string): Name of school in Chinese.
  - `NameOfSchoolEN` (string): Name of school in English.
  - `Region` (string): Region.
  - `RelatedPremise` (string): Related premise.
  - `RelatedPremises` (array): Array of related premises.
  - `SelfCertification` (object, null): Self-certification details.
  - `StructuralCalculation` (object): Structural calculation details.
  - `SubmissionType` (string): Submission type.
  - `__v` (int): Version key.
  - `_id` (objectId): Unique identifier for the application.
  - `address` (object): Address object.
  - `assignedBS` (objectId, string, null): Building Surveyor assigned to the application.
  - `assignedGR` (objectId, null): Government Representative assigned to the application.
  - `assignedSBS` (string, null): Senior Building Surveyor assigned to the application.
  - `createdAt` (date): Timestamp of application creation.
  - `updatedAt` (date): Timestamp of last update.

#### Collection: `notifications`

- **Description**: Stores notifications for users.
- **Statistics**:
  - Document Count: 1837
  - Size: 0.24 MB
  - Average Document Size: 0.13 KB
- **Fields**:
  - `_id` (objectId): Unique identifier for the notification.
  - `__v` (int): Version key.
  - `createdAt` (date): Timestamp of notification creation.
  - `eminute` (objectId): Reference to the associated e-minute.
  - `notificationType` (string): Type of notification (e.g., NEW_TASK, NEW_EMINUTE).
  - `requireSendEmail` (bool): Flag indicating if an email should be sent.
  - `task` (objectId): Reference to the associated task.
  - `user` (string): User to whom the notification is addressed.

#### Collection: `bsblocks`

- **Description**: Stores block IDs and their corresponding BDGIS codes.
- **Statistics**:
  - Document Count: 98397
  - Size: 6.40 MB
  - Average Document Size: 0.07 KB
- **Fields**:
  - `_id` (objectId): Unique identifier for the BS Block.
  - `__v` (int): Version key.
  - `bdgis` (string): BDGIS code.
  - `blockId` (string): Block ID.

#### Collection: `cases`

- **Description**: Stores case details related to applications.
- **Statistics**:
  - Document Count: 451
  - Size: 1.17 MB
  - Average Document Size: 2.65 KB
- **Fields**:
  - `ActualReplyDate` (null, date): Actual reply date.
  - `Area` (string): Area.
  - `AuditResult` (string): Audit result.
  - `CaseOfficer` (string): Case officer.
  - `Category` (string): Category of the case.
  - `District` (string): District.
  - `FileReference` (string): File reference.
  - `LAFileReference` (object): LA file reference.
  - `Nature` (null, string): Nature of the case.
  - `ObjectiontoLR` (string): Objection to LR.
  - `ReceivedDate` (date, null): Received date.
  - `Referrer` (object): Referrer information.
  - `Region` (string): Region.
  - `Remarks` (string): Remarks.
  - `Reminders` (array): Array of reminders.
  - `SubmissionType` (string): Submission type.
  - `SubstantialReplyDate` (null, date): Substantial reply date.
  - `TargetReplyDate` (date, null): Target reply date.
  - `ThreeTierReqt` (string): Three-tier requirement.
  - `ViaSCS` (bool): Via SCS flag.
  - `__v` (int): Version key.
  - `_id` (objectId): Unique identifier for the case.
  - `application` (objectId): Reference to the associated application.
  - `assignedBS` (objectId): Building Surveyor assigned to the case.
  - `assignedGR` (objectId): Government Representative assigned to the case.
  - `building_information` (object): Building information.
  - `caseDescription` (object): Case description.
  - `caseOfficerReceive` (string): Case officer receiving the case.
  - `caseOfficerReply` (string): Case officer replying to the case.
  - `createdAt` (date): Timestamp of case creation.
  - `deck_study` (object): Deck study details.
  - `documentChecklist` (object): Document checklist.
  - `dv` (object): DV details.
  - `frc` (object): FRC details.
  - `misc` (object): Miscellaneous details.
  - `moe` (object): MOE details.
  - `seniorCaseOfficerReceive` (string): Senior case officer receiving the case.
  - `seniorCaseOfficerReply` (string): Senior case officer replying to the case.
  - `site_inspection` (object): Site inspection details.
  - `structural_ccc_bs` (object): Structural CCC BS details.
  - `structural_schnlh` (object): Structural SCHNLH details.
  - `structural_schnlhkinds` (object): Structural SCHNLHKinds details.
  - `team` (string): Team assigned to the case.
  - `ubw` (object): UBW details.
  - `updatedAt` (date): Timestamp of last update.

#### Collection: `oauthtokens`

- **Description**: Stores OAuth tokens for authentication.
- **Statistics**:
  - Document Count: 3019
  - Size: 2.29 MB
  - Average Document Size: 0.78 KB
- **Fields**:
  - `_id` (objectId): Unique identifier for the OAuth token.
  - `__v` (int): Version key.
  - `accessToken` (string): Access token.
  - `accessTokenExpiresAt` (date): Access token expiration timestamp.
  - `client` (object): Client information.
  - `refreshToken` (string): Refresh token.
  - `refreshTokenExpiresAt` (date): Refresh token expiration timestamp.
  - `user` (objectId): Reference to the associated user.

#### Collection: `sysfilerefs`

- **Description**: Stores system file references.
- **Statistics**:
  - Document Count: 601808
  - Size: 204.70 MB
  - Average Document Size: 0.35 KB
- **Fields**:
  - `_id` (objectId): Unique identifier for the system file reference.
  - `__v` (int): Version key.
  - `createdDt` (date): Timestamp of file creation.
  - `createdName` (null, string): Name of the creator.
  - `createdPost` (null, string): Post of the creator.
  - `createdSection` (null, string): Section of the creator.
  - `display` (string): Display name of the file.
  - `dvExceed` (null, string): DV exceed information.
  - `dvStatusDt` (null, date): DV status timestamp.
  - `frefPref` (string, null): File reference prefix.
  - `frefSeq` (null, string): File reference sequence.
  - `frefSuf` (null, string): File reference suffix.
  - `frefYr` (null, string): File reference year.
  - `lastModifiedDt` (date): Timestamp of last modification.
  - `lastModifiedName` (null, string): Name of the last modifier.
  - `lastModifiedPost` (null, string): Post of the last modifier.
  - `lastModifiedSection` (null): Section of the last modifier.
  - `sysFileRefId` (string): System file reference ID.

#### Collection: `attachments`

- **Description**: Stores attachments related to applications and cases.
- **Statistics**:
  - Document Count: 370
  - Size: 0.13 MB
  - Average Document Size: 0.37 KB
- **Fields**:
  - `_id` (objectId): Unique identifier for the attachment.
  - `__v` (int): Version key.
  - `application` (objectId): Reference to the associated application.
  - `createdAt` (date): Timestamp of attachment creation.
  - `efolio` (null, string): E-folio number.
  - `file` (object, string): File details.
  - `filePartNo` (string): File part number.
  - `receivedDate` (date): Date the attachment was received.
  - `remarks` (string): Remarks about the attachment.
  - `subType` (string): Subtype of the attachment.
  - `submissionCase` (objectId): Reference to the associated case.
  - `sysFileRefId` (string): Reference to the associated system file.
  - `type` (string): Type of attachment.
  - `updatedAt` (date): Timestamp of last update.

#### Collection: `users`

- **Description**: Stores user information.
- **Statistics**:
  - Document Count: 116
  - Size: 0.04 MB
  - Average Document Size: 0.39 KB
- **Fields**:
  - `_id` (objectId): Unique identifier for the user.
  - `__v` (int): Version key.
  - `bdgis` (string): BDGIS code.
  - `begis` (string): BEGIS code.
  - `delegateTo` (string): User to whom tasks are delegated.
  - `department` (string): Department of the user.
  - `email` (string): Email address of the user.
  - `group` (string): Group of the user.
  - `lastLoginAt` (date): Timestamp of last login.
  - `letterLongPosition` (string): Long position on letter.
  - `letterLongPositionCn` (string): Long position on letter in Chinese.
  - `letterName` (string): Name on letter.
  - `letterNameCn` (string): Name on letter in Chinese.
  - `letterPosition` (string): Position on letter.
  - `letterPositionCn` (string): Position on letter in Chinese.
  - `lock` (bool): Account lock status.
  - `luPostName` (string): LU post name.
  - `name` (string): Name of the user.
  - `notificationEmail` (string): Notification email address.
  - `osdpEmail` (string): OSDP email address.
  - `osdpLoginId` (string): OSDP login ID.
  - `password` (string): Hashed password.
  - `phoneNumber` (string): Phone number.
  - `position` (string): Position of the user.
  - `role` (string): Role of the user.
  - `team` (string): Team of the user.
  - `userType` (string): Type of user.

#### Collection: `adrblkfilerefs`

- **Description**: Stores address block file references.
- **Statistics**:
  - Document Count: 566948
  - Size: 154.89 MB
  - Average Document Size: 0.28 KB
- **Fields**:
  - `_id` (objectId): Unique identifier for the address block file reference.
  - `__v` (int): Version key.
  - `adrBlkFileRefId` (string): Address block file reference ID.
  - `adrBlkId` (string): Address block ID.
  - `createdDt` (date): Timestamp of file creation.
  - `createdName` (null, string): Name of the creator.
  - `createdPost` (string): Post of the creator.
  - `createdSection` (null, string): Section of the creator.
  - `lastModifiedDt` (date): Timestamp of last modification.
  - `lastModifiedName` (null, string): Name of the last modifier.
  - `lastModifiedPost` (string): Post of the last modifier.
  - `lastModifiedSection` (string, null): Section of the last modifier.
  - `sysFileRefId` (string): System file reference ID.

### SQL Database Tables

- **SchoolApp_Submissions**: Stores submission data from the frontend.
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `FromId` (BIGINT, nullable): Foreign key.
  - `ApplicationNo` (STRING, nullable): Application number.
  - `SubmissionId` (STRING, nullable): Submission ID.
  - `FormName` (STRING, nullable): Form name.
  - `ApplicationType` (STRING, nullable): Application type.
  - *Other fields related to applicant and contact information, address, school details, and AP/RSE information.*
  - `Status` (STRING, nullable): Status of the submission.
  - `SubmittedDate` (DATE, nullable): Submission date.
  - `Synced` (BOOLEAN, default: false, not null): Indicates if the submission is synced to the backend.

- **SchoolApp_Infos**: Stores application information.
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `FromId` (BIGINT, nullable): Foreign key.
  - `ApplicationNo` (STRING, nullable): Application number.
  - `FormName` (STRING, nullable): Form name.
  - `ApplicationType` (STRING, nullable): Application type.
  - *Other fields related to applicant and contact information, address, school details, and AP/RSE information.*

- **ScsMasterTable**: Stores master data used by the frontend.
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `Type` (STRING, not null): Type of master data.
  - `Code` (STRING, not null): Code of the master data.
  - `Ordering` (BIGINT, nullable): Ordering of the data.
  - `DataValue` (STRING, nullable): Data value.
  - `CaptionEN` (STRING, nullable): Caption in English.
  - `CaptionTC` (STRING, nullable): Caption in Traditional Chinese.
  - `CaptionSC` (STRING, nullable): Caption in Simplified Chinese.
  - `Remarks` (STRING, nullable): Remarks.
  - `LongTextEN` (STRING, nullable): Long text in English.
  - `LongTextTC` (STRING, nullable): Long text in Traditional Chinese.
  - `LongTextSC` (STRING, nullable): Long text in Simplified Chinese.

- **ApRse**: Stores information about Authorized Persons (AP) and Registered Structural Engineers (RSE).
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `UUID` (STRING, nullable): UUID.
  - `Name` (STRING, nullable): Name.
  - `Name_tc` (STRING, nullable): Name in Traditional Chinese.
  - `RegistrationNumber` (STRING, nullable): Registration number.
  - `RegistrationType` (STRING, nullable): Registration type.
  - `ExpiryDate` (DATE, nullable): Expiry date.

- **AdrBlk**: Stores address block information imported from BCIS.
  - `ADR_BLK_ID` (BIGINT, primary key, auto-increment): Unique identifier.
  - `BLK_TYPE_ID` (BIGINT, not null): Block type ID.
  - `BLDG_CAT_ID` (BIGINT, not null): Building category ID.
  - `BLDG_USAGE_ID` (BIGINT, not null): Building usage ID.
  - *Other address-related fields.*

- **Sys_Meta_Data**: Stores system metadata imported from BCIS.
  - `SYS_META_DATA_ID` (BIGINT, primary key, auto-increment): Unique identifier.
  - `REC_TYPE` (STRING, not null): Record type.
  - `CODE` (STRING, not null): Code.
  - *Other metadata-related fields.*

- **LogEvents**: Stores log events for auditing.
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `LogAlias` (STRING, nullable): Log alias.
  - `IpAddress` (STRING, nullable): IP address.
  - *Other log-related fields.*

- **Staff**: Stores staff information.
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `UserId` (STRING, nullable): User ID.
  - `Password` (STRING, nullable): Hashed password.
  - *Other staff-related fields.*

- **Test**: A test table.
  - `id` (INTEGER, primary key, auto-increment): Unique identifier.
  - `name` (STRING, not null): Name.
  - `age` (INTEGER, nullable): Age.
  - `email` (STRING, not null): Email address.

- **ApplicationCase**: Stores application case information.
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `FromId` (BIGINT, nullable): Foreign key.
  - `ApplicationNo` (STRING, nullable): Application number.
  - `FileDate` (DATE, nullable): File date.

- **ApplicationFiles**: Stores application file information.
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `FromId` (BIGINT, nullable): Foreign key.
  - `ApplicationNo` (STRING, nullable): Application number.
  - `SubmissionId` (STRING, nullable): Submission ID.
  - `FileId` (STRING, nullable): File ID.
  - *Other file-related fields.*

- **BackendUpdate**: Stores backend update information.
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `ApplicationNo` (STRING, nullable): Application number.
  - `UpdateType` (STRING, nullable): Update type.
  - *Other update-related fields.*

- **GenOtp**: Stores OTP information for login verification.
  - `Id` (BIGINT, primary key, auto-increment): Unique identifier.
  - `ApplicationNo` (STRING, not null): Application number.
  - `UserId` (STRING, not null): User ID.
  - `Otp` (STRING, nullable): OTP.
  - *Other OTP-related fields.*

## Data Relationships

The code reveals several relationships between the entities:

-   **Application 1:N Cases**: An application can have multiple cases associated with it. This is evident from the `CaseSchema` having a field `application` which is a `Schema.Types.ObjectId` referencing the `Application` collection.
-   **Case 1:N Tasks**: A case can have multiple tasks associated with it. This is evident from the `TaskSchema` having a field `submissionCase` which is a `Schema.Types.ObjectId` referencing the `Case` collection.
-   **Application 1:N Attachments**: An application can have multiple attachments. This is evident from the `AttachemntSchema` having a field `application` which is a `Schema.Types.ObjectId` referencing the `Application` collection.
-   **Case 1:N Attachments**: A case can have multiple attachments. This is evident from the `AttachemntSchema` having a field `submissionCase` which is a `Schema.Types.ObjectId` referencing the `Case` collection.
-   **User 1:N Tasks**: A user can be assigned to multiple tasks. This is evident from the `TaskSchema` having a field `user` which is a `Schema.Types.ObjectId` referencing the `User` collection.
-   **User 1:N OAuthTokens**: A user can have multiple OAuth tokens. This is evident from the `OAuthTokenSchema` having a field `user` which is a `Schema.Types.ObjectId` referencing the `User` collection.
-   **BsBlock 1:N AdrBlkFileRefs**: An address block can have multiple file references. This is evident from the `AdrBlkFileRefSchema` having a field `adrBlkId` which is a string referencing the `BsBlock` collection.
-   **SysFileRef 1:N AdrBlkFileRefs**: A system file reference can be referenced by multiple address block file references. This is evident from the `AdrBlkFileRefSchema` having a field `sysFileRefId` which is a string referencing the `SysFileRef` collection.

## Key Considerations

-   **Data Types**: The code shows a mix of data types, including strings, numbers, dates, booleans, and object IDs. Choosing the appropriate data type for each field is crucial for data integrity and performance.
-   **Indexing**: Indexing frequently queried fields can significantly improve query performance. Consider indexing fields like `ApplicationNo`, `NameOfSchoolCN`, `NameOfSchoolEN`, `assignedBS`, `assignedGR`, `sysFileRefId`, `adrBlkId`, and `blockId`.
-   **Data Validation**: Implementing data validation rules at the model level can help ensure data quality. The code includes some basic validation, such as `enum` for `ApplicationType` and `SubmissionType`.
-   **Relationships**: Defining relationships between collections using Mongoose's `ref` option allows for efficient data retrieval and querying.
-   **Scalability**: As the LSCP grows, consider sharding the MongoDB database to improve scalability and performance.
-   **Security**: Ensure that sensitive data, such as passwords, is properly encrypted and protected. The code uses bcrypt for password hashing.

## Conclusion

This document provides a detailed overview of the physical data design for the LSCP. By following these guidelines, the LSCP can be implemented with a robust and efficient data management system that meets the needs of the Buildings Department and its users.