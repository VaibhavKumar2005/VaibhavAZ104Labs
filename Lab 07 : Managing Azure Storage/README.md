# Lab 07 – Managing Azure Storage (AZ-104)

## 📘 Overview

This lab showcases hands-on experience with **Azure Storage services** as part of the  
**AZ-104: Microsoft Azure Administrator** learning path.

The focus of this lab is on designing **secure, cost-efficient, and network-restricted storage solutions** using Azure-native features. It demonstrates how storage accounts can be configured for enterprise use cases involving controlled access, redundancy, and lifecycle automation.

> ⏱️ Estimated lab duration: ~50 minutes  
> ☁️ Platform: Microsoft Azure

---

## 🧭 Scenario Context

Organizations often maintain large volumes of **infrequently accessed data** on-premises.  
This lab simulates migrating such data to Azure to achieve:

- Lower storage costs using tiered storage and lifecycle policies
- Improved durability through Azure redundancy options
- Strong security using network and access controls
- Centralized blob and file storage for structured access

---

## 🧩 Azure Services & Features Demonstrated

- Azure Storage Account
- Blob Storage
- Azure File Shares
- Lifecycle Management Policies
- Shared Access Signatures (SAS)
- Virtual Networks (VNet)
- Storage Firewall & Network Rules

---

## 🔍 Implementation Highlights

### 🔹 Storage Account Design
- Standard performance storage account
- Geo-redundant storage (GRS) for resilience
- Public access disabled to minimize exposure
- Network rules applied to allow only trusted access

### 🔹 Lifecycle Management
- Automated policy to move blobs to a cooler tier after 30 days
- Demonstrates cost optimization for long-term data retention

### 🔹 Secure Blob Storage
- Private blob containers
- Retention policy for governance
- SAS tokens used to validate controlled, time-bound access

### 🔹 Azure File Storage with Network Isolation
- Azure File Share created for centralized file access
- Backup disabled for cost control in this scenario
- Access restricted to a Virtual Network only

---

## 📸 Visual Evidence

### Storage Account & Networking
![Search storage accounts](./01-search-storage-accounts.png)
![Create storage account](./02-create-storage-account.png)
![Specify basics](./03-specify-basics.png)
![Public network disabled](./04-public-network-disabled.png)
![Specify network settings](./05-specify-network-settings.png)
![Create and deploy](./06-create-and-deploy.png)
![Reach networking](./08-reach-networking.png)
![Disable public networks](./09-disable-public-networks.png)
![Check redundancy](./10-checking-redundancy.png)

### Lifecycle Management
![Lifecycle management](./11-lifecycle-management.png)
![Add lifecycle rule](./12-add-lifecycle-rule.png)

### Blob Storage & Access Control
![Base blob](./13-base-blob.png)
![Access policy](./14-access-policy.png)
![Data container](./15-data-container.png)
![Generate access key](./16-generate-access-key.png)
![Generate SAS](./17-generate-sas.png)

### Azure File Share & Virtual Network
![New file share](./18-new-file-share.png)
![Disable backup](./19-disable-backup.png)
![Select VNet](./20-selecting-vnet.png)
![Create VNet basics](./21-create-vnet-basics.png)
![Create and deploy VNet](./22-create-deploy-vnet.png)

---

## 🧠 Key Learnings

- Azure Storage provides fine-grained control over security and access
- Lifecycle policies are essential for long-term cost optimization
- Network-level restrictions significantly reduce attack surface
- SAS tokens allow secure sharing without exposing credentials
- Storage integration with VNets aligns with enterprise security practices

---

## 🧹 Resource Cleanup

All resources created during this lab were removed after completion to prevent unnecessary costs.

```powershell
# PowerShell
Remove-AzResourceGroup -Name az104-rg7

# Azure CLI
az group delete --name az104-rg7
