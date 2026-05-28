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
