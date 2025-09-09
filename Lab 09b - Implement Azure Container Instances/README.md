# Lab 9b - Implement Azure Container Instances

## Introduction
In this lab, you learn how to implement and deploy **Azure Container Instances** (ACI).  

This lab requires an Azure subscription. Your subscription type may affect feature availability. The steps assume **East US**.  
**Estimated timing:** 15 minutes  

---

## Scenario
Your organization runs a web application on a VM on-premises and wants to move to the cloud with minimal server overhead. You choose **Azure Container Instances** (ACI) and Docker.

---

## Job Skills
- **Task 1:** Deploy an Azure Container Instance using a Docker image.  
- **Task 2:** Test and verify deployment of an Azure Container Instance.

---

## Task 1: Deploy an Azure Container Instance using a Docker image

1. **Home Page and Search for Container Instances**  
   ![Home Page and Search for Container Instances](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%201.%20Home%20Page%20and%20Search%20for%20Container%20Instances.png)

2. **Click Create**  
   ![Click Create](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%202.%20Click%20Create.png)

3. **Basics Tab (Part 1)**  
   ![Basics 1](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%203.%20Basics%201.png)

4. **Basics Tab (Part 2)**  
   ![Basics 2](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%204.%20Basics%202.png)

5. **DNS Name Label**  
   ![DNS Name Label](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%205.%20DNS%20Name%20Label.png)

6. **See Logs Enabled**  
   ![Logs Enabled](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%206.%20See%20Logs%20enabled.png)

7. **Logs Disabled**  
   ![Logs Disabled](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%207.%20Logs%20Disabled.png)

8. **Review Advanced (No changes)**  
   ![Review Advanced](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%208.%20Review%20Advanced%20(No%20changes).png)

9. **Review and Create Container Instance**  
   ![Review and Create CI](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%209.%20Review%20and%20Create%20CI.png)

---

## Task 2: Test and verify deployment

10. **Click on Resource**  
   ![Click on Resource](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%2010.%20Click%20on%20Resource.png)

11. **Overview Blade – Copy FQDN**  
   ![Overview Blade](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%2011.%20Overview%20Blade%2C%20Copy%20FQDN.png)

12. **Pasting FQDN in Browser**  
   ![Pasting FQDN](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%2012.%20Pasting%20FQDN%20on%20a%20Browser%20service.png)

13. **Containers Blade**  
   ![Containers Blade](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%2013.%20Containers%20Blade.png)

14. **Containers Logs**  
   ![Containers Logs](https://raw.githubusercontent.com/VaibhavKumar2005/VaibhavAZ104Labs/main/Lab%2009b%20-%20Implement%20Azure%20Container%20Instances/Image%2014.%20Containers%20Logs.png)

---

## Cleanup
To avoid charges, delete the lab resources:  

- **Azure Portal:** Delete the resource group.  
- **PowerShell:**  
  ```powershell
  Remove-AzResourceGroup -Name resourceGroupName


