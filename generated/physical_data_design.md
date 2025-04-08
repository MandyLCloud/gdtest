# Physical Data Design for Licensing Self-Certification Portal (LSCP)

**Version 0.1**
**Date: 2025-01-22**

## 1. Introduction

This document outlines the physical data design for the Licensing Self-Certification Portal (LSCP) database, named `bd`. It provides an overview of the database structure, collection details, and considerations for physical implementation based on the database schema analysis. This document is intended for developers, database administrators, and stakeholders involved in the LSCP project.

## 2. Database Overview

The LSCP database, `bd`, is designed to efficiently manage data related to licensing self-certification processes. The database statistics are as follows:

- **Database Size:** 88.10 MB
- **Collections:** 12
- **Total Documents:** 1,278,983
- **Total Data Size:** 371.24 MB

This indicates a moderately sized database with a significant number of documents spread across 12 collections. The average document size varies across collections, suggesting different data storage needs.

## 3. Collections and Entities

The database is organized into 12 collections, each representing a key entity within the LSCP system. The following sections detail each collection's purpose, statistics, and key fields.

### 3.1. Collection: tasks

- **Purpose:** Stores information about tasks within the LSCP workflow, such as desk studies, inspections, and endorsements.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/Task.js`
- **Statistics:**
    - Document Count: 5,523
    - Size: 0.99 MB
    - Average Document Size: 0.18 KB
- **Key Fields:**
    - `_id`: Unique identifier for each task (objectId).
    - `application`: Reference to the application this task belongs to (objectId).
    - `submissionCase`: Reference to the case associated with the task (objectId).
    - `taskType`: Type of task (string, e.g., "DESK_STUDY", "INSPECTION_REPORT").
    - `status`: Current status of the task (string).
    - `createdAt`: Date and time when the task was created (date).
    - `user`: User assigned to the task (string, objectId).
    - `team`: Team associated with the task (string).

### 3.2. Collection: eminutes

- **Purpose:** Manages electronic minutes (e-minutes) for communication and endorsements within the system.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/Eminute.js`
- **Statistics:**
    - Document Count: 133
    - Size: 0.03 MB
    - Average Document Size: 0.24 KB
- **Key Fields:**
    - `_id`: Unique identifier for each e-minute (objectId).
    - `submissionCase`: Reference to the case the e-minute is related to (objectId).
    - `application`: Reference to the application (objectId).
    - `eminuteId`: Unique identifier for e-minute (string).
    - `from`: Sender of the e-minute (objectId, string).
    - `to`: Recipient of the e-minute (objectId, string).
    - `status`: Status of the e-minute (string).
    - `createdAt`: Date and time when the e-minute was created (date).
    - `subject`: Subject of the e-minute (string).
    - `content`: Content of the e-minute (string).

### 3.3. Collection: submissions

- **Purpose:** Stores submission data related to applications. Currently empty, suggesting this functionality might be pending or submissions are directly embedded within applications.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/Submission.js`
- **Statistics:**
    - Document Count: 0
    - Size: 0.00 MB
    - Average Document Size: 0.00 KB
- **Field Analysis:** No fields are analyzed as the collection is empty.

### 3.4. Collection: applications

- **Purpose:** Contains core application data, including applicant details, school information, and related premises.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/Application.js`
- **Statistics:**
    - Document Count: 381
    - Size: 0.36 MB
    - Average Document Size: 0.96 KB
- **Key Fields:**
    - `_id`: Unique identifier for each application (objectId).
    - `ApplicationNo`: Application number (string).
    - `ApplicationType`: Type of application (string).
    - `SubmissionType`: Submission type (string).
    - `FileReference`: File reference number (string).
    - `NameOfSchoolEN`, `NameOfSchoolCN`: School names in English and Chinese (string).
    - `ApplicantNameEN`, `ApplicantNameCN`: Applicant names in English and Chinese (string).
    - `ApplicantEmail`, `ApplicantMobile`, `ApplicantTel`: Applicant contact information (string).
    - `assignedBS`, `assignedGR`, `assignedSBS`: IDs or references to assigned personnel (objectId, string, null).
    - `createdAt`, `updatedAt`: Timestamps for creation and update (date).

### 3.5. Collection: notifications

