# 🚀 Azure Web App — Deployment Slots

Deployment slots are live app instances with their own hostnames that you can swap with the production slot to perform zero‑downtime deployments and testing in production-like environments.

---

## 🎯 What are Deployment Slots?
- Each Web App can have multiple slots (e.g., staging, testing, production).
- Slots run the same app code but can have different configurations and app settings.
- Swap operation exchanges content and configuration between slots with warm-up and swap-swap steps to minimize downtime.

---

## 🛠 Key Features
- Zero-downtime deployments via slot swap (warm-up before swap).
- Traffic routing: route a percentage of production traffic to a slot for testing (A/B testing/canary).
- Slot-specific app settings and connection strings (mark settings as "slot setting" to avoid being swapped).
- Swap with preview: validate a slot before completing swap (auto-swap behavior).
- Integration with CI/CD (GitHub Actions, Azure DevOps) for automated slot deploys.

---

## 🔧 Deployment & Management Notes
- Create slots in the App Service → Deployment slots blade.
- Use "Swap" to move a slot into production; swap process:
  1. Warm up target slot (optional warm-up actions).
  2. Swap site routing and (if configured) settings that are not marked as slot-specific.
  3. Post-swap warm-up for the new slot.
- Mark app settings and connection strings as "slot setting" to keep them sticky to the slot.
- When using slots with slot-specific hostnames, update DNS/traffic manager only for production hostnames.
- Be aware of resource usage: slots consume App Service plan resources (scale accordingly).

---

## ✅ Use Cases
- Staging validation before production release.
- Canary deployments by routing % traffic to a slot.
- Testing configuration differences (e.g., connection strings) without impacting prod.
- Quick rollback by swapping back to previous slot.

---

## 🧠 Exam Tips
- Understand slot behavior for app settings (slot vs. non-slot settings).
- Know how traffic routing to slots enables canary and A/B testing.
- Remember slots consume App Service plan compute — consider cost and scaling.
- Swap is atomic for routing but configuration swaps depend on slot-setting flags; misconfigured slot settings can cause outages after swap.
- Use Swap with Preview and warm-up routines for safer deployments.

---

## 📚 Reference
- [Deployment slots - Azure App Service](https://learn.microsoft.com/azure/app-service/deploy-staging-slots)
- [Swap with preview and warm-up](https://learn.microsoft.com/azure/app-service/deploy-staging-slots#swap-with-preview)
