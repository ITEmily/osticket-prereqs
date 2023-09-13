<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>
<br />
<br />
<br />
<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Step 1: Create an Azure Virtual Machine, Windows 10, 4 vCPUs.
- Step 2: Install/Enable IIS in Windows with CGI.
- Step 3: Prepare the virtual machine for osTicket.
- Step 4: Create a directory C:\PHP.
- Step 5: Continue to prepare the VM for osTicket.
- Step 6: Settings for MySQL installation.
- Step 7: Open IIS (Internet Information Service) as an Administrator.
- Step 8: Install osTicket v1.15.8.
- Step 9: Assign Permissions.
- Step 10: Set up osTicket in Browser.
- Step 11: Create a database called "osTicket". 
- Step 12: Clean up. 

<br />
<br />
<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/y3M3DBu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1: Create an Azure Virtual Machine, Windows 10, 4 vCPUs.  First, create a Resource Group.  I called mine "RG-osTicket".  Then create the Windows VM within that resource group. Mine is called "VM-Windows".
</p>
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/EeSwLgT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2: Install/Enable IIS in Windows with CGI.  IIS (Internet Information Services) is a web server that osTicket runs on.
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/EOnD5ve.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3: Prepare the virtual machine for osTicket. In the above picture I have labeled the installation files in the order they will be installed.  Begin by downloading and installing PHP Manager for IIS.  Then, download and install the Rewrite Module.
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/SZsvyGG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4: Create a directory C:\PHP.
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/EOnD5ve.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5: Continue to prepare the VM for osTicket.  Download PHP-7.3.8 and unzip the contents into the C:\PHP folder you just created. Then, download and install VC_redist and MySQL 5.5.62.
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/cW0VJCO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6: Settings for MySQL installation. When installing MySQL select the following options: Typical Setup, Launch the Configuration Wizard, and Standard Configuration. Make sure you remember your password for later access.
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/QTPwtzW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 7: Open IIS (Internet Information Service) as an Administrator.  Register PHP from within IIS.
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/AzEduJU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 8: Install osTicket v1.15.8.  Extract and copy the "upload" folder into C:\inetpub\wwwroot, and then rename the "upload" folder to "osTicket."
  Now we need to enable some extension. Go to IIS, click "sites", "default", "osTicket". Click "Enable or disable an extension." Right click and enable the following extensions: php_imap.dll, php_intl.dll, php_opcache.dll.
  Finally, rename ost-sampleconfig.php to ost-config.php.  Find it under C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/eYkqga6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 9: Assign Permissions.  Right Click ost-config.php and under "properties", security tab, advanced, disable inheritance.  Set new permissions for "everyone."
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/3FAjqdF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 10: Set up osTicket in Browser. In IIS go to sites, Default, osTicket.  On the right side of the screen click on "Browse *80". Click "continue" to set up osTicket in the browser. Before you fill in the MySQL Database information, download and install HeidiSQL. 
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/R8cFVNI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 11: Create a database called "osTicket".  
  Go back to osTicket in the browser and fill in MySQL Database name at osTicket. MySQL Username is "root" and use the password you had created earlier.
</p>
<br />
<br />
<br />
<br />
<p>
<img src="https://i.imgur.com/mENJmQL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 12: Clean up.  Delete C:\inetpb\wwwroot\osTicket\setup.
  Go to C:\inet\wwwroot\osTicket\include\ost-config.php and set permissions to "Read" only.
</p>
<br />


