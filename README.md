# <p align="center">
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

- Windows 10 VM in Azure
- RDP
- os Ticket
- enable IIS and CGI
- PHP manager for IIS
-  MySQL 5.5.62
<p>
<img src="https://i.imgur.com/8PmW7L3.png" height="80%" width="80%" alt="osticket to root file"/>
</p>
<p>

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/CfitwNr.png" height="80%" width="80%" alt="osticket to root file"/>
</p>
<p>
After you have finished installing the pre-reqs, download osTicket v1.15.8 from the Installation Files Folder. Extract and copy the "upload" folder to c:\inetpub\wwwroot, and rename it "upload" to "osTicket". Reload IIS (Open IIS, Stop and Start the server)
 
</p>
<br />

<p>
<img src="https://i.imgur.com/7MMi6FR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, Go to Sites ---> Defualt ---> osTicket. On the right, click "browse" *.80"
</p>
<br />

<p>
<img src="https://i.imgur.com/XHvNJgV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Note, if you notice, some of the extensions aren't enabled so we will now go back to IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/msFHN72.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Double-Click PHP Manager ---> Click "Enable or disable extension"
-Enable: php_imap.dll
-Enable: php_intl.dll
-Enable: php_opcache.dll
Refresh the osTicket site in your browser, and you should notice we now have all green checkmarks as they are enabled.
 
Note: We also want to Rename: ost-config.php From C:\linepub\wwwroot\osTicket\include\ost-sampleconfig.php ---> C:\linepub\wwwroot\osTicket\include\ost-config.php

</p>
<br />
<p>
<img src="https://i.imgur.com/kJOwCxc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After you have finished setting up osTicket in the browser, from the installation files, download and Install HeidiSQL and open it. Create a new session using root/password1 and connect to it. Creaate a database called "osTicket". Continue setting up osTicket in the browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/fuIUXZP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Hopefully at this point osTicket is installed with no errors. Lastly clean up and delete: C:\linetpub\wwwroots
 osticket\setup and set permissions to "read" only C:\linetpub\wwwroots\osticket\include\ost-config.php
</p>
<br />
