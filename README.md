<h1>SQL - Proxmox Server Setup (Virtual Machines) </h1>


<h2>Description</h2>
Project consists of a building a persistent server for my home lab.  Creating on premises resources for enterprise virtualization and Security Information and Event Management (SIEM) testing.


<h2>Utilities Used</h2>

- <b>Old computer I built with a dying graphics cards</b>

<h2>Virtual Environment Used </h2>

- <b>Proxmox</b>

<h2>Bios Settings:</h2>

<p align="center">
Continuous press the DELETE key after turning on the computer to enter the Bios menu.: <br/>
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
Select Proxmox VE GNU/Linux to initialize the installer:  <br/>
<img src="https://i.imgur.com/qZJHivm.jpeg" height="80%" width="80%" alt="RMA"/>
<br />
<br />
I used the Install Proxmox VE (Terminal UI) because my graphics cards is failing and this server will be running headless.:  <br/>
<img src="https://i.imgur.com/EQ0sMkF.jpeg" height="80%" width="80%" alt="Records"/>
<br />
<br />
Created a new view of the Customers Tables. To make the terminology match the RMA desk terminology.:  <br/>
<img src="https://i.imgur.com/2Fs7Hin.png" height="80%" width="80%" alt="Desk"/>
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
