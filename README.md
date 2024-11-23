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

Open IIS as an Admin

![image](https://github.com/user-attachments/assets/8d62e2f3-fb90-4c4d-8d3a-364842e12f35)

Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
Double Click PHP Manager 

![image](https://github.com/user-attachments/assets/736c6b6e-335d-4434-8b53-4f306cdcafba)

![image](https://github.com/user-attachments/assets/98142a8d-4299-4d59-94e2-199490ac1b16)
Click on Register New PHP
![image](https://github.com/user-attachments/assets/6a095213-54e4-4489-bcc5-59429e3c9a84)

Reload IIS (Open IIS, Stop and Start the server)

Install osTicket v1.15.8

![image](https://github.com/user-attachments/assets/c3434659-a6c1-45ef-8585-45530724f2b9)


From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
![image](https://github.com/user-attachments/assets/39ea68dd-0ae3-4b55-8972-0610496eda1a)



Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
![image](https://github.com/user-attachments/assets/b8922bb1-734e-46a3-a5e1-a78b7ce9e626)

![image](https://github.com/user-attachments/assets/745371d9-c86e-4a0e-9e50-51efc171b60e)

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes

![image](https://github.com/user-attachments/assets/eeafb5e3-8a1b-49f8-9d7a-a654a39b14e8)

</p>
<p>


</p>
<br />
