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

- Installing IIS(Internet Information Services) in Windows with CGI
- Installling PHP Manager
- Creating a directory
- Installing MySQL
- Installing HeidiSQL

<h2>Installation Steps</h2>

<p align="center">
First, Install ISS. In the control panel, select "Uninstall a program." You are not uninstalling anything but this is where you need to be in order to find ISS.

![image](https://github.com/user-attachments/assets/b49fa9cf-8149-4aa9-968e-843efdbaea5f)

<p align="center"></p>
In the left panel, select "Turn Windows features on or off" and from there, navigate and check the box labled "Internet Information Services."

![image](https://github.com/user-attachments/assets/59f38502-9240-4902-a4af-20a5fc3e0b78)

<p align="center"></p></p>
Select the + beside IIS -> World Wide Web Services -> Application Development Features -> check CGI

![image](https://github.com/user-attachments/assets/77545b2e-e9fa-4757-8a78-bf3b77a7e781)

<p align="center"><p>
Next, in the osTicket installation file double click "PHPmanagerforIss" and select next until you see the install button and proceed with installation. It will take a moment to finish.

![image](https://github.com/user-attachments/assets/e2f9302d-ad7d-45bd-baec-472c98021d27)

<p align="center"></p>
Once PHPmanager is installed, double click "rewrite_amd64_en-US" accept the terms and conditions and proceed with intstallation.

![image](https://github.com/user-attachments/assets/abf636f5-ac5d-4cfb-8d88-4840b89b8d1b)

<p align="center"></p>
In left panel, select "This PC' then double click "Windows (C). That is normally called the "C drive." Create a new folder in your C drive named "PHP." Left click inside folder -> New -> Folder

![image](https://github.com/user-attachments/assets/e81c99ab-a35f-458c-990c-35ff857befd2)

<p align="center"></p>
Once your file is created, go back to the osTicket installation files, left click the "php-7.3.8-nts-Win32-VC" and extract all into the PHP folder that you just created.

![image](https://github.com/user-attachments/assets/84bc0adb-ac3a-47f0-9d3b-f60da282265b)

<p align="center"></p>
You should now, see all of these subjects within the PHP folder.

![image](https://github.com/user-attachments/assets/f867be88-29e2-4f97-9c17-587960770ff3)

<p align="center"></p>
Back in the osTicket Installation files, double click "VC_redist.x86" agree to the terms and conditions and click install.

![image](https://github.com/user-attachments/assets/7a4fbf67-2370-49c6-a340-dc254bd35c3d)

<p align="center"></p>
Next, double click "mysql-5.5.62-win32" accept terms and conditons, and keep selecting next until you get to this screen. Select "Typical" installation and click next until install button appears and proceeed with installation.

![image](https://github.com/user-attachments/assets/28ec0a0e-4470-4d80-9b22-4bf1a2d38045)

<p align="center"></p>
Once the installation is done, the "mysql instance configuration wizard" will open and you want to select "standard configuration" and click next. You will then be prompted to this window. Make a secure password, then proceed. In the instance of this demonstration, I used the password "root."

![image](https://github.com/user-attachments/assets/be800474-2541-4519-a26e-b36d0d662744)

<p align="center"></p>
Select the first two bubbles and click exceute and wait for configuration process to complete.

![image](https://github.com/user-attachments/assets/2b4b164c-9ed6-4a28-b3db-746d008741ed)

<p align="center"></p>
In the start menu, type "Iss" and open "Internet Information Services Manager."

![image](https://github.com/user-attachments/assets/bad5e949-715a-4045-9198-dcb481bbff76)

<p align="center"></p>
Double click "PHP manager."

![image](https://github.com/user-attachments/assets/2286267d-37de-4ca2-93e4-2c4ff608cfb5)

<p align="center"></p>
Once PHP manager is opened, select "Register new PHP version" and provide a path by clicking the three dots.

![image](https://github.com/user-attachments/assets/f931774b-fca8-4139-a06e-ff4841f1df8e)

<p align="center"></p>
Go to your C drive and open up the PHP folder that you created earlier and select the "php-cgi" file and that will be the path and click "Ok" after selecting the open "button."

![image](https://github.com/user-attachments/assets/437db392-06ad-478f-a1e0-8b3013c82025)

<p align="center"></p>
In the right corner, under "Actions", select "stop" and then select "start" just to give the PHP manager a chance to update what you just did.

![image](https://github.com/user-attachments/assets/4824629a-54fc-4a1e-9f61-34c5cbcf3d2a)

<p align="center"></p>
Back in the osTicket installion file, left click "osTicket-v1.15.8" and extract all to your desktop. Once you are prompted to this window, select extract.

![image](https://github.com/user-attachments/assets/50c34bb5-11b7-4394-86c7-184e44a43579)

<p align="center"></p>
In the C drive there will be a folder named "inetpub" double click it, then open folder named "wwwroot."

![image](https://github.com/user-attachments/assets/2cfe4ed4-105a-4d80-a5a9-86a1cc5d9f84)

<p align="center"></p>
Open up the "osTicket-v1.15.8" that you just extracted and drag the "upload" folder into the "wwwroot" folder and rename the "upload" folder to "osTicket."

![image](https://github.com/user-attachments/assets/fc11aea8-e53f-45a1-8e47-3cad15df7c12)

<p align="center"></p>
Reload ISS(stop and Start) then in the left panel, click the arrow next to "OSTicket-VM" -> sites -> osTicket. On the right panel click "Browse *:80."

![image](https://github.com/user-attachments/assets/32ed265d-4ef4-4f71-8652-07711d9691f8)

<p align="center"></p>
You will now be redirected to the osTicket website in your browser, and osTicket is now successfully installed."

![image](https://github.com/user-attachments/assets/ebc8e307-785b-4c46-9adb-4ce0948120c8)
