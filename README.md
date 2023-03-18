<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com) IN PROGRESS

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services (IIS) with CGI
- Install Web Platform Installer
- Install MySQL and set up username and password
- Install osTicket
- Configure permissions 

<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/a/rwkeWdT" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

- Install/Enable IIS in Windows with CGI
  - Control Panel -> Program Files and Features -> Turn Windows features on or off -> [X]Internet Information Services
   - Expand Internet Information Services -> Expand World Wide Web Services -> [X] CGI
  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

  - Download and install PHP Manager for IIS
  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
- Download and install the Rewrite Module
  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 
- Create the directory c:\PHP
- Download PHP 7.3.8 and unzip the contents into C:\PHP

</p>
<br />
    
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
    
- Download and install VC redist.x86.exe
    
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

- Download and install MySQL 5.5.62
    - Typical setup ->
    - Launch Configureation Wizard (after instal) ->
    - Standard Configuration ->
    - Choose a password
