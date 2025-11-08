# 📱 Application Objects in Microsoft Entra ID

An **application object** is the global representation of an application in Microsoft Entra ID (formerly Azure AD). It serves as the template from which **service principals** (application instances) are created.

---

## 🧩 Key Components

### 1. **Application Objects**
- Global representation of your application
- Stores app configuration:
  - Name and logo
  - Reply URLs
  - Secrets/certificates
  - API permissions
  - User consent settings

### 2. **Service Principals**
- Local representation of app in specific tenant
- Created from application object
- Types:
  - Application service principal
  - Managed identity
  - Legacy

### 3. **Managed Identities**
- Automatically managed service principals
- Types:
  - System-assigned: Tied to resource lifecycle
  - User-assigned: Independent lifecycle

---

## 🛠️ Common Operations

### Application Registration
```powershell
# Create new app registration
az ad app create --display-name "MyApp" --web-redirect-uris "https://myapp.com"

# Create service principal
az ad sp create --id <application-id>
```

### Managed Identity
```bash
# Enable system-assigned
az webapp identity assign --name MyWebApp --resource-group MyRG

# Create user-assigned
az identity create --name MyManagedId --resource-group MyRG
```

---

## 🔑 Authentication Flow

1. App registration created in Entra ID
2. Service principal created in tenant
3. App authenticates using:
   - Client secret
   - Certificate
   - Managed identity

---

## 🧠 Exam Tips

- Know the difference between:
  - Application objects (global) vs Service principals (local)
  - System-assigned vs User-assigned managed identities
- Understand when to use:
  - Client secrets vs certificates
  - Managed identities vs service principals
- Remember managed identity benefits:
  - No credential management
  - Automatic rotation
  - Better security

---

## 📚 Reference

- [Application objects and service principals](https://learn.microsoft.com/azure/active-directory/develop/app-objects-and-service-principals)
- [Managed identities overview](https://learn.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview)
