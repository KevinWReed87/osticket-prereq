<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket
- HeidiSQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a Virtual Machine using Microsoft Azure
- Using Remote Desktop Protocol into your Windows 10 virtual machine
- Install / Enable IIS in Windows with CGI
- Download and install PHP Manager for IIS
- Download and install the Rewrite Module
- Create the directory C:\PHP
- Download PHP 7.3.8 and unzip the contents into C:\PHP
- Download and install VC_redist.x86.exe
- Download and install MySQL 5.5.62
- Open IIS as an Admin and register PHP from within IIS
- Install osTicket v1.15.8
- Download and install HeidiSQL
- Continue setting up osTicket in the browser




<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/QdFQkre.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p><img src="https://i.imgur.com/md4RHle.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> </p>

<p><img src="https://i.imgur.com/TRtmZBP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/></p>



<p>Creating a Virtual Machine using Microsoft Azure. Azure Virtual Machine Windows 10, 4 vCPUs Name: Vm-osticket Username: labuser Password: osTicketPassword1!
Then using the ip address assigned to the Virtual Machine to remote desktop into the VM.
</p>

<p>
<img src="https://i.imgur.com/GaO2jCL.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/hpIUUkF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Remote desktop in the virtual machine created with Microsoft Azure using the virtual machine ip address found on Azure.
</p>
<br />
<h2>Install / Enable IIS in Windows WITH CGI
</h2>
<p>
<img src="https://i.imgur.com/vJvgqN3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <img src="https://i.imgur.com/rFUQoyB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install and enable IIS in Windows WITH CGI. Right click start select run, type control themn programs. Turn windows features on and off. 
  Then select World Wide Web Services -> Application Development Features -> CGI then press ok for installation.
<br />

<p><img src="https://i.imgur.com/dt92GjH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/></p>
<p>
From the installation files download and install PHP Manager for IIS  (PHPManagerForIIS_V1.5.0.msi). Also download Rewrite Module (rewrite_amd64_en-US.msi)
</p>
<p><img src="https://i.imgur.com/AKeFDBm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/></p>
<p>Create a PHP folder inside the C: directory</p>
<br />

<p><img src="https://i.imgur.com/oW2wXGm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/></p>
<p>Download and extract all PHP files in to the previously created PHP folder under C:.
</p>

<p><img src="https://i.imgur.com/KXav9D9.png"</p>
<p>Download and install VC_redist.x86.exe.

Download and install mysql-5.5.62-win32.msi

Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Next ->
Password1 (root will be the username, but you don't need to set that up)</p>

<p><img src="https://i.imgur.com/pa8KSq6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/></p>

<p><img src="https://i.imgur.com/2lb5Sqi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/></p>

<p>After installing all of the required files, open IIS and run IIS as an Administrator and register PHP in IIS. Double-click on PHP --> Click on Register PHP new version. Follow the sequence in the C:\ directory, PHP -> php.cgi.exe. Once PHP has been registered make sure to restart the server, by clicking "Restart Server".
</p>

<p><img src="https://i.imgur.com/9Em2X90.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>After restarting the server, Install the osTicket file from the installation folder. Extract and copy the "upload folder" to c:\inetpub\wwwroot (simply dragging and dropping the file and renaming it "osTicket". Then restart IIS inside the server.</p>

<p><img src="https://i.imgur.com/FYPo5OZ.png"</p>
<p><img src="https://i.imgur.com/Q4xSVIg.png"</p>
<p>On the left expand the menus osTicket-VM -> Sites -> Default Web Site -> then click on osTicket.
On the right hit Browse *:80 and you should see the osTicket installer open inside of your default browser.
</p>

<p><img src="https://i.imgur.com/8mOuO3P.png"</p>
 <p>Go to IIS, sites, Defualt, osTicket, double click PHP Manager, click on Enable or Disable an extension. Enable the following extensions: php_imap.dll, php_intl.dll, php_opcache.dll and observe the changes in the osTicket site on the web browser
</p>

<h2>Rename: ost-config in PHP folder </h2>
<p>
<img src="https://imgur.com/F7El4Yy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go into file explorer and remove sample from "ost-sampleconfig.php by following C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php. Rename the file to "ost-config.php
</p>
<br />

<h2>Assign Permissions in ost-config.php and continue to setup osTicket </h2>
<p>
<img src="https://imgur.com/8ax66cQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to ost-config.php, right click, select properties, select security, and select advanced. Click on everyone, click on edit, and change to only read and read and view
</p>
<br />

<h2>Download and install HeidiSQL and continue to setup osTicket in the browser </h2>
<p>
<img src="https://imgur.com/R59XQRu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install HeidiSQL. Add in password from MySQL setup to connect the database. Once, connected to the database, continue to fill out the following information for osTicket in the web browser and click "Install Now"
</p>
<br />

<h2>Clean Up</h2>
<p>
<img src="https://imgur.com/yRw4fvm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Delete "setup" folder in osTicket file and Set permissions to Read only in ost-config.php
</p>
<br />
