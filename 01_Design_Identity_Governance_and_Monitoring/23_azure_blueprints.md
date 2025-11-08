# 📘 Azure Blueprints

Azure Blueprints enables standardized cloud deployments and governance by packaging various Azure components together.

---

## 🎯 Key Components

- **Artifacts**: Building blocks of a blueprint
  - Role assignments
  - Policy assignments
  - ARM templates
  - Resource groups

---

## 🧩 Blueprint Structure

- **Blueprint Definition**: Template of what should be deployed
- **Blueprint Assignment**: Instance of blueprint applied to a scope
- **Blueprint Version**: Supports versioning for tracking changes

---

## 🛠️ Implementation Example

```json
{
    "properties": {
        "parameters": {
            "location": {
                "type": "string",
                "defaultValue": "eastus"
            }
        },
        "resourceGroups": {
            "storageRG": {
                "name": "storage-rg",
                "location": "[parameters('location')]"
            }
        }
    }
}
```

---

## 🆚 Blueprints vs. ARM Templates

| Feature | Blueprints | ARM Templates |
|---------|------------|---------------|
| Scope | Multiple subscriptions | Single subscription |
| Relationship | Maintained with resources | One-time deployment |
| Versioning | Built-in | Manual |
| Orchestration | Multiple artifact types | Resources only |

---

## 🧠 Exam Tips

- Know difference between **blueprint definition** and **assignment**
- Understand **versioning** and **updating** blueprints
- Remember blueprints can work across **multiple subscriptions**
- Know supported **artifact types**

---

## 📚 Reference

- [Azure Blueprints documentation](https://learn.microsoft.com/azure/governance/blueprints/)
- [Blueprint samples](https://learn.microsoft.com/azure/governance/blueprints/samples/)
