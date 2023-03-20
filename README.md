<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




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

- ### [Files Needed for Install](https://drive.google.com/drive/u/0/folders/1aCM7PZgRW4mZPEfLPqWPdZRou0mpgJ-A)

</p>
<br />

<p>
<kbd><img src="https://i.imgur.com/dNY6K4Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/></kbd>
</p>
<p>

- Install/Enable IIS in Windows with CGI
  - Control Panel -> Program Files and Features -> Turn Windows features on or off -> [X] Internet Information Services
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
  - Run installer -> Typical setup -> Launch Configureation Wizard (after install) -> Standard Configuration -> Choose a password (This is the root password) -> Execute -> Finish (creates a database for osTicket)

</p>
<br />

<p>
<img src="https://i.imgur.com/WcLs47L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
- Open IIS as an Admin -> PHP manager -> Register new PHP version -> c:\PHP -> php-cgi 
  - (best practice to click the name of the server and restart)  
  
</p>
<br />  
  
<p>
<img src="https://i.imgur.com/bJRNylp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

-Intall osTicket
  - Download zipfiles for osTicket -> extract and copy "upload" folder to c:\inetpub\wwwroot -> Rename "upload" folder to "osTicket"

  
</p>
<br />

<p>
<img src="https://i.imgur.com/ggeYKLK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>  

- Reload IIS and enable extensions
  - Open IIS as an admin -> click the server and restart it
  - Expand sites -> Expand Default Web Site -> osTicket -> click "Browse *80
    - note that some extensions are not enabled
  
</p>
<br />  

<p>
<img src="https://i.imgur.com/RUKtqNG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>  
  
- Go back to IIS, sites -> Default -> osTicket
  - Double-click PHP Manager
  - Click "Enable or disable an extension"
    - Enable php_imap.dll
    - Enable php_intl.dll
    - Enable php_opcache.dll
  - Referesh the osTicke site in your browser, observe the changes

</p>
<br />  

<p>
<img src="https://i.imgur.com/dj2et1t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>  
  
- Rename: ost-config.php
  - From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
  - To: C:\inetpub\wwwroot\osTicket\include\ost-config.php  
  
</p>
<br />  
  
<p>
<img src="https://i.imgur.com/LuVHCJf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>  

- Assign Permissions: ost-config.php
 - Right click ost-config.php -> Properties -> Security -> Advanced ->
  - Disable inheritance -> Remove All
  - Add -> Select a principal -> Everyone -> Ok -> check Full Control -> Ok -> Apply -> Ok -> Ok
  
</p>
<br />  
  
<p>
<img src="https://i.imgur.com/RamFcVT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>  

- osTicket setup (in browser)
  - Name Helpdesk
  - Default email (recieves email from customers)
  - Type in admin credentials (for lab purposes take note of these for later use)
  
<p>
<img src="https://i.imgur.com/87zMWda.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>  

- Download and install HeidiSQL
  - Open Heidi SQL
  - Create a new session, root/password
  - Connect to the session
  - Create a database called "osTicket"
  
</p>
<br />

<p>
<img src="https://i.imgur.com/9wqTPWO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>  

- Browser setup of osTicket
  - MySQL Database: osTicket
  - MySQL Username: root
  - MySQL Password: password
  - Click "Install Now"
  
</p>
<br />

<p>
<img src="https://i.imgur.com/QCIgZp7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>  

- Clean up
  - Delete: C:\inetpub\wwwroot\osTicket\setup
  - Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

