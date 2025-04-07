

![BDlogo][image1]

**PROCESS DATA INTERFACE**

**FOR**

**COMBINED SYSTEM DEVELOPMENT SERVICES**

**FOR** 

**LICENSING SELF-CERTIFICATION PORTAL**

**OF**

**BUILDINGS DEPARTMENT**

**Version: 0.1**

**Jan 2025**

© The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

| Distribution |  |
| :---: | :---: |
| Copy No. | Holder |
| 1 | Buildings Department (BD) |
| 2 | Master Concept (Hong Kong) Limited (MC) |

|  Amendment History  |  |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Change Number | Revision Description | Pages Affected on Respective Version | Revision / Version Number | Date | Approval Reference |
| 1 |  1st draft | All | 0.1 | 16/01/2025 |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

**TABLE OF CONTENTS**

[1\. Introduction	](#1.-introduction)

[2\. System Data Process Interface	](#2.-system-data-process-interface)

[3\. External Interfaces](#3.-external-interfaces)

[3.1 List of External Interface Specification](#3.1-list-of-external-interface-specification)

[3.2 Interface Specification](#3.2-interface-specification)

[3.2.1 INT-SMIS-01- Data Import from SMIS](#3.2.1-int-smis-01--data-import-from-smis)

[3.2.2 INT-OSDP-01 \-Single Sign-On through OSDP](#3.2.2-int-osdp-01--single-sign-on-through-osdp)

[3.2.3 INT-MWMS2-01- Data Import from MWMS2](#3.2.3-int-mwms2-01--data-import-from-mwms2)

[3.2.4 INT-ESH-01 -Data Import from ESH](#3.2.4-int-esh-01--data-import-from-esh)

[3.2.5 INT-ERKS-01 -Data Import from ERKS](#3.2.5-int-erks-01--data-import-from-erks)

[3.2.6 INT-BRAVO-01 -Data Import from BRAVO](#3.2.6-int-bravo-01--data-import-from-bravo)

# **1\. Introduction** {#1.-introduction}

The Process Data Interface (PDI) consists of three sections, namely:

1. Introduction

- helps to explain the contents and purposes of the PDI.

2. System Data Process Interface

- defines the approach for handling the data process within the system     .

3. External Interfaces

- defines the handling approach for the system integration with external systems with interface specifications.

This PDI describes the approach for performing physical design and integration of LSCP for the Buildings Department (BD) with other external systems.

| Abbreviation | Other External System                   | Host                                    |
| :----------- | :-------------------------------------- | :-------------------------------------- |
| SMIS         | Statutory Management Information System | *To be confirmed*                       |
| OSDP         | Open Source Departmental Portal         | *To be confirmed* (likely CCGO Gateway) |
| MWMS2        | Minor Works Management System 2.0       | *To be confirmed*                       |
| ESH          | *Unknown*                               | *To be confirmed*                       |
| ERKS         | *Unknown*                               | *To be confirmed*                       |
| BRAVO        | *Unknown*                               | *To be confirmed*                       |


# **2\. System Data Process Interface** {#2.-system-data-process-interface}

The implemented physical data design the components of the physical process. The interface makes the database implemented using the physical environment appear as the Required System Logical Data Model to the processing components. It aims to ease the system implementation and future maintenance.

For every incoming process request, the function accepts and handles the input first. Then the function updates and enquires the database.

The following is the position of Process Data Interface (PDI) relative to the universal function model:

In/Out data process flow diagram

![][image2]

# 

# **3\. External Interfaces** {#3.-external-interfaces}

## 3.1 List of External Interface Specification {#3.1-list-of-external-interface-specification}

Here below shows the summary of the interface:

| System Scope | Interfacing Party/ System | Interface Spec. ID | Name | Interface Type | In / Out | Authentication / Encryption |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| External | SMIS | INT-SMIS-01 | Data Import from SMIS | Stored Procedure | In | *To be determined* |
| External | OSDP | INT-OSDP-01 | Single Sign-On through OSDP | HTTP Request Redirection | In | TLS 1.2 over HTTPS |
| External | MWMS2 | INT-MWMS2-01 | Data Import from MWMS2 | SFTP and Excel | In | SFTP |
| External | ESH | INT-ESH-01 | Data Import from ESH | SFTP | In |  SFTP|
| External | ERKS | INT-ERKS-01 | Data Import from ERKS | *To be confirmed* | In |  *To be confirmed*|
| External | BRAVO | INT-BRAVO-01 | Data Import from BRAVO | HTTP Request Redirection | In | *To be confirmed* |

**Note:**
-  Some of the authentication and encryption methods are marked "To be determined" or left blank. These will need to be clarified and confirmed based on the specific requirements and capabilities of each external system.

## 

## 3.2 Interface Specification {#3.2-interface-specification}

**(RY Note: the following sections are for reference only. Content is incorrect)**

### 3.2.1 INT-SMIS-01- Data Import from SMIS  {#3.2.1-int-smis-01--data-import-from-smis}

Target System:		SMIS

Interface Type:	Stored Procedure

In / Out:		In

Frequency:		Daily

*   **Description:** The LSCP system will call stored procedures in the SMIS database to import the necessary data. The exact data fields to be imported will need to be defined in the detailed design phase.

*   **Data Exchange:** The data will be transferred directly between the databases via the stored procedures.

*   **Authentication:** The authentication method for accessing the SMIS database will need to be determined (e.g., database user credentials, API keys).

*   **Error Handling:** The stored procedures should include error handling to manage potential issues during data transfer and logging.

*   **Data Mapping:**

| **SMIS Data Item** | **LSCP Data Item** | **Data Type** | **Description** |
| :---------------- | :---------------- | :----------- | :-------------- |
| *To be defined*  | *To be defined*  | *To be defined*  | *To be defined*  |
| ...             | ...             | ...          | ...             |

*   **Example Stored Procedure Call (Illustrative):**

```sql
EXECUTE SMIS.Import_LSCP_Data;
```

### 3.2.2 INT-OSDP-01 \-Single Sign-On through OSDP {#3.2.2-int-osdp-01--single-sign-on-through-osdp}

Target System:		OSDP

Interface Type:	URL redirection with departmental portal

In / Out:		In

Frequency:		Per user request

**Description:** Users from BD and other B/Ds will access the LSCP by logging into their respective departmental portals (OSDP). A link to redirect to the LSCP will be provided in the BD Departmental Portal and other B/Ds Departmental Portal. The connection between the other B/Ds departmental portal and the LSCP is SSL secured.

**Access from Buildings Departments (BD) Departmental Portal**

-   The link to access the LSCP will be: [https://lscp.bd.gov.hk](https://lscp.bd.gov.hk)

**Access from other B/Ds Departmental Portal**

-   Users from other B/Ds will access the LSCP through their own departmental portals.
-   Their departmental portals will redirect the request through the CCGO gateway.
-   The connection between the other B/Ds departmental portal and the LSCP will be SSL secured.

**Authentication and Authorization:**

-   For the departmental portal users who would like to access the LSCP, they have to apply for Intranet access to ITU.
-   The LSCP System administrator will register an account in the LSCP with regard to the submitted information.
-   LSCP authenticates the incoming user by the login name and the department code of the departmental portal account.
-   If and only if the account with the same login name and department code exists, the departmental portal user could login to the LSCP.
-   Both BD users and other B/Ds users will be authenticated in this way.

**Data Exchange:**

-   The departmental portal has to forward the “UID” and “Dpdeptid” to LSCP in the HTTP response header.
-   The UID and Dpdeptid should contain information of departmental portal user ID and department code.

**In/Out data process flow diagram**  
![][image4]

### 3.2.3 INT-MWMS2-01- Data Import from MWMS2 {#3.2.3-int-mwms2-01--data-import-from-mwms2}

Target System:		MWMS2

Interface Type:	SFTP and Excel

In / Out:		In

Frequency:		Daily

*   **Description:** The LSCP system will retrieve Excel files containing AP/RSE information from the MWMS2 system via a scheduled task (e.g., daily). The files will be transferred using SFTP.

*   **Data Exchange:**
    1. The MWMS2 system will generate and place Excel files in a designated SFTP server directory.
    2. The LSCP system will connect to the SFTP server, authenticate, and download the Excel files.
    3. The LSCP system will then parse the Excel files and import the data into its database.

*   **Authentication:** Authentication for SFTP access will likely use SSH keys or username/password credentials.

*   **Error Handling:** The system should handle potential errors during file transfer, parsing, and database import, with appropriate logging and retry mechanisms.

*   **Excel File Format:**

    | Field Name | Description                                                                   | Data Type | Format/Example |
    | :--------- | :---------------------------------------------------------------------------- | :-------- | :------------- |
    | AP\_ID     | Unique identifier for the Authorized Person                                  | Number    | 12345          |
    | AP\_NAME   | Name of the Authorized Person                                                | Text      | John Doe       |
    | AP\_REG\_NO | Registration number of the Authorized Person                               | Text      | AP-98765       |
    | RSE\_ID    | Unique identifier for the Registered Structural Engineer                    | Number    | 67890          |
    | RSE\_NAME  | Name of the Registered Structural Engineer                                   | Text      | Jane Smith     |
    | RSE\_REG\_NO| Registration number of the Registered Structural Engineer                   | Text      | RSE-54321      |
    | ...        | ...                                                                           | ...       | ...            |

    (Note: The exact format and content of the Excel file will need to be confirmed with the MWMS2 system owners.)

### 3.2.4 INT-ESH-01 -Data Import from ESH {#3.2.4-int-esh-01--data-import-from-esh}

Target System: ESH

Interface Type:	SFTP

In / Out:		In

Frequency:		Daily

*   **Description:** The LSCP system will retrieve site project information from the ESH system via a scheduled task (e.g., daily). The files will be transferred using SFTP. The imported information is used for validating if a user is involved in the site project.
*   **Data Exchange:**
    1. The ESH system will generate and place files in a designated SFTP server directory.
    2. The LSCP system will connect to the SFTP server, authenticate, and download the files.
    3. The LSCP system will then parse the files and import the data into its database.
*   **Authentication:** Authentication for SFTP access will likely use SSH keys or username/password credentials.
*   **Error Handling:** The system should handle potential errors during file transfer, parsing, and database import, with appropriate logging and retry mechanisms.
*   **File Format:**  The format needs to be confirmed. The file could be excel, csv or json.
*   **Data Mapping:**

| ESH Data Item | LSCP Data Item | Data Type | Description |
| :---- | :---- | :---: | :---- |
| File Reference | File Reference | string | BD Reference Number of the site project |
| Site Address | Site Address | string | address of the site project |
| AP Registration Number | AP Registration Number | string | Registration number of the AP that involve in the related site project |
| RSE Registration Number | RSE Registration Number | string | Registration number of the RSE that involve in the related site project |
| RGE Registration Number | RGE Registration Number | string | Registration number of the RGE that involve in the related site project |
| RC Registration Number | RC Registration Number | string | Registration number of the RC that involve in the related site project |

### 3.2.5 INT-ERKS-01 -Data Import from ERKS {#3.2.5-int-erks-01--data-import-from-erks}

Target System:		ERKS

Interface Type:	TBC

In / Out:		In

Frequency:		TBC

*   **Description:** This interface will likely involve importing data from the ERKS system into LSCP. The specifics of the data and the mechanism will need to be determined in consultation with the ERKS system owners.

*   **Data Exchange:** The method of data exchange (e.g., API, file transfer, database link) needs to be defined.

*   **Authentication:** The authentication and authorization mechanism for accessing ERKS data will need to be established.

*   **Error Handling:** Robust error handling will be required to address any issues during the data exchange process.

*   **Data Mapping:**  
    (This section will need to be filled in with the specific data elements that need to be mapped between ERKS and LSCP)

### 3.2.6 INT-BRAVO-01 -Data Import from BRAVO {#3.2.6-int-bravo-01--data-import-from-bravo}

Target System:		BRAVO

Interface Type:	HTTP Request Redirection

In / Out:		In

Frequency:		Per User Request

*   **Description:** The system can use [https://dp2.bd.hksarg/bravo/intranetSignOn](https://dp2.bd.hksarg/bravo/intranetSignOn) to redirect to BRAVO. Also, the SCS system could be redirected to BRAVO through a URL call with specified parameters.

*   **Data Exchange:** The LSCP system will make HTTP requests (GET or POST) to specific BRAVO URLs, passing any required parameters in the URL query string or request body. The BRAVO system will respond with the relevant data.

*   **Authentication:** The authentication method for accessing BRAVO (e.g., API keys, OAuth) will need to be determined.

*   **Error Handling:** The system should handle any errors returned by the BRAVO API and provide appropriate feedback to the user.

*   **URL Syntax (Examples):**

    *   **with Case number and Year**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?CASE_NUMBER=<CASE_NUMBER>&YEAR=<YEAR>`

    *   **with Block ID**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?BLOCK_ID=<BLOCK_ID>`

    *   **with full File Reference No**
        `https://dp2.bd.hksarg/bravo/BuildingSearchRedirection?SEARCH_TYPE=<SEARCH_TYPE>&SUBJECT_CODE=\<SUBJECT_CODE\>&CASE_NUMBER=\<CASE_NUMBER\>&YEAR=\<YEAR\>&SPECIAL_CAT=\<SPECIAL_CAT>`

    (Note: The exact URL syntax and parameter names need to be confirmed with the BRAVO system owners.)

*   **Data Mapping:**  
    (This section will need to be filled in with the specific data elements that need to be mapped between LSCP and BRAVO.)

### 

\*\*\* End of document\*\*\*

[image1]: <data:image/png;base64,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>

[image2]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAfUAAADoCAYAAAD2d33gAAAdIElEQVR4Xu3d2asl1fnGcf8Boa+88iJ44YUXIoIgiNAERIIECaIEUQwJihcqDhiNOBxjnJIYxSEOGaRjiGKiMSoOiGk1BjVqiBoHWqPGOM/z0A71y7PCu3/Vq2vvrnX6nKpa7/v9wKbP2XvtOnv1WqueWlW1q7ZpAACAC9vkTwAAgDoR6gAAOEGoAwDgBKEOAIAThDoAAE4Q6gAAOEGoAwDgBKEOAIAThDoAAE70DvVtttmGh/NHZPn/BQ9/D8/yuvLw9+ird8mShaI+0ds3ev29896+3usXXUn79i5ZslDUJ3r7Rq+/d97b13v9oitp394lSxaK+kRv3+j19857+3qvX3Ql7du7ZMlCUZ/o7Ru9/t55b1/v9YuupH17lyxZKOoTvX2j19877+3rvX7RlbRv75IlC0V9ordv9Pp75719vdcvupL27V2yZKGoT/T2jV5/77y3r/f6RVfSvr1LliwU9YnevtHr75339vVev+hK2rd3yZKFoj7R2zd6/b3z3r7e6xddSfv2LlmyUNQnevtGr7933tvXe/2iK2nf3iVLFor6RG/f6PX3znv7eq9fdCXt27tkyUJRn+jtG73+3nlvX+/1i66kfXuXLFko6hO9faPX3zvv7eu9ftGVtG/vkiULRX2it2/0+nvnvX291y+6kvbtXbJkoahP9PaNXn/vvLev9/pFV9K+vUuWLBT1id6+0evvnff29V6/6Erat3fJkoWiPtHbN3r9V8KXX37ZfP755/nTk+C9fb3Xry/1v6+++ip/unol7du7ZMlCh/Txxx+nz9b1uPbaa/PiM59++mnzq1/9qvnoo4/yl1acOpo+z1NPPZW/NBlTbd+hTLH+V1xxxWZ9es8992wef/zxvGgv7777blrG22+/nb+0Ii699NLmW9/6Vv70JEyxfVdSzfX77LPP0uf/9a9/PXtu3bp16bm777579typp57a7LDDDrPfu+j1O++8M3+6eiXt27tkyUKHpFDWZ/vjH//YPPvss5s8Pvzww7z4zFtvvZXe99JLL+UvrTgL9SeffDJ/aTKm2r5DmWL9L7/88mbHHXds3nnnnRTEGzZsaHbaaadmr732yov2YqGuvr8aCPXx1F4/9envfe97s98POuigVKfTTjtt9tzatWubww47bPZ7F0LdUaj/7W9/y19Kjj/++Obb3/522jX4xRdfNPvvv39z7rnnpg6i9+28887N66+/3rzyyivNAQcc0Gy33Xapg/39739P79e/++23X/PjH/84lX3ggQdSudNPP73Zfvvtm1133bW57777Zn/vrLPOSiterYyPOeaY9DcJ9embYv0V6upLbUcddVSz++67z37v6m/y6KOPNnvssUez7bbbpv7/9NNPbxLqGg/HHntsc+CBBzYbN26c2/8X9XctY2lpKf1tvec73/kOoT6S2ut3zjnnzGbh6sPqt0cccUSz2267pedsNn/11Ven39UvtddK/fXggw9u3nzzzfS8lnHkkUemPqnX1D9tTNSspH17lyxZ6JAs1LXS+d3vfjd7WONrl7dev/LKK5vLLrssdZaXX365uf3229Pz119/fdoVr86jFdMdd9zRnHjiiek1zZDuueee9LM6yS9+8Yv0un7Xyks/a8WpziVakaoj3XDDDWm3kX7W8gn16Zti/RXq6kPaLalDRdr9qM/529/+Nr0+r7998skn6efvfve7qf9+85vfTLMgC3WtALUBoJB+4YUX0jHIef1/UX/XGNN4+tnPfpZWylZuiqbYviup9vppQ1F10ARLG5T6WX3T+utDDz2Ufn7xxRebV199Nf2s8Fa/32effWZ9UqGuPqn1/dlnn53KWRbUrKR9e5csWeiQLNTVmJpF2MO28ESNq4bW4ze/+U16rr373TrMc889l17TSk4rxT/84Q+zUNdMR2wl98EHH6Tfb7311rRceeKJJ5q//vWvacvw+eefT59BW4qE+vRNsf4KdX2ub3zjG+mhfq3ff/CDH6TX5/W3W265JZWz80V0KEpBbaF++OGHpz77zDPPpNcX9f9F/V0zJM32jQKdUB9H7fWzmbj67k9+8pNZP9LeUfXDSy65ZDaTP//889MGqZ0QZxM37W1SmVNOOWW2XO2Z1a782pW0b++SJQsd0pZ2v4uVaXeEdqjrhDr9nD90jFChbisx0UpOKzyjlar932jLUis6/W4bEYR6HaZY/67d7/fee2/6rJqtzOtv2iOlPUs5C3V7PPjgg+n5Rf1/UX/X3/v9738/e629Mp6aKbbvSvJQP224am+U9hj9/Oc/T8+dcMIJaSNUh4m0O170b95X9XjsscdSqGsvrNHhqb333nv2e61K2rd3yZKFDqlPqGvLTisgldNWn7RD3XbFa0Wp5emhFZ52BXWFujYOTHsld/TRR6fjnZo1ibYSCfU6TLH+XaGuE+b0WdUv5/W3P//5z6mMfb1MffzCCy+chbpm5lpJauavWf6i/r+ov2tX/AUXXDB77dBDDyXUR+Khfj/96U9ne6NsXam+qf5ne47k5JNPTnulrK+qX2tjV7N9hXp7d7vO89Ch2dqVtG/vkiULHZKF+lVXXdU88sgjmzzeeOONtItRr+s4u7YC1TkU6DpeqOf/+c9/pnL6WTMNdYybb7559lpJqOvYjm1NPvzww+l92hVEqE/fFOuvUNdKSrsX9dAKTrMO9Sv103n9Ta/pZ812ND400znkkEM2OVHuP//5T/pZs/FF/X9Rf9exdK2EdWhKZTW2CPVxeKifJmaqR3vPkA776Dk9tNEpthGq4+n6SrNCW+/RelbjRRub77//fuqrGgf6t3Yl7du7ZMlCh7Toe+oXX3xx2pWjM921211l1ej21Qk1vsppJnPNNdds8l7ttpG//OUvvUNdnc12g+rv2G4irXD1L99TH8f69evTDHaRKda/63vq6rO2V2pef/vHP/6xyXs1q9F32/Pvqdu5JpqRz+v/i/q7TjjVngR7jzYy9E2RKdpS+6p/bKmPjKXW/lvKJj/tr7aJToLL91jpXA7rdwp0+xqbxoHK22vaIzXVCyKVKGnf3iVLFlqT9oU49L12HZfZmotz6Ex6nZhkx+61wqzhKxVe29d87WtfS3Wct3Kstf6L+ptm6QrevpbT/7XC1MaqZkZTNq991R8sAKbMa//dGurr6q/6tkdOe6NsZu9BSfv2LlmyUNTHe/tqtmMr766Vo/f6R5e3bzvM16xZs1l/mBr6b2wl7du7ZMlCUZ8I7Wuzna6VY4T6R2bt2w7z9qMG9N+4Stq3d8mShaI++coi4gN+5W3t8QG/Stq3d8mShaI+Edo3XwnqwUwnBmvfrpm6ZsA1yD83/TeOkvbtXbJkod6UnDhUK+/tq5Wfjp3mK0NTY/31bQ5dNhNblrdvHu46Zj1lHvsv+itp394lSxY6FF10Q59rS18VU7lFt2GdR2FuN8Xwbortu5LmrQxNTfXXleT0VR2rk64ep2uvY7557WvhPvXZeg3997XXXkufQ/ca2Fr6KrF9X113atN1FpajfYttu6aJXfK7JiXt27tkyUKHomtV9wn1G2+8cXbd4BK6uIGWrxmRd1Ns35WiFeG8laGpqf66cpvunKav7Oi757rwkj6/rsuObltqX/WPqc7Wa+m/uj67XblTXzfbGu2Lfukrm8u9cFf7yqG6q6DW6XZPhJqUtG/vkiULHUo71OfdIlIdQoGucnZhjHm37dPdsHRFLt3dSjcBsAtr6JrEorth2fv0uu361Hd1tTWp5/Weiy666H8f8L90tyDdlECfQVe0m+qFEKbYvkOqqf7qZ/mlL7VCtStnzbuNan4bYV0sRhsERj9rD4D0GSNburf1lNTUvssxhfppnaurGKrP6GqIRpd/1fpx3333Ta9p1v3ee++lmb36mC7jrb1Netx0003pPe1Q/+Uvf9n86Ec/Sj933VJYdIEv9W0tX/1a75f2Lba1vtbf09UU5U9/+lNaX2tZ+mz2vO6doD6udbyWp/X/1m6kbK2S9u1dsmShQ2mH+rxbRGqrTFfHUuOo4Rfdtk8dR6/pUpy33XZbuq61GlwbB7p8ppahq9TputhaWera22K3dNXlNW3WpI0Ju1uWrrttV+bKV8ZTMcX2HVJN9ddMXZ9XAbxu3brmX//61+y1RbdRzW8jrP6rckYrQPXPvmNE15ivRU3tuxxj1093DNRnUPh9//vfT+tfo8sU6zWtO9UnNcHRutUuVaz+etdddzUnnXRSWo9u3Lhxk1DXZEgblvNuKSzq09rI1Lr5uOOOS2GtsdC+xbZdGnzDhg3pCov6WWPg/vvvT31cn1nvsVscayzohkVdG9FDK2nf3iVLFjqUrlDvukVke/f7otv2aYWlBtRuGtFKy47raDfOddddl35Wx9UlOa3jqlO2G13X09bKsN3pRMd2uu6eNQVTbN8h1VR/rdy0gvz617+ePrceCuf2fac1NmTRbYTtkq86d8SCXOOhZIzUoqb2XY6x66eZrR1Lt3ujWx9UqLfvlKYbrmgD0kJd5UX9TetprTu7Qn3eLYVtmZr968qGNrHSOGnvfrdj6gp13b5YN0My2r2v1/7973+nv2cbsaKytgdrLCXt27tkyUKHkoe6BbC0r1HdDvVFt+3TCqvdeO1Q1wkXujuQHTPSSs9CXc91nYinAM//zlRPupti+w6plvrrErDtb2NoRaWbFalf6XrYi26jmt+cSMGsfqwVonara/eplIyRWtTSvss1Zv3UJ7WeVN/SelZ9Sp9HNwgShbr6prHQtxOd7dCOaFe39qx2hfq8WwqLDj/pM2h5drh1Uajr8NQxxxwze7/dQ0Qbxfp7urub0UmoY9+oqKR9e5csWehQ8lCfd+OJdqgvum1fvsJqh7p231ijqxOrE1moa6uufQtKzei1G0hbgrofsP0tHdPR+6doiu07pFrqb7Pm9i530R4hzZQW3UY1D3WxWYh2P9q5ICVjpBa1tO9yjVk/u4St+p5urKKH+qPdhEWh3t5jqUM/Wq/aTL29V0n9M98AtVCfd0thuxOnDkUpyHWHTv2+KNTPOOOMTW4+pGP1ek2TN/299ucl1AfUN9R1rFudSJ1h0W378hVWO9TPO++81ElVTid4aFZju2/sFpT6PLoFpXUcrRy1ZalOp/foZAyd3DFFU2zfIdVSfx1vVJ9UP9XuRtHxQW206gzpRbdR7Qp1nTyn123FJyVjpBa1tO9yjVk/BWB+dz67M6XCUqGufqeZufqYJkMKaQt1bViqb9lu87yvWqjPu6WwTuq0/qtQtnNOVKZ9i+12qNutivXVOdFufDt8QKiPqP099UWhrsbWSsl23cy7bd+ZZ56Zzng02gK1ZWoZWnGqI+hhJyDpLE8Lef2u1xTmog7VPu6p2Y+O2UzRFNt3SDXVX7svbRej9UftLtQKTebdRjW/jbDRuGgf85S+Y6QWNbXvcoxVPwtKnVDWplm31p06613h2z4UqXWl1qcW6u1157nnnpve3+6rCln7nnrXLYX1t7SnyZ7XyW+24St2i22b0eucEr1HEyz7uyqvjQP7e3mo5xstQytp394lSxY6RdoSbN8ectFt++ZRR1CHsN0/2i3Z/g67Oqm2Jtv0Hs3gteFhJx5NUe3tu7Vqq7/6oPqiZiBdJ60t5zaqueWMkamqrX1LTbl+CnVNgrSubE9qLNS1HtXzfa8Hog2JrlsK66JM6veiPqtJlZk3DrRxoXXzVL9qbErat3fJkoWiPtHbN3r9vfPevlOun4V6zkLdDiNhvpL27V2yZKGoT/T2jV5/77y375Trp6+idV3TQHtOtWs737uJzZW0b++SJQtFfaK3b/T6e+e9fb3XL7qS9u1dsmShqE/09o1ef++8t6/3+kVX0r69S5YsFPWJ3r7R6++d9/b1Xr/oStq3d8mShaI+0ds3ev29896+3usXXUn79i5ZslDUJ3r7Rq+/d97b13v9oitp394lSxaK+kRv3+j19857+3qvX3Ql7du7ZMlCUZ/o7Ru9/t55b1/v9YuupH17lyxZKOoTvX2j19877+3rvX7RlbRv75IlC0V9ordv9Pp75719vdcvupL27V2yZKGoT/T2jV5/77y3r/f6RVfSvr1LliwU9YnevtHr75339vVev+hK2rd3yZKFoj7R2zd6/b3z3r7e6xddSfv2LlmyUNQnevtGr7933tvXe/2iK2nf3iVLFor6RG/f6PX3znv7eq9fdCXt27tkyUJRn+jtG73+3nlvX+/1i66kfXuX1EJ5+H5Elv9f8PD38CyvKw9/j776lwTgRslKAkA9GNlAMEtLSynU9S8AXwh1IJjl7NIDUAdGNRCIzdLtwWwd8IVQBwLJT75htg74wogGgshn6czWAX8IdSAIBfiaNWuaXXbZZbNgB+ADoxkIQLNxhfn69evT7xbknAkP+EKoAwFYmJt8dk6oAz4Q6kBAeagD8IGRDQREqAM+MbKBgAh1wCdGNhAQoQ74xMgGAiLUAZ8Y2UBAhDrgEyMbCIhQB3xiZAMBEeqAT4xsICBCHfCJkQ0ERKgDPjGygYAIdcAnRjYQEKEO+MTIBgIi1AGfGNlAQIQ64BMjGwiIUAd8YmQDARHqgE+MbCAgQh3wiZENBESoAz4xsoGACHXAJ0Y2EBChDvjEyAYCItQBnxjZQECEOuATIxsIiFAHfGJkAwER6oBPjGwgIEId8ImRDQREqAM+MbKBgAh1wCdGNhAQoQ74xMgGAiLUAZ8Y2UBAhDrgEyMbCIhQB3xiZAMBEeqAT4xsICBCHfCJkQ0ERKgDPjGygYAIdcAnRjYQEKEO+MTIBgIi1AGfGNlAQIQ64BMjGwiIUAd8YmQDARHqgE+MbCAgQh3wiZENBESoAz4xsoGACHXAJ0Y2EBChDvjEyAYCItQBnxjZQECEOuATIxsIiFAHfGJkAwER6oBPjGwgIEId8ImRDQREqAM+MbKBgAh1wCdGNhDA0tLSJr/nob5+/fpNfgdQJ0IdCEChriC3cLdQV5jvsssum4U+gDoR6kAQCvL2Q2G+Zs2azWbtAOrFaAaCsNl6/mCWDvhBqAOB5IHOLB3whRENBJLP1pmlA74Q6kAwzNIBvxjVQDD5mfAA/CDUgYCYpQM+MbIBZ/Tdcz00E1+7du0mj/wkOT3ar+s99uCCNEB9CHWgYnl4t0Pagrn96NJ+vR3q7eUR9EAdCHWgMgrWPHAXhfbWaoe9/V37HcC0EOpABfIgX80Q7yMPeADTQKgDE9YO8ymGp83imb0D00CoAxM09TDv0g53AOMg1IGJUaDXHI6EOzAeQh2YEAvEMY+XrwTb00CwA8Mi1IGJsJPPPCHYgWER6sAEeD7JjGAHhkOoAyOzY+ie2dfwAKwu32sSoAIRTiqzY+wAVhehDozI8273HLN1YPUR6sCIIoU6s3Vg9RHqwIgizV4JdWD1EerAiLyfIJeLVl9gaIwwYEQeLjTTV4Sz/IGxMcKAEUU4893Y1fIArB5GGDAihVyU48yEOrD6GGHAiCzUve+Ct0An1IHVxQgDRmTH1L2HXZR6AmNjhAEjspDzeDMX0/4uPqEOrC5GGDCidsh5DPb8Zi6EOrC6GGHAiPKQs2PPtR9jt13t+Zn9eX0BrCxGGDCirpCzYM8DsRaLNky66gtg5TDCgBEtCrnawt0+76Kz+RfVF8DWY4QBI+oTclMP9z5hbvrUF8DyMcKAEZWEXDs8xwx4Bbce+hx9w9yU1BdAOUYYMKLlhJwCPQ/41Qx5C3H9jeUEedty6gugP0YYMKKtDbk8bPOgt0C2R5e8jC2vHeC2zHnL6Gtr6wtgMUYYMKLVCDkL5nY4t0M6f+Rl2hsDK2016gvg/zHCgBFFC7lo9QWGxggDRhQt5KLVFxgaIwwYUbSQi1ZfYGiMMGBE0UIuWn2BoTHCgBFFC7lo9QWGxggDRhQt5KLVFxgaIwwYUbSQi1ZfYGiMMGBE0UIuWn2BoTHCgBFFC7lo9QWGxggDRhQt5KLVFxgaIwwYUbSQi1ZfYGiMMGBE0UIuWn2BoTHCgBFFC7lo9QWGxggDRhQt5KLVFxgaIwwYUbSQi1ZfYGiMMGBE0UIuWn2BoTHCgBGNFXJffPFFegxtrPoCUTDCgBF1hdxOO+2UnrfHjjvu2Jx22mnNxo0b86Kbef7555trr702f3ozhx9+eLO0tJQ/veq66gtg5TDCgBF1hZxC/Mwzz2xee+215qmnnmpOP/30ZrvttmsOOeSQvOhmbrzxxmaHHXbIn94MoQ74xAgDRtQVcgr1iy++eJPnbr/99lT22WefTb/fcMMNzZ577pnC/qCDDmpefPHF9JoCXeX222+/ueVEob7//vun17bddtvmwAMPbN5+++302sMPP5zer/fss88+zT333PO/D/Ff55xzTvp822+/fXPGGWc0X331VXr+gQcemP2dgw8+uHnzzTdn72nrqi+AlcMIA0bUFXJdof7JJ5+ksrfcckvz2WefpfBUmQcffLDZa6+9mqOPPrr56KOPmrPOOiu9pmCeV04U6lreD3/4w+aqq65K5fSc6O8fdthh6T3HHXdcOhyg8L7//vtTufvuu6+5+uqr08aAwvzVV19NyzryyCObu+++O20IKOC7dNUXwMphhAEj6gq5rlAXlb3++uubt956q7nuuuvSc6+//npzxBFHNHvssUf6vb37fVE5Bfjuu++efpZLLrkkhbQosN97773m/fffT4Gvv6uNCh2r18933nln8/nnnzePPPJI8/LLLzfnn39+mrnbrF2HDFTulVdemS3fdNUXwMphhAEj6gq5rlB/4403UtkNGzY0n376aXPyySenENZzCtSuUF9UTqGu18y9996byuiMeAW8ZuT63XbnK9T1mo7r63ct86ijjkp7B7SxoOfyx2OPPTZbvumqL4CVwwgDRtQVcl2hrqC10NVsXT8/9NBDsxDuCvVF5RTqtrtdrrzyyrTL/JlnnknvWbduXQpyzcYt1HVmvWbfOvauWbuC/4orrkgbB7vttlsKeD3efffdtJGg3f+5rvoCWDmMMGBEXSGnUD/ppJPSbuxHH320ueiii1K5Sy+9NL1+3nnnpePc2gWuM+R33XXX2a70m2++OYWtXltUToGu2fbTTz+dwlphf/bZZ6dj5PpbL730UprpH3rooel3hfUFF1zQ7L333inUv/zyy7QRcOGFF85O4tPx9I8//nh2tr7+bq6rvgBWDiMMGFFXyOXfU1cQ67i1UeBqNq5Q1uPEE09M5S6//PL0mgJVGwaLyinUNbu2v7Hzzjun4+M6Lq4T3ex5nVin5enseJ0Qp134el7L04aAjtvLscceO3uPyuu4e5eu+gJYOYwwYETLDTmFr2bZNhvWLm/NkkXP6SS3LZUT7VZ/7rnnZie5mRdeeKH58MMPZ2Xeeeed9LNm70888UTnSXA6GU/H0VV+nuXWF0A/jDBgRNFCLlp9gaExwoARRQu5aPUFhsYIA0YULeSi1RcYGiMMGFG0kItWX2BojDBgRNFCLlp9gaExwoARRQu5aPUFhsYIA0YULeSi1RcYGiMMGFG0kItWX2BojDBgRGvXrm3Wr1+fP+2S6qn6Alg9hDowIoXc0tJS/rRLqmeUugJjIdSBEUWavRLqwOoj1IGRRdgFrzDneDqw+hhlwMgU6N4DT/XzvuECTIHvNQlQCc1kve6GZ7c7MBxCHZgIj8Ee6URAYAoIdWBC7Nhz7buq7ZACgQ4Mi1AHJsaCvdZA9LJhAtSIUAcmqrZwt88b4Wx+YKoIdWDiph7uhDkwHYQ6UIl2eI4Z8ApuPfQ5CHNgWgh1oDIK9DzgVzPkLcT1NwhyYNoIdaBiedjmQW+BbI8ueRlbXjvAbZnzlgFgGgh1wBkL5nY4t0M6f+Rl2hsDAOpCqAMA4AShDgCAE4Q6AABOEOoAADhBqAMA4AShDgCAE4Q6AABOEOoAADhBqAMA4AShDgCAE4Q6AABO/B8M+3rrKC03RQAAAABJRU5ErkJggg==>

[image3]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAc0AAAAfCAYAAACFxJaNAAASn0lEQVR4Xu2dBazlxPuGF3eCu0uQECyE4O4eCMECwd2Du2tYPLi7Lu5ui+4CwR0CBHe3/v7PbN7+3/Od9t5zzj1399yzfZKmM9Opvf36zXTazgx66MEHsmqqpmpqz7TUPmtVUxumqGs1VVOnTIOyAcxrr70WkyraQKVr61Ta9Z1Kw/ZTado6Ubuq0Kyoo9K1dSrt+k6lYfupNG2dqF1VaFbUUenaOpV2fafSsP1UmrZO1C4VmldffXU2ePDg7KyzzkqJW221VU2mIrTORx99FBclPvzww2zQoP4tk/1khg4dmm2zzTYp/Nhjj+XpjXD00UfHpLpjH3/88Wvi3YzrOmzYsOy9997L41zz66+/Po97epktRJZccsmY1BTNXl+OTTz55JO2pHfmmGOOmNQjrh37veKKK2xp7b3Fck1O0XpldKOW0rDMx5xwwgnZqaeemsel4RtvvJGnla1bxsjW8YYbbsjDzeh43XXXxaSG6EnTf//9N9t1112zDz74IE8rytcT3axfYaFJAbHffvtlBx10UErce++9azIVwTpHHnlkXeEiVl555ZjUdvxkOI5zzz03hZ9++uk8/ZZbbsnDRWAURecQ00bXQnOMMcbIJp544jyOLvPPP3+29tpr52lo2JMtRFZfffWYlM0000wxqQ5t369vI/hxbbvttrakdxp19CLa5AILLJAtvfTSefyqq67KzjjjjDx++OGHp0mg5U477ZTWa4RWtVSeVrT86quvUri/tJSGRT6G8M4775xttNFG2RFHHJHSdthhh6ThSy+9VJMvrtsTrerYik1Gn9OMjq04fehNU/SLaTFfT3SzfqWFpkMtw7nmmmuyc845pyZN67zwwgt5muebaqqpsrPPPjuFf/jhh2zHHXdMYZ5Af/755/zpTulw3333ZQcffHAev/DCC/NtFB2Dn8yhhx6ahz/++OM0Z109ffoxOBQAa6yxRh5/++23s+OOOy4/P56+hw8fngpNHfs///xTt73ddtst++STT1KY4zz55JPzZQON6PjjzeRzUG0UW1ANEH38enFT6lqeeOKJaf7jjz/m12eSSSbJl2MH2Ada82T2xx9/pHT2SR5dXzjqqKOy2267LYV5Ann44YfTdh3We+utt1JYN5iO87zzzkvXFXDGf/75Z3bggQemOODo/Tq7HbI/bAV7EFG7ormIcUBLbcO19GOQltTOG9Fyyy23rNNSeVzLIUOG1Gl50UUX5cuBYx577LFTuDctIWrJfSLKtHQHD25XhxxyyIiVjejUoGjd6EPKbFL3ruson+U6Pvjggw3ZJD7NbZJrvMcee9TY5DvvvJMvl45cu8suu6zGJuX03R544HnzzTdTWDpGyjR95JFHstNOO82zJmI+iPptt912dfq575N+7vOlHzSin8qEUalftK/CQtNrhN9++2223HLLZVtvvXVdTQ5WWmmlwnxTTjllLh55H3300ZTOQROnZjL55JOndJ5mlI9mF550KYAWWmihbLXVVkvLio4hOqi//vorhSUM+998883z5b4vQfpPP/2UnX766Xl8r732ys+PQnWKKaZIhaaO/ZdffqnbHk0Es88+ewovs8wyNU8PAw3Xda211sommGCCPC5d3GZUaGILMm6W63qddNJJyXjjusyfffbZFOZp1u0F+xhrrLGS4/b85NH1xeawl3HGGSdfvvDCC9ccm9KVJke/4IILprlf13XXXTfNl1pqqfyGJM5NO88889TYuJYtuuiiyR5EtMlvvvkm2Y/iXggRp2nMUaHJeq6l7h/X8oknnqjRBi3/+++/Oi1pQYpaKo9rOeOMM9ZpWXS/NKrleOONV6flxRdfXKcl5+VaRgfvdlXEq6++Wqdj0bq+v55sUvdu1DHaJE6Zues42WST1dkkcW0fuMbff/99jY7nn39+vlw6Lr744rne0lH6uk3eeeedNcePjpEyTctaBGO+eL3Q7/7776/Tz32f21jUDx8/UPQrLTQxIG5M8EKT2sKss86aJgpCwTr33HNPvrOYb955583zTjrppHm6xAHWJV3b0H6Jx+bQomOIJ4MI4PtQ86yOwcUHmnlA6dSmPC50IUTc3rjjjpsvI02FwUAk6kqtWjV8zk1PGgIjdlsAv+bcLDi1aaedNi1TPhzyZpttlsLelCM7+P3337N11lmnxqBB1wGnLDbeeOO6fII4Nw01zjJHH9l9993T3G3SbVxpkVho6uYXt956a96UVbQ+WnIv+nr9oaXy9Kblc889l6eD0hvRUufZm5acl2vhDj7aFbz88supNUzOOdorFK3r+5OOWu466t4tal6MOmqu8/b9ldmknL7bZJHTB//eAh2j/5SO8otRK1Gm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>

[image4]: <data:image/png;base64,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>
