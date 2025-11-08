# 💾 Azure Backup

Azure Backup is a managed service to back up and restore Azure VMs, files, databases, and workloads.

---

## 🎯 Key Features
- **Azure Recovery Services vault** for backup management.
- Backup types: VM backups, SQL backups (IaaS), Azure Files backup, Backup for SAP HANA, etc.
- Backup retention policies and scheduling.
- Instant restore and item-level recovery for some workloads.
- Soft delete for backups to prevent accidental removal.

---

## 🛠 Implementation Notes
- Choose vault type and region; configure policies and retention.
- Use Azure Backup agent, MARS agent, or native integration for VMs.
- Integrate with Key Vault for customer-managed keys if required.

---

## 🧠 Exam Tips
- Understand what Azure Backup protects (VMs, SQL in VM, Files, etc.).
- Know Recovery Services vault vs Recovery Services agent differences.
- Use backup policies to meet RPO/RTO and compliance requirements.

---

## 📚 Reference
- [Azure Backup documentation](https://learn.microsoft.com/azure/backup/)
