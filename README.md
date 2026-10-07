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

![Completed access review](images/Screenshot%202026-10-02%20132641.png)

## Mover Scenario

Arman Patel was initially assigned to the Finance access package. When the user moved to an IT role, I completed the following process:

1. The user requested the IT access package.
2. A business justification was provided.
3. The request was approved.
4. Entra provisioned membership in the IT group.
5. The previous Finance assignment was removed.
6. IT group membership was verified.

This demonstrates role-based access changes while preventing unnecessary accumulation of permissions.

![Access packages](images/Screenshot%202026-10-05%20164410.png)

![Mover access request](images/Screenshot%202026-10-05%20165139.png)

![IT access delivered](images/Screenshot%202026-10-06%20113122.png)

![IT group membership](images/Screenshot%202026-10-06%20113901.png)

## Leaver Scenario

Benjamin Thompson was used to demonstrate the employee offboarding process.

The following actions were completed:

1. Removed the Finance access-package assignment
2. Verified removal from governed groups
3. Revoked active sign-in sessions
4. Disabled the Entra user account
5. Confirmed the user had no remaining group memberships

![Access before removal](images/Screenshot%202026-10-07%20120640.png)

![Active sessions revoked](images/Screenshot%202026-10-07%20122629.png)

![User account disabled](images/Screenshot%202026-10-07%20125106.png)

![No remaining group memberships](images/Screenshot%202026-10-07%20125154.png)

## Governance Controls Demonstrated

- Least-privilege access
- Self-service access requests
- Business justification
- Approval-based provisioning
- Time-limited assignments
- Periodic access certification
- Role-change access removal
- Session revocation
- Account deactivation
- Deprovisioning verification

## Key Takeaways

This lab provided practical experience managing identities throughout their lifecycle. It demonstrated that identity governance involves more than granting access—it also requires approval, periodic validation, timely removal, and verification that deprovisioning was successful.

## Security and Privacy

This repository contains sanitized documentation from a lab environment. No passwords, access tokens, secrets, or production data are included.
