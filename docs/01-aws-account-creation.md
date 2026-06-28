# AWS Account Creation

---

## Executive Summary

This document outlines the process of establishing a new Amazon Web Services (AWS) account that serves as the foundation for a secure cloud environment.

The objective of this implementation is not only to provision an AWS account, but to prepare it according to cloud security best practices before any workloads are deployed.

This guide forms the first phase of the AWS Account Setup Playbook and establishes the governance baseline used throughout the remainder of the project.

---

# Objectives

At the completion of this guide, the following objectives should be achieved:

- Successfully create an AWS account.
- Access the AWS Management Console.
- Understand the AWS Console interface.
- Verify account ownership.
- Prepare the environment for security hardening.
- Prepare for Identity and Access Management (IAM) implementation.

---

# Business Context

Cloud environments should never begin with deploying services immediately after account creation.

Instead, organizations first establish governance, identity management, billing controls, monitoring, and security policies before provisioning infrastructure.

Following this methodology significantly reduces security risks while improving long-term operational management.

---

# Architecture Position

This guide represents Phase 1 of the overall AWS account architecture.

```
Internet User
      │
      ▼
AWS Account Created
      │
      ▼
Root Account Secured
      │
      ▼
IAM Administration
      │
      ▼
Billing Governance
      │
      ▼
Cloud Resource Deployment
```

---

# Prerequisites

Before beginning, ensure the following are available:

- Valid email address
- Mobile phone
- Payment method
- Stable Internet connection
- Modern web browser

---

# Implementation Steps

## Step 1 — Create the AWS Account

Create a new AWS account using a valid email address and establish account ownership.

### Purpose

Creating the account establishes the cloud tenancy that will contain all future AWS resources.

### Expected Outcome

A new AWS account is successfully provisioned.

---

## Step 2 — Verify the Account

Complete all verification steps requested by AWS, including email verification and identity verification where required.

### Why this is important

AWS performs identity verification to protect the platform against abuse and fraudulent account creation.

---

## Step 3 — Configure Initial Account Settings

Configure the account according to the onboarding wizard.

Typical configuration includes:

- Region selection
- Support plan selection
- Account preferences

---

## Step 4 — Sign in to the AWS Console

Access the AWS Management Console using the newly created account.

Verify that login is successful.

---

# Validation

The implementation is considered successful when:

- AWS Console is accessible.
- Root account login succeeds.
- No account verification tasks remain.
- The account dashboard loads successfully.

---

# Security Considerations

At this stage the AWS Root User should only be used for:

- Initial configuration
- Billing configuration
- MFA configuration
- Emergency account recovery

Routine administration should never be performed using the Root User.

---

# AWS Best Practices

AWS recommends:

- Enable MFA immediately.
- Create dedicated IAM administrators.
- Avoid daily use of the Root account.
- Configure billing alerts.
- Monitor account activity.

These recommendations are implemented throughout the remaining sections of this project.

---

# Lessons Learned

Key observations from this phase include:

- The AWS account is the security boundary for all deployed resources.
- Proper planning before resource deployment simplifies future administration.
- Establishing governance early reduces operational risk.

---

# Next Steps

The next guide covers securing the AWS Root User through Multi-Factor Authentication (MFA), establishing the first layer of account protection before creating IAM administrative users.

➡ Continue to:

`02-root-user-security.md`
