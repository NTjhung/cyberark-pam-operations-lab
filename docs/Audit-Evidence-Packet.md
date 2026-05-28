# Audit Evidence Packet

## Purpose

This document defines an audit evidence packet for the CyberArk PAM Operations Lab. The goal is to show what evidence should be retained to prove that privileged access is controlled, approved, monitored, reviewed, and remediated.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## Why Audit Evidence Matters

Privileged access creates high security and compliance risk. Auditors, security teams, and IAM teams may need to prove that privileged access is being managed properly.

Audit evidence helps answer questions such as:

- Who has privileged access?
- Who approved privileged access?
- Why was privileged access needed?
- When was privileged access used?
- Was the session monitored?
- Was the password rotated?
- Was access reviewed?
- Were exceptions documented?
- Were issues remediated?

## Evidence Categories

A complete PAM audit evidence packet may include:

| Evidence Category | Purpose |
|---|---|
| Safe design documentation | Shows how privileged accounts are organized |
| Privileged account inventory | Shows what accounts are managed |
| Access request records | Shows why access was requested |
| Approval records | Shows who approved access |
| Session records | Shows privileged access activity |
| Password rotation records | Shows credential management |
| Break-glass records | Shows emergency access usage |
| Access review records | Shows ongoing access validation |
| Troubleshooting records | Shows operational issues and remediation |
| Exception records | Shows approved deviations from policy |

## Safe Evidence

Safe evidence should document:

- Safe name
- Safe purpose
- Owner team
- Account types stored in the safe
- Environment
- Approval requirements
- Review frequency
- User or group access
- Auditor access
- Risk level

Example safe evidence:

| Safe Name | Owner Team | Account Type | Environment | Review Frequency |
|---|---|---|---|---|
| SAFE-WIN-PROD-ADMINS | Windows Server Team | Windows local admin | Production | Monthly |
| SAFE-LINUX-PROD-ROOT | Linux Team | Linux root/admin | Production | Monthly |
| SAFE-BREAKGLASS | IAM/Security Team | Emergency admin | Production | Monthly |

## Privileged Account Inventory Evidence

Privileged account inventory evidence should document:

- Account name
- Account type
- Owner team
- System or application
- Safe name
- Environment
- Approval requirement
- Rotation requirement
- Review frequency
- Risk level

Example account evidence:

| Account Name | Safe Name | Owner Team | Risk Level | Rotation Required |
|---|---|---|---|---|
| win-prod-localadmin | SAFE-WIN-PROD-ADMINS | Windows Server Team | High | Yes |
| sql-prod-dba | SAFE-DBA-PROD | Database Team | High | Yes |
| breakglass-admin01 | SAFE-BREAKGLASS | IAM/Security Team | Critical | Yes |

## Access Request Evidence

Access request evidence should include:

- Requester
- Privileged account requested
- Safe name
- Target system
- Business justification
- Requested duration
- Approver
- Approval decision
- Ticket or change number
- Date and time of request

Example access request evidence:

| Field | Example |
|---|---|
| Requester | Carlos Ramirez |
| Account Requested | win-prod-localadmin |
| Safe Name | SAFE-WIN-PROD-ADMINS |
| Business Justification | Troubleshoot production service outage |
| Requested Duration | 2 hours |
| Approver | Windows Server Team Lead |
| Ticket Number | INC-2026-00421 |
| Decision | Approved |

## Approval Evidence

Approval evidence should show:

- Who approved the request
- When approval occurred
- What access was approved
- Why access was approved
- Whether the duration was appropriate
- Whether any conditions were added

Example approval review questions:

1. Was the approver authorized?
2. Was the business justification valid?
3. Was the access time-limited?
4. Was the request tied to a ticket?
5. Was the correct account selected?
6. Was monitoring required?

## Session Monitoring Evidence

Session monitoring evidence should include:

- User
- Privileged account
- Safe name
- Target system
- Session start time
- Session end time
- Duration
- Approval reference
- Ticket number
- Review notes

Example session evidence:

| User | Account | Target System | Duration | Ticket |
|---|---|---|---|---|
| Carlos Ramirez | win-prod-localadmin | PROD-WIN-SRV-01 | 42 minutes | INC-2026-00421 |

## Password Rotation Evidence

Password rotation evidence should include:

- Account name
- Safe name
- Rotation date
- Rotation trigger
- Rotation result
- Validation result
- Approver or owner
- Ticket number
- Failure reason, if applicable
- Remediation notes

Example rotation evidence:

| Account | Rotation Trigger | Result | Validation |
|---|---|---|---|
| win-prod-localadmin | Scheduled rotation | Successful | Login tested successfully |
| breakglass-admin01 | Post-emergency use | Successful | Custodian confirmed |

## Break-Glass Evidence

Break-glass evidence should include:

- Account used
- Emergency reason
- Requester
- Approver
- Start time
- End time
- Ticket number
- Password rotation status
- Post-use review notes
- Remediation actions

Example break-glass evidence:

| Field | Example |
|---|---|
| Account Used | breakglass-admin01 |
| Reason | Emergency tenant recovery |
| Ticket Number | INC-2026-00721 |
| Password Rotated After Use | Yes |
| Post-Use Review Completed | Yes |

## Troubleshooting Evidence

Troubleshooting evidence should include:

- Affected account
- Safe name
- Target system
- Issue type
- Business impact
- Root cause
- Resolution
- Ticket number
- Evidence saved

Example troubleshooting evidence:

| Issue | Root Cause | Resolution |
|---|---|---|
| CPM verification failed | Password changed outside PAM | Account reconciled and verified |
| PSM session failed | User missing safe permission | Correct group permission added |

## Access Review Evidence

Access review evidence should show:

- Reviewed safe or group
- Reviewer
- Review date
- Users reviewed
- Decisions
- Access removed
- Exceptions
- Remediation status

Example access review evidence:

| User | Safe | Decision | Action |
|---|---|---|---|
| Dana Smith | SAFE-WIN-PROD-ADMINS | Remove | Access no longer required |
| Carlos Ramirez | SAFE-WIN-PROD-ADMINS | Approve | Access still required |

## Exception Evidence

Exceptions should be documented when normal policy cannot be followed.

Exception evidence should include:

- Exception type
- Business reason
- Risk accepted
- Approver
- Expiration date
- Compensating controls
- Review date

Examples of exceptions:

- Service account cannot rotate automatically
- Emergency access granted without standard approval
- Vendor access extended temporarily
- Account requires longer session duration

## Audit Questions

An auditor may ask:

1. Are privileged accounts inventoried?
2. Are privileged accounts assigned to safes?
3. Are safe owners documented?
4. Are access requests approved?
5. Are privileged sessions monitored?
6. Are passwords rotated?
7. Are break-glass accounts reviewed?
8. Are exceptions documented?
9. Are failed rotations investigated?
10. Are access reviews completed regularly?

## Evidence Retention Notes

PAM evidence should be retained according to the organization’s retention policy. Evidence should be protected because it may contain sensitive account, access, and infrastructure information.

Evidence should only be shared with authorized users.

## Summary

A strong audit evidence packet helps prove that privileged access is controlled, monitored, reviewed, and remediated. This supports least privilege, compliance, security operations, and privileged access governance.
