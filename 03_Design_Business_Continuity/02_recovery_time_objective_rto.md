# ⏳ Recovery Time Objective (RTO)

Recovery Time Objective (RTO) defines the maximum acceptable duration of time to restore a service after an outage.

---

## 🎯 What is RTO?
- The target time to recover service functionality (e.g., RTO = 2 hours).
- Drives DR runbooks, failover automation, and architecture (hot/warm/cold).

---

## 🧩 Considerations
- Business impact and SLA requirements.
- Automation level: manual, scripted, fully automated failover.
- Infrastructure readiness (pre-provisioned resources vs provisioning on failover).
- Testing and runbook maturity.

---

## 🛠 Example Strategies
- RTO = minutes: active-active or automated failover solutions (auto failover groups, cluster).
- RTO = hours: pre-warmed secondary environment with scripted cutover.
- RTO = days: cold standby with manual provisioning.

---

## 🧠 Exam Tips
- RTO is about time-to-recover (not data loss). Map RTO to solution (ASR, auto failover groups, replication).
- Shorter RTO generally increases complexity and cost.
- Validate RTO with regular DR drills.

---

## 📚 Reference
- [Disaster recovery fundamentals](https://learn.microsoft.com/azure/site-recovery/site-recovery-overview)
