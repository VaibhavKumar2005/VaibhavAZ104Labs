# Lab 09b - Implement Azure Container Instances

## Introduction
In this lab, you learn how to implement and deploy **Azure Container Instances** (ACI).  
This lab requires an Azure subscription. Your subscription type may affect feature availability. The steps assume **East US**.  
**Estimated timing:** 15 minutes

---

## Scenario
Your organization runs a web app on-premises and wants to move to the cloud with minimal server overhead. You choose **Azure Container Instances** (ACI) and Docker.

---

## Architecture Diagram
![Architecture Diagram](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/architecture-diagram.png)

---

## Job Skills
- **Task 1:** Deploy an Azure Container Instance using a Docker image.  
- **Task 2:** Test and verify deployment of an Azure Container Instance.

---

## Task 1: Deploy an Azure Container Instance using a Docker image

1. **Sign in to the Azure portal**  
   [https://portal.azure.com](https://portal.azure.com)  

   ![Azure Portal](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/01-azure-portal.png)

2. **Search for Container Instances** and click **+ Create**.  

   ![Create Container Instance](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/02-create-container-instance.png)

3. **Basics Tab Settings:**

   | Setting         | Value                                                   |
   |-----------------|---------------------------------------------------------|
   | Subscription    | Your Azure subscription                                 |
   | Resource group  | `az104-rg9` (or create new)                             |
   | Container name  | `az104-c1`                                              |
   | Region          | East US (or nearby)                                    |
   | Image source    | Quickstart images                                       |
   | Image           | `mcr.microsoft.com/azuredocs/aci-helloworld:latest`     |

   ![Basics Tab](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/03-basics-tab.png)

4. **Networking Tab:** Set DNS name label to a unique value.

   ![Networking](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/04-networking.png)

5. **Monitoring Tab:** Uncheck **Enable container instance logs**.

   ![Monitoring](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/05-monitoring.png)

6. **Review + Create** → wait ~2–3 minutes.

   ![Review Create](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/06-review-create.png)

---

## Task 2: Test and Verify Deployment

1. Click **Go to resource** after deployment.

   ![Go to Resource](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/07-go-to-resource.png)

2. Confirm the status is **Running**.

   ![ACI Overview](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/08-aci-overview.png)

3. Copy the FQDN and open in browser to see the **Welcome to Azure Container Instance** page.

   ![Web App Running](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/09-webapp.png)

4. Check the logs under **Containers → Logs** for HTTP GET requests.

   ![Container Logs](https://raw.githubusercontent.com/USERNAME/REPO/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/10-logs.png)

---

## Cleanup
To avoid charges:
- Via portal – delete the **resource group**
- PowerShell:
  ```powershell
  Remove-AzResourceGroup -Name resourceGroupName

