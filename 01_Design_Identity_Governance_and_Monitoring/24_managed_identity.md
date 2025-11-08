# 🔑 Managed Identities

Managed identities provide Azure services with an automatically managed identity in Microsoft Entra ID for authenticating to services that support Entra ID authentication.

---

## 📌 Types of Managed Identities

### 1. **System-assigned**
- Enabled directly on Azure service instance
- Lifecycle tied to resource
- Automatically deleted when resource is deleted

### 2. **User-assigned**
- Created as standalone Azure resource
- Can be assigned to multiple resources
- Independent lifecycle management

---

## 🛠️ Implementation Examples

```azurecli
# Enable system-assigned managed identity
az vm identity assign \
    --resource-group myResourceGroup \
    --name myVM \
    --identities [system]

# Create user-assigned managed identity
az identity create \
    --resource-group myResourceGroup \
    --name myManagedIdentity
```

---

## 🔄 Common Use Cases

- **Key Vault** access
- **Storage Account** access
- **SQL Database** authentication
- **Service Bus** messaging
- **Event Hub** publishing

---

## 🧠 Exam Tips

- Know differences between system and user-assigned
- Understand lifecycle management
- Remember supported services
- Know how to assign roles to managed identities

---

## 📚 Reference

- [Managed Identities overview](https://learn.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview)
- [Using managed identities](https://learn.microsoft.com/azure/active-directory/managed-identities-azure-resources/howto-use-managed-identities)
