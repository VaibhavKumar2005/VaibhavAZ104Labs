# Lab 09b - Implement Azure Container Instances

## Introduction
In this lab, you learn how to implement and deploy **Azure Container Instances** (ACI).  

This lab requires an Azure subscription. Your subscription type may affect the availability of features in this lab. You may change the region, but the steps are written using **East US**.  

**Estimated timing:** 15 minutes  

---

## Scenario
Your organization has a web application that currently runs on a virtual machine in your on-premises data center. The organization wants to move all applications to the cloud but doesn’t want to manage a large number of servers.  

You decide to evaluate **Azure Container Instances** and **Docker** as a solution.  

---

## Architecture Diagram
![Architecture Diagram](images/architecture-diagram.png)

---

## Job Skills
- **Task 1:** Deploy an Azure Container Instance using a Docker image.  
- **Task 2:** Test and verify deployment of an Azure Container Instance.  

---

## Task 1: Deploy an Azure Container Instance using a Docker image

1. **Sign in to the Azure portal**  
   [https://portal.azure.com](https://portal.azure.com)  

   ![Azure Portal](images/01-azure-portal.png)

2. **Search for Container Instances** and select **+ Create**.  

   ![Create Container Instance](images/02-create-container-instance.png)

3. **Basics Tab Settings:**  

   | Setting         | Value                                                   |
   |-----------------|---------------------------------------------------------|
   | Subscription    | Your Azure subscription                                 |
   | Resource group  | `az104-rg9` (or Create new)                             |
   | Container name  | `az104-c1`                                              |
   | Region          | East US (or region near you)                            |
   | Image source    | Quickstart images                                       |
   | Image           | `mcr.microsoft.com/azuredocs/aci-helloworld:latest`     |

   ![Basics Tab](images/03-basics-tab.png)

4. **Networking Tab:**  
   - DNS name label → any valid, globally unique name  

   ![Networking](images/04-networking.png)

5. **Monitoring Tab:**  
   - Uncheck **Enable container instance logs**  

   ![Monitoring](images/05-monitoring.png)

6. **Review + Create** → Wait for deployment (~2–3 min).  

   ![Review Create](images/06-review-create.png)

---

## Task 2: Test and Verify Deployment

1. After deployment, click **Go to resource**.  

   ![Go to Resource](images/07-go-to-resource.png)

2. On the **Overview blade**, verify status = **Running**.  

   ![ACI Overview](images/08-aci-overview.png)

3. Copy the **FQDN**, open in a browser →  
   Confirm the **Welcome to Azure Container Instance** page.  

   ![Web App Running](images/09-webapp.png)

4. In the **Container → Logs** section, verify log entries (HTTP GET requests).  

   ![Container Logs](images/10-logs.png)

---

## Cleanup
To avoid charges, delete the resources after completing the lab:

- **Azure Portal:**  
  - Delete the **resource group**.  
- **PowerShell:**  
  ```powershell
  Remove-AzResourceGroup -Name resourceGroupName
