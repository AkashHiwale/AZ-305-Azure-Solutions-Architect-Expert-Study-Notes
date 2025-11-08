# 🔐 Azure Key Vault – High Availability & Protection

Notes on Key Vault high availability, recovery, and best practices for protecting keys/secrets.

---

## 🎯 High Availability Features
- **Regional service with SLA**; use soft-delete and purge protection to avoid accidental loss.
- **Geo-redundant storage for backup** (use LTR/backup strategies and replicate to other regions manually).
- **Private endpoints** for network isolation and resilience via zone-redundant networking.

---

## 🛠 Best Practices
- Enable **soft delete** and **purge protection**.
- Use **Key Vault backups** and store backups in geo-redundant storage.
- Use **managed HSM** for higher availability and HSM-backed keys.
- Integrate with **Managed Identities** for secure access.

---

## 🧠 Exam Tips
- Soft delete and purge protection are crucial to prevent accidental permanent deletion.
- Managed HSM offers zone-redundant HSM-based key storage.
- Key Vault does not provide automatic cross-region replication for secrets — plan backups and replication.

---

## 📚 Reference
- [Azure Key Vault documentation](https://learn.microsoft.com/azure/key-vault/)
- [Managed HSM](https://learn.microsoft.com/azure/key-vault/managed-hsm/overview)
