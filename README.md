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
Once navigated to the appropriate screen activate the dependencies. This is where we activate IIS>WWS>ADF>CGI
  
</p>

<br />

<p>
Next step is to Install PHP from the OSTicket folder(Notice that we unzipped the folder to access the contents)
Create a DIRECTORY afte the name "PHP" > This is where you will extract all files within the php-7.3.8 folder and install.

</p>
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
