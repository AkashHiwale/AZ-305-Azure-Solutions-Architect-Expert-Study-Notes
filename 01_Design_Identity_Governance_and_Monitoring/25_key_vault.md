# 🔑 Azure Key Vault

Azure Key Vault is a cloud service for securely storing and accessing secrets, keys, and certificates.

---

## 🎯 Key Features

### 1. **Secret Management**
- Store and control access to tokens, passwords, certificates, API keys
- Secrets backed by Hardware Security Modules (HSMs)
- Centralized secret management

### 2. **Key Management**
- Create and control encryption keys
- Key operations performed within vault boundaries
- Support for HSM-protected keys

### 3. **Certificate Management**
- Provision, manage, and deploy public/private SSL/TLS certificates
- Integration with supported certificate authorities
- Certificate lifecycle management

---

## 🔐 Security Features

- **RBAC Integration**: Fine-grained access control
- **Soft Delete**: Recovery of deleted vaults/secrets
- **Purge Protection**: Prevent permanent deletion
- **Logging**: Azure Monitor integration
- **Private Endpoints**: Network isolation

---

## 🛠️ Implementation Examples

```bash
# Create Key Vault
az keyvault create \
    --name "myVault" \
    --resource-group "myRG" \
    --location "eastus"

# Add secret
az keyvault secret set \
    --vault-name "myVault" \
    --name "DBPassword" \
    --value "mySecretPassword123"
```

---

## 🧠 Exam Tips

- Know difference between **soft-delete** and **purge protection**
- Understand **access policies** vs **RBAC**
- Remember **backup/restore** capabilities
- Know integration with **managed identities**

---

## 📚 Reference

- [Azure Key Vault documentation](https://learn.microsoft.com/azure/key-vault/general/)
- [Key Vault security features](https://learn.microsoft.com/azure/key-vault/general/security-features)
