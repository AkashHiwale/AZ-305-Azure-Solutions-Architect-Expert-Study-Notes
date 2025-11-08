# 🏗️ Availability Zones

Availability Zones are physically separate datacenters within an Azure region that provide resiliency against datacenter failures.

---

## 🎯 Key Concepts
- Zone-redundant architecture places resources (VMs, managed disks, IPs) across zones.
- Provides higher SLA (e.g., 99.99% when using zone-redundant VMs).
- Zonal and zone-redundant services exist across Azure.

---

## 🧩 Use Cases
- Protect against datacenter-level failures within a region.
- Recommended for critical workloads requiring higher availability than Availability Sets.

---

## 🖼️ Diagram

Simple ASCII diagram (conceptual):
```
Region with Zones
+---------------------------------------------+
| Zone 1 | Zone 2 | Zone 3                    |
| VM-A   | VM-B   | VM-C                      |
| Disk1  | Disk2  | Disk3 (replicated)        |
+---------------------------------------------+
Cross-Zone Load Balancer -> VM-A, VM-B, VM-C
Zone-redundant Storage (ZRS/GZRS) spans zones
```

---

## 🧠 Exam Tips
- Availability Zones are region-scoped; ensure the region supports zones.
- Design for cross-zone load balancing and data replication.
- Combine with zone-redundant storage and zonal VMs for optimal resilience.

---

## 📚 Reference
- [Availability Zones](https://learn.microsoft.com/azure/availability-zones/)

