# Lab 07 – Managing Azure Storage (AZ-104)

## 📘 Overview

This lab demonstrates hands-on experience with Azure Storage services as part of the
AZ-104 Microsoft Azure Administrator learning path.

The focus is on secure storage configuration, lifecycle management, and network-restricted access.

---

## 📸 Screenshots

![Search storage accounts](./01-search-storage-accounts.png)

![Create storage account](./02-create-storage-account.png)

![Specify basics](./03-specify-basics.png)

![Public network disabled](./04-public-network-disabled.png)

![Lifecycle management](./11-lifecycle-management.png)

![Generate SAS](./17-generate-sas.png)

![Create file share](./18-new-file-share.png)

![Create VNet](./22-create-deploy-vnet.png)

---

## 🧹 Cleanup

```powershell
Remove-AzResourceGroup -Name az104-rg7
