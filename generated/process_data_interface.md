# Process Data Interface for Licensing Self-Certification Portal

![BDlogo](media/image1.jpg)

**Version: 0.1**

**Jan 2025**

? The Government of the Hong Kong Special Administrative Region

The contents of this document remain the property of and may not be reproduced in whole or in part without the express permission of the Government of the HKSAR.

## 1. Introduction

This Process Data Interface (PDI) document describes the data processing and external system integrations for the Licensing Self-Certification Portal (LSCP) being developed for the Buildings Department (BD).

The LSCP is designed to modernize and streamline the process of handling applications for certificates and notices related to Educational Premises (EP), Child Care Centres (CCC), and Temporary Places of Public Entertainment License (TPPEL).  It aims to:

*   Enable e-submission of applications and supporting documents by applicants, Authorized Persons (AP), and Registered Structure Engineers (RSE).
*   Facilitate e-processing of applications by BD users and other relevant departments like Education Bureau (EDB) and Social Welfare Department (SWD).
*   Provide e-tracking capabilities for all users to monitor application status.
*   Establish a centralized data repository for all application records and supporting documents, improving search and retrieval efficiency.

This document is structured into three main sections:

1.  **Introduction**: Provides an overview of the PDI's purpose and scope.
2.  **System Data Process Interface**: Defines the internal data handling approach within the LSCP system.
3.  **External Interfaces**: Details the system's integration with external systems, including interface specifications.

The PDI is crucial for ensuring seamless data flow and interoperability between the LSCP and other essential systems within and outside the Buildings Department.

**Abbreviations of External Systems:**

| Abbreviation | Other External System                   | Host                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      Ukraine, China, a. 1943-1940.

