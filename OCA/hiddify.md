# How to Deploy Hiddify Manager with Cloudzy’s One-Click App

Hiddify Manager is a robust and easy-to-use multi-protocol VPN solution designed for privacy enthusiasts and professionals alike. Whether you're setting up a secure connection for personal use or managing large-scale network configurations, Hiddify Manager provides the tools you need to ensure privacy, flexibility, and performance. 
Cloudzy’s One-Click App makes deploying Hiddify Manager on your VPS incredibly simple, saving you time and effort. With just a few steps, you can install and access Hiddify Manager, ready to customize and deploy to your specific needs. 
This comprehensive guide will walk you through the entire process—from deploying the VPS with Hiddify Manager pre-installed to accessing and configuring your admin panel. Let’s get started!

## Prerequisites  

Before you start deploying **Hiddify Manager** on your Cloudzy VPS using the One-Click App, ensure that you meet the following requirements:

- **Active Cloudzy Account**: Make sure you have an active Cloudzy account to access the Control Panel.  
- **Sufficient Credit**: Confirm that you have enough credit in your account to deploy a new VPS.  
- **Operating System Compatibility**: The Hiddify Manager One-Click App is compatible with Ubuntu Server version **22.04**.  

With these requirements in place, you’re ready to proceed with deploying **Hiddify Manager** on your Cloudzy VPS.

## Step 1: Select Hiddify Manager from the Applications Menu  

1. **Log in to Your Cloudzy Account**: Begin by logging into your account through the [Cloudzy Control Panel](https://panel.cloudzy.com).  

2. **Navigate to Applications**: On the left-hand menu, click on **Applications** under the “Management” section.  

3. **Select Hiddify Manager**: Under the **All Applications** category, locate **Hiddify Manager** and click on it. This will take you to the next step, where you can configure your VPS.   
  ![image](https://github.com/user-attachments/assets/2ce9d37f-852b-489d-9967-2ea290b1c2ae)

4. **Click Deploy Service**: After selecting Hiddify Manager, a green **Deploy Service** button will appear. Click on it to proceed to the VPS configuration page.  
 ![image](https://github.com/user-attachments/assets/746b4644-318f-4026-9766-7f7edd30e11d)

With Hiddify Manager selected, you are ready to configure your VPS in the next step.

### Step 2: Configure Your VPS

1. **Select Your Server Location**:  
   - Navigate to the VPS configuration page and select the server location that best suits your needs. Choose a location closer to your target audience for optimal performance. Popular choices include **Amsterdam**, **London**, and **Luxembourg**.    
![image](https://github.com/user-attachments/assets/d0771419-5c2d-4bdc-8281-37263437ab7a)


2. **Choose Your Operating System**:  
   - In the **Image** section, select **Ubuntu Server 22.04**, the recommended OS for Hiddify Manager. This ensures compatibility and stability.  
   ![image](https://github.com/user-attachments/assets/4939c4fd-4826-416b-a169-1554b3cc02f3)


3. **Choose Your VPS Plan**:  
   - Select a VPS plan that matches your resource requirements. For instance, you can pick a plan with **1 vCPU, 2 GB RAM, and 60 GB storage** for moderate usage. Adjust the plan if needed.  
   ![image](https://github.com/user-attachments/assets/ec57f711-f1e0-4c64-87db-2b5dcef27deb)


4. **Enable Networking Options and Assign a Hostname**:  
   - Ensure that **IPv4** is enabled for your VPS. Additionally, **IPv6** can be activated as a free option for expanded networking capabilities.  
   - Enter a custom hostname for your VPS, such as **HiddifyManager-NL-Amsterdam-DC2-2gb**, to help you identify it easily.  
   ![image](https://github.com/user-attachments/assets/7598a800-9df8-438c-a46c-ab51ed94f9cf)


5. **Set Up SSH Key (Optional)**:  
   - For a secure, passwordless connection to your VPS, add an **SSH Key**. If you're unfamiliar with SSH keys, refer to **[Cloudzy’s SSH key guide](https://cloudzy.com/kb/linux/connection/)**. Alternatively, you can proceed with password authentication.  
  ![image](https://github.com/user-attachments/assets/7dbfd91c-d82c-4d34-83f5-1c0ddf91396e)

6. **Deploy Your VPS**:  
   - After reviewing all your configurations, click the **Deploy Now** button to start creating your VPS.  
   - A progress bar will appear, showing the deployment stages, including **Preparing Network**, **Preparing Disk**, **Initializing**, and **Active**.  
   ![image](https://github.com/user-attachments/assets/07640430-580d-47f2-b766-b5477832a164)

### Step 3: Access Hiddify Manager via SSH

1. **Log in to Your VPS via SSH:**  
   After your VPS has been successfully deployed, connect to it using SSH.  
   - Use a terminal (or any SSH client) and enter the following command:
     ```bash
     ssh root@<Your_VPS_IP_Address>
     ```
   - You will be prompted to enter your VPS root password.

2. **Hiddify Manager Menu:**  
   Upon successful login, the Hiddify Manager interface will open automatically, displaying a menu with multiple options. Highlight and select **"admin" (Show admin link)** to retrieve the admin interface URL.  
   ![image](https://github.com/user-attachments/assets/0a6bf71f-9f6d-4753-9055-5b2b79bb4a7d)


3. **Access the Admin Interface:**  
   - After selecting **"admin"**, the terminal will provide the admin interface URL for the Hiddify Manager. Save this URL as you will need it for the next steps.

Your Hiddify Manager is now set up, and you are ready to configure it further using the admin panel.

### Step 4: Hiddify Manager Installation Confirmation and Admin Panel Access

1. **View Installation Confirmation:**  
   After selecting **"admin"** from the Hiddify Manager menu, the terminal will display a confirmation screen with the following details:  
   - **Global Information**: Country, city, and IP details of your server.  
   - **Service Status**: Ensure all listed services (e.g., `hiddify-cli`, `hiddify-nginx`, etc.) are marked as **active**.  
   - **Admin Access**: A QR code and secure URL are provided to access the Hiddify Manager admin interface.  
   ![image](https://github.com/user-attachments/assets/7f1d5e6a-6a6d-453d-91a7-c05d03130529)


2. **Access the Admin Interface:**  
   - **Scan the QR Code:** Use your mobile device or QR code scanner to access the admin interface directly.  
   - **Copy or Click the Link:** Alternatively, copy the secure link or click on it directly in your terminal to open the admin panel in your web browser.  
     ![image](https://github.com/user-attachments/assets/6c037ee5-53b6-4bc3-990c-65c0de7fdf80)


Your Hiddify Manager admin panel is now accessible for further configuration and management!
