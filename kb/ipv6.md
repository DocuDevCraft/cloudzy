## What is IPv6?
**IPv6** (Internet Protocol version 6) is the latest version of the Internet Protocol designed to replace **IPv4**, the previous standard. Unlike IPv4, which uses a 32-bit address system and can support around 4.3 billion addresses, IPv6 uses a 128-bit address system, allowing for an almost limitless number of unique IP addresses, solving the issue of IP address exhaustion.

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

Let me know when you're ready for the next section!
