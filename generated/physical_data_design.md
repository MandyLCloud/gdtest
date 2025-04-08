# Physical Data Design Document: Licensing Self-Certification Portal (LSCP)

**Version 0.1**

**Jan 2025**

## 1. Introduction

This document outlines the Physical Data Design for the Licensing
Self-Certification Portal (LSCP) project. It details the database
structure, including key entities, their attributes, and relationships,
and how the codebase interacts with this data layer. This document is
intended to provide a clear understanding of the system's data
architecture for developers, database administrators, and stakeholders.

## 2. Database Schema Overview

The LSCP database, named `bd`, is designed to store and manage data
related to licensing self-certification processes. Below is a summary of
the database's physical characteristics and an overview of its
collections.

### 2.1. Database Statistics

- **Database Name:** bd
- **Database Size:** 88.10 MB
- **Number of Collections:** 12
- **Total Documents:** 1,278,983
- **Total Data Size:** 371.24 MB

### 2.2. Collections Overview

The database is organized into 12 collections, each serving a specific
purpose:

| Collection Name   | Document Count | Size (MB) | Description                                    |
|-------------------|----------------|-----------|------------------------------------------------|
| tasks             | 5,523          | 0.99      | Stores tasks related to applications and cases |
| eminutes          | 133            | 0.03      | Stores electronic minutes records               |
| submissions       | 0              | 0.00      | Stores application submissions data             |
| applications      | 381            | 0.36      | Stores application forms data                 |
| notifications     | 1,837          | 0.24      | Stores system notifications                   |
| bsblocks          | 98,397         | 6.40      | Stores building block information             |
| cases             | 451            | 1.17      | Stores case-related information                |
| oauthtokens       | 3,019          | 2.29      | Stores OAuth tokens for authentication         |
| sysfilerefs       | 601,808        | 204.70    | Stores system file references                  |
| attachments       | 370            | 0.13      | Stores file attachments for applications/cases |
| users             | 116            | 0.04      | Stores user information                        |
| adrblkfilerefs    | 566,948        | 154.89    | Stores address block file references           |

### 2.3. Key Collection Schemas

#### 2.3.1. Collection: `applications`

This collection stores data related to application forms. Each document
represents an application and includes fields such as applicant
information, school details, and application status.

**Statistics:**

-   **Document Count:** 381
-   **Size:** 0.36 MB
-   **Average Document Size:** 0.96 KB

**Key Fields:**

-   `ApplicationNo` (String): Unique application identifier.
-   `ApplicationType` (String): Type of application (e.g., NEWSCH, EXTSCH).
-   `NameOfSchoolEN` (String): Name of the school in English.
-   `NameOfSchoolCN` (String): Name of the school in Chinese.
-   `ApplicantName` (String): Applicant's name.
-   `ApplicantEmail` (String): Applicant's email address.
-   `assignedBS` (ObjectId, String, Null): Building Surveyor assigned to the application.
-   `assignedGR` (ObjectId, Null): GR assigned to the application.
-   `createdAt` (Date): Date of application creation.
-   `updatedAt` (Date): Date of last update.

#### 2.3.2. Collection: `tasks`

The `tasks` collection manages workflow tasks within the LSCP system.
Documents in this collection track the status and assignment of various
tasks related to application processing.

**Statistics:**

-   **Document Count:** 5,523
-   **Size:** 0.99 MB
-   **Average Document Size:** 0.18 KB

**Key Fields:**

-   `taskType` (String): Type of task (e.g., DESK\_STUDY, INSPECTION\_REPORT).
-   `application` (ObjectId): Reference to the `applications` collection.
-   `submissionCase` (ObjectId): Reference to the `cases` collection.
-   `user` (String, ObjectId): User assigned to the task.
-   `status` (String): Current status of the task (e.g., ACTIVE, COMPLETED).
-   `createdAt` (Date): Date of task creation.

#### 2.3.3. Collection: `users`

This collection contains user profiles for the LSCP system. It stores
information about system users, their roles, and team assignments.

**Statistics:**

-   **Document Count:** 116
-   **Size:** 0.04 MB
-   **Average Document Size:** 0.39 KB

**Key Fields:**

-   `osdpLoginId` (String): Unique login ID for OSDP.
-   `name` (String): User's name.
-   `email` (String): User's email address.
-   `role` (String): User's role (e.g., GR, BS, SBS).
-   `team` (String): User's team assignment.
-   `department` (String): User's department.
-   `lastLoginAt` (Date): Date of last login.

#### 2.3.4. Collection: `sysfilerefs`

The `sysfilerefs` collection is used to manage file references within
the system. It stores metadata about files, including IDs and display
names.

**Statistics:**

-   **Document Count:** 601,808
-   **Size:** 204.70 MB
-   **Average Document Size:** 0.35 KB

**Key Fields:**

-   `sysFileRefId` (String): Unique file reference ID.
-   `display` (String): Display name of the file reference.
-   `createdDt` (Date): Date of file reference creation.
-   `lastModifiedDt` (Date): Date of last modification.

## 3. Codebase Integration with Data Design

The LSCP codebase, as represented in `code1.txt`, is structured to
interact with the database to manage and process the data defined in the
schema.

### 3.1. Models

The `models` directory in `bd-scs-backend-backend-main` contains
JavaScript files that define the Mongoose models for each collection in
the database. This directory includes files such as:

-   `AdrBlkFileRef.js`
-   `Application.js`
-   `Attachment.js`
-   `BsBlock.js`
-   `Case.js`
-   `Eminute.js`
-   `Notification.js`
-   `OAuthToken.js`
-   `Submission.js`
-   `SysFileRef.js`
-   `Task.js`
-   `User.js`

Each file corresponds to a collection in the database and defines the
schema for documents within that collection. For example, `Application.js`
likely defines the schema for the `applications` collection, mapping
fields like `ApplicationNo`, `ApplicationType`, and `NameOfSchoolEN` to
their respective data types in the MongoDB database.

### 3.2. Routes

The `routes` directory in `bd-scs-backend-backend-main` defines the API
endpoints for interacting with the database. Files in this directory,
such as:

-   `applications.js`
-   `attachments.js`
-   `cases.js`
-   `tasks.js`
-   `users.js`
-   `fileReferences.js`

These files handle HTTP requests (GET, POST, PUT, DELETE) to perform
CRUD operations on the corresponding collections. For instance,
`applications.js` would contain routes for fetching, creating, and
updating applications in the `applications` collection.

### 3.3. Utilities and Helpers

The `utils` directory in `bd-scs-backend-backend-main` contains utility
functions and helper classes that facilitate database interactions and
data processing. Key utilities include:

-   `MongoDBHelper.js`: Provides helper functions for connecting to and
    interacting with the MongoDB database.
-   `application.js`: Contains utility functions specific to
    application data, such as generating application numbers.
-   `sendEmail.js`: Implements functionality for sending emails, likely
    used for notifications related to database events.

These utilities abstract database interactions and business logic,
making the codebase more modular and maintainable.

## 4. Conclusion

The Physical Data Design Document provides a detailed overview of the
LSCP database and its integration with the codebase. The database schema
is well-defined, with collections structured to efficiently store and
manage application, case, user, and system-related data. The codebase
effectively utilizes Mongoose models to interact with these collections
through clearly defined API routes and utility functions, ensuring a
cohesive and robust system architecture.

\*\*\* End of Document \*\*\*