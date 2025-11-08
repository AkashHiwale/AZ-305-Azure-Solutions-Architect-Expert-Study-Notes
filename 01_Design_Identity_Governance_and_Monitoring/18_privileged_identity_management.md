# 👑 Privileged Identity Management (PIM)

Microsoft Entra Privileged Identity Management (PIM) helps minimize the number of people who have access to resources by providing **just-in-time privileged access** with time limits and approval requirements.

---

## 🎯 Key Features

- **Just-In-Time Access**: Temporary elevation of privileges
- **Time-Bound Access**: Set start/end times for role activation
- **Approval Workflow**: Require approval for role activation
- **Audit History**: Track role assignments and activations
- **MFA Requirement**: Enforce additional verification
- **Notifications**: Alert when roles are activated

---

## 🔑 What Can PIM Manage?

- **Microsoft Entra ID Roles**
  - Global Administrator
  - Security Administrator
  - Exchange Administrator
  
- **Azure Resource Roles**
  - Subscription Owner
  - Resource Group Contributor
  - Key Vault Administrator

---

## 📋 Assignment Types

1. **Eligible Assignments**
   - Users must activate role when needed
   - Requires justification/approval
   - Time-limited access

2. **Active Assignments**
   - Traditional permanent assignments
   - No activation required
   - Used for break-glass accounts

---

## 🛠️ Configuration Steps

1. **Enable PIM**
   ```powershell
   Enable-AzureADPrivilegedIdentityManagement
   ```

2. **Configure Role Settings**
   - Maximum activation duration
   - Approval requirements
   - Notification settings
   - MFA requirements

3. **Make Role Assignments**
   - Assign users as eligible
   - Set time bounds
   - Define approvers

---

## 🧠 Exam Tips

- PIM requires **Microsoft Entra ID P2** license
- Know difference between **eligible** and **active** assignments
- Understand **approval workflows** and **activation process**
- Remember PIM supports both **Entra ID** and **Azure resource** roles
- Be familiar with **break-glass account** scenarios

---

## 📚 Reference

- [Azure PIM documentation](https://learn.microsoft.com/entra/id-governance/privileged-identity-management/pim-configure)
- [PIM security best practices](https://learn.microsoft.com/entra/id-governance/privileged-identity-management/pim-security-wizard)
