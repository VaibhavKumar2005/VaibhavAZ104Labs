# Lab 07 - Managing Azure Storage

## 📘 Lab Overview

In this lab, you will learn to:
- Create and configure Azure storage accounts
- Secure blob containers with access policies and lifecycle rules
- Create and manage Azure File shares
- Restrict storage access to a virtual network

> ⏱️ **Estimated time:** 50 minutes

---

## 🧭 Lab Scenario

Your organization stores infrequently accessed data on-premises. To optimize storage costs and explore security, redundancy, and network restrictions, you will use Azure Storage to:
- Migrate data to blob and file storage
- Apply lifecycle policies
- Use virtual networks for secure access

---

## 🛠️ Tasks

### **Task 1: Create and Configure a Storage Account**
1. **Create storage account** with the following:
   - **Performance**: Standard
   - **Redundancy**: Geo-redundant storage (GRS)
   - **Public access**: Disabled
2. Configure **firewall settings**:
   - Enable access from selected networks only
   - Add client IP
3. Configure **lifecycle management**:
   - Create rule `Movetocool` to move blobs after 30 days

📸 **Related screenshots**:
- `1. Search Storage Accounts.png`
- `2. Create Storage Accounts.png`
- `3. Specify Basics.png`
- `4. Public Network Disabled.png`
- `5. Specify Network Settings.png`
- `6. Create and Deploy.png`
- `10. Checking Redundancy.png`
- `11. Lifestyle Management.png`
- `12. Adding Rule on Lifestyle Management.png`

---

### **Task 2: Create and Configure Secure Blob Storage**
1. **Create a container** with private access.
2. **Add retention policy** of 180 days.
3. **Upload a file** and configure:
   - **Blob type**: Block blob
   - **Tier**: Hot
   - **Folder**: `securitytest`
4. **Verify access** using Blob SAS URL.

📸 **Related screenshots**:
- `13. Base Blob.png`
- `14. Clicking on Access Policy.png`
- `15. Data Container.png`
- `16. Click On Generate Accesss Key.png`
- `17. Generating SAS Key for the image uploaded.png`

---

### **Task 3: Create and Configure Azure File Storage**
1. **Create a file share** named `share1`
2. **Disable backup**
3. **Upload a file** using Storage Browser
4. **Restrict access** to storage from a **virtual network** only

📸 **Related screenshots**:
- `18. New File Share.png`
- `19. Disable Backup.png`
- `20. Selecting VNet.png`
- `21. Creating VNet basics.png`
- `22. Creating and Deploying VNet.png`

---

## 🧹 Cleanup

After completing the lab, delete the resource group to avoid ongoing charges.

```powershell
# PowerShell
Remove-AzResourceGroup -Name az104-rg7

# Azure CLI
az group delete --name az104-rg7
