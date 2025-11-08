# 🗄️ Microsoft SQL Server (IaaS / On-prem)

Overview of Microsoft SQL Server deployment options and HA/DR considerations for IaaS and on-premises.

---

## 🎯 Key Options for HA/DR
- **Always On Availability Groups** — DB-level high availability and readable secondaries.
- **Failover Cluster Instances (FCI)** — Instance-level HA using shared storage (Windows Server Failover Clustering).
- **Log Shipping** — Transaction log backups shipped to secondary server; asynchronous.
- **Database Mirroring** (deprecated) — legacy option; replaced by AGs.
- **Backup/Restore** — Traditional approach for DR.

---

## 🧩 Considerations
- RPO/RTO requirements determine choice (AG for low RPO/RTO).
- Network latency and bandwidth for replication.
- Storage architecture (shared vs. distributed).
- Licensing implications (SQL Server edition and SA).

---

## 🧠 Exam Tips
- Use Always On AGs for read-scale and fast failover; FCI for instance-level HA.
- For IaaS VMs, combine Azure Backup, ASR, and SQL native HA for resilience.
- Understand trade-offs between synchronous (zero data loss) and asynchronous replication.

---

## 📚 Reference
- [SQL Server high availability](https://learn.microsoft.com/sql/sql-server/availability/always-on-availability-groups/windows/always-on-availability-groups-sql-server)
