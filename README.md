# healthcare-iam-lab
Hands-on lab demonstrating healthcare-focused Identity and Access Management (IAM) environment using Azure AD / Entra AD
# Healthcare IAM Lab (Azure AD / Entra ID)

This repo documents a hands-on lab where I designed and implemented a **healthcare-focused Identity & Access Management (IAM)** environment using Azure AD / Entra ID.

The goal of this lab is to simulate how a hospital would control access to **PHI (Protected Health Information)** in a HIPAA-regulated environment.

---

## 🎯 Objectives

- Create role-based access for different hospital staff (Doctors, Nurses, Billing, Admin, etc.)
- Protect access to a fictional EMR/PHI application using **Conditional Access**
- Enforce **MFA** for all clinical users
- Use **PIM (Privileged Identity Management)** for elevated access
- Configure **audit logging** to review PHI access

---

## 🩺 Hospital Scenario

In this lab, I created a fictional hospital tenant with the following roles:

- **Doctors** – Need broad access to EMR and PHI
- **Nurses** – Need focused access to patient charts and orders
- **Billing** – Need access only to billing-related data
- **IT Admins** – Need administrative permissions, tightly controlled
- **Security / Compliance** – Need access to logs and audit data

See: [`docs/user-roles-and-groups.md`](docs/user-roles-and-groups.md)

---

## 🛡️ Controls Implemented

### 1. Conditional Access for PHI Apps

- Require MFA for all users accessing the EMR/PHI application
- Block legacy authentication protocols
- Require compliant/managed device access (where applicable)
- Restrict access by location for certain roles (optional)

Details: [`docs/conditional-access-policies.md`](docs/conditional-access-policies.md)  
Screenshots: [`screenshots/`](screenshots/)

---

### 2. Privileged Identity Management (PIM)

- Just-In-Time activation for EMR Admin roles
- Approval workflow for elevated access
- Time-bound elevation with automatic expiration

Details: [`docs/pim-configuration.md`](docs/pim-configuration.md)

---

### 3. Audit Logging & Reviews

- Captured sign-in logs for EMR application access
- Demonstrated how to review and export audit logs
- Outlined a quarterly access review process

Details: [`docs/audit-logging-and-review.md`](docs/audit-logging-and-review.md)

---

## 🧰 Technologies Used

- Azure AD / Entra ID
- Conditional Access
- MFA
- Privileged Identity Management (PIM)
- Azure Sign-In Logs & Audit Logs

---

## 📌 How This Maps to Healthcare

This lab demonstrates how IAM and cloud security can enforce:

- **HIPAA Security Rule** (technical safeguards)
- **Minimum Necessary** access
- **Least privilege** for different clinical roles
- **Auditability** of PHI access

This is the kind of work I want to do professionally in **Healthcare IT / IAM / Cloud Security**.
