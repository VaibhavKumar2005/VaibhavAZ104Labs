# ☁️ Azure Lab: Create a Virtual Machine Using the Azure Portal

## 📘 Overview

In this exercise, we created a Linux-based Virtual Machine (VM) using the Azure Portal. The VM runs Ubuntu and is configured with SSH access. This lab is part of a hands-on exercise to understand how to deploy infrastructure on Microsoft Azure using the web-based portal interface.

---

## 🛠️ Lab Objective

Deploy a VM named `test-ubuntu-cus-vm` on Azure using the **Azure Portal**, configure basic settings, generate SSH keys, and verify the deployment.

---

## 🧭 Steps to Create the VM

### 1. **Navigate to Create Resource**

From the Azure homepage, click on **"Create a resource"**.

![Create Resource - Portal Homepage](Image%201.%20Create%20Resource%20click%20on%20Portal%20Homepage.png)

---

### 2. **Search for Virtual Machine**

In the marketplace, search for **"Virtual Machine"**.

![Search VM](Image%202.%20Search%20VM.png)

---

### 3. **Configure Basic VM Settings**

#### Instance Details:

- **Subscription:** Concierge Subscription  
- **Resource Group:** Select the sandbox resource group  
- **Virtual Machine Name:** `test-ubuntu-cus-vm`  
- **Region:** Select closest to you  
- **Image:** Ubuntu Server 24.04 LTS – Gen2  
- **Size:** Standard D2s v3  
- **Architecture:** x64  
- **Availability Options:** No infrastructure redundancy  
- **Security Type:** Standard

![Naming the VM](Image%203.%20Creating%20VM%20-%20Naming.png)

![Selecting Size](Image%204.%20Creating%20VM%20-%20Sizing.png)

---

### 4. **Set Up Authentication**

- **Authentication Type:** SSH public key  
- **Username:** (Your preferred username)  
- **SSH Key Source:** Generate a new key pair  
- **Key Pair Name:** `test-ubuntu-cus-vm_key`

![Key Authentication](Image%205.%20Creating%20VM%20-%20Key%20for%20Auth.png)

---

### 5. **Configure Networking**

Allow SSH connections by enabling inbound port 22.

![Inbound Port Rules](Image%206.%20Creating%20VM%20-%20Inbound%20Port%20Rules.png)

---

### 6. **Review and Create the VM**

Review all settings and select **Create**.

![Review and Create](Image%207.%20Review%20and%20Create%20VM.png)

---

### 7. **Generate and Download SSH Key Pair**

Click **Download private key and create resource** to complete the setup.

![Generating Key Pair](Image%208.%20Generating%20Key%20Pair.png)

---

### 8. **Deployment and Access the VM**

Monitor deployment progress and navigate to the VM resource once completed.

![Deployment Process](Image%209.%20Deployment%20and%20heading%20to%20the%20resource.png)

---

### 9. **VM is Running**

Once deployed, you can view the VM status and IP address from the **Overview** page.

![VM Running](Image%2010.%20VM%20Running.png)

---

## 🔐 Connecting to the VM

Use the downloaded `.pem` private key and the public IP address shown in the VM's overview page to SSH into the VM:

```bash
ssh -i /path/to/test-ubuntu-cus-vm_key.pem <your-username>@<Public-IP>

