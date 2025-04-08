![](media/image3.jpg){width="1.3090277777777777in"
height="1.3090277777777777in"}

**Disaster Recovery Plan** **(T373)**

**of**

**FOR PILOT SYSTEM OF**

**SELF-CERTIFICATION SYSTEM (SCS)**

**FOR THE**

**BUILDINGS DEPARTMENT**

Version: 0.1

**Nov 2024**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be
reproduced in whole or in part without the express permission of the
Government of the HKSAR

+--------+-------------------------------------------------------------+
| **Di   |                                                             |
| stribu |                                                             |
| tion** |                                                             |
+========+=============================================================+
| Copy   | Holder                                                      |
| No.    |                                                             |
+--------+-------------------------------------------------------------+
| 1      | > Buildings Department (BD)                                 |
+--------+-------------------------------------------------------------+
| 2      | > Master Concept (Hong Kong) Limited                        |
+--------+-------------------------------------------------------------+

  -------------------------------------------------------------------------------------
  **Amendment                                                               
  History**                                                                 
  ------------- ------------------------- ------------ ---------- --------- -----------
  Change Number Revision Description      Pages        Revision / Date      Approval
                                          Affected on  Version              Reference
                                          Respective   Number               
                                          Version                           

  1             First draft               N/A          0.1        6/11/24   

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            

                                                                            
  -------------------------------------------------------------------------------------

**Table of Contents**

