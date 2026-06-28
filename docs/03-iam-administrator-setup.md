# IAM Administrator Setup

---

# Executive Summary

Following the security hardening of the AWS Root User, the next critical step is to establish a dedicated AWS Identity and Access Management (IAM) administrator account.

AWS recommends that the Root account should not be used for routine administrative activities. Instead, organizations should create dedicated IAM users with administrative privileges to improve accountability, enhance security, and reduce operational risk.

This document describes the implementation of the IAM administrator account that will be used for day-to-day administration of the AWS environment.

---

# Objectives

The objectives of this implementation are to:

- Create a dedicated IAM administrator account.
- Eliminate the need to use the Root account for routine administration.
- Apply AWS Identity and Access Management (IAM) best practices.
- Establish secure administrative access.
- Prepare the AWS environment for future workloads.

---

# Business Context

Enterprise cloud environments rarely use the Root account after the initial account configuration.

Instead, administrative activities are performed through IAM users or IAM roles.

This provides:

- Accountability
- Auditability
- Permission management
- Improved security
- Compliance with AWS security recommendations

---

# Why IAM Matters

AWS Identity and Access Management (IAM) is the service responsible for authentication and authorization within AWS.

IAM enables organizations to:

- Create users
- Create groups
- Assign permissions
- Implement least privilege
- Secure cloud resources

Rather than assigning permissions directly to individual users, AWS recommends assigning permissions through IAM groups.

---

# Implementation Overview

The implementation consisted of the following activities:

1. Navigate to the IAM Console.
2. Create an Administrators group.
3. Attach the AWS managed **AdministratorAccess** policy.
4. Create an IAM administrator user.
5. Add the user to the Administrators group.
6. Configure console access.
7. Validate successful sign-in.

---

# Validation

The implementation is considered successful when:

- The IAM user is created successfully.
- The Administrators group exists.
- The AdministratorAccess policy is attached.
- The IAM user is a member of the Administrators group.
- The IAM administrator can successfully sign in to the AWS Management Console.

---

# Security Best Practices

During implementation, the following AWS best practices were applied:

- Avoid using the Root account for daily administration.
- Assign permissions through groups instead of directly to users.
- Use AWS managed policies where appropriate.
- Enable MFA for privileged accounts.
- Regularly review IAM permissions.

---

# Lessons Learned

Creating a dedicated IAM administrator account significantly improves the security posture of an AWS environment.

Delegating administrative responsibilities to IAM users reduces dependency on the Root account while improving accountability and operational control.

---

# Next Guide

The next implementation guide focuses on securing the IAM administrator account using Multi-Factor Authentication (MFA).

➡ Continue to:

04-iam-user-mfa.md
