# Access Request Workflow

## Purpose

This document defines a privileged access request workflow for the CyberArk PAM Operations Lab. The goal is to show how privileged access can be requested, approved, used, monitored, and documented.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## Why Access Requests Matter

Privileged access should not be granted casually or permanently without a business need. A structured access request workflow helps ensure that privileged access is:

- Requested for a valid reason
- Reviewed by the correct approver
- Limited to the correct account or safe
- Time-bound when possible
- Monitored when needed
- Documented for audit evidence

## Access Request Workflow

A standard privileged access request workflow may include:

1. User identifies the need for privileged access.
2. User submits an access request.
3. Request includes business justification.
4. Approver reviews the request.
5. Approver approves or denies access.
6. User accesses the privileged account through the approved workflow.
7. Privileged session is monitored or logged if required.
8. Password is rotated based on policy or after use.
9. Access activity is retained as audit evidence.
10. Access is reviewed during the next access review cycle.

## Access Request Fields

Each privileged access request should include:

| Field | Description |
|---|---|
| Requester | User requesting privileged access |
| Account Requested | Privileged account being requested |
| Safe Name | Safe where the privileged account is stored |
| System/Application | Target system or application |
| Business Justification | Reason access is needed |
| Requested Duration | How long access is needed |
| Approver | Person or team responsible for approving access |
| Risk Level | Low, medium, high, or critical |
| Session Monitoring Required | Whether the session should be monitored |
| Ticket Number | Change, incident, or service request reference |
| Decision | Approved, denied, or needs more information |

## Example Request

| Field | Example |
|---|---|
| Requester | Carlos Ramirez |
| Account Requested | win-prod-localadmin |
| Safe Name | SAFE-WIN-PROD-ADMINS |
| System/Application | PROD-WIN-SRV-01 |
| Business Justification | Need temporary admin access to troubleshoot production service outage |
| Requested Duration | 2 hours |
| Approver | Windows Server Team Lead |
| Risk Level | High |
| Session Monitoring Required | Yes |
| Ticket Number | INC-2026-00421 |
| Decision | Approved |

## Approval Criteria

Approvers should review:

1. Is the requester authorized to use this account?
2. Is there a valid business reason?
3. Is the requested duration reasonable?
4. Is the request tied to a ticket or change record?
5. Is the correct safe being used?
6. Is session monitoring required?
7. Is password rotation required after use?
8. Is this production, non-production, or emergency access?

## Approval Decision Options

| Decision | Meaning |
|---|---|
| Approve | Access is allowed for the requested purpose |
| Deny | Access is not allowed |
| Request More Information | More details are needed before deciding |
| Escalate | Request needs review by a higher-level approver |

## Example Approval Outcomes

| Request | Decision | Reason |
|---|---|---|
| Production server admin access for outage troubleshooting | Approve | Valid incident ticket and production support need |
| Break-glass account access for routine maintenance | Deny | Break-glass accounts should not be used for normal work |
| Service account password retrieval with no ticket | Request More Information | Missing business justification and ticket |
| Network admin access for firewall change | Approve | Approved change ticket exists |

## Access Duration Guidance

Privileged access should be limited to the minimum time required.

| Access Type | Suggested Duration |
|---|---|
| Emergency production troubleshooting | 1 to 4 hours |
| Approved maintenance window | Length of maintenance window |
| Non-production support | Same business day |
| Break-glass access | Emergency only |
| Contractor privileged access | Time-limited and reviewed frequently |

## Session Monitoring Guidance

Session monitoring should be considered for:

- Production administrator access
- Break-glass access
- Database administrator access
- Network device access
- Vendor or contractor privileged access
- Sensitive application administration

Session monitoring supports audit readiness and helps investigate privileged activity.

## Password Rotation Guidance

Password rotation should be considered:

- After privileged account use
- After emergency access
- After contractor access
- On a scheduled rotation cycle
- After a suspected compromise
- When an account owner changes
- After an employee with privileged access leaves

## Access Request Risks

Common risks include:

- Access approved without business justification
- Access granted for too long
- No ticket or change record
- Wrong safe or account selected
- Session monitoring not enabled for high-risk access
- Password not rotated after use
- Contractor access not removed after project completion
- Break-glass account used for routine work

## Audit Evidence

Evidence that should be retained:

- Access request record
- Business justification
- Approval or denial decision
- Approver name or team
- Access duration
- Ticket or change number
- Session monitoring record, if applicable
- Password rotation record, if applicable
- Remediation notes, if access was denied or corrected

## Summary

A strong privileged access request workflow helps enforce least privilege, reduce standing access, support approvals, document business need, and provide audit evidence for privileged account use.
