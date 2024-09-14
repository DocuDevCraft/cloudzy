# How to Deploy WireGuard with Cloudzy’s One-Click App

Setting up a WireGuard VPN on your Cloudzy VPS is a fast and secure way to establish a private network connection. With Cloudzy’s One-Click App, deploying WireGuard is both efficient and straightforward. This guide will walk you through the entire process—from configuring your VPS to setting up and activating the WireGuard client on your local machine. Whether you're using WireGuard for personal privacy, secure communication, or business networking, this step-by-step tutorial will help you get up and running quickly and securely.
## Prerequisites

Before you start deploying **WireGuard** on your Cloudzy VPS using the One-Click App, ensure that you meet the following requirements:

- **Active Cloudzy Account**: Make sure you have an active Cloudzy account to access the Control Panel.
- **Sufficient Credit**: Confirm that you have enough credit in your account to deploy a new VPS.
- **Operating System Compatibility**: The WireGuard One-Click App is compatible with Ubuntu Server versions 20.04, 22.04, and 24.04.

## Step 1: Select WireGuard from the Applications Menu

1. **Log in to Your Cloudzy Account**: Begin by logging into your account through the Cloudzy Control Panel.
2. **Navigate to Applications**: On the left-hand menu, go to the “Applications” section.
4. **Select WireGuard**: Under the "All Applications" category, find and click on the WireGuard option. This will take you to the next step, where you can configure your VPS.
![image](https://github.com/user-attachments/assets/a10c9374-ceba-42c3-8e1c-355b7071662d)
6. **Click Deploy Service**: After selecting WireGuard, a blue “Deploy Service” button will appear. Click on this to start configuring your WireGuard VPS.
![image](https://github.com/user-attachments/assets/cb923636-2001-4dc1-852f-959732861f3c)

## Step 2: Configure Your VPS

1. **Select Your Server Location**: On the configuration page, choose a server location that best fits your needs from the available options. For optimal performance, you might want to select a location closer to your target audience. Popular choices include locations like Dallas, Miami, and Frankfurt.
![image](https://github.com/user-attachments/assets/a1272cf6-6fa1-4d7f-bea9-0981a68b22b3)

2. **Choose Your Operating System**: Under the “Image” section, select the operating system for your WireGuard VPS. WireGuard is compatible with **Ubuntu Server 20.04**, **Ubuntu Server 22.04**, and **Ubuntu Server 24.04**. Choose the version that meets your preference or project requirements.
![image](https://github.com/user-attachments/assets/57a04ad1-319b-45b9-badf-56a967b81f51)


3. **Choose Your VPS Plan**: Select a VPS plan based on your resource needs. For example, you can opt for a plan with **1 vCPU, 2 GB of RAM, and 60 GB of storage** if you’re deploying a moderate workload. You can always resize or upgrade your plan later if necessary.
![image](https://github.com/user-attachments/assets/00f3527d-09a5-461c-9650-e7251be66676)

4. **Review IPv4 and IPv6 Options**: You can choose between **IPv6**, which is free of charge, and **IPv4**, which may incur a nominal additional cost. Select the option that best suits your networking needs.
![image](https://github.com/user-attachments/assets/627967ef-9ff0-43ce-a439-86cead1365a1)

5. **Set Up SSH Key (Optional)**: For secure, passwordless access to your VPS, you can add an SSH key by clicking “Add New SSH Key.” If you're unfamiliar with SSH keys or need guidance on setting them up, refer to **[Cloudzy’s guide on SSH key configuration](https://cloudzy.com/kb/linux/connection/)**. You can skip this step if you prefer to use traditional password authentication.
   ![image](https://github.com/user-attachments/assets/6a5ea2eb-54f2-4232-8e9c-673a5afcb4d4)

7. **Assign a Hostname**: Enter a hostname for your VPS, such as “WireGuard-DTX-2gb” or any custom name that will help you easily identify your VPS.  
   ![image](https://github.com/user-attachments/assets/495912dc-aff9-4fca-90c3-30583587a18c)

8. **Review and Deploy**: After confirming all your settings, click the "Deploy Now" button to create your WireGuard VPS. The system will initiate the deployment process, which you can monitor through the progress bar.
 ![image](https://github.com/user-attachments/assets/2dad0161-cbb8-4b4a-93a4-00ffe1133c08)

## Step 3: Access Your WireGuard Server

1. **Wait for VPS Creation:** After clicking “Deploy Now,” the system will take a few minutes to configure your VPS. You'll see a progress indicator showing the stages such as “Preparing Network,” “Preparing Disk,” “Initializing,” and finally, “Active.”  
![image](https://github.com/user-attachments/assets/e2fc0235-cf8e-4fbd-8a32-f1382f3dc136)

2. **Retrieve Login Information:** Once your VPS has been created successfully, you’ll be taken to a confirmation screen displaying your server’s IP address, username, and password. Make sure to note these credentials to access your WireGuard server.
![image](https://github.com/user-attachments/assets/14080b0d-d7c4-4926-9248-19931dd96259)

4. **Connect via SSH:**
   - Open a terminal (or use an SSH client) and connect to your VPS by typing the following command:
     ```bash
     ssh root@<Your_VPS_IP_Address>
     ```
   - You will likely receive a security warning asking if you want to continue connecting due to the server's fingerprint. Type `yes` to proceed with the connection.  
     ![image](https://github.com/user-attachments/assets/01519a81-5ea8-4b81-8c49-9db279d9034f)

   - After typing `yes`, enter the password you noted earlier to access your VPS.

5. **Verify WireGuard Installation:**
   - After successfully logging in, you will see a confirmation message indicating that the WireGuard server has been installed.  
   ![image](https://github.com/user-attachments/assets/f5d70918-deb9-4390-8a10-fecc1a5555a3)

6. **Access WireGuard Configuration:**
   - You can check the client configuration details by running the following command to view the `/root/client.conf` file:
     ```bash
     cat /root/client.conf
     ```
   - This file will contain important information such as:  
     ![image](https://github.com/user-attachments/assets/04cc042b-4db3-4e4b-ab3e-683a784d8566)

     - The interface details (IP address and DNS).
     - The private key for the WireGuard server.
     - The public key for the peer connection.
     - The endpoint (IP address and port) for configuring the client.
  
Your WireGuard server is now fully configured and ready for secure connections.

## Step 4: Configure the WireGuard Client on Windows

1. **Download and Install the WireGuard Client:**  
   Go to [WireGuard’s official Windows download page](https://download.wireguard.com/windows-client/). Download the installer (`wireguard-installer.exe`) and follow the installation instructions.  
   ![image](https://github.com/user-attachments/assets/774394aa-9c04-42bf-8e3f-0ef4d87a520a)


3. **Create the Client Configuration File:**  
   Open **Notepad** on your Windows machine and paste the contents of the `client.conf` file that you obtained from your VPS server.  
![image](https://github.com/user-attachments/assets/5b4f58e0-8a0d-49cb-b9a3-1b219462be0f)


4. **Save the Configuration File:**  
   Save the file as `client.conf` and make sure to select **All files** in the "Save as type" dropdown to avoid accidentally adding `.txt` to the filename. Save it to a convenient location on your computer.  
![image](https://github.com/user-attachments/assets/f920df01-12df-4d9e-a778-ba54e7076bad)

5. **Import the Tunnel Configuration:**  
   Open the WireGuard application and click on **Import tunnel(s) from file**.  
   ![image](https://github.com/user-attachments/assets/1e0a3d4f-21e3-4b3c-abc9-0ab37acba1e5)  
 
   Browse for the `client.conf` file that you saved earlier and select it.  
   ![image](https://github.com/user-attachments/assets/a4726267-fc56-4ef9-963a-33db00696798)


7. **Activate the Tunnel: Part 1 - Initial Connection:**  
   After importing the tunnel configuration, you will see the tunnel listed in the application. Press the **Activate** button to establish the connection.  
   ![image](https://github.com/user-attachments/assets/d1a77f3f-5950-4ce4-8769-2fb6da22df48)


9. **Activate the Tunnel: Part 2 - Monitoring Status:**  
   Once the connection is active, the status will change to **Active**, displaying details such as the public key, DNS settings, and data transfer stats. You can monitor the connection in the WireGuard interface to ensure everything is functioning correctly.  
   ![image](https://github.com/user-attachments/assets/e82ca43e-d469-4fa7-82bb-23128e3f43c6)


Your WireGuard connection is now established, allowing secure communication with your VPS.
