# osTicket-Dependencies-setup 


<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Video Demonstration</h2>

- ### [YouTube: How to Easily Install a Ticketing System In Windows 10!](https://youtu.be/SongQlaEtc8)




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL
- PHP Manager
 Heidi SQL
- osTicket v1.15.8
- Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Portal Virtual Machines 
- Internet Information Services (IIS Manager)
- Configure CGI within IIS 
- Install PHP Manager
- Install MySQL 
- Register PHP within IIS Manager
- VC Redist
- Rewrite Module
- osTicket v1.15.8

<h2>Installation Steps</h2>


![INTRO](https://github.com/user-attachments/assets/35e46185-3daa-46ce-8a42-b57647ae2bb1)

<p>
Create a Azure account: Build a resource group and a VM
</p>
<br />

![PART1 OF iis](https://github.com/user-attachments/assets/24750683-0f02-4ef7-9a9b-f65e58a0ba1a)


<p>
Once logged in to the VM install CGI by following the steps: Open Control Panel>Click on Uninstall Programs> Turn On/Off
  <br/>
Enable all dependencies for osTicket Software IIS>WWS>ADF>CGI
</p>

<br /> <hr>

![PART 2 IIS](https://github.com/user-attachments/assets/0240ff01-6a1b-40a7-b4f9-d6a767895cfd)


<p>
Next step is to Install remaining files in order:
<br />
PHPManagerForIIS> rewrite_amd64> php_7.3.8 (this file should go to its own directory)> VC_redist.x86> MySQL-5.5.62>
</p>
<br />


![PHPSTAGE](https://github.com/user-attachments/assets/d2533178-7eb0-4d85-af9b-cb88c76c0948)


<p>rewrite_amd64</p>

![PHP_PART2](https://github.com/user-attachments/assets/78017acd-8957-4b23-9d30-2c23b8db04f6)

<p>
  
Create a DIRECTORY after the name "PHP" > This is where you will extract all files within the php-7.3.8 folder and install other files such as:

Install VC_redist.x86

Next Install mysql-5.5.62 file
  -Install using typical set up
  -Credentials root/root
</p>
<hr>

![root](https://github.com/user-attachments/assets/238a6251-32ff-44b3-8580-76d421620ff9)

<br />

![php_part3](https://github.com/user-attachments/assets/6c44851f-49bd-435d-b324-2169adb043a9)

<p>SELECT STANDARD CONFIGURATION for the above image</p>
<hr>
<br />

![_REDOP_PHP](https://github.com/user-attachments/assets/f0f91c58-dd69-4a6f-baf5-ce3e41988edc)

<p>Open IIS as Admin> Select sites> PHP Manager> Register new PHP version</p>

![Php_final](https://github.com/user-attachments/assets/fa10ebcb-efc0-421d-9c3c-24cbd69420f2)

<p> Now we register PHP in IIS:
  Open IIS Manager>OStickets>sites>PHP MANAGER
  Once done Reload IIS Manager (STOP AND START)
</p>
<br />
<p> Install osTicket v1.15.8<p/>
<p>-From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”<p/>
<br />
<hr>
 
![Screenshot 2025-02-03 152922](https://github.com/user-attachments/assets/894e682b-e76c-4ce1-b737-1d9967bd39a8)

![Screenshot 2025-02-03 152934](https://github.com/user-attachments/assets/e72ee558-e1ce-4ecc-878b-158601e35c00)

<hr>

<p>Select the Inet folder> Select wwwroot> Copy and Paste Default folder from osTicket folder>Rename the folder to "osTicekt" case sensitive</p>

![Screenshot 2025-02-03 153033](https://github.com/user-attachments/assets/36136313-afd3-4bae-a65b-d873fa1effd6)


<p>
-Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
RELOAD IIS MANAGER and go to sites -> Default_> "Browse *:80"
</p>

![osticket_part2](https://github.com/user-attachments/assets/fbf8d994-5e2b-4f9c-b92a-d784144f701c)

<p>Once all pre-requesites are created the website OSTICKET should be UP and RUNNING
<br />
NOTE* They are final configurations to complete
</p>

![osticket_part3](https://github.com/user-attachments/assets/f38e4cbf-d481-4a7a-88c7-626ea6bbaa2c)


<p>
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
</p>

![osticket_part4-1](https://github.com/user-attachments/assets/c32797dd-15f2-4c86-8568-9e4f02fc1de2)


<p>
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
</p>

![osticket_part4-2](https://github.com/user-attachments/assets/43c10cf9-7986-4d98-ba15-04146f462008)

<p> 
Refresh the osTicket site in your browser, observe the changes

</p>

![osticket_part5](https://github.com/user-attachments/assets/1747c82a-0510-4de7-9cb2-9ebb10fb4fd6)


<p>Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All</p>

![osticket_part6](https://github.com/user-attachments/assets/e16a633c-3867-4596-bdf0-183dc468d1fe)


<p>New Permissions -> Everyone -> All
<br /> 
Now we need to create a Database to hold all files from the osTicket software.

</p>

![osTicket_part7_preinstallation](https://github.com/user-attachments/assets/6e1c1d45-392d-48b4-9598-ce3b218f2de0)


<p>Install HeidiSQL</p>


![database_setpart1](https://github.com/user-attachments/assets/6aa0adf0-893b-418f-b115-1997ada6f886)


<p>Create a New Database by clicking New 
<br/> 
Keep credentials as root and root</p>

![database_part2](https://github.com/user-attachments/assets/71bc84b1-5090-462d-8c10-ffc39d0acaf0)

![database_part3](https://github.com/user-attachments/assets/a0c1d2e3-4a5c-4f13-a70e-b7287eb0b851)

<p>Make sure to name it exactly osTicket</p>

![database_part4](https://github.com/user-attachments/assets/b07c2c6a-539c-4d3a-b20f-1558aeac4fef)

<p>Congratulations if all steps were completed correctly osTicket System Software</p>

![osTicket_final](https://github.com/user-attachments/assets/2f61c2c6-c97b-4c0e-98d2-4482499df896)

<hr>
<h1>Summary</h1>
<p>This project serves as a comprehensive guide for setting up osTicket in both on-premises and cloud-based environments, making it valuable for IT professionals, system administrators, and help desk teams. The Technologies, Applications, and Services used were
<mark>osTicket</mark> – Open-source help desk and ticketing system.
<mark>IIS (Internet Information Services)</mark> – Web server for hosting osTicket.
<mark>MySQL/MariaDB</mark> – Database management for osTicket.
<mark>PHP </mark>– Required for running osTicket on IIS.
<mark>Azure Storage (Optional) </mark> – Cloud-based storage for backups and scalability
<br/>




</p></P>
