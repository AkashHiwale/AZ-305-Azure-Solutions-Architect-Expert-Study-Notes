# 🟦 Azure SQL Database – Backup & High Availability Features

Covers built-in backup, point-in-time restore, Active Geo-Replication, and Auto-Failover Groups for Azure SQL.

---

## 🧾 Backups & Point-in-Time Restore (PITR)
- Azure SQL performs automated backups (full, differential, transaction log).
- PITR allows restore to any point within retention window (default 7-35 days depending on tier).
- Long-term retention (LTR) for weekly/monthly/yearly backups up to many years.

---

## 🔁 Active Geo-Replication
- Create up to four readable secondary databases in different regions (async).
- Useful for read scale-out and manual failover.
- RPO is asynchronous (some data loss possible).

---

## 🔄 Auto-Failover Groups
- Group databases for coordinated failover across primary and secondary servers.
- Supports automated failover with configurable grace period.
- Ideal for business continuity across regions; supports read-write listener endpoint.

---

## 🧠 Exam Tips
- PITR is for single database restore within retention window; LTR for long-term retention.
- Active Geo-Replication provides readable secondaries; Auto-Failover Groups provide coordinated failover for multiple DBs.
- Understand difference between zone-redundant and geo-redundant options for Azure SQL Managed Instance.

---

## 📚 Reference
- [Azure SQL automated backups](https://learn.microsoft.com/azure/azure-sql/backup-overview)
- [Active geo-replication](https://learn.microsoft.com/azure/azure-sql/database/active-geo-replication)
- [Auto-failover groups](https://learn.microsoft.com/azure/azure-sql/database/auto-failover-group-overview)