- **Purpose:** Manages notifications within the LSCP system, likely for task assignments and e-minute updates.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/Notification.js`
- **Statistics:**
    - Document Count: 1,837
    - Size: 0.24 MB
    - Average Document Size: 0.13 KB
- **Key Fields:**
    - `_id`: Unique identifier for each notification (objectId).
    - `user`: Recipient user (string).
    - `notificationType`: Type of notification (string, e.g., "NEW_TASK", "NEW_EMINUTE").
    - `task`: Reference to the related task (objectId).
    - `eminute`: Reference to the related e-minute (objectId).
    - `createdAt`: Date and time when the notification was created (date).

### 3.6. Collection: bsblocks

- **Purpose:** Stores Building Block (BS Block) data, likely related to geographical or zoning information.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/BsBlock.js`
- **Statistics:**
    - Document Count: 98,397
    - Size: 6.40 MB
    - Average Document Size: 0.07 KB
- **Key Fields:**
    - `_id`: Unique identifier for each BS Block (objectId).
    - `blockId`: Block identifier (string).
    - `bdgis`: BDGIS code (string).

### 3.7. Collection: cases

- **Purpose:** Manages cases related to applications, containing detailed information for processing and tracking.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/Case.js`
- **Statistics:**
    - Document Count: 451
    - Size: 1.17 MB
    - Average Document Size: 2.65 KB
- **Key Fields:**
    - `_id`: Unique identifier for each case (objectId).
    - `application`: Reference to the related application (objectId).
    - `assignedBS`, `assignedGR`: IDs or references to assigned personnel (objectId).
    - `caseOfficerReceive`, `caseOfficerReply`, `seniorCaseOfficerReceive`, `seniorCaseOfficerReply`: Case officer information (string).
    - `Category`, `Nature`: Case categorization and nature (string).
    - `ReceivedDate`, `TargetReplyDate`, `SubstantialReplyDate`, `ActualReplyDate`: Dates related to case processing (date, null).
    - Various nested objects for different aspects of case details (e.g., `deck_study`, `building_information`, `structural_schnlh`).
    - `createdAt`, `updatedAt`: Timestamps for creation and update (date).

### 3.8. Collection: oauthtokens

- **Purpose:** Stores OAuth 2.0 access and refresh tokens for API authentication.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/OAuthToken.js`
- **Statistics:**
    - Document Count: 3,019
    - Size: 2.29 MB
    - Average Document Size: 0.78 KB
- **Key Fields:**
    - `_id`: Unique identifier for each OAuth token (objectId).
    - `accessToken`: OAuth access token (string).
    - `refreshToken`: OAuth refresh token (string).
    - `accessTokenExpiresAt`, `refreshTokenExpiresAt`: Expiry dates for tokens (date).
    - `user`: Reference to the user associated with the token (objectId).

### 3.9. Collection: sysfilerefs

- **Purpose:** Manages system file references, likely used for tracking and retrieving files within the system. This collection is quite large, indicating extensive file management.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/SysFileRef.js`
- **Statistics:**
    - Document Count: 601,808
    - Size: 204.70 MB
    - Average Document Size: 0.35 KB
- **Key Fields:**
    - `_id`: Unique identifier for each system file reference (objectId).
    - `sysFileRefId`: System file reference identifier (string).
    - `frefPref`, `frefSeq`, `frefYr`, `frefSuf`: File reference components (string, null).
    - `display`: Display name for the file reference (string).
    - `createdDt`, `lastModifiedDt`: Timestamps for creation and last modification (date).
    - `createdName`, `lastModifiedName`: User names associated with creation and modification (string, null).

### 3.10. Collection: attachments

- **Purpose:** Stores attachments related to applications and cases, including files uploaded by users and system-generated documents.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/Attachment.js`
- **Statistics:**
    - Document Count: 370
    - Size: 0.13 MB
    - Average Document Size: 0.37 KB
- **Key Fields:**
    - `_id`: Unique identifier for each attachment (objectId).
    - `application`: Reference to the related application (objectId).
    - `submissionCase`: Reference to the related case (objectId).
    - `sysFileRefId`: System file reference ID (string).
    - `efolio`: E-folio number (string, null).
    - `type`: Type of attachment (string, enum `AttachemntType`).
    - `subType`: Subtype of attachment (string).
    - `file`: File details (object, string).
    - `createdAt`, `updatedAt`: Timestamps for creation and update (date).

### 3.11. Collection: users

