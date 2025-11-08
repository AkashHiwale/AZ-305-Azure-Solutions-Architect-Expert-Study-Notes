# 📁 Azure File Share Backup

Notes on protecting Azure Files with Azure Backup and native snapshot options.

---

## 🎯 Protection Options
- **Azure Backup**: Native backup for Azure File Shares (Recovery Services vault).
- **Snapshots**: Storage account-level snapshots (fast, incremental).
- **Soft delete for file shares**: Recover deleted shares within retention.

---

## 🛠 Design Considerations
- Choose backup frequency and retention to meet RPO/RTO.
- Use snapshots for fast restore; use Azure Backup for longer retention and management.
- Use lifecycle and cost considerations for large file shares.

---

## 🧠 Exam Tips
- Azure Backup supports file share backups via Recovery Services vault.
- Snapshots are immediate and cost-effective for short-term restore needs.
- Understand restore options: file-level and share-level.

---

## 📚 Reference
- [Azure Files backup](https://learn.microsoft.com/azure/backup/backup-azure-file-share)
