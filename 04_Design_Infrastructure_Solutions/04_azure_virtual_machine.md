# 🖥️ Azure Virtual Machines (VMs)

Azure Virtual Machines provide IaaS compute in the cloud for running Windows/Linux workloads with full OS control.

---

## 🎯 Overview
- VM = virtualized compute instance with OS, CPU, memory, and disks.
- Choose VM size/series based on CPU, memory, storage, and networking needs.
- Managed Disks simplify storage management and availability.

---

## 🧩 VM Series Examples
- General purpose: B, Dsv3, Dv4
- Compute optimized: Fsv2
- Memory optimized: Ev3, M
- Storage optimized: Lsv2
- GPU: NC/ND/NCv3 (AI/graphics)
- Burstable: B-series for low-cost variable loads

---

## 💾 Disks & Storage
- Managed Disks types: Standard HDD, Standard SSD, Premium SSD, Ultra SSD.
- OS disk + one or more data disks (page blobs).
- Ephemeral OS disks for stateless, low-latency scenarios.
- Use disk caching (ReadOnly/ReadWrite) depending on workload.
- Snapshots and managed disk backup via Azure Backup.

---

## 🌐 Networking
- NICs attached per VM; configure IP (public/private), NSGs, and UDRs.
- Place VMs inside VNets and subnets for isolation.
- Use Azure Load Balancer / Application Gateway for inbound traffic and health probes.
- Use Private Endpoints and service endpoints for secure service access.

---

## 🏗 Availability & HA
- Availability Set: distribute VMs across fault/update domains within a datacenter.
- Availability Zone: span VMs across physically separate datacenters for higher SLA.
- Use Proximity Placement Groups for low-latency VM placement.
- Combine with Managed Disks redundancy (ZRS/GRS where supported) and VM scale sets.

---

## ⚙️ Scaling & Orchestration
- Azure Virtual Machine Scale Sets (VMSS) for autoscaling identical VM instances.
- Scale based on metrics, schedule, or custom rules.
- VMSS supports orchestration modes and integration with load balancers.

---

## 🧰 Images, Extensions & Automation
- Base images: marketplace or custom images (Azure Compute Gallery).
- Use cloud-init (Linux) or Custom Script Extension / Desired State Configuration for provisioning.
- Extensions: VM Agent, Diagnostics, Backup, Antimalware, CustomScript.
- Automate deployments with ARM templates, Bicep, Terraform, or Azure CLI.

---

## 🔁 Backup & Disaster Recovery
- Use Azure Backup (Recovery Services vault) for VM-level backups (snapshot-based).
- Azure Site Recovery (ASR) for replication and orchestrated failover between regions.
- Define RPO/RTO targets and choose appropriate replication options (async/sync).

---

## 🔐 Security & Compliance
- Use Managed Identities for secure access to Key Vault and other services.
- Harden VMs: Just-in-time (JIT) VM access, NSGs, endpoint protection, update management.
- Use Azure Defender for Cloud to monitor vulnerabilities and security posture.
- Disk encryption: platform-managed or customer-managed keys via Key Vault.

---

## 📊 Monitoring & Diagnostics
- Install Azure Monitor VM agent and Dependency Agent for insights.
- Collect metrics, guest OS logs, performance counters, and alerts.
- Integrate with Log Analytics for queries and Workbooks for visualization.

---

## 💰 Pricing & Cost
- Billing based on VM size, OS, storage, networking, and licensing (bring-your-own or Azure Hybrid Benefit).
- Use spot (low-priority) VMs for interruptible workloads to reduce cost.
- Deallocate vs delete: deallocating stops compute billing but retains disks.

---

## 🧠 Exam Tips
- Know when to use VM vs PaaS offerings (control vs management overhead).
- Understand Availability Set vs Availability Zone and their SLA implications.
- VMSS is the recommended pattern for scalable stateless services.
- Use Managed Disks and Azure Backup for simple recovery; use ASR for orchestrated DR.
- Use Azure Hybrid Benefit and Reserved Instances to optimize costs.

---

## 📚 Reference
- [Azure Virtual Machines overview](https://learn.microsoft.com/azure/virtual-machines/)
- [VM sizing guidance](https://learn.microsoft.com/azure/virtual-machines/sizes)
- [Managed Disks documentation](https://learn.microsoft.com/azure/virtual-machines/disks-types)
