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
<br />
