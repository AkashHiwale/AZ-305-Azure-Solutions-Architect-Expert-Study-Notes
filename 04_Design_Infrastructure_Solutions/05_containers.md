# 🐳 Containers (Overview & Azure Options)

Containers package applications and dependencies into lightweight, portable images. They enable consistent deployment across environments and support microservices and cloud-native architectures.

---

## 🎯 Key Concepts
- **Image**: Immutable filesystem and configuration (built from Dockerfile or OCI-compliant tools).
- **Container**: Running instance of an image.
- **Registry**: Stores images (e.g., Azure Container Registry - ACR, Docker Hub).
- **Orchestration**: Scheduling, scaling, networking, and lifecycle (e.g., Kubernetes).

---

## 🔧 Container Runtimes & Image Formats
- Common runtimes: containerd, Docker Engine.
- Image format: OCI image spec (compatible with Docker images).
- Build tools: Docker, BuildKit, Podman, Kaniko (for CI/CD).

---

## 🏗 Azure Hosting Options
- **Azure Kubernetes Service (AKS)**  
  - Fully managed Kubernetes control plane.  
  - Use for production-grade orchestration, autoscaling, networking (Calico/Azure CNI), and integrations (Ingress, Service Mesh).  
- **Azure Container Instances (ACI)**  
  - Serverless containers, fast start, per-second billing.  
  - Best for burst, task-based, or simple container runs without orchestration.  
- **App Service for Containers**  
  - PaaS for single-container or multi-container (Docker Compose) apps.  
  - Easier for web apps needing PaaS features (deploy slots, auth).  
- **Azure Container Apps**  
  - Serverless, managed container hosting with Dapr and KEDA for event-driven scaling. Good for microservices without managing Kubernetes control plane.  
- **Azure Red Hat OpenShift (ARO)**  
  - Managed OpenShift for enterprise Kubernetes with Red Hat support.
- **AKS + Virtual Nodes (ACI integration)** for bursty scale.

---

## 🧰 Registries & Image Management
- **Azure Container Registry (ACR)**: private registry with geo-replication, content trust, and tasks for image builds.
- Use ACR Tasks or CI pipelines to build and push images.
- Enable image scanning (Microsoft Defender for Cloud integration) and vulnerability assessment.

---

## 🌐 Networking & Service Exposure
- AKS networking options: Kubenet vs Azure CNI (pod IPs on VNet).
- Use Ingress (NGINX / Application Gateway Ingress Controller) or Azure Load Balancer for traffic routing.
- Secure inbound with Application Gateway WAF, Private Link, or internal load balancers.
- Use Network Policies (Calico) for pod-level network controls.

---

## 💾 Storage & State
- Ephemeral containers vs stateful apps: use Persistent Volumes (Azure Disks, Azure Files) for state.
- Use ReadWriteOnce (disks) or ReadWriteMany (Azure Files) depending on access patterns.
- Consider blob-backed object stores for large unstructured data.

---

## 🔒 Security & Identity
- Image security: scan images, sign images (content trust), minimize base image footprint.
- Secrets: integrate with Azure Key Vault; use Kubernetes secrets with proper RBAC.
- Use Managed Identities / Pod Identity (Azure AD Workload Identity) for pod-to-Azure-service auth.
- Enforce RBAC, Pod Security Standards/Policies, and Azure Policy for AKS.

---

## ⚙️ CI/CD & Immutable Deployments
- Build images in CI (GitHub Actions, Azure DevOps), push to ACR, deploy to AKS/ACI/App Service.
- Use GitOps (Flux/ArgoCD) for declarative deployments.
- Use image tags and immutable artifact promotion (avoid latest in prod).

---

## 📊 Monitoring & Observability
- Use Azure Monitor for containers (container insights) + Log Analytics for metrics/logs.
- Application-level telemetry via Application Insights.
- Use Prometheus/Grafana in AKS for Kubernetes-native metrics and alerting.

---

## ✅ Use Cases & Decision Guidance
- Use **AKS** for complex microservices, multi-container orchestration, and production workloads.
- Use **ACI** for simple, short-lived tasks or burst capacity.
- Use **Container Apps** for serverless microservices without Kubernetes management.
- Use **App Service for Containers** for web workloads that benefit from PaaS features.

---

## 🧠 Exam Tips
- Know differences between AKS, ACI, Container Apps, and App Service for Containers.
- Understand networking choices (kubenet vs Azure CNI) and impact on VNet integration.
- Remember storage types for containers (Azure Disk vs Azure Files) and access modes.
- Use ACR with geo-replication and tasks for reliable image distribution and CI integration.
- Secure images and runtimes: scanning, minimal base images, and managed identities for auth.

---

## 📚 Reference
- [Azure Kubernetes Service (AKS)](https://learn.microsoft.com/azure/aks/)
- [Azure Container Instances (ACI)](https://learn.microsoft.com/azure/container-instances/)
- [Azure Container Apps](https://learn.microsoft.com/azure/container-apps/)
- [Azure Container Registry (ACR)](https://learn.microsoft.com/azure/container-registry/)