[3.2.1.  9.  1960-1990.

[3.2.1.  1990-2000.

[3.2.1.  2000-2010.

[3.2.1.  2010-2020.

[3.2.1.  2020-2030.

[3.2.1.  2030-2040.

[3.2.1.  2040-2050.

[3.2.1.  2050-2060.

[3.2.1.  2060-2070.

[3.2.1.  2070-2080.

[3.2.1.  2080-2090.

[3.2.1.  2090-2100.

[3.2.1. 2100-2110.

[3.2.1. 2110-2120.

[3.2.1. 2120-2130.

[3.2.1. 2130-2140.

[3.2.1. 2140-2150.

[3.2.1. 2150-2160.

[3.2.1. 2160-2170.

[3.2.1. 2170-2180.

[3.2.1. 2180-2190.

[3.2.1. 2190-2200.

[3.2.1. 2200-2210.

[3.2.1. 2210-2220.

[3.2.1. 2220-2230.

[3.2.1. 2230-2240.

[3.2.1. 2240-2250.

[3.2.1. 2250-2260.

[3.2.1. 2260-2270.

[3.2.1. 2270-2280.

[3.2.1. 2280-2290.

[3.2.1. 2290-2300.

[3.2.1. 2300-2310.

[3.2.1. 2310-2320.

[3.2.1. 2320-2330.

[3.2.1. 2330-2340.

[3.2.1. 2340-2350.

[3.2.1. 2350-2360.

[3.2.1. 2360-2370.

[3.2.1. 2370-2380.

[3.2.1. 2380-2390.

[3.2.1. 2390-2400.

[3.2.1. 2400-2410.

[3.2.1. 2410-2420.

[3.2.1. 2420-2430.

[3.2.1. 2430-2440.

[3.2.1. 2440-2450.

[3.2.1. 2450-2460.

[3.2.1. 2460-2470.

[3.2.1. 2470-2480.

[3.2.1. 2480-2490.

[3.2.1. 2490-2500.

[3.2.1. 2500-2510.

[3.2.1. 2510-2520.

[3.2.1. 2520-2530.

[3.2.1. 2530-2540.

[3.2.1. 2540-2550.

[3.2.1. 2550-2560.

[3.2.1. 2560-2570.

[3.2.1. 2570-2580.

[3.2.1. 2580-2590.

[3.2.1. 2590-2600.

[3.2.1. 2600-2610.

[3.2.1. 2610-2620.

[3.2.1. 2620-2630.

[3.2.1. 2630-2640.

[3.2.1. 2640-2650.

[3.2.1. 2650-2660.

[3.2.1. 2660-2670.

[3.2.1. 2670-2680.

[3.2.1. 2680-2690.

[3.2.1. 2690-2700.

[3.2.1. 2700-2710.

[3.2.1. 2710-2720.

[3.2.1. 2720-2730.

[3.2.1. 2730-2740.

[3.2.1. 2740-2750.

[3.2.1. 2750-2760.

[3.2.1. 2760-2770.

[3.2.1. 2770-2780.

[3.2.1. 2780-2790.

[3.2.1. 2790-2800.

[3.2.1. 2800-2810.

[3.2.1. 2810-2820.

[3.2.1. 2820-2830.

[3.2.1. 2830-2840.

[3.2.1. 2840-2850.

[3.2.1. 2850-2860.

[3.2.1. 2860-2870.

[3.2.1. 2870-2880.

[3.2.1. 2880-2890.

[3.2.1. 2890-2900.

[3.2.1. 2900-2910.

[3.2.1. 2910-2920.

[3.2.1. 2920-2930.

[3.2.1. 2930-2940.

[3.2.1. 2940-2950.

[3.2.1. 2950-2960.

[3.2.1. 2960-2970.

[3.2.1. 2970-2980.

[3.2.1. 2980-2990.

[3.2.1. 2990-3000.

[3.2.1. 3000-3010.

[3.2.1. 3010-3020.

[3.2.1. 3020-3030.

[3.2.1. 3030-3040.

[3.2.1. 3040-3050.

[3.2.1. 3050-3060.

[3.2.1. 3060-3070.

[3.2.1. 3070-3080.

[3.2.1. 3080-3090.

[3.2.1. 3090-3100.

[3.2.1. 3100-3110.

[3.2.1. 3110-3120.

[3.2.1. 3120-3130.

[3.2.1. 3130-3140.

[3.2.1. 3140-3150.

[3.2.1. 3150-3160.

[3.2.1. 3160-3170.

[3.2.1. 3170-3180.

[3.2.1. 3180-3190.

[3.2.1. 3190-3200.

[3.2.1. 3200-3210.

[3.2.1. 3210-3220.

[3.2.1. 3220-3230.

[3.2.1. 3230-3240.

[3.2.1. 3240-3250.

[3.2.1. 3250-3260.

[3.2.1. 3260-3270.

[3.2.1. 3270-3280.

[3.2.1. 3280-3290.

[3.2.1. 3290-3300.

[3.2.1. 3300-3310.

[3.2.1. 3310-3320.

[3.2.1. 3320-3330.

[3.2.1. 3330-3340.

[3.2.1. 3340-3350.

[3.2.1. 3350-3360.

[3.2.1. 3360-3370.

[3.2.1. 3370-3380.

[3.2.1. 3380-3390.

[3.2.1. 3390-3400.

[3.2.1. 3400-3410.

[3.2.1. 3410-3420.

[3.2.1. 3420-3430.

[3.2.1. 3430-3440.

[3.2.1. 3440-3450.

[3.2.1. 3450-3460.

[3.2.1. 3460-3470.

[3.2.1. 3470-3480.

[3.2.1. 3480-3490.

[3.2.1. 3490-3500.

[3.2.1. 3500-3510.

[3.2.1. 3510-3520.

[3.2.1. 3520-3530.

[3.2.1. 3530-3540.

[3.2.1. 3540-3550.

[3.2.1. 3550-3560.

[3.2.1. 3560-3570.

[3.2.1. 3570-3580.

[3.2.1. 3580-3590.

[3.2.1. 3590-3600.

[3.2.1. 3600-3610.

[3.2.1. 3610-3620.

[3.2.1. 3620-3630.

[3.2.1. 3630-3640.

[3.2.1. 3640-3650.

[3.2.1. 3650-3660.

[3.2.1. 3660-3670.

[3.2.1. 3670-3680.

[3.2.1. 3680-3690.

[3.2.1. 3690-3700.

[3.2.1. 3700-3710.

[3.2.1. 3710-3720.

[3.2.1. 3720-3730.

[3.2.1. 3730-3740.

[3.2.1. 3740-3750.

[3.2.1. 3750-3760.

[3.2.1. 3760-3770.

[3.2.1. 3770-3780.

[3.2.1. 3780-3790.

[3.2.1. 3790-3800.

[3.2.1. 3800-3810.

[3.2.1. 3810-3820.

[3.2.1. 3820-3830.

[3.2.1. 3830-3840.

[3.2.1. 3840-3850.

[3.2.1. 3850-3860.

[3.2.1. 3860-3870.

[3.2.1. 3870-3880.

[3.2.1. 3880-3890.

[3.2.1. 3890-3900.

[3.2.1. 3900-3910.

[3.2.1. 3910-3920.

[3.2.1. 3920-3930.

[3.2.1. 3930-3940.

[3.2.1. 3940-3950.

[3.2.1. 3950-3960.

[3.2.1. 3960-3970.

[3.2.1. 3970-3980.

[3.2.1. 3980-3990.

[3.2.1. 3990-4000.

[3.2.1. 4000-4010.

[3.2.1. 4010-4020.

[3.2.1. 4020-4030.

[3.2.1. 4030-4040.

[3.2.1. 4040-4050.

[3.2.1. 4050-4060.

[3.2.1. 4060-4070.

[3.2.1. 4070-4080.

[3.2.1. 4080-4090.

[3.2.1. 4090-4100.

[3.2.1. 4100-4110.

[3.2.1. 4110-4120.

[3.2.1. 4120-4130.

[3.2.1. 4130-4140.

[3.2.1. 4140-4150.

[3.2.1. 4150-4160.

[3.2.1. 4160-4170.

[3.2.1. 4170-4180.

[3.2.1. 4180-4190.

[3.2.1. 4190-4200.

[3.2.1. 4200-4210.

[3.2.1. 4210-4220.

[3.2.1. 4220-4230.

[3.2.1. 4230-4240.

[3.2.1. 4240-4250.

[3.2.1. 4250-4260.

[3.2.1. 4260-4270.

[3.2.1. 4270-4280.

[3.2.1. 4280-4290.

[3.2.1. 4290-4300.

[3.2.1. 4300-4310.

[3.2.1. 4310-4320.

[3.2.1. 4320-4330.

[3.2.1. 4330-4340.

[3.2.1. 4340-4350.

[3.2.1. 4350-4360.

[3.2.1. 4360-4370.

[3.2.1. 4370-4380.

[3.2.1. 4380-4390.

[3.2.1. 4390-4400.

[3.2.1. 4400-4410.

[3.2.1. 4410-4420.

[3.2.1. 4420-4430.

[3.2.1. 4430-4440.

[3.2.1. 4440-4450.

[3.2.1. 4450-4460.

[3.2.1. 4460-4470.

[3.2.1. 4470-4480.

[3.2.1. 4480-4490.

[3.2.1. 4490-4500.

[3.2.1. 4500-4510.

[3.2.1. 4510-4520.

[3.2.1. 4520-4530.

[3.2.1. 4530-4540.

[3.2.1. 4540-4550.

[3.2.1. 4550-4560.

[3.2.1. 4560-4570.

[3.2.1. 4570-4580.

[3.2.1. 4580-4590.

[3.2.1. 4590-4600.

[3.2.1. 4600-4610.

[3.2.1. 4610-4620.

[3.2.1. 4620-4630.

[3.2.1. 4630-4640.

[3.2.1. 4640-4650.

[3.2.1. 4650-4660.

[3.2.1. 4660-4670.

[3.2.1. 4670-4680.

[3.2.1. 4680-4690.

[3.2.1. 4690-4700.

[3.2.1. 4700-4710.

[3.2.1. 4710-4720.

[3.2.1. 4720-4730.

[3.2.1. 4730-4740.

[3.2.1. 4740-4750.

[3.2.1. 4750-4760.

[3.2.1. 4760-4770.

[3.2.1. 4770-4780.

[3.2.1. 4780-4790.

[3.2.1. 4790-4800.

[3.2.1. 4800-4810.

[3.2.1. 4810-482