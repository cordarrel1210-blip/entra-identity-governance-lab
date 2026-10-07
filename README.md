# Microsoft Entra Identity Governance Lab

## Overview

This hands-on Identity Governance and Administration (IGA) lab demonstrates how Microsoft Entra ID can govern access throughout the user lifecycle.

I configured entitlement management, access packages, approval workflows, assignment expiration, access reviews, and Joiner–Mover–Leaver processes.

## Objectives

- Create an identity governance catalog
- Govern Finance and IT security groups
- Create departmental access packages
- Require business justification and approval
- Configure time-limited access
- Perform access reviews
- Demonstrate Joiner, Mover, and Leaver scenarios
- Verify access provisioning and removal

## Technologies Used

- Microsoft Entra ID
- Entra Entitlement Management
- Entra Access Reviews
- Microsoft My Access
- Entra security groups

## Lab Resources

| Resource | Purpose |
|---|---|
| Finance Access Catalog | Contains governed Finance resources |
| Finance-Application-Users | Provides Finance group membership |
| IT Application Access | Provides IT group membership |
| Finance-Application-Users group | Represents access to Finance resources |
| IT-Application-User group | Represents access to IT resources |

## Joiner Scenario

Amanda Welch requested access to the Finance application through Microsoft My Access.

The access package required business justification and approval before granting time-limited access. After approval, Entra Entitlement Management automatically provisioned the user into the Finance group.

## Access Review

I configured an access review for the Finance access package with:

- Weekly review frequency
- Three-day review duration
- Reviewer justification
- Email reminders
- Automatic removal following reviewer nonresponse

The assignment was reviewed and approved, demonstrating periodic access recertification.

![Completed access review](images/Screenshot%202026-10-
