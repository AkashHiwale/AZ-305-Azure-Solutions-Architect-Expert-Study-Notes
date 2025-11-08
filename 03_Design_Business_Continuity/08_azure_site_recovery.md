# 🔁 Azure Site Recovery (ASR)

Azure Site Recovery orchestrates replication and failover for VMs and physical servers to Azure or between Azure regions.

---

## 🎯 Key Features
- Replication for VMware, Hyper-V, and physical servers to Azure.
- Replication for Azure VMs across regions.
- Orchestrated failover and failback.
- Test failover for non-disruptive DR drills.
- Integration with Recovery Services vault.

---

## 🛠 Implementation Notes
- Configure replication policy, recovery plan, and network mappings.
- Choose replication method (continuous replication for low RPO).
- Use test failover to validate runbooks and configuration.

---

## 🧠 Exam Tips
- ASR is DR orchestration, not backup. Use both for complete protection.
- Understand recovery plans, site mappings, and test failover process.
- ASR supports application consistency using pre/post scripts and Agent integrations.

---

## 📚 Reference
- [Azure Site Recovery documentation](https://learn.microsoft.com/azure/site-recovery/)
