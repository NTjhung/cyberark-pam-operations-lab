# Password Rotation Plan

## Purpose

This document defines a password rotation plan for the CyberArk PAM Operations Lab. The goal is to show how privileged account passwords can be rotated, monitored, documented, and reviewed.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## Why Password Rotation Matters

Privileged account passwords create high risk if they are shared, reused, exposed, or not changed regularly. Password rotation helps reduce the risk of credential misuse by changing passwords based on policy, after use, or after security events.

Password rotation supports:

- Credential security
- Least privilege
- Audit readiness
- Incident response
- Reduced shared account risk
- Stronger privileged access controls

## Password Rotation Goals

The goals of this password rotation plan are to:

1. Reduce risk from shared privileged passwords.
2. Ensure privileged account passwords are changed on a defined schedule.
3. Rotate passwords after high-risk use.
4. Document service account rotation concerns.
5. Support audit evidence collection.
6. Reduce the chance of stale or unmanaged privileged credentials.

## Rotation Schedule

| Account Type | Environment | Suggested Rotation Frequency | Rotation Risk |
|---|---|---|---|
| Windows local admin | Production | Every 30 days or after use | Medium |
| Windows local admin | Non-production | Every 60 to 90 days | Low |
| Linux root/admin | Production | Every 30 days or after use | Medium |
| Database admin | Production | Every 30 days or after use | High |
| Network device admin | Production | Every 30 days or after use | High |
| Break-glass account | Production | After use and during scheduled review | Critical |
| Service account | Production | Planned rotation window | High |
| Application admin | Production | Every 30 to 60 days | Medium |

## Rotation Triggers

Password rotation should occur when:

- A privileged account is used for emergency access
- A privileged session ends
- A contractor no longer needs access
- A privileged user leaves the organization
- A password may have been exposed
- A security incident occurs
- A scheduled rotation cycle is reached
- Account ownership changes
- An audit finding requires remediation

## Service Account Rotation Considerations

Service accounts require extra planning because password changes may affect applications, scheduled tasks, integrations, or services.

Before rotating a service account password, confirm:

1. What application or service uses the account?
2. Who owns the application?
3. Is there a maintenance window?
4. Are there dependent systems?
5. Is there a rollback plan?
6. Has the new password been tested?
7. Are application owners available during the change?
8. Is the rotation documented in a ticket?

## Rotation Approval Matrix

| Account Type | Approval Required | Approver |
|---|---|---|
| Production local admin | Yes | System owner or support team lead |
| Database admin | Yes | Database owner or DBA lead |
| Network admin | Yes | Network team lead |
| Break-glass account | Yes | IAM/Security manager |
| Service account | Yes | Application owner |
| Non-production local admin | Optional | Support team lead |

## Password Rotation Workflow

A standard password rotation workflow may include:

1. Identify the account requiring rotation.
2. Confirm account owner and safe.
3. Confirm whether the account is interactive or service-based.
4. Confirm rotation schedule or trigger.
5. Confirm approval if required.
6. Open or reference a ticket.
7. Rotate the password according to policy.
8. Validate the account still works.
9. Confirm dependent services are not broken.
10. Document the rotation result.
11. Save evidence for audit.

## Example Rotation Record

| Field | Example |
|---|---|
| Account Name | win-prod-localadmin |
| Safe Name | SAFE-WIN-PROD-ADMINS |
| System | PROD-WIN-SRV-01 |
| Rotation Trigger | Scheduled 30-day rotation |
| Approval Required | Yes |
| Approver | Windows Server Team Lead |
| Ticket Number | CHG-2026-00214 |
| Rotation Result | Successful |
| Validation Result | Login tested successfully |
| Evidence Saved | Yes |

## Failed Rotation Handling

If password rotation fails, the issue should be documented and escalated.

Common failed rotation causes include:

- Incorrect current password
- Account locked
- Target system unavailable
- Network connectivity issue
- Permission issue
- Platform mismatch
- Service account dependency
- Password complexity conflict
- Account disabled
- Incorrect system address

## Failed Rotation Troubleshooting Steps

1. Confirm the target system is online.
2. Confirm the account is active.
3. Confirm the account is not locked.
4. Confirm the correct platform or policy is assigned.
5. Confirm password complexity requirements.
6. Confirm network connectivity.
7. Confirm permissions required to change the password.
8. Review recent account changes.
9. Escalate to the account owner if needed.
10. Document the root cause and resolution.

## Break-Glass Rotation

Break-glass account passwords should be treated as critical.

Break-glass passwords should be rotated:

- After any use
- After a suspected exposure
- After emergency testing
- During scheduled security reviews
- When an authorized custodian leaves
- When required by policy

Break-glass rotation should always be documented.

## Audit Evidence

The following evidence should be retained:

- Rotation date and time
- Account name
- Safe name
- System or application
- Rotation trigger
- Approver
- Ticket or change number
- Rotation result
- Validation result
- Failure reason, if applicable
- Remediation notes

## Risk Notes

Password rotation risk increases when:

- The account is used by an application
- Ownership is unclear
- No maintenance window exists
- Password dependencies are undocumented
- Password complexity requirements are unknown
- The account is used by multiple systems
- There is no rollback plan

## Summary

Password rotation is a core PAM control. A strong rotation plan helps reduce credential risk, support least privilege, improve audit readiness, and ensure privileged accounts are managed in a controlled and documented way.
