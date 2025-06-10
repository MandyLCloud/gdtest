# Data Catalogue: Licensing Self-Certification Portal (LSCP) - Buildings Department

**Version:** 1.1
**Date:** January 21, 2025

? The Government of the Hong Kong Special Administrative Region

## 1. Introduction

This document provides a data catalogue for the Licensing Self-Certification Portal (LSCP) used by the Buildings Department. It outlines the data architecture, database specifications, and key data elements within the system.

## 2. Definitions

| Abbreviation | Definition                                     | N/A | :----------- | :--------------------------------------------- | N/A |---|---| N/A | LSCP         | Licensing Self-Certification Portal            | N/A |---|---| N/A | RSE          | Registered Structural Engineer                 | N/A |---|---| N/A | OTP          | One-Time Password                              | N/A |---|---| N/A | LSO          | Licensing Subject Officer                      | N/A |---|---| N/A | MongoDB      | NoSQL document-oriented database               | N/A |---|---| N/A | MSSQL        | Microsoft SQL Server                           | N/A |---|---|
## 3. Data Architecture Overview

The LSCP system employs a dual-database architecture: MongoDB and Microsoft SQL Server.

### MongoDB Database

- **Purpose:** Handles frontend operational data and user sessions.
- **Key Database:** `bd`
- **Database Size:** 88.10 MB
- **Total Documents:** 1,278,983

### Microsoft SQL Server Database

- **Purpose:** Serves as the transactional database, storing structured data related to applications, submissions, and system reference data.
- **Key Database:** `bd_scs`
- **Data Synchronization:** Occurs through application services between MongoDB and MSSQL.

## 4. Database Specifications

### 4.1 MongoDB Collections (Database: bd)

#### Database Statistics
- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1278983
- Total Data Size: 371.24 MB

#### Collections Overview
- tasks: 5523 documents, 0.99 MB
- eminutes: 133 documents, 0.03 MB
- submissions: 0 documents, 0.00 MB
- applications: 381 documents, 0.36 MB
- notifications: 1837 documents, 0.24 MB
- bsblocks: 98397 documents, 6.40 MB
- cases: 451 documents, 1.17 MB
- sysfilerefs: 601808 documents, 204.70 MB
- attachments: 370 documents, 0.13 MB
- adrblkfilerefs: 566948 documents, 154.89 MB
- users: 116 documents, 0.39 KB
- oauthtokens: 3019 documents, 2.29 MB

#### 4.1.1 tasks

- **Document Count:** 5523
- **Size:** 0.99 MB

| Field Name     | Data Type | Description                       | N/A | :------------- | :-------- | :-------------------------------- | N/A |---|---|---| N/A | `_id`          | objectId  | Unique identifier                 | N/A |---|---|---| N/A | `createdAt`    | date      | Creation timestamp                | N/A |---|---|---| N/A | `submissionCase` | objectId  | Reference to submission case    | N/A |---|---|---| N/A | `team`         | string    | Team assigned to the task       | N/A |---|---|---|
#### 4.1.2 eminutes

- **Document Count:** 133
- **Average Document Size:** 0.24 KB

| Field Name     | Data Type     | Description                       | N/A | :------------- | :------------ | :-------------------------------- | N/A |---|---|---| N/A | `comment`      | string        | Comment text                      | N/A |---|---|---| N/A | `createdAt`    | date          | Creation timestamp                | N/A |---|---|---| N/A | `eminuteId`    | string        | Minute identifier                 | N/A |---|---|---| N/A | `status`       | string        | Status of the minute              | N/A |---|---|---| N/A | `submissionCase` | objectId      | Reference to submission case    | N/A |---|---|---| N/A | `to`           | objectId/string | Recipient reference               | N/A |---|---|---|
#### 4.1.4 applications

- **Document Count:** 381
- **Size:** 0.36 MB

| Field Name          | Data Type     | Description                               | N/A | :------------------ | :------------ | :---------------------------------------- | N/A |---|---|---| N/A | `_id`               | objectId      | Unique identifier                         | N/A |---|---|---| N/A | `AddressOfPremiseCN`| string        | Premises address (Chinese)                | N/A |---|---|---| N/A | `ApplicationNo`     | string        | Application number                        | N/A |---|---|---| N/A | `NameOfSchoolCN`    | string        | School name (Chinese)                     | N/A |---|---|---| N/A | `assignedBS`        | objectId/string | Assigned Building Surveyor                | N/A |---|---|---| N/A | `assignedSBS`       | string        | Assigned Senior Building Surveyor         | N/A |---|---|---| N/A | `updatedAt`         | date          | Last update timestamp                     | N/A |---|---|---|
#### 4.1.6 bsblocks

