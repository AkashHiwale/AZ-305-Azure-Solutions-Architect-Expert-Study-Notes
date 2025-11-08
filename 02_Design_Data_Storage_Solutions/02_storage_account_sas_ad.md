# 🔑 Azure Storage Account – SAS & Azure Active Directory

Azure Storage supports secure access using Shared Access Signatures (SAS) and Azure Active Directory (Azure AD).

---

## 🎯 SAS (Shared Access Signature)

- Grants limited access to storage resources without exposing account keys.
- Types:
  - **Account SAS**
  - **Service SAS**
  - **User Delegation SAS** (uses Azure AD)
- SAS tokens can restrict:
  - Permissions
  - Services
  - Resource types
  - IP ranges
  - Protocols
  - Expiry time

---

## 🎯 Azure Active Directory Integration

- Enables identity-based access to blobs and queues.
- Supports RBAC for granular permissions.
- Recommended for enterprise scenarios over SAS.
- Integrates with managed identities for secure access from Azure resources.

---

## 🧠 Exam Tips

- Use **User Delegation SAS** for secure, time-bound access.
- Prefer **Azure AD** for managed, auditable access control.
- SAS tokens can be revoked by regenerating account keys.

---

## 📚 Reference

- [SAS documentation](https://learn.microsoft.com/azure/storage/common/storage-sas-overview)
- [Azure AD authentication](https://learn.microsoft.com/azure/storage/common/storage-auth-aad)
