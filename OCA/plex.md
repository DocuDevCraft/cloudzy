# How to Deploy Plesk with Cloudzy’s One-Click App

Setting up a web hosting environment with **Plesk** on your Cloudzy VPS is a streamlined process with Cloudzy’s One-Click App. Plesk provides a robust control panel for managing websites, servers, and domains, making it an ideal choice for web developers and system administrators. This guide will take you through the steps, from configuring your VPS to accessing the Plesk interface for the first time.

## Prerequisites

Before you start deploying **Plesk** on your Cloudzy VPS using the One-Click App, ensure that you meet the following requirements:

- **Active Cloudzy Account**: Ensure you have an active Cloudzy account to access the Control Panel.
- **Sufficient Credit**: Verify that you have enough credit in your account to deploy a new VPS.
- **Operating System Compatibility**: The Plesk One-Click App is compatible with **Ubuntu Server versions 20.04, 22.04, and 24.04**.

## Step 1: Select Plesk from the Applications Menu

1. **Log in to Your Cloudzy Account**: Start by logging into your account through the Cloudzy Control Panel.
2. **Navigate to Applications**: In the left-hand menu, go to the “Applications” section.
3. **Select Plesk**: Under "All Applications," find and click on the **Plesk** option. This will take you to the configuration page for your VPS.  
   ![image](https://github.com/user-attachments/assets/57f306aa-a0b0-4d6a-8750-9cb72b5f4052)

5. **Click Deploy Service**: After selecting Plesk, a blue “Deploy Service” button will appear. Click on it to start configuring your Plesk VPS.
   ![image](https://github.com/user-attachments/assets/f4472320-d856-424f-9d61-afb9ace09505)

## Step 2: Configure Your VPS

1. **Select Your Server Location**: On the configuration page, choose a server location that best suits your needs. Cloudzy offers several options, such as **Amsterdam**, **Dallas**, and **Frankfurt**. Selecting a location closer to your target audience can enhance performance.  
![image](https://github.com/user-attachments/assets/b66ca359-4f47-4ba0-bbbf-2c07184f78d8)

2. **Choose Your Operating System**: Under the “Image” section, select the operating system for your Plesk VPS. Plesk is compatible with **Ubuntu Server 20.04**, **Ubuntu Server 22.04**, and **Ubuntu Server 24.04**. Choose the version that best matches your requirements.  
![image](https://github.com/user-attachments/assets/54b2d33d-9d3d-40bf-a087-1d1e543f95e6)

3. **Choose Your VPS Plan**: Select a VPS plan based on your resource needs. For instance, a plan with **1 vCPU, 2 GB of RAM, and 60 GB of storage** is sufficient for moderate workloads. Remember, you can upgrade your plan later if needed.  
![image](https://github.com/user-attachments/assets/78abe96e-b508-4ae2-87a9-1eb77ef7d5cb)

4. **Review IPv4 and IPv6 Options**: Decide between **IPv6** (free of charge) and **IPv4** (may have a nominal additional cost) depending on your networking requirements.  
![image](https://github.com/user-attachments/assets/553562e3-3377-42c5-a408-cddf4b25b161)

5. **Set Up SSH Key (Optional)**: For secure, passwordless access to your VPS, you can add an SSH key by clicking “Add New SSH Key.” If you need guidance on setting up SSH keys, refer to **[Cloudzy’s guide on SSH key configuration](https://cloudzy.com/kb/linux/connection/)**. This step is optional; you can skip it if you prefer to use password authentication.  
![image](https://github.com/user-attachments/assets/ee8fd4d7-96d7-4748-ad64-9421f0009c3b)

6. **Assign a Hostname**: Enter a hostname for your VPS, like “Plesk-Server” or a custom name that will help you identify this VPS easily.  
   ![image](https://github.com/user-attachments/assets/b070a2fa-7c47-44be-bf4f-024de9238fc1)


8. **Review and Deploy**: After confirming all your settings, click the "Deploy Now" button. The system will begin the deployment process, which you can track through the progress indicator.  
![image](https://github.com/user-attachments/assets/f8d6f95b-1e0f-4aaf-a725-8ac2bce45a76)

Your VPS will now be set up with Plesk, and you'll soon be able to access the Plesk interface for management and configuration.
