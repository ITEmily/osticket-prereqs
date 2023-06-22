<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Step 1: Create an Azure Virtual Machine, Windows 10, 4 vCPUs
- Step 2: Install/Enable IIS in Windows with CGI
- Step 3: Prepare the virtual machine for osTicket.
- Step 4: Create a directory C:\PHP.
- Step 5: Continue to prepare the VM for osTicket.
- Step 6: Settings for MySQL installation.
- Step 7 Open IIS (Internet Information Service) as an Administrator. 

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/y3M3DBu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1: Create an Azure Virtual Machine, Windows 10, 4 vCPUs.  First, create a Resource Group.  I called mine "RG-osTicket".  Then create the Windows VM within that resource group. Mine is called "VM-Windows".
</p>
<br />

<p>
<img src="https://i.imgur.com/EeSwLgT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2: Install/Enable IIS in Windows with CGI.  IIS (Internet Information Services) is a web server that osTicket runs on.
</p>
<br />

<p>
<img src="https://i.imgur.com/EOnD5ve.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3: Prepare the virtual machine for osTicket. In the above picture I have labeled the installation files in the order they will be installed.  Begin by downloading and installing PHP Manager for IIS.  Then, download and install the Rewrite Module.
</p>
<br />

<p>
<img src="https://i.imgur.com/SZsvyGG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4: Create a directory C:\PHP.
</p>
<br />

<p>
<img src="https://i.imgur.com/EOnD5ve.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5: Continue to prepare the VM for osTicket.  Download PHP-7.3.8 and unzip the contents into the C:\PHP folder you just created. Then, download and install VC_redist and MySQL 5.5.62.
</p>
<br />

<p>
<img src="https://i.imgur.com/cW0VJCO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6: Settings for MySQL installation. When installing MySQL select the following options: Typical Setup, Launch the Configuration Wizard, and Standard Configuration. Make sure you remember your password for later access.
</p>
<br />

<p>
<img src="https://i.imgur.com/QTPwtzW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 7: Open IIS (Internet Information Service) as an Administrator.  
</p>
<br />

<p>
<img src="https://i.imgur.com/AzEduJU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 8
</p>
<br />

<p>
<img src="https://i.imgur.com/eYkqga6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 9
</p>
<br />

<p>
<img src="https://i.imgur.com/3FAjqdF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 10
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