- **Purpose:** Manages user accounts and their roles, permissions, and team assignments within the LSCP system.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/User.js`
- **Statistics:**
    - Document Count: 116
    - Size: 0.04 MB
    - Average Document Size: 0.39 KB
- **Key Fields:**
    - `_id`: Unique identifier for each user (objectId).
    - `osdpLoginId`: OSDP login ID (string, unique).
    - `name`: User's name (string).
    - `email`: User's email address (string).
    - `password`: Hashed password (string).
    - `role`: User's role (string, enum `ROLES`).
    - `team`: User's team assignment (string).
    - `department`: User's department (string, enum `DEPARTMENTS`).
    - `userType`: User type (string, enum `USER_TYPES`).
    - `lastLoginAt`: Last login timestamp (date).

### 3.12. Collection: adrblkfilerefs

- **Purpose:** Address Block File References, likely linking address blocks to file references for document management. This collection is also large, similar to `sysfilerefs`.
- **Model File (from `code1.txt`):** `bd-scs-backend-backend-main/models/AdrBlkFileRef.js`
- **Statistics:**
    - Document Count: 566,948
    - Size: 154.89 MB
    - Average Document Size: 0.28 KB
- **Key Fields:**
    - `_id`: Unique identifier for each address block file reference (objectId).
    - `adrBlkFileRefId`: Address block file reference ID (string).
    - `adrBlkId`: Address block ID (string).
    - `sysFileRefId`: System file reference ID (string).
    - `createdDt`, `lastModifiedDt`: Timestamps for creation and last modification (date).
    - `createdName`, `lastModifiedName`: User names associated with creation and modification (string, null).

## 4. Data Relationships

Based on the field analysis, we can infer the following relationships:

-   **Applications to Cases:** One-to-many relationship. One application can have multiple cases (e.g., revisions, different submission types). The `application` field in the `cases` collection establishes this relationship.
-   **Cases to Tasks:** One-to-many relationship. One case can have multiple tasks associated with it. The `submissionCase` field in the `tasks` collection establishes this relationship.
-   **Cases to Eminutes:** One-to-many relationship. One case can have multiple e-minutes. The `submissionCase` field in the `eminutes` collection establishes this relationship.
-   **Applications/Cases to Attachments:** One-to-many relationship. Applications and Cases can have multiple attachments. The `application` and `submissionCase` fields in the `attachments` collection establish these relationships.
-   **OAuthTokens to Users:** Many-to-one relationship. Multiple OAuth tokens can belong to one user. The `user` field in the `oauthtokens` collection establishes this relationship.
-   **AdrBlkFileRefs to SysFileRefs:** Many-to-one relationship. Multiple address block file references can refer to one system file reference. The `sysFileRefId` field in the `adrblkfilerefs` collection establishes this relationship.
-   **SysFileRefs to Attachments and AdrBlkFileRefs:** One-to-many relationship. One system file reference can be linked to multiple attachments and address block file references. The `sysFileRefId` field in the `attachments` and `adrblkfilerefs` collections establishes these relationships.

## 5. Considerations for Physical Design

-   **Indexing:** To optimize query performance, especially for frequently accessed collections like `sysfilerefs`, `adrblkfilerefs`, and `tasks`, consider indexing fields used in queries, such as `application`, `submissionCase`, `taskType`, `sysFileRefId`, `adrBlkId`, `blockId`, `user`, `role`, `notificationType`, and `createdAt`.
-   **Data Types:** The schema effectively uses `objectId` for relationships and `date` for timestamps. String types are used for textual data, and integers/booleans are used where appropriate. Reviewing the field analysis, the chosen data types seem suitable.
-   **Storage:** The database size is currently manageable. However, with the expected growth in documents, especially in `sysfilerefs` and `adrblkfilerefs`, consider database sharding or other scaling strategies for long-term scalability.
-   **Performance:** Regularly monitor database performance and optimize queries as needed. Consider using database profiling tools to identify slow queries and optimize them.
-   **Backup and Recovery:** Implement a robust backup and recovery strategy to ensure data durability and availability.

## 6. Conclusion

This Physical Data Design document provides a solid foundation for the LSCP database. By understanding the database structure, collection details, and data relationships, developers and administrators can effectively build, manage, and maintain the LSCP system. Continuous monitoring and optimization will be crucial to ensure the database remains performant and scalable as the system evolves.

\*\*\* End of Document \*\*\*