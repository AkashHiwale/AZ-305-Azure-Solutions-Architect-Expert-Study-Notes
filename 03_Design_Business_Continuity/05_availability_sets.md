# 🧩 Availability Sets

Availability Sets help maintain VM availability by distributing VMs across fault and update domains within a single datacenter/region.

---

## 🎯 Key Concepts
- **Fault Domain (FD)**: Physical hardware failure boundary (rack).
- **Update Domain (UD)**: Logical reboot/maintenance boundary.
- Azure guarantees 99.95% SLA for VMs in an Availability Set with two or more instances.

---

## 🧩 Use Cases
- Protect VMs from rack/hardware failure and planned maintenance.
- Used for classic IaaS VM high availability designs when VMs are in same region/zone.

---

## 🖼️ Diagram

Simple ASCII diagram (conceptual):
```
Region / Datacenter
+-------------------------------------- +
| Fault Domain 1    | Fault Domain 2   |
| (Rack A)          | (Rack B)         |
|  UD1: VM1         |  UD1: VM3        |
|  UD2: VM2         |  UD2: VM4        |
+-------------------------------------- +
Load Balancer -> VM1, VM2, VM3, VM4
```


---

## 🧠 Exam Tips
- Availability Sets do NOT protect against zone-level outages; use Availability Zones for that.
- Use Availability Sets when you need HA within a datacenter and zonal placement is not available.
- Combine with load balancer and health probes for application-level HA.

---

## 📚 Reference
- [Availability Sets](https://learn.microsoft.com/azure/virtual-machines/availability-set-overview)

