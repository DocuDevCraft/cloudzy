

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

### Step 3: Access Your Hiddify Manager VPS

1. **Wait for VPS Deployment:**  
   After clicking the **Deploy Now** button, Cloudzy will begin setting up your VPS. The deployment process includes several stages, such as **Preparing Network**, **Preparing Disk**, **Initializing**, and finally, **Active**. This process may take a few minutes.  
   ![image](https://github.com/user-attachments/assets/d862725c-2727-4a46-ab20-7868cce5e4f1)


2. **Retrieve Login Credentials:**  
   Once your VPS has been successfully created, a confirmation screen will display your server’s **IP Address**, **Username**, and **Password**. Make sure to save these credentials, as you will need them to access your VPS.  
   ![image](https://github.com/user-attachments/assets/4ee56f0e-0768-40fe-b6ae-5a3aabd33913)


3. **Connect to the VPS via SSH:**  
   - Open your terminal or SSH client.  
   - Enter the following command, replacing `<Your_VPS_IP_Address>` with the IP address of your VPS:  
     ```bash
     ssh root@<Your_VPS_IP_Address>
     ```  
   - When prompted, enter the password from the VPS deployment confirmation screen.  
   - If you receive a security warning about the server's authenticity, type `yes` to proceed.  
   ![image](https://github.com/user-attachments/assets/ssh-login-prompt)

4. **Verify Hiddify Installation:**  
   After successfully logging into your VPS, the terminal will show the Hiddify Manager setup interface, allowing you to confirm the installation and proceed to the next steps.  
   ![image](https://github.com/user-attachments/assets/hiddify-manager-login)

You are now connected to your VPS and ready to configure the Hiddify Manager for secure traffic management. Let’s proceed!


After your VPS is deployed successfully, you can move on to access and configure Hiddify Manager.

