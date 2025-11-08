# 🔒 Azure Storage Account Encryption

Azure Storage provides encryption for data at rest and in transit.

---

## 🎯 Encryption Types

| Type                    | Description                                      |
|-------------------------|--------------------------------------------------|
| **At-rest**             | SSE with Microsoft-managed keys (default)        |
| **Customer-managed keys** | Use Azure Key Vault for BYOK                   |
| **In-transit**          | TLS/HTTPS enforced                              |

- All data encrypted by default.
- Supports double encryption for compliance.
- Key rotation supported.

---

## 🧠 Exam Tips

- Know difference between Microsoft-managed and customer-managed keys.
- Encryption is transparent to applications.
- Use Key Vault for BYOK scenarios.

---

## 📚 Reference

- [Storage encryption](https://learn.microsoft.com/azure/storage/common/storage-service-encryption)