- **Document Count:** 98397
- **Size:** 6.40 MB

| Field Name     | Data Type | Description                       | N/A | :------------- | :-------- | :-------------------------------- | N/A |---|---|---| N/A | `_id`          | string  | Unique identifier                 | N/A |---|---|---| N/A | `blockId`    | string      | Block Identifier                | N/A |---|---|---|
#### 4.1.8 oauthtokens

- **Document Count:** 3019
- **Size:** 2.29 MB

| Field Name     | Data Type | Description                       | N/A | :------------- | :-------- | :-------------------------------- | N/A |---|---|---| N/A | `_id`          | objectId  | Unique identifier                 | N/A |---|---|---| N/A | `accessToken`    | string      | Access Token                | N/A |---|---|---| N/A | `refreshToken` | string  | Refresh Token    | N/A |---|---|---|
#### 4.1.10 attachments

- **Document Count:** 370
- **Size:** 0.13 MB

| Field Name     | Data Type | Description                       | N/A | :------------- | :-------- | :-------------------------------- | N/A |---|---|---| N/A | `_id`          | objectId  | Unique identifier                 | N/A |---|---|---| N/A | `application`    | objectId      | Application Reference                | N/A |---|---|---| N/A | `file` | string  | File Name    | N/A |---|---|---|
#### 4.1.12 adrblkfilerefs

- **Document Count:** 566948
- **Size:** 154.89 MB

| Field Name     | Data Type | Description                       | N/A | :------------- | :-------- | :-------------------------------- | N/A |---|---|---| N/A | `_id`          | objectId  | Unique identifier                 | N/A |---|---|---| N/A | `adrBlkFileRefId`    | string      | Address Block File Reference ID                | N/A |---|---|---| N/A | `createdDt` | date  | Created Date    | N/A |---|---|---|
#### 4.1.14 sysfilerefs

- **Document Count:** 601808
- **Size:** 204.70 MB

| Field Name     | Data Type | Description                       | N/A | :------------- | :-------- | :-------------------------------- | N/A |---|---|---| N/A | `_id`          | objectId  | Unique identifier                 | N/A |---|---|---| N/A | `display`    | string      | Display Name                | N/A |---|---|---| N/A | `createdName` | string  | Created By    | N/A |---|---|---|
#### 4.1.16 notifications

- **Document Count:** 1837
- **Size:** 0.24 MB

| Field Name     | Data Type | Description                       | N/A | :------------- | :-------- | :-------------------------------- | N/A |---|---|---| N/A | `_id`          | objectId  | Unique identifier                 | N/A |---|---|---| N/A | `createdAt`    | date      | Created Date                | N/A |---|---|---| N/A | `notificationType` | string  | Notification Type    | N/A |---|---|---|
#### 4.1.18 cases

- **Document Count:** 451
- **Size:** 1.17 MB

| Field Name     | Data Type | Description                       | N/A | :------------- | :-------- | :-------------------------------- | N/A |---|---|---| N/A | `_id`          | objectId  | Unique identifier                 | N/A |---|---|---| N/A | `application`    | objectId      | Application Reference                | N/A |---|---|---| N/A | `Category` | string  | Case Category    | N/A |---|---|---|
#### 4.1.20 users

- **Document Count:** 116
- **Size:** 0.39 KB

| Field Name     | Data Type | Description                       | N/A | :------------- | :-------- | :-------------------------------- | N/A |---|---|---| N/A | `_id`          | objectId  | Unique identifier                 | N/A |---|---|---| N/A | `email`    | string      | User Email                | N/A |---|---|---| N/A | `role` | string  | User Role    | N/A |---|---|---|
### 4.2 MSSQL Tables (Database: bd_scs, Schema: dbo)

#### 4.2.1 __EFMigrationsHistory

