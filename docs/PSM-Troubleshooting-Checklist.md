# PSM Troubleshooting Checklist

## Purpose

This document provides a troubleshooting checklist for Privileged Session Manager related issues in the CyberArk PAM Operations Lab. The goal is to show how privileged session access, session launch failures, connection problems, and monitoring issues can be reviewed and documented.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## What Is PSM?

PSM stands for Privileged Session Manager. In a CyberArk PAM environment, PSM is commonly associated with privileged session isolation, controlled access, session monitoring, and session recording workflows.

PSM helps users connect to privileged systems without directly exposing credentials.

## Why PSM Troubleshooting Matters

Privileged session issues can prevent administrators, vendors, and support teams from accessing systems they need to manage. They can also affect audit visibility if session monitoring or recording does not work as expected.

PSM troubleshooting helps ensure privileged sessions are:

- Launched correctly
- Routed through the approved workflow
- Monitored when required
- Logged for audit review
- Connected to the correct target system
- Available during support or emergency work

## Common PSM Issues

Common PSM-related issues include:

- User cannot launch a session
- Connection fails
- Target system is unavailable
- Incorrect target address
- Incorrect account selected
- User lacks permission to use the account
- Safe permissions are missing
- Session recording not available
- Session disconnects unexpectedly
- Authentication failure
- Network or firewall issue
- RDP, SSH, or connection component issue
- Account locked or disabled
- Policy or platform mismatch

## Troubleshooting Workflow

A standard PSM troubleshooting workflow may include:

1. Identify the user reporting the issue.
2. Identify the privileged account being used.
3. Identify the safe name.
4. Identify the target system.
5. Confirm the user has permission to access the safe or account.
6. Confirm the account is active and not locked.
7. Confirm the target system is online.
8. Confirm the correct connection method is being used.
9. Confirm the target address is correct.
10. Confirm network connectivity.
11. Confirm whether the issue affects one user or multiple users.
12. Confirm whether the issue affects one account or multiple accounts.
13. Review recent changes to the target system, account, safe, or policy.
14. Document the root cause and resolution.

## PSM Issue Matrix

| Issue | Possible Cause | Troubleshooting Action |
|---|---|---|
| Session will not launch | User lacks safe permission | Confirm user or group has correct access |
| Session fails to connect | Target system offline | Confirm system is online and reachable |
| Authentication failure | Password mismatch or account issue | Verify account status and password management |
| Session disconnects | Network instability | Check network, firewall, or target system logs |
| Recording missing | Session monitoring not configured or unavailable | Confirm recording/monitoring settings |
| Wrong target opens | Incorrect address or account metadata | Validate target system details |
| Access denied | User not authorized for account | Review safe permissions and access workflow |
| Account locked | Failed login attempts | Unlock account and review cause |
| RDP/SSH issue | Connection component problem | Validate protocol and target settings |

## User Permission Checks

If a user cannot launch a PSM session, check:

- Is the user assigned to the correct safe?
- Does the user have permission to use the privileged account?
- Is the user in the correct group?
- Is approval required before use?
- Has the request been approved?
- Is the request within the approved time window?
- Is the account restricted to certain users or groups?
- Does the user have the required role for access?

## Account Checks

If the session fails because of account issues, check:

- Is the privileged account active?
- Is the account locked?
- Is the account disabled?
- Is the password current?
- Was the password changed outside PAM?
- Does the account have rights on the target system?
- Is the account assigned to the correct safe?
- Is the account assigned to the correct platform or policy?

## Target System Checks

If the connection fails, check:

- Is the target system online?
- Is the target system reachable from the network?
- Is the target address correct?
- Is DNS resolving correctly?
- Is the correct port open?
- Is RDP, SSH, or the required protocol enabled?
- Is the target system accepting connections?
- Were there recent firewall or network changes?

## Session Monitoring Checks

If session monitoring or recording is not working, check:

- Is session monitoring expected for this account?
- Is the account in a safe that requires monitoring?
- Is the correct connection workflow being used?
- Was the session launched through PSM?
- Is the issue affecting all sessions or only one session?
- Is the session record available after the session ends?
- Are audit logs available for the session?

## Common Escalation Scenarios

Escalate PSM issues when:

- Production access is blocked during an incident
- Multiple users cannot launch sessions
- Multiple accounts fail under the same connection type
- Break-glass access is affected
- Vendor access is blocked during an approved maintenance window
- Session recording is missing for high-risk privileged access
- Authentication failures suggest a password mismatch or account compromise
- Network or firewall changes may be blocking privileged access

## Documentation Requirements

Each PSM issue should document:

| Field | Description |
|---|---|
| User | User who reported the issue |
| Account Name | Privileged account being used |
| Safe Name | Safe where the account is stored |
| Target System | System, server, database, network device, or application |
| Connection Type | RDP, SSH, web, database, or other connection type |
| Issue Type | Launch failure, authentication failure, disconnect, recording issue, or other issue |
| Business Impact | Impact to users, systems, or operations |
| Root Cause | Cause of the issue |
| Resolution | Steps taken to fix the issue |
| Ticket Number | Incident, change, or request reference |
| Evidence Saved | Yes or no |

## Example Troubleshooting Record

| Field | Example |
|---|---|
| User | Carlos Ramirez |
| Account Name | win-prod-localadmin |
| Safe Name | SAFE-WIN-PROD-ADMINS |
| Target System | PROD-WIN-SRV-01 |
| Connection Type | RDP |
| Issue Type | Session launch failure |
| Business Impact | Admin unable to troubleshoot production server |
| Root Cause | User was missing safe access permission |
| Resolution | Correct group permission was added and session was retested |
| Ticket Number | INC-2026-00618 |
| Evidence Saved | Yes |

## Preventive Controls

To reduce PSM issues:

- Keep safe permissions reviewed and documented
- Validate target system information during onboarding
- Keep account ownership current
- Confirm session monitoring requirements during onboarding
- Test high-risk privileged access workflows
- Review failed session reports
- Document approved access workflows
- Review vendor and contractor access regularly
- Confirm break-glass session procedures are documented

## Summary

PSM troubleshooting is an important part of PAM operations. A structured troubleshooting process helps restore privileged access, support audit evidence, improve session monitoring reliability, and reduce risk from unmanaged privileged sessions.
