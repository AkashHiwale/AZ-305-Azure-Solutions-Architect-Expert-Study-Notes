# 🛡️ Azure Storage Data Redundancy

Azure Storage offers multiple redundancy options to protect against data loss.

---

## 🎯 Redundancy Options

| Option   | Description                    | Use Case                |
|----------|-------------------------------|-------------------------|
| **LRS**  | Locally redundant, single DC  | Lowest cost, least resilient |
| **ZRS**  | Zone-redundant, across zones  | High availability       |
| **GRS**  | Geo-redundant, secondary region | Disaster recovery      |
| **GZRS** | Geo-zone-redundant            | Best resilience         |

---

## 🧠 Exam Tips

- GRS/GZRS for disaster recovery.
- ZRS for high availability within region.
- LRS is lowest cost, least resilient.

---

## 📚 Reference

- [Redundancy options](https://learn.microsoft.com/azure/storage/common/storage-redundancy)
