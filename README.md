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
- Install C++ Redistributalbe
- Configure permissions and install osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/dNY6K4Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

- Install/Enable IIS in Windows with CGI
  - Control Panel -> Program Files and Features -> Turn Windows features on or off -> [X]Internet Information Services
  - Expand Internet Information Services -> Expand World Wide Web Services -> [X] CGI (Allows the install of PHP manager)
  
</p>
<br />

<p>
<img src="https://i.imgur.com/QBmYejL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

  - Download and install PHP Manager for IIS
    - Run installer -> click next -> click "I agree" -> click install
  
</p>
<br />

<p>
<img src="https://i.imgur.com/vksH9WA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
- Download and install the Rewrite Module
  - Run installer -> click "I accept the terms in the Liscense Agreement -> click Install -> click Finish
  
</p>
<br />

<p>
<img src="https://i.imgur.com/DUCxe4i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 
- Create the directory c:\PHP
- Download PHP 7.3.8 and unzip the contents into C:\PHP

</p>
<br />
    
<p>
<img src="https://i.imgur.com/7RPcVT9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
    
- Install C++ Redistributable
  - Download and install VC redist.x86.exe (needed for PHP)
    - Run installer -> click "Agree to the license terms and conditions" -> click install
    
</p>
<br />

<p>
<img src="https://i.imgur.com/qZENG3F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

- Download and install MySQL 5.5.62
  - Run installer -> Typical setup -> Launch Configureation Wizard (after install) -> Standard Configuration -> Choose a password (This is the root password) -> Execute
