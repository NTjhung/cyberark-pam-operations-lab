# Privileged Account Onboarding

## Purpose

This document defines a privileged account onboarding workflow for the CyberArk PAM Operations Lab. The goal is to show how privileged accounts can be identified, reviewed, assigned to the correct safe, documented, and placed under PAM control.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## What Is Privileged Account Onboarding?

Privileged account onboarding is the process of adding elevated accounts into a Privileged Access Management system so they can be controlled, monitored, rotated, and audited.

Privileged accounts may include:

- Local administrator accounts
- Domain administrator accounts
- Linux root accounts
- Database administrator accounts
- Network device administrator accounts
- Application administrator accounts
- Service accounts
- Cloud administrator accounts
- Break-glass accounts

## Why Onboarding Matters

Privileged accounts that are not onboarded into PAM may create risk because they can be:

- Shared without tracking
- Used without approval
- Missing a documented owner
- Missing password rotation
- Difficult to audit
- Left active after projects end
- Unknown to security teams
- Used outside standard access workflows

Onboarding privileged accounts into PAM helps reduce these risks.

## Onboarding Workflow

A standard privileged account onboarding process should include the following steps:

1. Identify the privileged account.
2. Confirm the account owner.
3. Confirm the system or application the account belongs to.
4. Classify the account risk level.
5. Select the correct safe.
6. Define who can request access.
7. Define who can approve access.
8. Define password rotation expectations.
9. Define session monitoring requirements.
10. Document the onboarding request.
11. Add the account to PAM.
12. Validate access and ownership.
13. Save evidence for audit.

## Onboarding Request Details

Each privileged account onboarding request should collect:

| Field | Description |
|---|---|
| Account Name | Name of the privileged account |
| System/Application | System, server, database, network device, or application |
| Account Type | Local admin, domain admin, service account, DBA, network admin, etc. |
| Environment | Production, non-production, cloud, lab, or development |
| Owner Team | Team responsible for the account |
| Business Owner | Person or team responsible for approving access |
| Risk Level | Low, medium, high, or critical |
| Safe Name | Safe where the account should be stored |
| Approval Required | Whether access requests require approval |
| Rotation Required | Whether password rotation is required |
| Session Monitoring Required | Whether privileged sessions should be monitored |
| Review Frequency | How often access should be reviewed |

## Sample Onboarding Matrix

| Account Name | Account Type | Environment | Owner Team | Safe Name | Approval Required | Rotation Required | Review Frequency |
|---|---|---|---|---|---|---|---|
| win-prod-localadmin | Windows Local Admin | Production | Windows Server Team | SAFE-WIN-PROD-ADMINS | Yes | Yes | Monthly |
| linux-prod-root | Linux Root | Production | Linux Team | SAFE-LINUX-PROD-ROOT | Yes | Yes | Monthly |
| sql-prod-dba | Database Admin | Production | Database Team | SAFE-DBA-PROD | Yes | Yes | Monthly |
| net-fw-admin | Network Admin | Production | Network Team | SAFE-NETWORK-ADMINS | Yes | Yes | Monthly |
| appsvc-prod-payroll | Service Account | Production | Application Team | SAFE-APP-SERVICE-ACCOUNTS | Yes | Planned | Quarterly |
| breakglass-admin01 | Emergency Admin | Production | IAM/Security Team | SAFE-BREAKGLASS | Yes | Yes | Monthly |

## Risk Classification

Privileged accounts should be classified by risk.

| Risk Level | Example | Reason |
|---|---|---|
| Low | Read-only support account | Limited access |
| Medium | Non-production local admin | Elevated access in lower-risk environment |
| High | Production local admin | Can modify production systems |
| Critical | Domain admin or break-glass account | Broad or emergency administrative access |

## Approval Requirements

Approval should be required for:

- Production administrator accounts
- Break-glass accounts
- Database administrator accounts
- Network administrator accounts
- Service accounts with sensitive access
- Any account with broad administrative access

Approval may be optional for:

- Non-production support accounts
- Read-only accounts
- Low-risk lab accounts

## Password Rotation Planning

During onboarding, determine whether password rotation is required.

Password rotation should be required for:

- Production administrator accounts
- Shared privileged accounts
- Break-glass accounts
- Local administrator accounts
- Database administrator accounts
- Network device accounts

Password rotation may need special planning for:

- Service accounts
- Application accounts
- Accounts tied to scheduled tasks
- Accounts used by integrations
- Accounts where rotation could break an application

## Session Monitoring Planning

Session monitoring should be considered for high-risk privileged accounts.

Session monitoring is especially important for:

- Production server access
- Database administrator access
- Network device administration
- Break-glass account usage
- Vendor or contractor privileged access
- Sensitive application administration

## Validation Checklist

Before completing onboarding, confirm:

- The account owner is documented.
- The safe name is correct.
- The access approver is documented.
- The rotation requirement is documented.
- The session monitoring requirement is documented.
- The account risk level is documented.
- The review frequency is documented.
- The account has a business need.
- Audit evidence is saved.

## Common Onboarding Issues

Common issues during privileged account onboarding include:

- Incorrect safe selection
- Missing account owner
- Missing business owner
- Unclear password rotation requirements
- Service account rotation risk
- Incorrect platform assignment
- Missing approval workflow
- Missing access review schedule
- Duplicate or stale privileged accounts

## Remediation Notes

If an onboarding issue is found:

1. Pause onboarding until ownership is confirmed.
2. Confirm the correct safe.
3. Confirm approval requirements.
4. Confirm password rotation impact.
5. Confirm session monitoring needs.
6. Update the onboarding record.
7. Save evidence of the correction.

## Summary

Privileged account onboarding is a core PAM process. A strong onboarding workflow helps ensure privileged accounts are controlled, assigned to the correct safe, reviewed regularly, rotated when appropriate, and supported with audit evidence.