| Column Name | Data Type | Length | Nullable | PK  | Description          | N/A | :---------- | :-------- | :----- | :------- | :-: | :------------------- | N/A |---|---|---|---|---|---| N/A | `MigrationId` | nvarchar  | 300  | No       | Yes | Migration identifier | N/A |---|---|---|---|---|---|
#### 4.2.2 AdrBlk

**Description:** Stores building address information.

| Column Name     | Data Type | Length | Nullable | PK  | Description                     | N/A | :-------------- | :-------- | :----- | :------- | :-: | :------------------------------ | N/A |---|---|---|---|---|---| N/A | `BLK_TYPE_ID`   | bigint    | 8      | Yes      | No  | Block type ID                   | N/A |---|---|---|---|---|---| N/A | `BLDG_USAGE_ID` | bigint    | 8      | Yes      | No  | Building usage ID               | N/A |---|---|---|---|---|---| N/A | `SYS_DISTRICT_ID`| bigint    | 8      | Yes      | No  | System district ID              | N/A |---|---|---|---|---|---| N/A | `BLK_DESC_E_ID` | bigint    | 8      | Yes      | No  | Block description English ID    | N/A |---|---|---|---|---|---| N/A | `BLK_NO_ALPHA`  | nvarchar  | 20     | Yes      | No  | Block number (alphanumeric)     | N/A |---|---|---|---|---|---| N/A | `BLDG_NAME_E2`  | nvarchar  | 90     | Yes      | No  | Building name English 2         | N/A |---|---|---|---|---|---| N/A | `BLDG_NAME_C1`  | nvarchar  | 160    | Yes      | No  | Building name Chinese 1         | N/A |---|---|---|---|---|---| N/A | `BLDG_NAME_C3`  | nvarchar  | 160    | Yes      | No  | Building name Chinese 3         | N/A |---|---|---|---|---|---| N/A | `CreatedAt`     | datetime2 | 8      | Yes      | No  | Creation timestamp              | N/A |---|---|---|---|---|---|
#### 4.2.3 AdrBlk_Temp

**Description:** Temporary table for building address information.

| Column Name     | Data Type       | Length | Nullable | PK  | Description                     | N/A | :-------------- | :-------------- | :----- | :------- | :-: | :------------------------------ | N/A |---|---|---|---|---|---| N/A | `BLK_TYPE_ID`   | bigint          | 8      | Yes      | No  | Block type ID                   | N/A |---|---|---|---|---|---| N/A | `updatedAt`     | datetimeoffset  | 10     | No       | No  | Last update timestamp           | N/A |---|---|---|---|---|---|
#### 4.2.4 ApplicationCases

| Column Name | Data Type | Length | Nullable | PK  | Description          | N/A | :---------- | :-------- | :----- | :------- | :-: | :------------------- | N/A |---|---|---|---|---|---| N/A | `Id`        | bigint    | 8      | No       | Yes | Case ID (identity)   | N/A |---|---|---|---|---|---| N/A | `CreatedAt` | datetime2 | 8      | Yes      | No  | Creation timestamp | N/A |---|---|---|---|---|---| N/A | `UpdatedAt` | datetime2 | 8      | Yes      | No  | Last update timestamp | N/A |---|---|---|---|---|---| N/A | `FromId`    | bigint    | 8      | Yes      | No  | Source ID            | N/A |---|---|---|---|---|---|
#### 4.2.6 ApRse

**Description:** Stores application file information.

| Column Name | Data Type | Length | Nullable | PK  | Description          | N/A | :---------- | :-------- | :----- | :------- | :-: | :------------------- | N/A |---|---|---|---|---|---| N/A | `FileName`  | nvarchar  | 200  | Yes      | No  | File name            | N/A |---|---|---|---|---|---| N/A | `SignType`  | nvarchar  | 60   | Yes      | No  | Sign type            | N/A |---|---|---|---|---|---| N/A | `CreatedAt` | datetime2 | 8      | Yes      | No  | Creation timestamp | N/A |---|---|---|---|---|---| N/A | `RemoveStatus`| nvarchar | 100  | Yes      | No  | Remove status        | N/A |---|---|---|---|---|---|
#### Other MSSQL Tables

The following tables are also present in the `bd_scs` database:

*   `BackendUpdate`
*   `GenOtp`
*   `LogEvents`
*   `SchoolApp_Submission`
*   `ScsMasterTable`
*   `Sys_Meta_Data`