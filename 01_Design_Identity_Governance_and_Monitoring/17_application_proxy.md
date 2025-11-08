# 🌐 Azure Application Proxy

Azure Application Proxy is a feature of Microsoft Entra ID that enables secure remote access to on-premises web applications without requiring VPN connectivity.

---

## 🎯 Key Benefits

- **Secure remote access** without VPN
- **No DMZ** required
- **Single Sign-On (SSO)** capability
- **Conditional Access** support
- **Pre-authentication** with Microsoft Entra ID

---

## 🧩 Components

### 1. **Connector**
- Lightweight agent installed on Windows Server
- Handles outbound connections to Azure
- Can be installed on multiple servers for high availability
- No inbound ports needed

### 2. **External Endpoint**
- Azure-hosted endpoint for user access
- Format: `https://app-name.msappproxy.net`
- Can use custom domain

### 3. **Application Configuration**
- Pre-authentication settings
- URL settings
- Cookie settings
- Connector group assignment

---

## 🛠️ Implementation Steps

1. **Enable Application Proxy**
   ```powershell
   # First, install the connector
   # Then register it in Azure AD
   Connect-AzureAD
   Set-AzureADApplicationProxyApplication
   ```

2. **Install Connector**
   - Download from Azure portal
   - Install on Windows Server
   - Register with Microsoft Entra ID

3. **Configure Applications**
   - Internal URL
   - External URL
   - Pre-authentication method
   - Connector group selection

---

## 🔒 Security Features

- **Pre-authentication**
  - Microsoft Entra ID
  - Pass-through
  - None (not recommended)

- **Conditional Access**
  - Device compliance
  - Location-based access
  - MFA requirements

---

## 🧠 Exam Tips

- Know the **components** (Connector, Endpoint, Configuration)
- Understand **pre-authentication options**
- Remember: No inbound ports needed
- Application Proxy requires **Premium P1 license**
- Can integrate with **existing load balancers**

---

## 📚 Reference

- [Azure Application Proxy documentation](https://learn.microsoft.com/azure/active-directory/app-proxy/application-proxy)
- [Application Proxy security](https://learn.microsoft.com/azure/active-directory/app-proxy/application-proxy-security)
