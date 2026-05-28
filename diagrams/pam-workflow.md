# CyberArk PAM Workflow Diagram

## Purpose

This document provides a simple workflow diagram for the CyberArk PAM Operations Lab. The goal is to show how privileged access can move from request to approval, session use, password rotation, review, and audit evidence.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## High-Level PAM Workflow

```text
User / Admin
    |
    v
Privileged Access Request
    |
    v
Business Justification Provided
    |
    v
Approver Reviews Request
    |
    +-------------------------+
    |                         |
    v                         v
Approved                  Denied
    |                         |
    v                         v
Access Granted          Remediation / More Info
    |
    v
Privileged Session Launched
    |
    v
Session Monitored / Logged
    |
    v
Session Ends
    |
    v
Password Rotation / Verification
    |
    v
Audit Evidence Retained
    |
    v
Access Review / Ongoing Governance
```

## Privileged Account Onboarding Workflow

```text
Identify Privileged Account
    |
    v
Confirm Account Owner
    |
    v
Classify Account Risk
    |
    v
Select Correct Safe
    |
    v
Define Access Approvers
    |
    v
Define Rotation Requirements
    |
    v
Define Session Monitoring Requirements
    |
    v
Onboard Account Into PAM
    |
    v
Validate Access and Ownership
    |
    v
Save Audit Evidence
```

## Safe Design Workflow

```text
Identify Account Type
    |
    v
Identify Environment
    |
    v
Assign Owner Team
    |
    v
Assign Safe Name
    |
    v
Define Approval Requirement
    |
    v
Define Session Monitoring Requirement
    |
    v
Define Password Rotation Requirement
    |
    v
Define Review Frequency
    |
    v
Document Safe Design
```

## Access Request Workflow

```text
Requester Needs Privileged Access
    |
    v
Submit Access Request
    |
    v
Add Business Justification
    |
    v
Add Ticket or Change Reference
    |
    v
Approver Reviews Request
    |
    +------------------------------+
    |                              |
    v                              v
Approve                       Deny / Request Info
    |                              |
    v                              v
Time-Limited Access Granted   Document Decision
    |
    v
Launch Privileged Session
    |
    v
Monitor Session If Required
    |
    v
Save Evidence
```

## Password Rotation Workflow

```text
Rotation Trigger Occurs
    |
    v
Identify Privileged Account
    |
    v
Confirm Account Owner
    |
    v
Confirm Rotation Risk
    |
    v
Rotate Password
    |
    v
Validate Account Works
    |
    +------------------------------+
    |                              |
    v                              v
Successful                    Failed
    |                              |
    v                              v
Save Evidence                 Troubleshoot / Escalate
                                   |
                                   v
                               Document Resolution
```

## PSM Session Monitoring Workflow

```text
Access Request Approved
    |
    v
User Launches Privileged Session
    |
    v
Session Routes Through Controlled Workflow
    |
    v
Session Metadata Captured
    |
    v
Session Activity Monitored or Recorded
    |
    v
Session Ends
    |
    v
Session Reviewed If Needed
    |
    v
Evidence Retained
```

## Break-Glass Workflow

```text
Emergency Occurs
    |
    v
Normal Access Unavailable
    |
    v
Break-Glass Access Requested
    |
    v
Emergency Reason Documented
    |
    v
Approval Obtained If Possible
    |
    v
Break-Glass Account Used
    |
    v
Emergency Resolved
    |
    v
Password Rotated After Use
    |
    v
Post-Use Review Completed
    |
    v
Audit Evidence Saved
```

## Audit Evidence Workflow

```text
Access Request
    |
    v
Approval Decision
    |
    v
Session Record
    |
    v
Password Rotation Record
    |
    v
Troubleshooting Notes If Needed
    |
    v
Access Review Decision
    |
    v
Evidence Packet
    |
    v
Audit / Compliance Review
```

## Summary

This workflow diagram shows how CyberArk PAM operations can support privileged access control, safe design, access approvals, password rotation, session monitoring, break-glass handling, and audit evidence collection.