[**1. INTRODUCTION 1**](#introduction)

[**2. BACKUP STRATEGY 1**](#backup-strategy)

[**3. DISASTER RECOVERY PROCEDURES 2**](#disaster-recovery-procedures)

> [3.1. PREPARATION OF DR SITE 2](#preparation-of-dr-site)
>
> [3.1.1. Contact Point for Disaster Recovery
> 2](#contact-point-for-disaster-recovery)
>
> [3.1.2. Disaster Recovery Site Location
> 4](#disaster-recovery-site-location)
>
> [3.1.3. Disaster Recovery Equipment 4](#_heading=h.35nkun2)
>
> [3.2. DISASTER RECOVERY 6](#disaster-recovery)
>
> [3.2.1. Backup the VM from Production VM (Initial/One Time)
> 6](#backup-the-vm-from-production-vm-initialone-time)
>
> [3.2.2. Restore CDPSS Web Application
> 7](#restore-lscp-web-application)
>
> [3.2.3. Recovery Data & Data Files 8](#recovery-data-data-files)
>
> [3.2.4. Config DR backup Server static route and IP address
> 9](#config-dr-backup-server-static-route-and-ip-address)

[**4. PLANNING FOR DISASTER RECOVERY DRILL
9**](#planning-for-disaster-recovery-drill)

> [4.1. STAGE 0 -- SITE READINESS 9](#stage-0-site-readiness)
>
> [4.1.1. Network Connection 9](#network-connection)
>
> [4.1.2. Server Status Check 10](#server-status-check)
>
> [4.2. STAGE 1 -- SYSTEM ENVIRONMENT SET UP TEST
> 10](#stage-1-system-environment-set-up-test)
>
> [4.2.1. Procedure to start-up the DR DB Server
> 10](#procedure-to-start-up-the-dr-db-server)
>
> [4.2.2. Procedure to start-up the DR Web Server
> 10](#procedure-to-start-up-the-dr-web-server)
>
> [4.2.3. Procedure to start-up the DR Backend Server
> 10](#procedure-to-start-up-the-dr-backend-server)
>
> [4.2.4. Procedure to start-up the DR API Server
> 10](#procedure-to-start-up-the-dr-api-server)
>
> [4.3. STAGE 2 -- APPLICATION SYSTEM TEST
> 11](#stage-2-application-system-test)
>
> [4.3.1. Procedure to test API service 11](#_heading=h.4k668n3)
>
> [4.3.2. Procedure to test Web Server 11](#_heading=h.1egqt2p)
>
> [4.3.3. Procedure to test Backend Server
> 11](#procedure-to-test-backend-portal)

[**5. CURRENT AND MINIMUM HARDWARE CAPACITY
11**](#current-and-minimum-hardware-capacity)

#  INTRODUCTION

> The Disaster Recovery Plan (DRP) defines the disaster recovery
> procedures in case the system of pilot project of self-certification
> system (SCS) for Buildings Department (BD) is being interrupted. It
> contains the information needed to post-interruption decision-making
> and the response to any disruptive or extended interruption of the
> system's normal operations and services.
>
> This document should be updated whenever there is any change in the
> hardware, software, operation procedure, and responsible party of the
> system. Moreover, regular drill should be conducted to ensure the
> procedures are correct and workable and this document should be
> reviewed after every Disaster Recovery (DR) drill.

# BACKUP STRATEGY

> Offsite backup is the process of transferring data from primary site
> to a separate storage device, i.e. de-duplicated backup disk at DR
> site. If the original data is lost or damaged, the data restoration
> from the backup disk could help the system switch the operation to DR
> site to sustain the service at an acceptable degraded level.
>
> The backup includes following:

-   Data; and

-   Data File (e.g. supporting document of Form A, Form B or Quality
    Supervision Form, Generated report)

> Application backup is not necessary, because the application
> installation or update will be installed on both Production and DR
> sites every single time.

1.   [DATA BACKUP]{.smallcaps}

> At least two types of data should be backed up. They are:

-   Database

-   Data File

> The data stored in the MSSQL will be stored in local storage and copy
> through Veeam to DR site by scheduler and script setup on Production
> server

1.  \
    [SYSTEM BACKUP]{.smallcaps}

> As the system should not have many changes regularly, it is
> recommended to perform a full system image backup after any system
> patching.
>
> Backup will be run by Veeam and backup to SAN storage. Veeam
> Replication will be run from SAN storage to Dell Data Domain to store
> the SAN data. There is also a weekly backup job to backup data to
> tape.
>
> The following system image of servers will be backup:
>
> prd-scs-log-01
>
> prd-scs-esetnod32
>
> prd-scs-proxy
>
> prd-scs-filer
>
> prd-scs-admin-api-01
>
> prd-scs-admin-frontend-01
>
> prd-scs-admin-backend-01
>
> prd-scs-db-01
>
> prd-scs-admin-api-02
>
> prd-scs-admin-frontend-01
>
> prd-scs-admin-backend-02
>
> prd-scs-db-02
>
> scspad
>
> scspdb
>
> scsplog
>
> scspwg
>
> scspwi

# DISASTER RECOVERY PROCEDURES

##  PREPARATION OF DR SITE

###  Contact Point for Disaster Recovery

> The following is the list of contact point for disaster recovery of
> SCS:

  ------------------------------------------------------------------------------
  **Role**         **Department**   **Contact      **Contact    **Contact No.
                                    Point**        No. at       after office
                                                   office       hour**
                                                   hours**      
  ---------------- ---------------- -------------- ------------ ----------------
  Chief DR         BD                                           
  Commander                                                     

  Business DR      BD                                           
  Commander                                                     

  End-user         BD                                           
  Coordinator                                                   

  Project Team     MCI              Harry          +852 9092    +852 9092 7057
                                                   7057         

  Project Team     MCI              Harry          +852 9092    +852 9092 7057
                                                   7057         
  ------------------------------------------------------------------------------

![](media/image5.png){width="6.626049868766404in"
height="6.444444444444445in"}

### Disaster Recovery Site Location

BD Headquarters (BDHQ), North Tower, West Kowloon Government Offices
(WKGO), 11 Hoi Ting Road, Yau Ma Tei, Kowloon

AIA DR Site

**Disaster Recovery Equipment**

+--------+--------+-----+-----+-----+-------------+------+----------+
| **     | **Host | **  | **R | *   | **IP        | **   | **Host   |
| Role** | Name** | vCP | AM\ | *Di | Addresses** | Data | Server / |
|        |        | U** | (GB | sk\ |             | Cent | Zone**   |
|        |        |     | )** | (GB |             | er** |          |
|        |        |     |     | )** |             |      |          |
+========+========+=====+=====+=====+=============+======+==========+
| v      | dr     | 16  | 39  | 1.3 | 19          | AIA  | dr-scs   |
| Center | -scs-\ |     |     | 3TB | 2.168.20.18 |      | -admin-\ |
|        | vcen   |     |     |     | /           |      | s        |
|        | ter-01 |     |     |     |             |      | erver-01 |
|        |        |     |     |     | 1           |      |          |
|        |        |     |     |     | 0.5.174.225 |      |          |
+--------+--------+-----+-----+-----+-------------+------+----------+
| Veeam  | dr     | 8   | 24  | 300 | 19          | AIA  | dr-scs   |
| Backup | -scs-\ |     |     | +   | 2.168.20.19 |      | -admin-\ |
| Server | bac    |     |     |     | /           |      | s        |
|        | kup-01 |     |     | 1TB |             |      | erver-01 |
|        |        |     |     |     | 1           |      |          |
|        |        |     |     |     | 0.5.161.224 |      |          |
+--------+--------+-----+-----+-----+-------------+------+----------+
| Kiwi   | dr     | 4   | 8   | 300 | 19          | AIA  | dr-scs   |
| Log\   | -scs-\ |     |     | +   | 2.168.20.10 |      | -admin-\ |
| Server | log-01 |     |     |     |             |      | s        |
|        |        |     |     | 500 |             |      | erver-01 |
+--------+--------+-----+-----+-----+-------------+------+----------+
| API\   | dr     | 2   | 8   | 90  | 19          | AIA  | dr-scs   |
| Server | -scs-\ |     |     |     | 2.168.22.11 |      | -admin-\ |
|        | a      |     |     |     |             |      | s        |
|        | dmin-\ |     |     |     |             |      | erver-01 |
|        | api-01 |     |     |     |             |      |          |
+--------+--------+-----+-----+-----+-------------+------+----------+
| Fro    | dr     | 2   | 8   | 90  | 19          | AIA  | dr-scs   |
| ntend\ | -scs-\ |     |     |     | 2.168.22.12 |      | -admin-\ |
| Server | a      |     |     |     |             |      | s        |
|        | dmin-\ |     |     |     |             |      | erver-01 |
|        | front  |     |     |     |             |      |          |
|        | end-01 |     |     |     |             |      |          |
+--------+--------+-----+-----+-----+-------------+------+----------+
| Ba     | dr     | 2   | 8   | 90  | 19          | AIA  | dr-scs   |
| ckend\ | -scs-\ |     |     |     | 2.168.22.13 |      | -admin-\ |
| Server | a      |     |     |     |             |      | s        |
|        | dmin-\ |     |     |     |             |      | erver-01 |
|        | back   |     |     |     |             |      |          |
|        | end-01 |     |     |     |             |      |          |
+--------+--------+-----+-----+-----+-------------+------+----------+
| Dat    | dr     | 2   | 8   | 90  | 19          | AIA  | dr-scs   |
| abase\ | -scs-\ |     |     | +   | 2.168.22.14 |      | -admin-\ |
| Server | db-01  |     |     |     |             |      | s        |
|        |        |     |     | 500 |             |      | erver-01 |
+--------+--------+-----+-----+-----+-------------+------+----------+
| File\  | dr     | 2   | 8   | 90  | 19          | AIA  | dr-scs   |
| Server | -scs-\ |     |     | +   | 2.168.22.16 |      | -admin-\ |
|        | filer  |     |     |     |             |      | s        |
|        |        |     |     | 1TB |             |      | erver-01 |
+--------+--------+-----+-----+-----+-------------+------+----------+
| Re     | dr     | 2   | 4   | 90  | 19          | AIA  | dr-scs   |
| verse\ | -scs-\ |     |     |     | 2.168.22.15 |      | -admin-\ |
| Proxy\ | proxy  |     |     |     | /           |      | s        |
| Server |        |     |     |     |             |      | erver-01 |
|        |        |     |     |     | 1           |      |          |
|        |        |     |     |     | 0.5.174.228 |      |          |
+--------+--------+-----+-----+-----+-------------+------+----------+

[GCIS environment]{.underline}

Because of the DR nature of GCIS (P1/P2 architecture), no physical
hardware is used for DR.

##  DISASTER RECOVERY

### Backup the VM from Production VM (Initial/One Time)

The DR's VMs will be installed and configured via restore related VM
snapshot of Production on LSCP Backup Server via Veeam.

> ![](media/image1.png){width="4.65625in"
> height="2.2708333333333335in"}\
> \
> Backup list:

+-----------------------+----------------------+----------------------+
|                       | > Production VM      | DR VM                |
+=======================+======================+======================+
| vCenter               | prd-scs-vcenter-01   | dr-scs-vcenter-01    |
+-----------------------+----------------------+----------------------+
| Proxy                 | prd-scs-proxy        | dr-scs-proxy         |
+-----------------------+----------------------+----------------------+
| Kiwi Log Servers      | prd-scs-log-01       | dr-scs-log-01        |
+-----------------------+----------------------+----------------------+
| File Server           | prd-scs-filer        | dr-scs-filer         |
+-----------------------+----------------------+----------------------+
| Application Server    | prd-s                | dr-s                 |
|                       | cs-admin-frontend-01 | cs-admin-frontend-01 |
|                       |                      |                      |
|                       | prd-s                | dr-s                 |
|                       | cs-admin-frontend-02 | cs-admin-frontend-02 |
+-----------------------+----------------------+----------------------+
| API Server            | prd-scs-admin-api-01 | dr-scs-admin-api-01  |
|                       |                      |                      |
|                       | prd-scs-admin-api-02 | dr-scs-admin-api-01  |
+-----------------------+----------------------+----------------------+
| Backend Server        | prd-                 | dr-                  |
|                       | scs-admin-backend-01 | scs-admin-backend-01 |
|                       |                      |                      |
|                       | prd-                 | dr-                  |
|                       | scs-admin-backend-02 | scs-admin-backend-02 |
+-----------------------+----------------------+----------------------+
| Database              | prd-scs-db-01        | dr-scs-db-01         |
|                       |                      |                      |
| Server (SQL Server) 1 | prd-scs-db-02        | dr-scs-db-02         |
+-----------------------+----------------------+----------------------+

> [GCIS]{.underline}
>
> The servers in Production VM and DR VM are the same but in P1 and P2
> respectively. Please refer to **[System Manual]{.underline}**.

### Restore LSCP Web Application

> [As DR VM servers will be keep to available on DR site in parallel
> with Production, every new application updates will be deployed to
> production VM and DR VM in same time]{.underline}

+-----------------------+-----------------------+-----------------------+
| Frontend Website      | > scspad (GCIS P1)    | scspad (GCIS P2)      |
| Application for       |                       |                       |
| public users          |                       |                       |
+=======================+=======================+=======================+
| Backend Application   | > prd-s               | dr-s                  |
|                       | cs-admin-frontend-01\ | cs-admin-frontend-01\ |
|                       | > prd-                | dr-                   |
|                       | scs-admin-frontend-02 | scs-admin-frontend-02 |
+-----------------------+-----------------------+-----------------------+

[GCIS]{.underline}

[GCIS DR will perform by GCIS and we just need check the url and data
after DR or Drill. The link will be
[[www1.scs.bd.gov.hk]{.underline}](http://www1.scs.bd.gov.hk)]{.mark}

###  Recovery Data & Data Files

The Database BAK file will be daily backup and copied from production to
DR site by Scheduler and programming script.

The Data File (e.g. supporting documents and submission forms) files
will be daily batch backup from production to DR site by Scheduler and
programming script.

The backup database and data files will be stored on PRD ( D:\\backup)

via Veeam copy to DR VM & Path (D:\\backup), it will be manual restored
if need to setup DR

+-------------+---------------+-----------+--------------+------------+
| > Server    | > Production  | Copy to   | Restore to   | Files      |
|             | > VM          |           | DR VM        |            |
+=============+===============+===========+==============+============+
| File Server | prd-scs-filer | D         | D:\\bac      | Data File  |
|             |               | :\\backup | kend\\upload | (e.g.      |
|             |               |           | (d           | supporting |
|             |               |           | r-scs-filer) | documents  |
|             |               |           |              | and        |
|             |               |           |              | submission |
|             |               |           |              | forms)     |
+-------------+---------------+-----------+--------------+------------+
| Database    | prd-scs-db-01 | D         | dr-scs-db-01 | SQL Server |
| Server (SQL |               | :\\backup |              | Database   |
| Server)     | prd-scs-db-02 |           |              | BAK        |
+-------------+---------------+-----------+--------------+------------+

Restore sql server database from .bak file Using SQL-Server Management
Studio

1.  Connect to your SQL Server, right-click on the "Databases"
    directory, and choose "Restore Database"

> ![](media/image4.png){width="6.052924321959755in"
> height="2.7123961067366578in"}

2.  Click the button beneath the "Source" section next to "Device"

3.  In the "Select backup device" press "Add"

4.  Select the backup file or files (.bak) you are going to restore,
    then click "OK"

5.  In the "Restore Database" window specify the database's name you
    will restore and click "OK" to start

> ![ssms restore options](media/image2.png){width="4.472569991251094in"
> height="2.648337707786527in"}

### Config DR backup Server static route and IP address

The DR's VMs will be installed and configured and parallel run with
below URL and IP.

DR URL
[[www1.[scs.bd.ccgo.hksarg]{.mark}]{.underline}](http://www1.scs.bd.ccgo.hksarg)

IP 10.5.174.245

No DNS required for additional configuration for DR restore, just notice
users to use DR URL to visit DR web application.

[GCIS]{.underline}

The DR's VMs will be installed and configured and parallel run with
below URL and IP.

DR URL [[www1.scs.bd.gov.hk]{.mark}](http://www1.scs.bd.gov.hk)

IP 172.21.131.38

No DNS required for additional configuration for DR restore, just notice
users to use DR URL to visit DR web application.

# PLANNING FOR DISASTER RECOVERY DRILL

##  STAGE 0 -- SITE READINESS

### Network Connection

1.  Make sure all switches are powered on.

2.  Make sure all network cables are connected properly.

3.  Try reset the switch by unplug and reconnect power if the above
    procedure didn't help.

### Server Status Check

1.  Login to the DR servers by sharepoint administrator account.

2.  Open "Event Viewer" inside "Programs 🡪 Administration Tools".

3.  Check all the "Warning" and "Error" logs.

> 4\. Report to SM&S contractor for any warnings and errors found to see
> if they have adverse impacts to CDPSS.

##  STAGE 1 -- SYSTEM ENVIRONMENT SET UP TEST

###  Procedure to start-up the DR DB Server 

1.  After Power on the server, make sure the below service is in a
    "Running" state

> "SQL Server (MSSQLSERVER)"

### Procedure to start-up the DR Web Server

1.  After Power on the server, make sure the below service is in a
    "Running" state

> "Office Online"

2.  If the service is not in a "Running" state, start the service
    manually.

### Procedure to start-up the DR Backend Server

1.  After Power on the server, make sure the below service is in a
    "Running" state

> "Office Online"

2.  If the service is not in a "Running" state, start the service
    manually.

### Procedure to start-up the DR API Server

1.  After Power on the server, make sure the below service is in a
    "Running" state

> "Office Online"

2.  If the service is not in a "Running" state, start the service
    manually.

##  STAGE 2 -- APPLICATION SYSTEM TEST

###  Procedure to test Frontend (GCIS)

1.  Before the DR test date, create a record in the frontend

2.  On DR day, check both
    [[https://www2.scs.bd.gov.hk/]{.underline}](https://cdpssdr.bd.gov.hk/)
    and
    [[https://www2.scs.bd.gov.hk/api]{.underline}](https://www2.scs.bd.gov.hk/api)
    are accessible

3.  Check if the record from 1. exists in those environments

### Procedure to test Backend Portal

On DR day, make sure the LSCP backend can be accessed by: {backend
domain} or {OSDP}

# CURRENT AND MINIMUM HARDWARE CAPACITY

> Please refer to the following document:

-   Site Specification; and

-   System Manual
