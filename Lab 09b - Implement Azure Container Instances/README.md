# Lab 09b - Implement Azure Container Instances

## Introduction
In this lab, you learn how to implement and deploy **Azure Container Instances** (ACI).  
This lab requires an Azure subscription. Your subscription type may affect feature availability. The steps assume **East US**.  
**Estimated timing:** 15 minutes

---

## Scenario
Your organization runs a web application on a VM on-premises and wants to move to the cloud with minimal server overhead. You choose **Azure Container Instances** (ACI) and Docker.

---

## Architecture Diagram
![Architecture Diagram](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/architecture-diagram.png)

---

## Job Skills
- **Task 1:** Deploy an Azure Container Instance using a Docker image.  
- **Task 2:** Test and verify deployment of an Azure Container Instance.

---

## Task 1: Deploy an Azure Container Instance using a Docker image

1. **Sign in to the Azure portal**  
   https://portal.azure.com

   ![Azure Portal](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/01-azure-portal.png)

2. **Search for Container instances** and select **+ Create**.

   ![Create Container Instance](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/02-create-container-instance.png)

3. **Basics tab – use the following settings:**

   | Setting         | Value                                                   |
   |-----------------|---------------------------------------------------------|
   | Subscription    | Your Azure subscription                                 |
   | Resource group  | `az104-rg9` (or Create new)                             |
   | Container name  | `az104-c1`                                              |
   | Region          | East US (or region near you)                            |
   | Image source    | Quickstart images                                       |
   | Image           | `mcr.microsoft.com/azuredocs/aci-helloworld:latest`     |

   ![Basics Tab](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/03-basics-tab.png)

4. **Networking tab:** set a unique **DNS name label**.

   ![Networking](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/04-networking.png)

5. **Monitoring tab:** uncheck **Enable container instance logs**.

   ![Monitoring](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/05-monitoring.png)

6. **Review + Create** → deploy (~2–3 min).

   ![Review + Create](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/06-review-create.png)

---

## Task 2: Test and verify deployment

1. After deployment, click **Go to resource**.

   ![Go to Resource](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/07-go-to-resource.png)

2. On the **Overview** blade, verify **Status = Running**.

   ![ACI Overview](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/08-aci-overview.png)

3. Copy the **FQDN** and open it in a browser to see the welcome page.

   ![Web App Running](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/09-webapp.png)

4. Open **Settings → Containers → Logs** and verify HTTP GET entries.

   ![Container Logs](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/images/10-logs.png)

---

## Cleanup
Delete the lab resources to avoid charges:

- **Azure Portal:** delete the **resource group**.  
- **PowerShell:**
  ```powershell
  Remove-AzResourceGroup -Name resourceGroupName

