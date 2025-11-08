# 🧮 Azure Batch

Azure Batch is a managed service for running large-scale parallel and high-performance computing (HPC) batch jobs in Azure. It provisions and manages compute resources, schedules jobs and tasks, and handles orchestration so you can focus on workload logic.

---

## 🎯 Overview
- Managed job scheduling and cluster management for batch and HPC workloads.
- Handles provisioning of VMs (compute nodes), job/task execution, retries, and teardown.
- Integrates with Azure Storage for input/output staging and supports containers.

---

## 🛠 Key Concepts
- **Pool**: A collection of compute nodes (VMs) that run tasks.  
- **Compute node**: Individual VM in a pool.  
- **Job**: A container for tasks, representing a unit of work.  
- **Task**: Single unit of work executed on a compute node.  
- **Job schedule**: Definition to run jobs on a recurring basis.

---

## ⚙️ Features & Capabilities
- Automatic provisioning and autoscaling of pools.  
- Support for Linux and Windows nodes; provision from Marketplace or custom images.  
- Low-priority (spot) VMs to reduce cost.  
- Container support (run tasks in Docker containers from ACR/Docker Hub).  
- Task dependencies, retries, and exit conditions.  
- Integration with Azure Storage for input/output staging (SAS support).

---

## 🔧 Job Orchestration & Execution
- Submit jobs via Portal, Azure CLI, REST API, or SDKs (.NET, Python, Java).  
- Use job preparation tasks to install dependencies and configure nodes before tasks run.  
- Tasks can upload output files to Blob Storage using outputFile settings.  
- Use constraints (max wall-clock time, max retries) to handle failures and timeouts.

---

## 📈 Autoscaling & Sizing
- Autoscale pools based on queued tasks, custom metrics or formulas.  
- Choose VM sizes for CPU, memory, GPU and storage I/O needs.  
- Combine dedicated and low-priority nodes for cost/performance balance.  
- Consider provisioning time, regional quotas, and data locality when designing autoscale rules.

---

## 🔒 Security & Networking
- Use Managed Identity to grant Batch jobs access to Key Vault or Storage without secrets.  
- Deploy Batch pools into a VNet for private access to internal resources.  
- Use Private Endpoints for Storage to avoid public endpoints.  
- Keep secrets in Key Vault and fetch at runtime via managed identity.

---

## 📊 Monitoring & Diagnostics
- Collect stdout/stderr and task logs; upload to Blob Storage for analysis.  
- Integrate with Azure Monitor for metrics and alerts (pool utilization, queued tasks, failed tasks).  
- Use Batch metrics and job/task logs to troubleshoot failures and performance issues.

---

## ✅ Common Use Cases
- Media rendering and transcoding.  
- Large-scale simulations and scientific computing.  
- Distributed ETL and batch data processing.  
- Batch ML model training and inference (non-real-time).

---

## 🧠 Exam Tips
- Understand the pool → job → task model and lifecycle.  
- Know autoscale policies and the cost trade-offs of low-priority (spot) VMs.  
- Use managed identities + Key Vault to avoid embedding secrets.  
- Plan for input/output staging to Storage and VNet isolation for secure production workloads.  
- Batch is intended for batch/HPC workloads, not low-latency interactive services.

---

## 📚 Reference
- [Azure Batch documentation](https://learn.microsoft.com/azure/batch/)
- [Autoscale pools in Azure Batch](https://learn.microsoft.com/azure/batch/batch-autoscale-overview)
