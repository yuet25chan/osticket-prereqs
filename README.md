# osticket-prereqs
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

- Windows 10, at least 4vCPUs </b> (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager for IIS - ensures PHP is properly configured to run ISS
- Rewrite Module - facilitates URL rewriting and redirects users to URLS
- VC_redist.x86
- MySQL
- HeidiSQL

<h2> osTicket Installation Steps</h2>
<p>

 1. **Download and Extract the osTicket Installation File** <br>
Once the Windows 10 virtual machine has been set up in Azure, you can log into the virtual machine by using your credentials. Open the Microsoft Edge web browser on the virtual machine download the osTicket installation zip file, and unzip it to desktop.

![Pic1](https://github.com/user-attachments/assets/289c54b8-830f-4b0f-839d-046e4e0e119c)

2. **Enable IIS** <br>
Open **Control Panel** -> **Programs** -> **Turn Windows features on and off**.
![Programs and Features ](https://github.com/user-attachments/assets/ceb5a698-8b9b-4d7a-9947-2bbfb3aea78b)
![Turn Windows Feature on and off](https://github.com/user-attachments/assets/7ac84dd2-cdd7-4eb4-a15f-9153b3ce25ac)

Select **World Wide Web Services**-> **Application Development Feature** -> **Enable CGI** <br>
![CGI](https://github.com/user-attachments/assets/bfe08f43-7292-4308-a588-0a2dffcfdafe)
   
</p>
<br />
<h2>Install Necessary Components</h2>

From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)

![image](https://github.com/user-attachments/assets/723b64f1-4016-4c35-90db-371c953f4d13)


Create the directory C:\PHP (Create a file in Windows C: drive and name it "PHP" )

From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
![image](https://github.com/user-attachments/assets/105690e2-5f05-4186-92c8-2c03bdcc8c5f)




From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)

![image](https://github.com/user-attachments/assets/9c580100-d6fd-41c4-9856-422273ca6f6f)



Typical Setup and click on Install

![image](https://github.com/user-attachments/assets/4617e01c-eb33-483a-bf1b-8e0878b13258)



Launch Configuration Wizard (after install) 
![image](https://github.com/user-attachments/assets/827e85e9-ed23-48de-99b9-daf90b4de1bf)


Standard Configuration ->
![image](https://github.com/user-attachments/assets/f6907a29-ab2f-4545-b582-3c1aaacfedd7)

![image](https://github.com/user-attachments/assets/b32ede0c-dc10-4a96-99e7-74a0e565d409)


Username: root
Password: root

![image](https://github.com/user-attachments/assets/736c6b6e-335d-4434-8b53-4f306cdcafba)
Open IIS as an Admin
  
</p>
<p>


</p>
<br />
