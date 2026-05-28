# PAM Overview

## Purpose

This document provides a high-level overview of Privileged Access Management concepts used in this CyberArk PAM Operations Lab.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment. Instead, this project uses original documentation, sanitized examples, sample data, and workflow notes.

## What Is Privileged Access Management?

Privileged Access Management, or PAM, is the process of controlling, securing, monitoring, and auditing accounts that have elevated access.

Privileged accounts may include:

- Local administrator accounts
- Domain administrator accounts
- Service accounts
- Application administrator accounts
- Database administrator accounts
- Cloud administrator accounts
- Network device administrator accounts
- Emergency access accounts

These accounts are higher risk because they can make major changes to systems, applications, infrastructure, and data.

## Why PAM Matters

Without a PAM process, privileged accounts may become risky because they can be:

- Shared by multiple users
- Poorly documented
- Not rotated regularly
- Used without approval
- Difficult to audit
- Left active after a project ends
- Exposed during troubleshooting
- Used outside normal access request processes

PAM helps reduce risk by placing privileged accounts under stronger controls.

## CyberArk PAM Concepts Covered

This lab focuses on the following CyberArk PAM concepts:

| Concept | Description |
|---|---|
| Safes | Logical containers used to store and manage privileged accounts |
| Privileged Accounts | Accounts with elevated access to systems or applications |
| Password Rotation | Process of changing privileged account passwords based on policy |
| Access Request | Process users follow to request privileged access |
| Approval Workflow | Review and approval process before privileged access is granted |
| CPM | Component commonly associated with password management and rotation |
| PSM | Component commonly associated with privileged session isolation and monitoring |
| Break-Glass Access | Emergency access used when normal access workflows are unavailable |
| Audit Evidence | Records that show privileged access was requested, approved, used, reviewed, and monitored |

## Example PAM Workflow

A basic PAM workflow may look like this:

1. Identify a privileged account.
2. Assign the account to the correct safe.
3. Define who can request or approve access.
4. Configure password management expectations.
5. Require approval for sensitive access.
6. Launch privileged sessions through a controlled workflow.
7. Monitor or review session activity.
8. Rotate passwords based on policy.
9. Retain audit evidence.
10. Review access on a regular schedule.

## Example Use Case

A systems administrator needs temporary access to a privileged local administrator account on a production server.

A PAM workflow could require:

1. The administrator submits an access request.
2. The request is reviewed by an approver.
3. Access is granted for a limited time.
4. The session is launched through a monitored workflow.
5. Activity is logged.
6. The privileged password is rotated after use.
7. Evidence is retained for audit review.

## Security Goals

The security goals of this PAM lab are to demonstrate how an organization can:

- Reduce standing privileged access
- Control who can access privileged accounts
- Require approvals for sensitive access
- Rotate privileged account passwords
- Monitor privileged sessions
- Document privileged access activity
- Support audit and compliance requirements
- Improve least privilege enforcement

## Lab Scope

This project does not include CyberArk screenshots because screenshots were not permitted.

Instead, the project includes:

- PAM overview documentation
- Safe design matrix
- Privileged account onboarding runbook
- Access request workflow
- Password rotation plan
- PSM session monitoring workflow
- CPM troubleshooting checklist
- PSM troubleshooting checklist
- Break-glass plan
- Audit evidence packet
- Sample privileged account inventory
- Sample safe design matrix
- Sample password rotation schedule
- Workflow diagram

## Summary

Privileged Access Management is a critical IAM and security control. This project demonstrates CyberArk PAM operational understanding through original documentation, sample data, runbooks, and workflow planning based on hands-on CyberArk access.
