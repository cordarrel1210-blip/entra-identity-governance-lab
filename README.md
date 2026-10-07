# Microsoft Entra Identity Governance Lab

## Overview

This hands-on Identity Governance and Administration (IGA) lab demonstrates how Microsoft Entra ID can govern access throughout the user lifecycle.

I configured entitlement management, access packages, approval workflows, time-limited assignments, access reviews, and Joiner–Mover–Leaver processes. The lab shows how organizations can provide appropriate access, periodically review it, and remove it when it is no longer required.

## Objectives

- Create an identity governance catalog
- Add Finance and IT security groups as governed resources
- Create access packages for departmental access
- Require business justification and manager approval
- Configure assignment expiration
- Perform an access review
- Demonstrate Joiner, Mover, and Leaver scenarios
- Verify access provisioning and removal
- Revoke user sessions and disable a departed user

## Technologies Used

- Microsoft Entra ID
- Microsoft Entra Entitlement Management
- Microsoft Entra Access Reviews
- Microsoft My Access portal
- Entra security groups

## Lab Resources

| Resource | Purpose |
|---|---|
| Finance Access Catalog | Contains governed Finance resources and access packages |
| Finance-Application-Users | Provides membership in the Finance application group |
| IT Application Access | Provides membership in the IT application group |
| Finance-Application-Users group | Represents access to Finance resources |
| IT-Application-User group | Represents access to IT resources |

## Joiner Scenario

A new user, Amanda Welch, requested access to the Finance application through the My Access portal.

The access package required:

- Business justification
- Approval before access was granted
- A limited assignment period
- Periodic access review

After approval, Entra Entitlement Management automatically provisioned the user into the Finance group.

## Access Review

I configured an access review for the Finance access package with the following controls:

- Weekly review frequency
- Three-day review duration
- Reviewer justification
- Email reminders
- Automatic removal when reviewers do not respond

The assignment was reviewed and approved, demonstrating periodic access recertification.

![Completed access review](images/03-access-review-approved.png)

## Mover Scenario

Arman Patel was initially assigned to the Finance access package. When the user moved to an IT role, the following lifecycle process was completed:

1. The user requested the IT access package.
2. A business justification was provided.
3. The request was approved.
4. Entra provisioned membership in the IT group.
5. The previous Finance assignment was removed.
6. IT group membership was verified.

This demonstrates role-based access changes while preventing unnecessary accumulation of permissions.

![Access packages](images/02-access-packages.png)

![Mover request](images/04-mover-request.png)

![IT access delivered](images/05-mover-access-delivered.png)

![IT group membership](images/06-it-group-membership.png)

## Leaver Scenario

Benjamin Thompson was used to demonstrate the offboarding process.

The user was first assigned Finance access so the removal process could be tested. The following offboarding actions were then completed:

1. Removed the Finance access-package assignment
2. Verified removal from governed groups
3. Revoked active sign-in sessions
4. Disabled the Entra user account
5. Confirmed that the user had no remaining group memberships

These controls help prevent former users from retaining access to organizational resources.

![Leaver assignment before removal](images/07-leaver-assignment.png)

![Sessions revoked](images/08-sessions-revoked.png)

![Account disabled](images/09-account-disabled.png)

![No remaining groups](images/10-no-group-memberships.png)

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
- Verification of deprovisioning

## Key Takeaways

This lab provided practical experience managing identities across their lifecycle. It demonstrated that identity governance involves more than granting access—it also requires approval, periodic validation, timely removal, and verification that deprovisioning was successful.

## Security and Privacy

This repository contains sanitized documentation from a lab environment. Tenant identifiers, user principal names, object IDs, and other environment-specific information should be redacted. No passwords, access tokens, secrets, or production data are included.
