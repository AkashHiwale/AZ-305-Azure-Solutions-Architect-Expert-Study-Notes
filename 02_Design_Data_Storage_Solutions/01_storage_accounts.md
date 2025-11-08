# 💾 Azure Storage Accounts

A storage account provides a unique namespace for your Azure Storage data that is accessible from anywhere in the world over HTTP or HTTPS.

---

## 🎯 Types of Storage Accounts

| Type | Use Case | Services Supported |
|------|-----------|-------------------|
| **Standard General-purpose v2** | Most scenarios | Blob, File, Queue, Table |
| **Premium block blobs** | High-performance blob scenarios | Blob only |
| **Premium file shares** | Enterprise file shares | File only |
| **Premium page blobs** | VM disks | Page blobs only |

---

## 🔐 Security Features

- **Encryption**
  - At-rest (Azure Storage Service Encryption)
  - In-transit (TLS/HTTPS)
  - Customer-managed keys support
  
- **Authentication**
  - Azure AD integration
  - Shared Key
  - SAS tokens (account, service, user delegation)

- **Network Security**
  - Private endpoints
  - Service endpoints
  - Network rules
  - Storage firewall

---

## 🌟 Performance Tiers

### Access Tiers
- **Hot**: Frequently accessed data
- **Cool**: Infrequently accessed, stored ≥30 days
- **Archive**: Rarely accessed, stored ≥180 days

### Performance Tiers
- **Standard**: HDD-based storage
- **Premium**: SSD-based storage
  - Higher IOPS
  - Lower latency

---

## 💰 Redundancy Options

| Option | Description | RPO/RTO |
|--------|-------------|---------|
| **LRS** | Three copies, single datacenter | Lower cost, higher risk |
| **ZRS** | Three copies across zones | Zone resilience |
| **GRS** | Six copies, secondary region | Region failover |
| **GZRS** | ZRS + secondary region | Best resilience |

---

## 🧠 Exam Tips

- Know when to use each **account type**
- Understand **redundancy options** and their trade-offs
- Remember **security features** and authentication methods
- Know **access tier** differences and when to use each
- Understand **networking options** for secure access

---

## 📚 Reference

- [Storage Account overview](https://learn.microsoft.com/azure/storage/common/storage-account-overview)
- [Storage redundancy options](https://learn.microsoft.com/azure/storage/common/storage-redundancy)
- [Storage security best practices](https://learn.microsoft.com/azure/storage/blobs/security-recommendations)
