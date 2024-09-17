## Prerequisites

Before deploying **LAMP** on your Cloudzy VPS using the One-Click App, ensure you meet the following requirements:

- **Active Cloudzy Account**: Make sure you have an active Cloudzy account to access the Cloudzy Control Panel.
- **Available Credit**: Verify that you have enough credit in your Cloudzy account to deploy a new VPS.
- **Operating System Compatibility**: The LAMP One-Click App is compatible with **Ubuntu Server 20.04**, **Ubuntu Server 22.04**, and **Ubuntu Server 24.04**.

## Step 1: Select LAMP from the Applications Menu

1. **Log in to Your Cloudzy Account**: Start by logging into your account through the Cloudzy Control Panel.
   
2. **Navigate to Applications**: On the left-hand menu, select the "Applications" section to view all available One-Click Apps.  
   
4. **Select LAMP**: Under the "All Applications" category, locate and click on the **LAMP** application to move to the next configuration step.  
![image](https://github.com/user-attachments/assets/3196f4a1-4adf-41d1-84a7-4e901db749ba)

6. **Click Deploy Service**: Once you’ve selected the LAMP application, a blue **"Deploy Service"** button will appear. Click this button to proceed with configuring your LAMP VPS.  
![image](https://github.com/user-attachments/assets/fa4cc452-54af-48b6-b37f-c81bb3c953a9)

## Step 2: Configure Your VPS

1. **Select Your Server Location**: On the configuration page, choose a server location from the available options. For optimal performance, select a location closest to your target audience. For example, popular options include Dallas, Miami, or Frankfurt.  
   ![image](https://github.com/user-attachments/assets/f9551a4c-1c74-46c8-8852-334689f19ece)

2. **Choose Your Operating System**: Under the “Image” section, select the operating system on which your LAMP stack will run. The LAMP One-Click App is compatible with **Ubuntu Server 20.04**, **Ubuntu Server 22.04**, and **Ubuntu Server 24.04**. Pick the version that suits your needs.  
   ![image](https://github.com/user-attachments/assets/d17fd39e-a350-422e-a1b9-c57fe35bc614)

3. **Select Your VPS Plan**: Choose a VPS plan based on your performance requirements. For instance, you can select a plan with **1 vCPU, 2 GB of RAM, and 60 GB of storage** for a moderate workload. Ensure the selected plan fits your needs for CPU, memory, bandwidth, and storage.  
   ![image](https://github.com/user-attachments/assets/c8a70500-487f-414f-9ea0-6878c7e3ce0a)

4. **Review IPv4 and IPv6 Options**: Decide between **IPv6**, which is free, or **IPv4**, which may have a small associated cost. Choose the option that best fits your networking needs.  
   ![image](https://github.com/user-attachments/assets/95c9f9f2-7489-4785-b3f0-9ba6b9f8623f)

5. **Set Up SSH Key (Optional)**: For a secure password-less connection, you can add an SSH key by clicking “Add New SSH Key.” If you're unfamiliar with SSH keys, refer to **[Cloudzy’s guide on SSH key configuration](https://cloudzy.com/kb/linux/connection/)**. If you prefer to use a password login, you can skip this step.

6. **Assign a Hostname**: Enter a unique hostname for your VPS. For example, you can use something like **“LAMP-DTX-2gb”** or customize it according to your preference.
   
7. **Review and Deploy**: After confirming all your settings, click the **“Deploy Now”** button to start deploying your LAMP VPS. You’ll be able to track the progress through the status bar, showing steps like “Preparing Network” and “Initializing.”
