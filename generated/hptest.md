```markdown
<img src="media/image1.jpg" style="width:2.03125in;height:1.52083in" alt="BDlogo" />

# Handover Plan: Combined System Development Services for Licensing Self-Certification Portal (LSCP)

## Introduction

This Handover Plan outlines the process for transitioning the Licensing Self-Certification Portal (LSCP) from the development team, Master Concept (Hong Kong) Limited (MC), to the Buildings Department (BD) for ongoing maintenance and support.  This document serves as a checklist of handover materials and provides essential information for the support staff.  This is Stage 1 of the document generation.

## Handover Plan Purpose and Scope

This plan aims to ensure a smooth and efficient handover of the LSCP system, including all necessary documentation, source code, administration accounts, backups, hardware, and software licenses. The scope encompasses all components of the LSCP deployed in the Production, UAT, and DR environments, including both on-premise (WKGO) and GCIS infrastructure.

## System Overview

The LSCP facilitates site inspection and site monitoring record management for BD officers and public users.  The system architecture comprises a multi-tiered structure, with frontend web and mobile applications, backend application servers, database servers, and supporting infrastructure components like reverse proxies, load balancers, and firewalls.  The system is deployed across both on-premise and GCIS environments, with distinct configurations for Production, UAT, and DR.  Key system functionalities include user authentication (including iAM Smart integration), TCP assignments, form submissions, site project management, and data interfaces with external systems like MWMS and BCIS.

## Roles and Responsibilities

| Role                    | Responsibility                                                                                                                                |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Master Concept (MC)     | Deliver all handover materials as outlined in this plan, including documentation, source code, accounts, backups, and licensing information. |
| Buildings Department (BD) | Verify the completeness and accuracy of the handover materials, ensuring the system is operational and ready for ongoing support.              |
| BD Support Staff        | Assume responsibility for the maintenance, support, and ongoing operation of the LSCP system after the handover is complete.                |


## Knowledge Transfer Requirements

To ensure the BD support staff are adequately prepared to maintain the LSCP, the following knowledge transfer activities are required:

* **Documentation Review:** Thorough review of all provided documentation, including system manuals, operation manuals, and DR plans.
* **System Training:** Hands-on training sessions covering system administration, troubleshooting, and common operational procedures.
* **Code Walkthrough:**  Explanation of the application architecture, code structure, and key functionalities for both frontend and backend components.
* **Handover Meetings:**  Regular meetings between MC and BD to discuss outstanding issues, clarify requirements, and track progress.

## Project Closure Criteria

The handover will be considered complete when the following criteria are met:

* **All handover materials delivered and verified:** BD confirms receipt and accuracy of all documentation, source code, accounts, backups, etc.
* **Knowledge transfer complete:** BD support staff demonstrate sufficient understanding of the system and its operation.
* **System stability confirmed:**  The LSCP system operates as expected in all environments (Production, UAT, and DR) for a defined period.
* **Outstanding issues resolved:** All identified issues and bugs are addressed and closed.
* **Formal sign-off:**  Both MC and BD officially sign-off on the handover, acknowledging the successful completion of the transition.


```