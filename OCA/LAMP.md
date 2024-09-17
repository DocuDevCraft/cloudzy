# How to Deploy LAMP Stack with Cloudzy’s One-Click App

Deploying a LAMP stack (Linux, Apache, MySQL, PHP) on your Cloudzy VPS using the One-Click App is an efficient and easy way to set up a reliable web hosting environment. LAMP provides the foundational software needed to host dynamic websites and web applications. This guide will take you step-by-step through the process of selecting, configuring, and deploying your LAMP stack, and how to manage your server once it’s running. Whether you’re building a personal website or a professional web application, this tutorial will help you get your LAMP stack up and running in no time.


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
   ![image](https://github.com/user-attachments/assets/c9f10317-f948-483a-8360-014b4b13639a)


7. **Assign a Hostname**: Enter a unique hostname for your VPS. For example, you can use something like **“LAMP-DTX-2gb”** or customize it according to your preference.  
   ![image](https://github.com/user-attachments/assets/c04d56f4-d980-4960-b167-2dc595052e9f)

8. **Review and Deploy**: After confirming all your settings, click the **“Deploy Now”** button to start deploying your LAMP VPS. You’ll be able to track the progress through the status bar, showing steps like “Preparing Network” and “Initializing.”  
![image](https://github.com/user-attachments/assets/4eb3690c-6079-46ad-a9dd-da1a7b1eb0a3)

## Step 3: Access Your LAMP Server

1. **Wait for VPS Creation**: After clicking "Deploy Now," the system will start creating your VPS. The process usually takes a few minutes, during which a progress bar will show steps like “Preparing Network,” “Preparing Disk,” “Initializing,” and finally, “Active.”
![image](https://github.com/user-attachments/assets/55553e6b-f8ef-42ee-b77d-b63426ca3a0c)


2. **Retrieve Login Information**: Once the VPS is created successfully, you’ll be directed to a confirmation screen that displays your server’s IP address, username, and password. Save this information, as it’s required to access your server.  
![image](https://github.com/user-attachments/assets/edb11ff5-655e-457a-8217-8e4185491c0c)


3. **Connect via SSH**:
   - Open a terminal or SSH client and connect to your VPS using the following command:
     ```bash
     ssh root@<Your_VPS_IP_Address>
     ```
   - When connecting for the first time, you’ll be asked to confirm the server’s fingerprint. Type `yes` to proceed.  
     ![image](https://github.com/user-attachments/assets/83246ed3-c759-4260-8954-d6b19817b81f)

   
   - Enter the password displayed in the VPS creation confirmation screen to log into your server.

4. **LAMP Stack Information**: 
   After logging in, you will see detailed information about your LAMP stack setup. The following details will be provided:
   - **Web server name**: The name of your web server (e.g., cloudzy).
   - **HTTP port**: The default port for web traffic (usually port 80).
   - **HTTPS port**: The default secure web traffic port (typically port 443).
   - **Document root**: The directory where your website files are stored (`/root/www` by default).
   - **MySQL server**: Information such as MySQL port (3306), user (lamp), and password (provided).
   - **phpMyAdmin HTTP/HTTPS port**: Details for accessing phpMyAdmin.  

   ![image](https://github.com/user-attachments/assets/80ae76bb-9fa1-4379-95f5-7a97893ce88b)


5. **View and Edit the Default Virtual Host Configuration**:
   The default configuration file for your LAMP server’s virtual host is located in `/root/config/vhosts/default.conf`. This file defines how Apache serves your website and includes essential details such as:
   - **DocumentRoot**: Specifies the directory where your website files are stored (`${APACHE_DOCUMENT_ROOT}`).
   - **ServerName**: The name of the server (`${APACHE_SERVER_NAME}`).
   - **SSL Configuration**: Settings for enabling HTTPS using self-signed certificates. The SSL certificate and key files are stored in `/etc/apache2/ssl/cert.pem` and `/etc/apache2/ssl/cert-key.pem`.

   To view this configuration, use the following command:
   ```bash
   cat /root/config/vhosts/default.conf
   ```

   You can also edit the file using a text editor like `nano`:
   ```bash
   nano /root/config/vhosts/default.conf
   ```

   Here is an example of the `default.conf` configuration:
   ```bash
   <VirtualHost *:80>
       ServerAdmin webmaster@localhost
       DocumentRoot ${APACHE_DOCUMENT_ROOT}
       ServerName ${APACHE_SERVER_NAME}
       <Directory ${APACHE_DOCUMENT_ROOT}>
           AllowOverride all
       </Directory>
   </VirtualHost>

   <VirtualHost *:443>
       ServerAdmin webmaster@localhost
       DocumentRoot ${APACHE_DOCUMENT_ROOT}
       ServerName ${APACHE_SERVER_NAME}
       <Directory ${APACHE_DOCUMENT_ROOT}>
           AllowOverride all
       </Directory>
       SSLEngine on
       SSLCertificateFile /etc/apache2/ssl/cert.pem
       SSLCertificateKeyFile /etc/apache2/ssl/cert-key.pem
   </VirtualHost>
   ```

This configuration allows your LAMP server to serve websites over HTTP and HTTPS. Your LAMP stack is now fully set up and ready for use.

## Step 4: Access phpMyAdmin and MySQL

Now that your LAMP stack is fully set up, you can manage your MySQL databases and web server using phpMyAdmin. This step will guide you through accessing phpMyAdmin and configuring MySQL.

1. **Create an SSH Tunnel**:
   - Since phpMyAdmin is not directly accessible from outside your VPS, you’ll need to create an SSH tunnel to access it securely. Use the following command to create the tunnel:
     ```bash
     ssh -L 8080:127.0.0.1:8080 root@<Your_VPS_IP_Address> -N
     ```
   - This command will forward port `8080` on your local machine to port `8080` on your VPS, allowing you to access phpMyAdmin locally.  

![image](https://github.com/user-attachments/assets/9b487982-85be-415e-ac56-d08d90a42c46)



2. **Access phpMyAdmin**:
   - Open your browser and navigate to:
     ```
     http://127.0.0.1:8080
     ```
   - You will now be able to access the phpMyAdmin page.

3. **Manage Databases with phpMyAdmin**:
   - Once logged in, you’ll have access to the phpMyAdmin interface where you can create, edit, and manage your MySQL databases.
   - From the left panel, you can browse through your existing databases like `lamp`, `mysql`, and others.
   - You can also create new databases, manage users, run SQL queries, and import/export database backups.  

![image](https://github.com/user-attachments/assets/744fc004-6fb1-4914-908f-c85aa1b403e9)

Your MySQL server and phpMyAdmin are now fully configured and accessible through the SSH tunnel. You can start managing your databases securely and efficiently from your local machine.
