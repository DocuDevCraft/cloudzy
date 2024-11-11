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



## Step 3: Access Your Plesk Server

1. **Wait for VPS Deployment**: After clicking “Deploy Now,” Cloudzy will start setting up your VPS. The deployment process goes through several stages like “Preparing Network,” “Preparing Disk,” and “Initializing.” This might take a few minutes, so please be patient until the status shows “Active.”  
![image](https://github.com/user-attachments/assets/4a57e911-01c6-4dbb-9348-9cb59ebfb77a)


3. **Retrieve Login Credentials**: Once your VPS has been successfully created, a confirmation screen will display your server’s IP address, username, and password. Be sure to save these credentials, as you’ll need them to access your Plesk panel.  
![image](https://github.com/user-attachments/assets/f783fb9d-0249-4a01-a266-58a33f4ae7a9)


5. **Log in via SSH**: Once the deployment is complete, connect to your VPS using SSH to retrieve your Plesk login credentials. Refer to [Cloudzy’s guide on connecting to a Linux VPS via SSH](https://cloudzy.com/kb/connect-to-linux-vps-via-ssh/) for detailed instructions if needed.
   - Open a terminal (or SSH client) and use the following command:
     ```bash
     ssh root@[Your_VPS_IP_Address]
     ```
   - Enter the password provided by Cloudzy during the VPS setup.

6. **Retrieve Plesk Login Information**: After logging in, you will see a message displaying your Plesk instance URL along with the **Admin Username** and **Admin Password**. Take note of these credentials, as shown in the terminal output:
   ```
   You can now access your Plesk instance at https://[Your_VPS_IP_Address]
   Admin Username: admin
   Admin Password: [Your_Plesk_Password]
   ```

## Step 4: Access and Log In to Plesk

1. **Access Plesk in Browser**:
   - Open your web browser and navigate to the Plesk URL provided in the SSH terminal output (e.g., `https://[Your_VPS_IP_Address]`).
   - If a security warning appears due to a self-signed SSL certificate, you can proceed by clicking "Continue" or "Advanced" and then "Proceed."  
     

2. **Log In to Plesk**: Use the **Admin Username** and **Admin Password** provided in the SSH session to access the Plesk control panel.  
![image](https://github.com/user-attachments/assets/1d6dc3a4-3662-41d3-a002-450f04fbe76b)
3. **Complete Initial Setup**:
   - After logging in, you will see a setup page where you need to provide your contact information and set a new password.
   - Enter your contact name, email address, and desired password.
   - Click "Generate" if you'd like to use a suggested password.  
![image](https://github.com/user-attachments/assets/675905ca-9229-4570-b580-d069931bcbbb)

Your Plesk instance is now accessible, and you can start managing websites, domains, and applications through the Plesk dashboard.
