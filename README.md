# 🚨 Anti FiveHub: Protect Your FiveM Server 🚨

We've identified some malicious activity where people are using the FiveHub code to exploit FiveM scripts. To help you prevent abuse and protect your system, follow these steps.

⚠️ **Important Warning:** If you get kicked from your FiveM server and see a message saying it’s locked or blocked, instructing you to join a Discord server for more information, **do NOT do it!** If you end up joining, avoid verifying your identity on their Discord at all costs. Stay safe.

## Steps to Remove Malicious Resources from Your FiveM Server

### 1. Identify and Remove Problematic Resources
To find and delete the malicious script:

- Open your `resources` folder.
- Right-click on the folder and select **"Open with Code"** (using VSCode).
- Use the search function to look for `PerformHttpRequest`.
  - Check for any lines of code similar to this:  
    `https://fivehub-panel.site/api.php?key=`
- Once identified, **remove** the script that uses this URL.
- Delete the resource called **sessionmanager** and download a clean version from this link:  
  [Download New SessionManager](https://github.com/citizenfx/cfx-server-data)

### 2. Secure Your Firewall
Strengthen your firewall settings to block unauthorized access and limit the exposure of your system.

#### Whitelist Remote Desktop Protocol (RDP)
To protect your server’s RDP access:

- Open your **Firewall** settings.
- Navigate to **Inbound Rules**.
- Look for **"Remote Desktop - User Mode (TCP-In)"**.
- Click on **"Scope"** or **"Ranges"**.
- Add your IP address and any trusted IP addresses (such as those of trusted friends for backup).
- Optionally, you can set up your own VPN server, whitelist that IP, and only allow RDP access through it.
<img src="/image1.png">

#### Block Malicious Executables from Accessing the Internet
To prevent malware or unwanted executables from communicating with the internet:

- Go to your **Firewall** settings.
- Navigate to **Inbound Rules**.
- Create a new rule for the program located at:  
  `C:/Desktop/Microstub.exe`
- Block its internet access.

### 3. Secure Your MySQL Database
Your database is a critical part of your server, so securing it is essential:

- Always use **strong passwords** for your MySQL users.
- Ensure that the **root user** has access **only locally** (i.e., on the server itself) and not remotely.

### 4. Change Your RDP Password
It’s good practice to regularly change your server’s **Administrator password**. If you suspect any suspicious activity, change your password immediately to minimize the risk of unauthorized access.

---

## 5. Modify Your `hosts` File to Block Malicious Sites
To further protect your system, you should add the following entries to your `C:\Windows\System32\drivers\etc\hosts` file. This will block access to malicious domains:

```
127.0.0.1 cipher-panel.me 
127.0.0.1 ciphercheats.com
127.0.0.1 keyx.club
127.0.0.1 dark-utilities.xyz

127.0.0.1 fivehub.xyz
127.0.0.1 fivehub-panel.site
```

### How to Edit the Hosts File:
1. Open **Notepad** as Administrator.
2. Navigate to `C:\Windows\System32\drivers\etc\hosts`.
3. Add the lines above to the end of the file.
4. Save the file.

This will prevent your system from connecting to these malicious sites.

---
## More ideas to stop this?
Just edit the readme.md and i'll look into it and publish it! Thanks for the contribution. 

## Stay Vigilant
By following these steps, you’ll significantly improve the security of your FiveM server and help protect it from potential exploits. Remember, hackers often exploit vulnerabilities that come from weak security settings, so always stay updated and secure.

Stay safe out there!


#FiveHub #FiveM #RemoteControl #Hacked #ScriptKiddies
