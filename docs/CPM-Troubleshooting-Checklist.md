# CPM Troubleshooting Checklist

## Purpose

This document provides a troubleshooting checklist for Central Policy Manager related issues in the CyberArk PAM Operations Lab. The goal is to show how password management, password rotation, verification, and reconciliation issues can be reviewed and documented.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## What Is CPM?

CPM stands for Central Policy Manager. In a CyberArk PAM environment, CPM is commonly associated with password management, password verification, password change, and password reconciliation workflows.

CPM helps ensure privileged account passwords are managed according to policy.

## Why CPM Troubleshooting Matters

Password rotation and verification failures can create security and operational risk. If privileged account passwords are not managed correctly, accounts may become stale, unmanaged, locked, or unavailable during urgent support work.

CPM troubleshooting helps identify why password management tasks fail and what steps are needed to restore normal password management.

## Common CPM Issues

Common CPM-related issues include:

- Password change failure
- Password verification failure
- Password reconciliation failure
- Account locked
- Incorrect current password
- Target system unavailable
- Network connectivity issue
- Platform mismatch
- Account disabled
- Permission issue
- Password complexity conflict
- Service account dependency issue
- Incorrect address or account name
- Missing or incorrect policy settings

## Troubleshooting Workflow

A standard CPM troubleshooting workflow may include:

1. Identify the affected privileged account.
2. Confirm the safe name.
3. Confirm the target system or application.
4. Review the failed CPM action.
5. Confirm whether the issue is password change, verify, or reconcile.
6. Check whether the target system is reachable.
7. Confirm the privileged account is active and unlocked.
8. Confirm the correct platform or policy is assigned.
9. Confirm password complexity requirements.
10. Confirm the account has permission to change or verify the password.
11. Review recent changes to the account or target system.
12. Escalate to the system owner if needed.
13. Document the root cause and remediation.

## CPM Issue Matrix

| Issue | Possible Cause | Troubleshooting Action |
|---|---|---|
| Password change failed | Target system unavailable | Confirm system is online and reachable |
| Password verify failed | Stored password does not match target | Confirm account status and reconcile if appropriate |
| Password reconcile failed | Reconcile account permission issue | Confirm reconcile account permissions |
| Account locked | Too many failed attempts | Unlock account and review cause |
| Password complexity failure | New password does not meet target policy | Review target system password requirements |
| Platform mismatch | Wrong platform assigned | Confirm correct platform or policy |
| Account disabled | Account inactive on target system | Confirm account status with system owner |
| Network failure | Firewall, DNS, or routing issue | Confirm connectivity to target system |
| Service account issue | Password rotation may break service | Coordinate with application owner |

## Password Change Failure Checks

If password change fails, check:

- Is the target system online?
- Is the account active?
- Is the account locked?
- Is the current password correct?
- Is the correct platform assigned?
- Does the account have permission to change its password?
- Are password complexity rules being met?
- Are there network or firewall issues?
- Is the account tied to an application or service?
- Was there a recent system or policy change?

## Password Verification Failure Checks

If password verification fails, check:

- Does the stored password match the target system password?
- Was the password changed outside CyberArk?
- Is the account locked or disabled?
- Is the target system reachable?
- Is the account name correct?
- Is the system address correct?
- Is the correct platform assigned?
- Did someone manually reset the password?

## Password Reconciliation Failure Checks

If reconciliation fails, check:

- Is the reconcile account configured?
- Does the reconcile account have required permissions?
- Is the reconcile account active and unlocked?
- Is the target account active?
- Is the target system reachable?
- Are password rules being met?
- Was the account moved, renamed, or disabled?
- Does the reconcile account have rights on the target system?

## Service Account Rotation Checks

Service accounts require additional care. Before rotating a service account password, check:

1. Which application uses the account?
2. Who owns the application?
3. Are there dependent services?
4. Is there a maintenance window?
5. Is there a rollback plan?
6. Has the application owner approved the change?
7. Will password rotation break scheduled tasks or integrations?
8. Has the rotation been tied to a change ticket?

## Escalation Criteria

Escalate CPM issues when:

- Production account rotation fails
- Break-glass account management fails
- A service account rotation may impact an application
- The reconcile account lacks required permissions
- The target system is unavailable
- The account owner is unknown
- The account appears to be changed outside the PAM workflow
- Multiple accounts fail under the same platform or policy

## Documentation Requirements

Each CPM issue should document:

| Field | Description |
|---|---|
| Account Name | Affected privileged account |
| Safe Name | Safe where the account is stored |
| Target System | System or application tied to the account |
| Issue Type | Change, verify, reconcile, lockout, or other issue |
| Error Summary | Short description of the failure |
| Business Impact | Impact to users, systems, or operations |
| Root Cause | Cause of the issue |
| Resolution | Steps taken to fix the issue |
| Owner | Account or system owner |
| Ticket Number | Incident, change, or request reference |
| Evidence Saved | Yes or no |

## Example Troubleshooting Record

| Field | Example |
|---|---|
| Account Name | win-prod-localadmin |
| Safe Name | SAFE-WIN-PROD-ADMINS |
| Target System | PROD-WIN-SRV-01 |
| Issue Type | Password verification failure |
| Error Summary | Stored password did not match target system |
| Business Impact | Password checkout risk for production admin account |
| Root Cause | Password was changed outside PAM process |
| Resolution | Account password reconciled and verified |
| Owner | Windows Server Team |
| Ticket Number | INC-2026-00514 |
| Evidence Saved | Yes |

## Preventive Controls

To reduce CPM issues:

- Keep account ownership documented
- Use correct safe and platform assignments
- Avoid manual password changes outside PAM
- Review service account dependencies
- Test rotation for high-risk accounts
- Review failed rotation reports
- Keep reconcile accounts healthy
- Document password policy requirements
- Use change windows for service account rotations

## Summary

CPM troubleshooting is an important part of PAM operations. A structured troubleshooting process helps identify password management issues, reduce privileged account risk, support operational continuity, and retain audit evidence.
