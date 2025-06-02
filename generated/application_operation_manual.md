# Application Operation Manual - Licensing Self-Certification Portal (LSCP)

**Version: 0.1**

**Date: Jan 2025**

? The Government of the Hong Kong Special Administrative Region

## 1. Purpose

This Application Operation Manual (AOM) provides relevant information to the application operation staff of the Licensing Self-Certification Portal (LSCP) system. It documents the instructions for all work to be performed when running the application system, including job submission, report checking, and dispatching.

## 2. Scope

This manual describes relevant information for the application operation staff of the LSCP system.

## 3. References

*   System Analysis and Design Report
*   System Manual (T351)
*   Program Manual (T321)
*   Computer Operation Procedure Manual (T356)

## 4. Definitions and Conventions

Nil.

## 5. System Description

### 5.1 System Description

The LSCP system is composed of two sub-systems:

*   LSCP Web
*   LSCP Mobile

### 5.2 Job Identification/Description

The batch job names and their corresponding locations are listed in the following table:

| N/A | Job Name                            | Job Description/ File Location                                                     | Running Location   | Automatic / Manual Trigger | N/A |-----|-------------------------------------|------------------------------------------------------------------------------------|--------------------|-----------------------------| N/A |---|---|---|---|---| N/A | 1   | INT-MWMS2-01 Data Import from MWMS2 | Import AP/RSE/RGE/RC Basic Information into LSCP database                          | Application Server | Automatic                   | N/A |---|---|---|---|---| N/A | 2   | UF-WEB-010-15 App-158 Notification  | Notify representatives & TCP(s) of outstanding un-filed Form APP-158               | Application Server | Automatic                   | N/A |---|---|---|---|---| N/A | 3   | UF-WEB-010-10 Form A Notification   | Notify representatives & TCP(s) of outstanding un-filed Form APP-A                 | Application Server | Automatic                   | N/A |---|---|---|---|---| N/A | 4   | Import SMIS Excel into LSCP         | Import data from SMIS allowing users to create site projects and supervision plans | Application Server | Manual                      | N/A |---|---|---|---|---| N/A | 5   | Production backup                   | N/A | Veeam backup       | Automatic                   | N/A |---|---|---|---|---|
### 5.3 Scheduled Batch Job

#### 5.3.1 INT-MWMS2-01 Data Import from MWMS2

| **ID/ Name**  | N/A |
|---------------|-----| N/A |---|---| N/A | **Hostname**  | N/A |
|---|---| N/A | **IP**        | N/A |
|---|---| N/A | **Task**      | N/A |
|---|---| N/A | **Frequency** | N/A |
|---|---| N/A | **Files**     | N/A |
|---|---|
## 6. System Media Input and Output

### 6.1 Input Tapes/ Discs

LSCP application use Veeam for backup and restore (Refer to Computer Operation Manual).

## 7. System Output Reports

### 7.1 Daily Reports

*(Details of daily reports are not specified in the provided documents.)*

## 8. Operations Description

### 8.1 Online Schedule

#### 8.1.1 LSCP Web Service

| **Day**          | **Time**      | N/A |------------------|---------------| N/A |---|---| N/A | Monday to Friday | 00:00 ? 23:59 | N/A |---|---| N/A | Saturday         | 00:00 ? 23:59 | N/A |---|---| N/A | Sunday           | 00:00 ? 23:59 | N/A |---|---| N/A | Public Holiday   | 00:00 ? 23:59 | N/A |---|---|
## 9. Run Job Specifications

### 9.1 Data Import from MWMS

#### 9.1.1 Functions

The contractors? information can be imported from MWMS through the Batch job.

## 10. Error Handling

### 10.1 Critical Error Handling

*   Try to access the BD Common Home from FrontEnd Server.
*   If it still fails, please try to restart frontend server. Make sure the necessary service is running after restart.
*   Please refer to section 6.1 (shut down) and 7.10 (start up) of Computer Operation Procedure Manual
*   If not, please restart the load balancer. Please refer to section 6.10.1 (shut down) and 7.1.1 (start-up) of Computer Operation Procedure Manual.

## Appendix: System Architecture

The entire LSCP system is composed of two sub systems: LSCP Web and LSCP Mobile.

<img src="media/image2.png" style="width:6.62605in;height:5.91667in" />

The following diagram illustrates the architecture of the LSCP for
Production site and UAT site in another perspective.

<img src="media/image3.png" style="width:6.62605in;height:5.81944in" />