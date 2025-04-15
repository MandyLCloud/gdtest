---
title: Program Manual - Interest Calculation Program
version: 1.0
date: 2024-10-27
---

# Program Manual - Interest Calculation Program

## Distribution Information

| Recipient          | Title                     | Date Distributed | Version | N/A |--------------------|---------------------------|------------------|---------| N/A |---|---|---|---| N/A | John Smith         | Lead Developer            | 2024-10-27       | 1.0     | N/A |---|---|---|---| N/A | Alice Johnson      | Quality Assurance Manager | 2024-10-27       | 1.0     | N/A |---|---|---|---| N/A | Robert Williams    | Database Administrator    | 2024-10-27       | 1.0     | N/A |---|---|---|---| N/A | Emily Brown        | Business Analyst          | 2024-10-27       | 1.0     | N/A |---|---|---|---|
## Amendment History

| Version | Date       | Author        | Description                                                                 | Sections Affected | N/A |---------|------------|---------------|-----------------------------------------------------------------------------|-------------------| N/A |---|---|---|---|---| N/A | 1.0     | 2024-10-27 | John Smith    | Initial Release                                                               | All               | N/A |---|---|---|---|---| N/A | 1.1     | 2024-11-15 | Alice Johnson | Updated validation rules for interest rate and loan amount.                 | Processing Logic  | N/A |---|---|---|---|---| N/A | 1.2     | 2024-12-01 | Robert Williams | Modified database table names to reflect production environment.           | Table/File Usage  | N/A |---|---|---|---|---| N/A | 1.3     | 2025-01-10 | Emily Brown   | Clarified business rules regarding compound interest calculation frequency. | Processing Logic  | N/A |---|---|---|---|---|
## Table of Contents

