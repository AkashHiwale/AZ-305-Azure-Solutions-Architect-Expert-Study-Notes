# 🧾 Azure Blob Data Protection

Blob data protection techniques to prevent accidental or malicious data loss.

---

## 🎯 Protection Features
- **Soft Delete for Blobs**: Recover deleted blobs within retention window.
- **Blob Versioning**: Keep previous versions of blobs automatically.
- **Immutable Storage (WORM)**: Legal hold and time-based retention (immutable blobs).
- **Snapshots**: Point-in-time snapshots for quick restore.
- **Storage Account Backup**: Use backup strategies and replication (GRS/GZRS).

---

## 🛠 Design Notes
- Combine versioning + soft delete for robust protection.
- Use immutable storage for compliance requirements.
- Lifecycle management transitions between tiers and can clean up old versions.

---

## 🧠 Exam Tips
- Understand difference between soft delete and immutable storage.
- Versioning retains prior blob states automatically; snapshots are manual/incremental.
- Use GRS/GZRS for region-level protection in addition to data protection features.

---

## 📚 Reference
- [Blob soft delete](https://learn.microsoft.com/azure/storage/blobs/soft-delete-overview)
- [Blob versioning](https://learn.microsoft.com/azure/storage/blobs/versioning-overview)
- [Immutable storage for blobs](https://learn.microsoft.com/azure/storage/blobs/immutable-storage-overview)
