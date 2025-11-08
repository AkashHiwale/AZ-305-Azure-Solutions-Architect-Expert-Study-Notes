# 🌐 Azure Web App (App Service)

Azure App Service (Web Apps) is a fully managed platform for building, deploying, and scaling web apps and APIs with support for multiple languages and frameworks.

---

## 🎯 Overview
- PaaS for hosting web apps, mobile backends, and RESTful APIs.
- Supports .NET, Java, Node.js, Python, PHP, and containers.
- Integrates with CI/CD (GitHub Actions, Azure DevOps) and developer tooling.

---

## 🧩 Hosting Plans & Tiers
- **Free / Shared** — Development/testing with limited features.
- **Basic (B)** — Dev/test workloads, no autoscale.
- **Standard (S)** — Autoscale, custom domains, backups.
- **Premium (P)** — Higher scale, VNet integration, dedicated compute.
- **Isolated (I)** — App Service Environment for network isolation and max scale.
- App Service Plan defines VM size and pricing; multiple apps can share a plan.

---

## 🛠 Deployment Options
- ZIP deploy, Run From Package
- Git/GitHub/GitHub Actions, Azure DevOps pipelines
- Docker containers from ACR or Docker Hub
- Deployment slots (staging/canary) — see deployment-slots note for details
- Slot swap for zero-downtime deployments

---

## 🔁 Scaling
- Vertical scale: change App Service Plan SKU.
- Horizontal scale: scale out to multiple instances (manual or autoscale rules).
- Autoscale based on metrics (CPU, memory, HTTP queue length) or schedule.
- Scale-per-slot consumes plan resources.

---

## 🔐 Networking & Security
- VNet Integration (outbound) for app to reach resources in VNet.
- Private Endpoints / Private Link via ASE or App Service Environment v2/v3 patterns.
- Authentication & Authorization (Easy Auth) — integrate with Microsoft Entra ID, social providers.
- Managed identities for accessing Key Vault and other resources.
- IP restrictions, access restrictions, and TLS (custom certs via App Service or App Service Managed Certificates).
- Always use HTTPS and restrict to minimum required inbound endpoints.

---

## 💾 Backup & Recovery
- Built-in backup (Standard and above) configurable per app with retention policies.
- App content vs backing up underlying storage/DBs — use Azure Backup for VM/DB workloads where applicable.
- App snapshots and slot-based rollback strategies.

---

## 📊 Monitoring & Diagnostics
- Integrates with Application Insights for telemetry, tracing, and performance.
- App Service diagnostics, logs (web server, application, detailed error messages).
- Metrics in Azure Monitor; alerts and autoscale rules based on those metrics.

---

## ✅ Use Cases
- Host web front-ends, REST APIs, and microservices (non-containerized or containerized).
- Mobile backends and serverless-like web workloads that require more control than Functions.
- Rapid CI/CD deployment patterns with staging and canary releases.

---

## 🧠 Exam Tips
- Know differences between App Service Plan tiers and when to use ASE (Isolated) vs Premium v3.
- Understand deployment slots, slot settings, and traffic routing for canary deployments.
- VNet Integration is outbound only; to secure inbound traffic use Private Endpoint patterns or ASE.
- Use Managed Identity + Key Vault to avoid storing secrets in app settings.
- Monitor apps with Application Insights and set alerts to trigger autoscale if needed.

---

## 📚 Reference
- [App Service overview](https://learn.microsoft.com/azure/app-service/overview)
- [App Service plans](https://learn.microsoft.com/azure/app-service/overview-hosting-plans)
- [Deploy to Azure App Service](https://learn.microsoft.com/azure/app-service/deploy-continuous-deployment)
- [VNet integration for App Service](https://learn.microsoft.com/azure/app-service/overview-vnet-integration)
