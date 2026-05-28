# Break-Glass Plan

## Purpose

This document defines a break-glass access plan for the CyberArk PAM Operations Lab. The goal is to show how emergency privileged access can be documented, controlled, monitored, and reviewed.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## What Is Break-Glass Access?

Break-glass access is emergency access used when normal privileged access workflows are unavailable or not functioning.

Break-glass accounts are typically used only during urgent situations such as:

- CyberArk access outage
- Identity provider outage
- MFA outage
- Network outage
- Production incident
- Administrative lockout
- Emergency security response
- Failed privileged access workflow

## Why Break-Glass Planning Matters

Break-glass accounts are powerful and high risk. They can help restore access during emergencies, but they can also create security risk if they are not protected, monitored, and reviewed.

A break-glass plan helps ensure emergency access is:

- Documented
- Restricted
- Monitored
- Reviewed after use
- Rotated after use
- Not used for normal daily administration

## Break-Glass Account Rules

Break-glass accounts should follow these rules:

1. Use only for emergency access.
2. Do not use for routine administration.
3. Limit the number of people who know or can use the account.
4. Store credentials securely.
5. Require approval when possible.
6. Monitor all use.
7. Rotate the password after use.
8. Review use immediately after an emergency.
9. Document the reason for access.
10. Keep break-glass accounts separate from normal admin accounts.

## Example Break-Glass Accounts

| Account Name | Purpose | Owner Team | Risk Level | Daily Use Allowed? |
|---|---|---|---|---|
| breakglass-admin01 | Emergency tenant or platform recovery | IAM/Security Team | Critical | No |
| breakglass-server01 | Emergency production server access | Windows Server Team | Critical | No |
| breakglass-network01 | Emergency network device access | Network Team | Critical | No |

## Break-Glass Safe Design

Break-glass accounts should be stored in a dedicated safe.

Example safe:

```text
SAFE-BREAKGLASS
