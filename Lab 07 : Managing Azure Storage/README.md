# Lab 07 – Managing Azure Storage (AZ-104)

## 📘 Overview

This lab documents hands-on experience with **Azure Storage services** as part of the  
**AZ-104: Microsoft Azure Administrator** learning path.

The objective of this lab is to demonstrate how Azure Storage can be configured for
**security, cost optimization, redundancy, and network-restricted access** in an
enterprise-style scenario.

---

## 🧭 Scenario Context

Organizations often store large volumes of infrequently accessed data on-premises.
This lab simulates migrating such data to Azure in order to:

- Reduce storage costs using lifecycle policies
- Improve availability using redundancy options
- Secure access using network and access controls
- Centralize blob and file storage

---

## 🧩 Azure Services Demonstrated

- Azure Storage Account  
- Blob Storage  
- Azure File Shares  
- Lifecycle Management  
- Shared Access Signatures (SAS)  
- Virtual Networks (VNet)  
- Storage Firewall Rules  

---

## 📸 Visual Evidence

### Storage Account & Networking

![Search Storage Accounts](01.%20Search%20Storage%20Accounts.png)

![Create Storage Accounts](02.%20Create%20Storage%20Accounts.png)

![Specify Basics](03.%20Specify%20Basics.png)

![Public Network Disabled](04.%20Public%20Network%20Disabled.png)

![Specify Network Settings](05.%20Specify%20Network%20Settings.png)

![Create and Deploy](06.%20Create%20and%20Deploy.png)

![Reaching Networking](08.%20Reaching%20on%20Networking.png)

![Disable Public Networks](09.%20Disable%20public%20Networks.png)

![Checking Redundancy](10.%20Checking%20Redundancy.png)

---

### Lifecycle Management

![Lifecycle Management](11.%20Lifestyle%20Management.png)

![Add Lifecycle Rule](12.%20Adding%20Rule%20on%20Lifestyle%20Management.png)

---

### Blob Storage & Access Control

![Base Blob](13.%20Base%20Blob.png)

![Access Policy](14.%20Clicking%20on%20Access%20Policy.png)

![Data Container](15.%20Data%20Container.png)

![Generate Access Key](16.%20Click%20On%20Generate%20Access%20Key.png)

![Generate SAS](17.%20Generating%20SAS%20Key%20for%20the%20image%20uploaded.png)

---

### Azure File Share & Virtual Network

![New File Share](18.%20New%20File%20Share.png)

![Disable Backup](19.%20Disable%20Backup.png)

![Selecting VNet](20.%20Selecting%20VNet.png)

![Creating VNet Basics](21.%20Creating%20VNet%20basics.png)

![Create and Deploy VNet](22.%20Creating%20and%20Deploying%20VNet.png)

---

## 🧠 Key Learnings

- Azure Storage offers granular control over security and access
- Lifecycle policies help reduce long-term storage costs
- Network restrictions significantly improve storage security
- SAS tokens enable secure, temporary access without exposing credentials
- Integrating storage with VNets aligns with enterprise security practices

---

## 🧹 Resource Cleanup

All resources created during this lab were deleted after completion to avoid unnecessary costs.

```powershell
Remove-AzResourceGroup -Name az104-rg7
