<h1>Proxmox Server Setup (Virtual Machines) </h1>


<h2>Description</h2>
Project consists of a building a persistent server for my home lab.  Creating on premises resources for enterprise virtualization and Security Information and Event Management (SIEM) testing.


<h2>Utilities Used</h2>

- <b>Old computer I built with a dying graphics cards</b>

<h2>Sever Installed </h2>

- <b>Proxmox</b>

<h2>Bios Settings:</h2>

<p align="center">
To enter the Bios menu continuous press the DELETE key after powering the computer on: <br/>
<img src="https://i.imgur.com/NFBhLCl.jpeg" height="80%" width="80%" alt="Creating"/>
<br />
<br />
Find and enable SVM Mode (Secure Virtual Machine):  <br/>
Save and exit the Bios menu:  <br/>
<img src="https://i.imgur.com/ugEpUHT.jpeg" height="80%" width="80%" alt="ERD"/>
<br />
<br />
Continuous press F12 on reboot to enter the boot menu: <br/>
Select Boot from USB: <br/>
<img src="https://i.imgur.com/Ys7jEOx.jpeg" height="80%" width="80%" alt="Keys"/>
<br />
<br />
<h2>Proxmox install:</h2>

<p align="center">
Select Proxmox VE GNU/Linux to initialize the installer:  <br/>
<img src="https://i.imgur.com/qZJHivm.jpeg" height="80%" width="80%" alt="RMA"/>
<br />
<br />
I used the Install Proxmox VE (Terminal UI) because my graphics cards is failing and this server will be running headless:  <br/>
<img src="https://i.imgur.com/EQ0sMkF.jpeg" height="80%" width="80%" alt="Records"/>
<br />
<br />
Accept the ULA:  <br/>
Select the drive to install Proxmox:  <br/>
Select your Country, Timezone, and Keyboard:  <br/>
<img src="https://i.imgur.com/r9EIJ1y.png" height="80%" width="80%" alt="Desk"/>
<br />
<br />
Add a strong root password:  <br/>
Add an Administrator email:  <br/>
Use a real email, this email can be used in the future with advanced features and updates:  <br/>
<img src="https://i.imgur.com/L551WLF.png" height="80%" width="80%" alt="Desk"/>
<br />
<br />
Select Management Interface (Internet access):  <br/>
Pick a hostname, something.something:  <br/>
Pick an IP address for your Proxmox ensure this IP is outside of your DCHP range:  <br/>
Select your gateway and DNS server address (Depending on your setup, these may be the same):  <br/>
<img src="https://i.imgur.com/JtQJOzc.png" height="80%" width="80%" alt="Desk"/>
<br />
<br />
Verify your info and Install:  <br/>
Wait for the instal to finish and the computer to restart:  <br/>
This server will be headless, we will login into the Proxmox server over the network:  <br/>
<img src="https://i.imgur.com/7CO1IN5.png" height="80%" width="80%" alt="Desk"/>
<br />
<br />
<h2>Proxmox and Network settings:</h2>
 
<p align="center">
Verfy your server IP is outside of your DCHP:  <br/>
Fix your IP address on your network for your new server: <br/>
<img src="https://i.imgur.com/FyWXyk9.png" height="80%" width="80%" alt="Desk"/>
<br />
<br />
Navigate to your Proxmox server address in a web browser:  <br/>
User name, root:  <br/>
Use your admin password and login:  <br/>
<img src="https://i.imgur.com/pEEyKWe.png" height="80%" width="80%" alt="Desk"/>
<br />
<br />
Click OK for No valid subscription, Proxmox does not require a subscription:  <br/>
Under your data center select your server, then open your sell:  <br/>
Ensure your local file is using all of your space:  <br/>
First delete your local file with the following command <br/> 
lvremove /dev/pve/data <br/>
Alocate the entire drive to your local storage for your VM <br/> 
lvresize -l +100%FREE /dev/pve/root  <br/>
Last resize command <br/> 
resize2fs /dev/mapper/pve-root:  <br/>
<img src="https://i.imgur.com/c2uExS0.png" height="80%" width="80%" alt="Desk"/>
<br />
<br />
Navigate to Storage in the Datacenter tab:  <br/>
Highlight local-lvm and click remove: <br/>
This is not a required step, but it is good practice to clear any links to folders you have deleted:  <br/>
<img src="https://i.imgur.com/Eaa0zi4.png" height="80%" width="80%" alt="Desk"/>
<br />
<br />
Add VM and Docker Container abilities to Proxmox; <br/>
Navigate to Datacenter. Storage, local:  <br/>
Highlight local and Click edit: <br/>
Under the general tab, click the Content Dropdown and select all options, click OK:  <br/>
<img src="https://i.imgur.com/6V0Q1f3.png" height="80%" width="80%" alt="Desk"/>
<br />
<br />
 
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
