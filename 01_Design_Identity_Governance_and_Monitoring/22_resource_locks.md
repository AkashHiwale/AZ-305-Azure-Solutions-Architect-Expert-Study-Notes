# 🔒 Azure Resource Locks

Resource locks prevent accidental deletion or modification of Azure resources. They provide an additional layer of protection for critical resources.

---

## 🎯 Types of Locks

1. **ReadOnly (CanNotDelete)**
   - Can read but cannot modify/delete
   - Prevents any changes to resource

2. **Delete**
   - Can modify but cannot delete
   - Prevents accidental deletion

---

## 🔑 Key Points

- Locks can be applied at:
  - Subscription level
  - Resource group level
  - Individual resource level
- Child resources inherit locks
- Even owners need to remove lock first before deletion
- Requires appropriate RBAC permissions

---

## 🛠️ Implementation Examples

```azurecli
# Add delete lock to resource group
az lock create --name LockGroup --lock-type CanNotDelete \
    --resource-group MyResourceGroup

# Add read-only lock to storage account
az lock create --name StorageLock --lock-type ReadOnly \
    --resource-group MyResourceGroup \
    --resource-name mystorageaccount \
    --resource-type Microsoft.Storage/storageAccounts
```

---

## 🧠 Exam Tips

- Know difference between **DeleteLock** and **ReadOnlyLock**
- Understand **inheritance** of locks
- Remember locks override RBAC permissions
- Know how to manage locks using Portal, CLI, PowerShell

---

## 📚 Reference

- [Azure Resource Locks documentation](https://learn.microsoft.com/azure/azure-resource-manager/management/lock-resources)
