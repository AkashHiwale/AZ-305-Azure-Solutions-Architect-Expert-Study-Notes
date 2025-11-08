# 🔐 Authentication & Authorization in Azure

Authentication (AuthN) and Authorization (AuthZ) are fundamental security concepts in Azure that control access to resources and services.

---

## 📌 Key Concepts

- **Authentication (AuthN)**: Verifies WHO you are
  - Username/password
  - Multi-factor authentication (MFA)
  - Certificates
  - Managed identities
  
- **Authorization (AuthZ)**: Determines WHAT you can do
  - Role-Based Access Control (RBAC)
  - Azure Policy
  - Resource locks

---

## 🛠️ Authentication Methods

- **Azure AD Authentication**
  - Username/password
  - Windows Integrated Authentication
  - Federation services (ADFS)
  - Passwordless (FIDO2, Microsoft Authenticator)

- **Multi-Factor Authentication (MFA)**
  - Something you know (password)
  - Something you have (phone, token)
  - Something you are (biometrics)

- **Conditional Access**
  - Location-based access
  - Device compliance
  - Risk-based policies
  - Session controls

---

## 🔑 Authorization Components

- **Role-Based Access Control (RBAC)**
  - Built-in roles
  - Custom roles
  - Scope levels (Management Group/Subscription/Resource Group/Resource)
  
- **Azure AD Privileged Identity Management (PIM)**
  - Just-in-time access
  - Time-bound elevation
  - Approval workflows
  
- **Azure Policy**
  - Enforce standards
  - Assess compliance
  - Guard rails for resources

---

## 💡 Best Practices

- Implement least privilege access
- Enable MFA for all users
- Use Conditional Access policies
- Regular access reviews
- Monitor and audit authentication events
- Implement Zero Trust principles

---

## 🧠 Exam Tips

- Know different authentication methods and when to use them
- Understand RBAC role assignments and inheritance
- Be familiar with Conditional Access scenarios
- Know how PIM works for privileged access
- Understand difference between authentication and authorization

---

## 📚 Reference

- [Azure AD authentication documentation](https://learn.microsoft.com/azure/active-directory/authentication/)
- [Azure RBAC documentation](https://learn.microsoft.com/azure/role-based-access-control/)