1.  [Purpose and Scope](#purpose-and-scope)
    *   1.  Purpose
    *   2.  Scope
        *   2.1 Development Tools and Platform
    *   3.  Reference
2.  [Program Overview](#program-overview)
    *   1.  Basic Program Information
    *   2.  Table/File Usage
    *   3.  Processing Logic
        *   3.1 Pre-submit Validity Check
        *   3.2 Event Steps
        *   3.3 Window Navigation
        *   3.4 Arithmetic/Logic Steps
        *   3.5 Additional Requirements
        *   3.6 Program Limits
    *   4.  Dialogue Design
3.  [Detailed Program Description](#detailed-program-description)
    *   1.  Input Data
    *   2.  Output Data
    *   3.  Algorithms
4.  [Security Considerations](#security-considerations)
5.  [Error Handling](#error-handling)
6.  [Audit Logging](#audit-logging)
7.  [Performance](#performance)
8.  [Disaster Recovery](#disaster-recovery)
9.  [Appendix](#appendix)
    *   1.  Data Dictionary
    *   2.  Code Listing

## Purpose and Scope

### Section 1: Purpose

The purpose of this document is to provide a comprehensive guide to the Interest Calculation Program. This manual details the program's functionality, design, and operational procedures. It serves as a reference for developers, testers, database administrators, and business analysts involved in the maintenance and support of the program.

### Section 2: Scope

This document covers all aspects of the Interest Calculation Program, including its functionality, data structures, processing logic, and user interface. It outlines the program's interactions with the database, its security features, and its error handling mechanisms. The scope includes the program's design, development, testing, and deployment.

#### Section 2.1: Development Tools and Platform

| Tool/Platform      | Version | Description                                                                 | N/A |----------------------|---------|-----------------------------------------------------------------------------| N/A |---|---|---| N/A | Programming Language | Java 17 | The primary language used for developing the application logic.              | N/A |---|---|---| N/A | Database             | Oracle 19c | The database system used for storing and retrieving loan and interest data. | N/A |---|---|---| N/A | IDE                  | IntelliJ IDEA | The integrated development environment used for coding and debugging.       | N/A |---|---|---| N/A | Operating System     | Linux   | The operating system on which the application is deployed.                  | N/A |---|---|---| N/A | Build Tool           | Maven   | Used for dependency management and building the application.                 | N/A |---|---|---|
### Section 3: Reference

| Document Name                               | Version | Description                                                                                               | Location                               | N/A |---------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|----------------------------------------| N/A |---|---|---|---| N/A | Program Specification Document              | 1.0     | Detailed specifications of the Interest Calculation Program, including functional and non-functional requirements. | Project Repository/specs/program_spec.md | N/A |---|---|---|---| N/A | Database Schema Document                    | 1.2     | Description of the database schema used by the Interest Calculation Program.                               | Project Repository/docs/db_schema.pdf  | N/A |---|---|---|---| N/A | User Interface Design Document              | 0.9     | Mockups and descriptions of the user interface for the Interest Calculation Program.                         | Project Repository/docs/ui_design.pdf  | N/A |---|---|---|---| N/A | Software Development Standards Document     | 2.0     | Guidelines and standards for software development within the organization.                                  | Company Intranet/standards.html        | N/A |---|---|---|---| N/A | Security Policy Document                    | 1.5     | Security policies and procedures for protecting sensitive data.                                            | Company Intranet/security_policy.pdf   | N/A |---|---|---|---|
```

```markdown
## Section 4: Definitions and Conventions

| Term | Definition | N/A |---|---| N/A |---|---| N/A | Program | A specific software application or module within the system. | N/A |---|---| N/A | Table | A database table used by the system. | N/A |---|---| N/A | Field | A specific data element within a table. | N/A |---|---| N/A | Validation | A process to ensure data accuracy and integrity. | N/A |---|---| N/A | Event | A trigger or action that initiates a process within the system. | N/A |---|---| N/A | Window | A user interface screen or page. | N/A |---|---| N/A | Logic | The set of rules and calculations performed by the program. | N/A |---|---| N/A | Amendment | A change or update to the program. | N/A |---|---| N/A | User | An individual interacting with the program. | N/A |---|---| N/A | System | The overall software environment. | N/A |---|---| N/A | API | Application Programming Interface. | N/A |---|---| N/A | UI | User Interface. | N/A |---|---| N/A | SQL | Structured Query Language. | N/A |---|---| N/A | Server | A computer that provides resources to other computers. | N/A |---|---| N/A | Client | A computer that accesses resources from a server. | N/A |---|---| N/A | Database | An organized collection of data. | N/A |---|---| N/A | Error Code | A code indicating a specific error condition. | N/A |---|---| N/A | Log File | A file containing a record of events. | N/A |---|---| N/A | Configuration File | A file containing settings for the program. | N/A |---|---|
## Section 5: Program List

### Section 5.1: Web Application

| Program Name | Description | Technology | Location | N/A |---|---|---|---| N/A |---|---|---|---| N/A | User Management | Manages user accounts and permissions. | Java, Spring Boot, React | /user-management | N/A |---|---|---|---| N/A | Data Entry | Allows users to enter and update data. | Java, Spring Boot, Thymeleaf | /data-entry | N/A |---|---|---|---| N/A | Reporting | Generates reports based on data in the system. | Java, Spring Boot, JasperReports | /reporting | N/A |---|---|---|---| N/A | Audit Log | Tracks user actions and system events. | Java, Spring Boot, MySQL | /audit-log | N/A |---|---|---|---| N/A | Configuration | Manages system-wide settings. | Java, Spring Boot, Angular | /configuration | N/A |---|---|---|---| N/A | Batch Processing | Processes large volumes of data in the background. | Java, Spring Batch, Quartz | /batch-processing | N/A |---|---|---|---| N/A | Security | Handles authentication and authorization. | Java, Spring Security | /security | N/A |---|---|---|---| N/A | API Gateway | Manages access to backend services. | Java, Spring Cloud Gateway | /api-gateway | N/A |---|---|---|---| N/A | Dashboard | Provides a visual overview of system status. | React, Redux | /dashboard | N/A |---|---|---|---| N/A | Help System | Provides user assistance and documentation. | HTML, JavaScript | /help | N/A |---|---|---|---|
```

```markdown
## Section 6: Program Specification

### Section 6.1: Public User Authentication with Password

#### Detailed program specifications

This section details the specifications for the Public User Authentication with Password program. This program allows public users to authenticate themselves using a username and password. Successful authentication grants access to specific resources and functionalities within the system.

#### Basic Program Information

| Field | Value | N/A |---|---| N/A |---|---| N/A | Program Name | Public User Authentication | N/A |---|---| N/A | Program ID | AUTH-PUB-001 | N/A |---|---| N/A | Description | Authenticates public users based on username and password. | N/A |---|---| N/A | Input | Username, Password | N/A |---|---| N/A | Output | Authentication Token, User Role | N/A |---|---| N/A | Technology | Java, Spring Boot, MySQL | N/A |---|---| N/A | Security Requirements | Password encryption, rate limiting, account lockout | N/A |---|---|
#### Amendment History

| Version | Date | Author | Description | N/A |---|---|---|---| N/A |---|---|---|---| N/A | 1.0 | 2023-10-26 | System Architect | Initial Release | N/A |---|---|---|---| N/A | 1.1 | 2023-11-15 | Security Engineer | Implemented rate limiting and account lockout features. | N/A |---|---|---|---| N/A | 1.2 | 2024-01-20 | Developer | Added password complexity requirements. | N/A |---|---|---|---|
#### Table/File Usage

| Table/File Name | Purpose | Columns Used | Access Type | N/A |---|---|---|---| N/A |---|---|---|---| N/A | `public_users` | Stores public user credentials. | `user_id`, `username`, `password_hash`, `salt`, `account_status`, `failed_login_attempts`, `last_login` | Read | N/A |---|---|---|---| N/A | `user_roles` | Stores user roles and permissions. | `user_id`, `role_id` | Read | N/A |---|---|---|---| N/A | `roles` | Stores role definitions. | `role_id`, `role_name`, `permissions` | Read | N/A |---|---|---|---| N/A | `login_attempts` | Tracks login attempts to prevent brute-force attacks. | `ip_address`, `username`, `timestamp` | Write | N/A |---|---|---|---| N/A | `application.properties` | Configuration file. | `spring.datasource.url`, `spring.datasource.username`, `spring.datasource.password`, `security.password.salt`, `security.login.max_attempts` | Read | N/A |---|---|---|---|
#### Processing Logic

##### Pre-submit Validity Check

| Field | Validation Rule | Error Message | N/A |---|---|---| N/A |---|---|---| N/A | Username | Required, Minimum length 5 characters, Maximum length 50 characters, Alphanumeric only | "Username must be between 5 and 50 alphanumeric characters." | N/A |---|---|---| N/A | Password | Required, Minimum length 8 characters, Must contain at least one uppercase letter, one lowercase letter, one number, and one special character | "Password must be at least 8 characters long and contain at least one uppercase letter, one lowercase letter, one number, and one special character." | N/A |---|---|---|
##### Event steps

| Step | Description | System Action | N/A |---|---|---| N/A |---|---|---| N/A | 1 | User enters username and password. | Display login form. | N/A |---|---|---| N/A | 2 | User submits the form. | Capture username and password. | N/A |---|---|---| N/A | 3 | System validates input. | Check username and password against validation rules. | N/A |---|---|---| N/A | 4 | System checks account status. | Verify if the account is active or locked. | N/A |---|---|---| N/A | 5 | System authenticates user. | Retrieve user's salt and password hash from `public_users` table.  Compare the hash of the entered password with the stored hash. | N/A |---|---|---| N/A | 6 | On successful authentication. | Generate authentication token and retrieve user roles from `user_roles` and `roles` tables. Update `last_login` timestamp in `public_users` table. | N/A |---|---|---| N/A | 7 | On failed authentication. | Increment `failed_login_attempts` in `public_users` table. If attempts exceed the limit, lock the account. Log the failed attempt in `login_attempts` table. | N/A |---|---|---| N/A | 8 | System returns authentication token and user roles. | Grant access to authorized resources. | N/A |---|---|---|
##### Window Navigation

| Window | Navigation | N/A |---|---| N/A |---|---| N/A | Login Page | Initial page displayed to the user. | N/A |---|---| N/A | Home Page | Navigated to after successful login. | N/A |---|---| N/A | Account Locked Page | Navigated to if the account is locked due to too many failed login attempts. | N/A |---|---|
##### Arithmetic/Logic steps

| Step | Description | Formula/Logic | N/A |---|---|---| N/A |---|---|---| N/A | Password Hashing | Generate a secure hash of the password. | `password_hash = SHA256(password + salt)` | N/A |---|---|---| N/A | Account Lockout | Determine if the account should be locked. | `IF failed_login_attempts >= max_login_attempts THEN account_status = 'LOCKED'` | N/A |---|---|---| N/A | Rate Limiting | Limit the number of login attempts from a specific IP address. | `IF login_attempts_from_ip > max_attempts_per_minute THEN reject_login` | N/A |---|---|---|
##### Additional Requirements

| Requirement | Description | N/A |---|---| N/A |---|---| N/A | Password Complexity | Passwords must meet specific complexity requirements (length, character types). | N/A |---|---| N/A | Account Lockout | Accounts should be locked after a certain number of failed login attempts. | N/A |---|---| N/A | Rate Limiting | Implement rate limiting to prevent brute-force attacks. | N/A |---|---| N/A | Audit Logging | Log all successful and failed login attempts. | N/A |---|---| N/A | Secure Storage | Store passwords securely using hashing and salting. | N/A |---|---|
##### Program Limits

| Limit | Value | N/A |---|---| N/A |---|---| N/A | Maximum Username Length | 50 characters | N/A |---|---| N/A | Minimum Password Length | 8 characters | N/A |---|---| N/A | Maximum Login Attempts | 5 | N/A |---|---| N/A | Account Lockout Duration | 30 minutes | N/A |---|---|
#### Dialogue Design

| Element | Description | Example | N/A |---|---|---| N/A |---|---|---| N/A | Login Form | Form for entering username and password. | Includes fields for "Username" and "Password" with appropriate labels. | N/A |---|---|---| N/A | Success Message | Message displayed upon successful login. | "Login successful! Redirecting..." | N/A |---|---|---| N/A | Error Message (Invalid Credentials) | Message displayed when login fails due to incorrect username or password. | "Invalid username or password. Please try again." | N/A |---|---|---| N/A | Error Message (Account Locked) | Message displayed when the account is locked. | "Your account is locked due to too many failed login attempts. Please try again in 30 minutes." | N/A |---|---|---| N/A | Error Message (Generic Error) | Message displayed for unexpected errors. | "An unexpected error occurred. Please try again later." | N/A |---|---|---| N/A | Password Reset Link | Link to initiate password reset process. | "Forgot your password?" | N/A |---|---|---|