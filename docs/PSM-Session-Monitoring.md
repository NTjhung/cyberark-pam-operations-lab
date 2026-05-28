# PSM Session Monitoring

## Purpose

This document defines a Privileged Session Monitoring workflow for the CyberArk PAM Operations Lab. The goal is to show how privileged sessions can be controlled, monitored, reviewed, and documented for audit purposes.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## What Is PSM?

PSM stands for Privileged Session Manager. In a CyberArk PAM environment, PSM is commonly associated with secure privileged session access, session isolation, session monitoring, and session recording workflows.

PSM helps organizations reduce privileged access risk by allowing users to access privileged systems through a controlled and monitored session instead of directly exposing credentials.

## Why Session Monitoring Matters

Privileged sessions are high risk because users with elevated access can make major changes to systems, applications, databases, and infrastructure.

Session monitoring helps with:

- Audit readiness
- Incident investigation
- Privileged activity review
- Insider threat reduction
- Vendor access monitoring
- Contractor access monitoring
- Change validation
- Evidence collection

## Session Monitoring Goals

The goals of privileged session monitoring are to:

1. Track who used privileged access.
2. Track what system or account was accessed.
3. Confirm whether access was approved.
4. Monitor privileged activity.
5. Support audit and compliance requirements.
6. Investigate suspicious or unexpected activity.
7. Provide evidence for access reviews.

## Example Session Monitoring Workflow

A standard PSM session monitoring workflow may include:

1. User requests privileged access.
2. Access request is approved.
3. User launches the privileged session through the PAM platform.
4. Session is isolated through a controlled access path.
5. Session metadata is logged.
6. Session activity is monitored or recorded if required.
7. Session ends.
8. Password rotation occurs if required.
9. Session record is retained as audit evidence.
10. Activity is reviewed if needed.

## Session Metadata to Capture

Privileged session records should capture:

| Field | Description |
|---|---|
| User | Person who launched the session |
| Privileged Account | Account used for the privileged session |
| Safe Name | Safe where the privileged account is stored |
| Target System | Server, database, network device, or application accessed |
| Session Start Time | When the session started |
| Session End Time | When the session ended |
| Duration | Length of privileged session |
| Ticket Number | Incident, change, or request reference |
| Approval Status | Whether access was approved |
| Session Status | Completed, failed, terminated, or reviewed |
| Review Notes | Notes from audit or security review |

## Example Session Record

| Field | Example |
|---|---|
| User | Carlos Ramirez |
| Privileged Account | win-prod-localadmin |
| Safe Name | SAFE-WIN-PROD-ADMINS |
| Target System | PROD-WIN-SRV-01 |
| Session Start Time | 2026-05-28 10:00 AM |
| Session End Time | 2026-05-28 10:42 AM |
| Duration | 42 minutes |
| Ticket Number | INC-2026-00421 |
| Approval Status | Approved |
| Session Status | Completed |
| Review Notes | Session aligned with approved troubleshooting request |

## Sessions That Should Be Monitored Closely

The following sessions should receive stronger monitoring:

- Production server administration
- Database administration
- Network device administration
- Break-glass account usage
- Vendor privileged access
- Contractor privileged access
- Domain administrator access
- Cloud administrator access
- Sensitive application administration

## Session Review Questions

When reviewing privileged sessions, ask:

1. Who launched the session?
2. Was the user authorized?
3. Was there an approved access request?
4. Was the session tied to a ticket or change record?
5. Was the duration reasonable?
6. Was the correct privileged account used?
7. Was the target system expected?
8. Was the activity consistent with the business justification?
9. Was password rotation required after the session?
10. Were there any suspicious actions?

## Session Risk Indicators

Potential risk indicators include:

- Session launched without approval
- Session launched outside business hours
- Session duration longer than expected
- Session used against an unexpected system
- Break-glass account used for routine work
- Contractor session with no ticket
- Multiple failed session launches
- Session terminated unexpectedly
- Activity inconsistent with the request
- Use of highly privileged accounts without justification

## Session Monitoring Review Process

A basic review process may include:

1. Export or review session records.
2. Filter by high-risk safes or accounts.
3. Identify sessions involving production systems.
4. Identify sessions involving break-glass accounts.
5. Confirm each session has a business justification.
6. Confirm each session has a ticket or change reference.
7. Review any failed or unusual sessions.
8. Document findings.
9. Escalate suspicious activity.
10. Save evidence for audit.

## Example Review Result

| Session | Result | Notes |
|---|---|---|
| Carlos Ramirez to PROD-WIN-SRV-01 | Approved | Matched incident ticket |
| Vendor Admin to PROD-APP-01 | Review Further | Missing change record |
| breakglass-admin01 to tenant admin portal | Escalate | Break-glass use requires immediate review |

## Audit Evidence

Session monitoring evidence should include:

- Session user
- Privileged account used
- Target system
- Start and end time
- Duration
- Ticket or change reference
- Approval status
- Review notes
- Any remediation actions
- Password rotation status, if applicable

## Common Session Monitoring Issues

Common issues include:

- Missing ticket reference
- Missing approval
- Incorrect account used
- Session not recorded when expected
- Failed connection
- User unable to launch session
- Target system unavailable
- Wrong platform or connector
- Access denied due to permissions
- Session launched outside approved window

## Summary

PSM session monitoring supports privileged access security by helping organizations control, monitor, review, and document privileged activity. A strong session monitoring workflow improves audit readiness and helps detect risky privileged access behavior.
