# Safe Design Matrix

## Purpose

This document defines a sample CyberArk safe design matrix for the PAM Operations Lab. The goal is to show how privileged accounts can be organized, controlled, and reviewed using a structured safe design.

This project is based on hands-on CyberArk access. Screenshots are not included because screenshot capture was not permitted in the CyberArk environment.

## What Is a Safe?

A safe is a logical container used to store and manage privileged accounts. Safes help separate access by system type, business function, environment, sensitivity, and support team.

A good safe design helps with:

- Least privilege
- Separation of duties
- Cleaner access reviews
- Better audit evidence
- Easier ownership tracking
- Easier privileged account onboarding
- Easier password rotation planning

## Safe Design Principles

The safe design should follow these principles:

1. Separate production and non-production access.
2. Separate Windows, Linux, database, network, and application accounts.
3. Assign safe ownership to the correct support team.
4. Avoid placing unrelated privileged accounts in the same safe.
5. Limit access to users with a business need.
6. Require approvals for sensitive or production access.
7. Review safe membership regularly.
8. Document the safe purpose and account ownership.

## Sample Safe Design Matrix

| Safe Name | Account Type | Environment | Owner Team | Access Level | Approval Required | Review Frequency |
|---|---|---|---|---|---|---|
| SAFE-WIN-PROD-ADMINS | Windows local admin accounts | Production | Windows Server Team | High | Yes | Monthly |
| SAFE-WIN-NONPROD-ADMINS | Windows local admin accounts | Non-Production | Windows Server Team | Medium | No | Quarterly |
| SAFE-LINUX-PROD-ROOT | Linux root/admin accounts | Production | Linux Team | High | Yes | Monthly |
| SAFE-DBA-PROD | Database administrator accounts | Production | Database Team | High | Yes | Monthly |
| SAFE-NETWORK-ADMINS | Network device admin accounts | Production | Network Team | High | Yes | Monthly |
| SAFE-APP-SERVICE-ACCOUNTS | Application service accounts | Production | Application Team | Medium | Yes | Quarterly |
| SAFE-BREAKGLASS | Emergency access accounts | Production | IAM/Security Team | Critical | Yes | Monthly |
| SAFE-CLOUD-ADMINS | Cloud administrator accounts | Cloud | Cloud/IAM Team | High | Yes | Monthly |

## Safe Naming Standard

A consistent naming standard helps make safes easier to understand.

Recommended format:

```text
SAFE-[SYSTEM TYPE]-[ENVIRONMENT]-[PURPOSE]
