# _osTicketpre


<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL
- PHP Manager


<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Portal 
- Internet Information Services (IIS Manager)
- Configure CGI within IIS (IIS>WorldWideWebServices>ApplicationDevelopmentFeatures>CGI)
- Install PHP Manager and create a DIRECTORY of its own.
- Install MySQL (Typical Set up> Launch Configuration Wizard after install> Standard Configuration___Credentials usually is ROOT,ROOT____)
- Register PHP within IIS Manager
<h2>Installation Steps</h2>


![INTRO](https://github.com/user-attachments/assets/35e46185-3daa-46ce-8a42-b57647ae2bb1)

<p>
Createa Azure account: Build a resource group and a VM
</p>
<br />

![PART1 OF iis](https://github.com/user-attachments/assets/24750683-0f02-4ef7-9a9b-f65e58a0ba1a)

<p>
Once logged in to the VM install CGI by following the steps: Open Control Panel>Click on Uninstall Programs> Turn On/Off
</p>

<br />

![PART 2 IIS](https://github.com/user-attachments/assets/0240ff01-6a1b-40a7-b4f9-d6a767895cfd)

<p>
Enable all dependencies for osTicket Software IIS>WWS>ADF>CGI
  
</p>

<br />

<p>
Next step is to Install PHP from the OSTicket folder(Notice that we unzipped the folder to access the contents)
  
Create a DIRECTORY after the name "PHP" > This is where you will extract all files within the php-7.3.8 folder and install.

Install rewrite_amd64 file

Install VC_redist.x86

Next Install mysql-5.5.62 file in the order that you are reading. Up to down.
  -Install using typical set up
  -Credentials root/root
</p>
<br />

<p>
When installing select Standard Configuration
</p>
<br />

![Php_final](https://github.com/user-attachments/assets/5d3c6d64-bb16-4725-96ab-e00648e2c72a)
![PHP_PART2](https://github.com/user-attachments/assets/78017acd-8957-4b23-9d30-2c23b8db04f6)

<p>Open IIS Manager>OStickets>sites>
</p>
