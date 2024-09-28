# Getting Started with IPv6 on Cloudzy
As the internet grows, so does the need for more IP addresses, and that's where IPv6 comes in. Unlike the older IPv4, which has a limited number of addresses, IPv6 offers a much larger supply, making it easier for devices to connect directly to the internet. It also simplifies how devices communicate, which can lead to faster and more reliable connections. With IPv6, there’s no need for complicated workarounds, and it provides an overall smoother and more secure online experience.

## Prerequisites

Before starting with IPv6 on your Cloudzy VPS, ensure the following:

- **Active Cloudzy Account**: You must have a Cloudzy account and be logged into the Cloudzy Cloud Panel.
- **IPv6 Support on Your Network**: Verify that your local network and internet service provider support IPv6.
  
## Cloudzy Offers IPv6 by Default
When you create a new VPS in the Cloudzy panel, **IPv6** is enabled by default, which provides modern, scalable internet protocol addressing. To use **IPv4**, users must manually select the "Enable IPv4" option during the server creation process. This ensures compatibility with older systems and networks that still rely on IPv4.  
![image](https://github.com/user-attachments/assets/6c46df53-1226-4db8-a6d9-d5037612aec4)

### Recording Your IPv6 Address When Creating a Cloud VPS

When you create a new VPS in the **Cloudzy** control panel, **IPv6** is assigned to your VPS by default. You will see the IPv6 address listed during the creation process. It's essential to take note of this IPv6 address as you will need it to connect to your VPS later.

1. After the VPS creation process, a screen displaying your **IPv6 address** will appear alongside your VPS username and password.
2. You can copy the IPv6 address by clicking the clipboard icon next to it, ensuring you have it saved for future use.  
   ![image](https://github.com/user-attachments/assets/463dff06-2ddd-41b4-9a83-c7da296fe0ad)

If you forget to record your IPv6 address, you can always find it in the **Services** section of the Cloudzy control panel, where your active VPS details are displayed.

## How to SSH into Your IPv6 VPS

Once you have your IPv6 address, you can use it to connect to your VPS via **SSH**. This method requires that both your local machine and your network fully support IPv6. If your client does not support IPv6, you won’t be able to connect to the VPS unless IPv4 was enabled during the setup process.

### SSH to Your IPv6 VPS:
1. Open your terminal (or SSH client).
2. Use the following command to initiate the SSH connection:
   ```bash
   ssh root@[your_IPv6_address]
   ```
   For example, if your IPv6 address is `2601:abcd:1234:5678::1`, you would enter:
   ```bash
   ssh root@2601:abcd:1234:5678::1
   ```
3. You will then be prompted for the password you received during the VPS setup process.

For a more detailed step-by-step guide on how to connect via SSH, please refer to **[Cloudzy’s SSH Guide](https://cloudzy.com/kb/linux/connection/)**, which covers the basics of setting up SSH access on your VPS.

## Manage and Change Your IPv6 Address

One of the major advantages of using **IPv6** over **IPv4** is the large number of available addresses. With IPv6, you are assigned an entire subnet of addresses, giving you the flexibility to change and manage your IPv6 address without relying on the Cloudzy Cloud Panel to assign a new one. In contrast, with IPv4, you are typically limited to a single IP address assigned by the Cloudzy Cloud Panel.

#### Finding Your IPv6 Subnet

To manage and change your IPv6 address, you first need to identify your current IPv6 subnet. Follow these steps to find your IPv6 subnet using the `ip a` command:

1. Log in to your VPS via SSH.
2. Run the following command:
   ```bash
   ip a
   ```
   This command will display all your network interfaces along with the assigned IPv6 addresses. Look for an address that looks something like this:
   ```bash
   inet6 2605:abcd:1234:5678::1/64 scope global
   ```
   The `/64` part indicates your subnet prefix, meaning you have a range of addresses to work with.

### Changing Your IPv6 Address

Once you know your IPv6 subnet, you can assign a different address within that range. For example, if your current address is `2605:abcd:1234:5678::1`, you can assign another address like `2605:abcd:1234:5678::2`.

1. Open your network configuration file. On Ubuntu, this is typically found at `/etc/netplan/50-cloud-init.yaml`. Use the following command to open the file:
   ```bash
   sudo nano /etc/netplan/50-cloud-init.yaml
   ```
2. Modify the IPv6 address under the `addresses` section. Change the current address to any valid address within your subnet:
   ```yaml
   network:
     version: 2
     ethernets:
       eth0:
         dhcp6: false
         addresses:
           - 2605:abcd:1234:5678::2/64
   ```
3. Save the file and apply the changes:
   ```bash
   sudo netplan apply
   ```

### Connect with Your New IPv6 Address

After applying the changes, you can now SSH into your VPS using the new IPv6 address. For example:
```bash
ssh root@2605:abcd:1234:5678::2
```

Unlike **IPv4**, where you're often limited to a single address assigned by the Cloudzy Cloud Panel, **IPv6** allows you to choose and manage multiple addresses from your assigned subnet. This flexibility makes it easier to configure your network based on your specific needs.

Here’s the revised instruction:


## Enabling IPv4 After VPS Deployment

While Cloudzy assigns an **IPv6** address by default when you deploy your VPS, you might find that some applications or services you wish to use require an **IPv4** address. Fortunately, Cloudzy makes it easy to enable **IPv4** even after your VPS has been deployed.

### Steps to Enable IPv4:

1. **Access the Cloudzy Cloud Panel**: Log in to your Cloudzy account and go to the **Services** section to find your active VPS.

2. **Click on Your VPS**: Locate the VPS you wish to enable IPv4 on and click directly on the VPS name to access the management page.

3. **Enable IPv4**: In the **Access** tab of your VPS settings, you will see an option to **Enable IPv4**. Click on this option.  
   ![image](https://github.com/user-attachments/assets/f610f1af-5684-485e-84f2-2e9f783556b1)

5. **Confirm IPv4 Enabling**: A pop-up will appear confirming that enabling IPv4 will not incur any additional costs (as of now). Click **Enable** to proceed.  
   ![image](https://github.com/user-attachments/assets/ff735446-3b16-4a58-a124-132ca1bede99)

5. **IPv4 Assigned**: Once enabled, your VPS will be assigned an **IPv4** address, which will appear in the **Access** section alongside your existing IPv6 address.  
   ![image](https://github.com/user-attachments/assets/eb2d4bd3-ce7c-41d0-bf67-aaa118ff892c)

Now, with both **IPv4** and **IPv6** enabled, you can use either protocol to access and manage your VPS. This flexibility is beneficial for ensuring compatibility with older systems and services that require IPv4.

## Setting Up a AAAA Record for IPv6

When you are working with an **IPv6** address, it is important to configure a **DNS AAAA record** to map your domain name to your IPv6 address. The AAAA record is similar to an A record used for IPv4, but it specifically handles IPv6 addresses. This step is crucial if you want your domain name to resolve to an IPv6 address.

For example, if you want your domain (e.g., `web.example.com`) to point to your VPS’s IPv6 address, follow these steps:

1. In your DNS management interface, create a new AAAA record.
2. Under **Name**, enter the subdomain (e.g., `web`).
3. In the **IPv6 address** field, input your IPv6 address, such as `2605:abcd:1234:5678::2`.
4. Save the record.  
![image](https://github.com/user-attachments/assets/fd2f90b9-1dc1-4b39-b75c-2ba0fc5d60b3)

This will allow your domain `web.example.com` to resolve to the specified IPv6 address, enabling visitors to access your website via IPv6.

Embracing IPv6 not only future-proofs your network but also provides you with greater flexibility and scalability, ensuring smoother and more efficient internet connectivity.



