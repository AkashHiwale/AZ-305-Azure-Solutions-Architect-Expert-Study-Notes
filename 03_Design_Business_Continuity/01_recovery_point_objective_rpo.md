# ⏱️ Recovery Point Objective (RPO)

Recovery Point Objective (RPO) defines the maximum acceptable amount of data loss measured in time — how far back in time you must be able to recover.

---

## 🎯 What is RPO?
- The maximum tolerated age of data after an outage (e.g., RPO = 15 minutes means you can lose up to 15 minutes of data).
- Drives backup frequency, replication strategy, and recovery design.

---

## 🧩 Considerations
- Application tolerance to data loss.
- Backup/replication interval (snapshot, transaction log, continuous replication).
- Cost vs. protection: lower RPO typically increases cost.
- RPO depends on storage, database technology, and network bandwidth.

---

## 🛠 Example Strategies
- RPO = seconds/minutes: use continuous replication (e.g., Data Guard, Always On, Azure Site Recovery with near-constant replication).
- RPO = hours: frequent snapshots or log shipping.
- RPO = daily: daily backups.

---

## 🧠 Exam Tips
- RPO relates to data loss; design choices (frequency, replication) determine achievable RPO.
- Lower RPO requires near-real-time replication or frequent transaction log shipping.
- Always document required RPOs per workload and map to solution options.

---

## 📚 Reference
- [Azure backup and RPO considerations](https://learn.microsoft.com/azure/backup/backup-overview)
