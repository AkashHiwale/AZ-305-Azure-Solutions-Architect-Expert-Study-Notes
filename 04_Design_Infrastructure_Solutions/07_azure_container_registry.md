# 🏷️ Azure Container Registry (ACR)

Private, managed container registry for storing and managing Docker/OCI images with enterprise features.

---

## ▶ Key Features
- Private OCI/Docker registry, AAD auth, RBAC
- ACR Tasks (image build/patch automation), geo-replication, retention policies
- Content-signing and vulnerability scanning integration

---

## ▶ Design Notes
- Use ACR geo-replication for multi-region deployments
- Use service principals or managed identities for secure AKS/ACI pulls

---

## 🧠 Exam Tips
- Prefer AAD-based auth and Task automation; use geo-replication to reduce latency.

---

## 📚 Reference
- [Azure Container Registry](https://learn.microsoft.com/azure/container-registry/)
