# Root User Security

---

# Executive Summary

The AWS Root User is the most privileged identity within an AWS account and has unrestricted access to every AWS service and resource.

Protecting the Root account is therefore the highest security priority immediately after creating an AWS account.

This guide documents the security hardening activities performed on the Root account before delegating day-to-day administrative activities to an AWS Identity and Access Management (IAM) administrator.

---

# Objectives

The objectives of this implementation are to:

- Secure the AWS Root User.
- Reduce the attack surface.
- Prepare the account for IAM delegation.
- Implement AWS security best practices.
- Minimize the operational use of the Root account.

---

# Why Root User Security Matters

The Root User possesses unrestricted administrative permissions across the AWS account.

Unlike IAM users, Root permissions cannot be restricted through IAM policies.

For this reason AWS recommends that the Root account should only be used for:

- Initial account configuration
- Billing administration
- Account recovery
- Tasks requiring Root privileges

Routine administrative work should instead be performed through dedicated IAM users.

---

# Security Controls Implemented

The following controls were implemented during this phase:

- Root account protected.
- MFA configured.
- Root account reserved for emergency use.
- Administrative activities delegated to IAM.

---

# Implementation Overview

The implementation consisted of the following activities:

1. Sign in using the Root account.
2. Access Security Credentials.
3. Configure Multi-Factor Authentication (MFA).
4. Verify MFA registration.
5. Validate Root account protection.

---

# Validation

Successful implementation is confirmed when:

- Root account authentication succeeds.
- MFA is enabled.
- Recovery options are configured.
- Root account is no longer used for routine administration.

---

# Security Best Practices

AWS recommends:

- Never share Root credentials.
- Enable MFA immediately.
- Avoid creating Root access keys.
- Store recovery information securely.
- Use IAM users for administration.

---

# Lessons Learned

Securing the Root account significantly improves the security posture of an AWS environment.

This implementation establishes a trusted administrative foundation before introducing IAM identities.

---

# Next Guide

The next document covers creating a dedicated IAM Administrator account to replace the Root account for day-to-day cloud administration.

➡ Continue to:

03-iam-administrator-setup.md
