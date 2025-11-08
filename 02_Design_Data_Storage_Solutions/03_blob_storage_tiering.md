# 🗂️ Azure Blob Storage Tiering

Azure Blob Storage offers multiple access tiers to optimize cost and performance for different data usage patterns.

---

## 🎯 Access Tiers

| Tier     | Use Case                | Retention | Cost      | Retrieval |
|----------|-------------------------|-----------|-----------|-----------|
| **Hot**  | Frequently accessed     | None      | Highest   | Instant   |
| **Cool** | Infrequently accessed   | ≥30 days  | Lower     | Instant   |
| **Archive** | Rarely accessed      | ≥180 days | Lowest    | Hours     |

---

## 🌟 Tier Management

- Data can be moved between tiers manually or via lifecycle management policies.
- Archive tier requires rehydration before access.

---

## 🧠 Exam Tips

- Know retention requirements for cool/archive.
- Understand cost implications of tier changes.
- Use lifecycle management for automated tiering.

---

## 📚 Reference

- [Blob storage tiers](https://learn.microsoft.com/azure/storage/blobs/access-tiers-overview)
