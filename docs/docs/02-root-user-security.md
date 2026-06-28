# Root User Security

---

# Executive Summary

The AWS Root User possesses unrestricted access to all resources within an AWS account. Because of these elevated privileges, securing the Root User is the most critical task immediately after creating an AWS account.

This guide documents the implementation of security controls that protect the Root account using AWS security best practices.

---

# Objectives

This implementation aims to:

- Secure the AWS Root User.
- Configure Multi-Factor Authentication (MFA).
- Reduce unauthorized access risks.
- Prepare the environment for IAM delegation.
- Ensure compliance with AWS security recommendations.

---

# Why Root User Security Matters

The Root User has unrestricted access to every AWS service and billing function.

Unlike IAM users, the Root account cannot have its permissions reduced.

For this reason, AWS recommends that the Root account be used only for tasks that explicitly require Root credentials.

Daily administration should always be delegated to IAM users.

---

# Security Architecture

```
AWS Root Account
        │
        ▼
Enable MFA
        │
        ▼
Store Recovery Method
        │
        ▼
Use Only for Emergency Tasks
        │
        ▼
Delegate Daily Administration to IAM
```

---

# Implementation Steps

## Step 1 – Sign in as the Root User

Authenticate using the Root account credentials.

### Purpose

The Root User is required to configure account-level security settings.

---

## Step 2 – Navigate to Security Credentials

Open the Security Credentials page.

This section contains:

- Password management
- MFA configuration
- Access keys
- Account security settings

---

## Step 3 – Configure Multi-Factor Authentication (MFA)

Select an MFA method.

AWS currently supports:

- Passkeys
- Security Keys
- Authenticator Applications

For this implementation, MFA was configured to strengthen account security.

---

## Step 4 – Complete MFA Registration

Scan the QR Code (or register the selected authentication device).

Verify the generated authentication codes.

---

## Step 5 – Validate MFA

Confirm that:

- MFA shows as Enabled.
- The device is successfully registered.
- Future logins require MFA verification.

---

# Validation Checklist

Successful implementation should confirm:

- Root account secured
- MFA enabled
- Device registered
- Recovery process available

---

# Security Best Practices

AWS recommends:

- Never share Root credentials.
- Enable MFA immediately.
- Store recovery information securely.
- Do not create Root access keys.
- Use the Root account only when absolutely necessary.

---

# Risk Assessment

If MFA is not enabled, the AWS account is significantly more vulnerable to:

- Credential theft
- Phishing attacks
- Unauthorized account takeover
- Financial abuse
- Data compromise

---

# Lessons Learned

Key observations from this implementation include:

- Root account protection is the highest security priority.
- MFA significantly increases account security.
- Administrative work should be delegated to IAM users after initial configuration.

---

# Next Steps

The next guide documents the creation of a dedicated IAM Administrator account, allowing administrative activities to be performed without using the Root User.

➡ Continue to:

`03-iam-administrator-setup.md`
