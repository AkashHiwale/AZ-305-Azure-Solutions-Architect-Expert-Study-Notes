# 📜 Azure Policy

Azure Policy helps enforce organizational standards and assess compliance at scale across your Azure environment.

---

## 🎯 Key Concepts

- **Policy Definition**: Rule for resource creation/management
- **Initiative Definition**: Collection of policy definitions
- **Assignment**: Application of policy/initiative to scope
- **Compliance**: Resource state vs policy rules
- **Remediation**: Corrective action for non-compliant resources

---

## 📋 Common Policy Types

| Type | Example |
|------|---------|
| **Allow/Deny** | Restrict VM sizes |
| **Append** | Add required tags |
| **Audit** | Check encryption status |
| **DeployIfNotExists** | Enable diagnostic settings |
| **Modify** | Add network security rules |

---

## 🛠️ Implementation Example

```json
{
    "if": {
        "allOf": [{
            "field": "type",
            "equals": "Microsoft.Storage/storageAccounts"
        },
        {
            "field": "Microsoft.Storage/storageAccounts/networkAcls.defaultAction",
            "notEquals": "Deny"
        }]
    },
    "then": {
        "effect": "deny"
    }
}
```

---

## 🧠 Exam Tips

- Know different **policy effects** (Deny, Audit, Append, etc.)
- Understand **inheritance** in policy assignments
- Remember built-in policies vs custom policies
- Know how to use **initiatives** for multiple policies

---

## 📚 Reference

- [Azure Policy documentation](https://learn.microsoft.com/azure/governance/policy/)
- [Built-in policy definitions](https://learn.microsoft.com/azure/governance/policy/samples/built-in-policies)
