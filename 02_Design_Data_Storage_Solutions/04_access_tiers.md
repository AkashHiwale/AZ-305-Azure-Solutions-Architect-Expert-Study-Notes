# 📊 Azure Storage Access Tiers

Azure Storage access tiers help optimize costs based on how frequently data is accessed.

---

## 🎯 Access Tiers Overview

| Tier     | Description                  | Typical Use Case         |
|----------|------------------------------|-------------------------|
| **Hot**  | Frequent access              | Active files, logs      |
| **Cool** | Infrequent access            | Backups, older docs     |
| **Archive** | Rarely accessed           | Compliance, long-term   |

- Tiers can be set at blob or account level.
- Lifecycle policies automate tier transitions.

---

## 🧠 Exam Tips

- Know retention requirements for cool/archive.
- Understand cost implications of tier changes.
- Hot tier: highest cost, lowest latency; Archive: lowest cost, highest latency.

---

## 📚 Reference

- [Access tiers](https://learn.microsoft.com/azure/storage/blobs/access-tiers-overview)
