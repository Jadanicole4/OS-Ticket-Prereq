<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial provides a detailed overview of the prerequisites and step-by-step instructions for installing the open-source help desk ticketing system, osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 November 2021 Update (Version 21H2)

<h2>List of Prerequisites</h2>

- IIS (Internet Information Services) W/ CGI
- PHP Manager for IIS
- Microsoft URL Rewrite Module for IIS (x64)
- PHP 7.3.8 Non-Thread Safe (NTS) for Windows (x86)
- Microsoft Visual C++ 2015-2019 Redistributable (x86)
- MySQL Community Server 5.5.62

<h2>Installation Step 1: Setup a Virtual Machine in Azure </h2>

<p>
<img src="https://i.imgur.com/Dz7njNQ.png"/>
</p>
<p>
To create a virtual machine in Azure, navigate to the Virtual Machines section.
</p>
<br />

<p>
<img src="https://i.imgur.com/fQ0LMOl.png"/>
</p>
<p>
Next, click the "Create" dropdown button, highlighted in blue.
</p>
<br />

<p>
<img src="https://i.imgur.com/Nk76zt5.png"/>
</p>
<p>
Next, select "Azure Virtual Machine" on the dropdown menu.
</p>
<br />

<p>
<img src="https://i.imgur.com/DiHCgLV.png"/>
</p>
<p>
Next, enter the project details in the resource group and name it "OS-Ticket."
</p>
<br />

<p>
<img src="https://i.imgur.com/lIfT0RL.png"/>
</p>
<p>
Next, name the VM "OSticket-vm"
</p>
<br />

<p>
<img src="https://i.imgur.com/KES4AI6.png"/>
</p>
<p>
Select, the image Windows 10
</p>
<br />

<p>
<img src="https://i.imgur.com/mSZUu9b.png"/>
</p>
<p>
Select a virtual machine size that includes at least 2 vCPUs to ensure sufficient processing power for your needs.
</p>
<br />

<p>
<img src="https://i.imgur.com/0weHDLA.png"/>
</p>
<p>
Fill out the username and password fields, ensuring that the password meets the required security criteria, such as including a mix of uppercase and lowercase letters, numbers, and special characters for better protection.
</p>
<br />

<p>
<img src="https://i.imgur.com/oxVaHJj.png"/>
</p>
<p>
For licensing, please check the box.
</p>
<br />

<p>
<img src="https://i.imgur.com/zNl5fus.png"/>
</p>
<p>
Please note that the system pre-fills most tabs, and at this point, you will not need to make any changes or adjustments. Click "Next" until you reach the "Review and Create" section.
</p>
<br />

<p>
<img src="https://i.imgur.com/d2bOUvT.png"/>
</p>
<p>
Now, review and create Virtual Machine, and notice it states "Deployment in progress".
</p>
<br />

<p>
<img src="https://i.imgur.com/KIOXPBJ.png"/>
</p>
<p>
Congratulations! If all allocations are correct, you will have successfully created a virtual machine on your resource page with a valid IP address.
</p>
<br />

<h2>Installation Step 2: How to Connect to Remote Desktop and Install the osTicket Requirements. </h2>

<p>
<img src="https://i.imgur.com/5QHNzKD.png"/>
</p>
<p>
Open Remote Desktop on your computer, enter the public IP address of the virtual machine previously created on Azure, and press Connect.
</p>
<br />

<p>
<img src="https://i.imgur.com/PeMqNl3.png"/>
</p>
<p>
Enter the secure username and password you created earlier and press Enter.
</p>
<br />

<p>
<img src="https://i.imgur.com/VHiOCR6.png"/>
</p>
<p>
You should now be logging into the virtual machine on your desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/q19BpWf.png"/>
</p>
<p>
Once you are on the virtual machine desktop, open Microsoft Edge, and download all required files.
</p>
<br />

<p>
<img src="https://i.imgur.com/oTfuD6T.png"/>
</p>
<p>
Utilizing this link, we will install the requirements needed to set up osTicket.
[https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0]
</p>
<br />

<h2>Installation Step 3: How to Install the OS Ticket requirements </h2>

<p>
<img src="https://i.imgur.com/P8gzBzq.png"/>
</p>
<p>
Once files have been downloaded, navigate to your downloaded file, right click and select extract all.
</p>
<br />

<p>
<img src="https://i.imgur.com/HsZThTq.png"/>
</p>
<p>
Browse the destination folder and nevigate to desktop and press extract.
</p>
<br />

<p>
<img src="https://i.imgur.com/kEgCfjH.png"/>
</p>
<p>
Now, navigate to the Control Panel on your VM, notice the "Programs," section and then choose "Uninstall a program," highlighted in blue underneath "Programs."
</p>
<br />

<p>
<img src="https://i.imgur.com/RkL3bde.png"/>
</p>
<p>
In the next window, select "Turn Windows features on or off." Located on the left side of the menu.

<p>
<img src="https://i.imgur.com/DAsvV7c.png"/>
</p>
<p>
When the "Turn Windows features on or off" window opens, expand "Internet Information Services."
</p>
<br />

<p>
<img src="https://i.imgur.com/OrmkRF3.png"/>
</p>
<p>
Expand "Application Development Features," select "CGI," press "OK," and allow the system to update."
</p>
<br />

<p>
<img src="https://i.imgur.com/RJ4dkQ3.png"/>
</p>
<p>
From your desktop, open the file folder that was downloaded.
</p>
<br />

<p>
<img src="https://i.imgur.com/SuWaYMU.png"/>
</p>
<p>
Extract and install PHP Manger.
</p>
<br />

<p>
<img src="https://i.imgur.com/CGLgwDz.png"/>
</p>
<p>
Rewrite AMD file
</p>
<br />

<p>
<img src="https://i.imgur.com/agePjuE.png"/>
</p>
<p>
Once these files are downloaded, open File Explorer, navigate to the C: drive, create a new folder, and name it "PHP."
</p>
<br />

<p>
<img src="https://i.imgur.com/GORT89U.png"/>
</p>
<p>
Extract the files from the zipped PHP file and move them into the newly created PHP folder in the C: drive.
</p>
<br />

<p>
<img src="https://i.imgur.com/Ft7otPN.png"/>
</p>
<p>
Go back to the file folder for osTicket and download Microsoft Visual C++.
</p>
<br />

<p>
<img src="https://i.imgur.com/UQfApeT.png"/>
</p>
<p>
Once that is complete, install MySQL.
</p>
<br />

<p>
<img src="https://i.imgur.com/ua2tPGY.png"/>
</p>
<p>
Once MySQL is downloaded, select the standard configuration.
</p>
<br />

<p>
<img src="https://i.imgur.com/MBoyAgH.png"/>
</p>
<p>
Next, create a root password for the user.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZRmOwFH.png"/>
</p>
<p>
Open Windows and run IIS Manager as an administrator.
</p>
<br />

<p>
<img src="https://i.imgur.com/ns7x8If.png"/>
</p>
<p>
Once IIS manager is open navigate to PHP manager.
</p>
<br />

<p>
<img src="https://i.imgur.com/yUvdkxu.png"/>
</p>
<p>
Register new PHP.
</p>
<br />

<p>
<img src="https://i.imgur.com/SGnTlsS.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
Once done start and stop services to reset PHP.
</p>
<br />

<p>
<img src="https://i.imgur.com/qIiVKGw.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
In IIS Manager, navigate to the Connections tab and select the "Default Web Site."
</p>
<br />

<p>
<img src="https://i.imgur.com/AmJ3Hen.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
Now, on the right-hand tab under "Manage folder," select "Browse *80 (HTTP)."
</p>
<br />

<p>
<img src="https://i.imgur.com/2vz2Do9.png"/>
</p>
<p>
If everything is correct so far, it should take you to the osTicket installer.
</p>
<br />

<p>
<img src="https://i.imgur.com/wPI5kE3.png"/>
</p>
<p>
Head back to the PHP manager and select PHP extensions.
</p>
<br />

<p>
<img src="https://i.imgur.com/JLtuTGk.png"/>
</p>
<p>
Make sure the correct ones are enabled.
</p>
<br />

<p>
<img src="https://i.imgur.com/M24mZOp.png"/>
</p>
<p>
On your Windows C drive, navigate to inetpub > wwwroot > osTicket > include.
</p>
<br />

<p>
<img src="https://i.imgur.com/WDc3Dev.png"/>
</p>
<p>
Navigate down to the file named ost-sampleconfig.php 
</p>
<br />

<p>
<img src="https://i.imgur.com/Yr44cgc.png"/>
</p>
<p>
change this to ost-config.php.
</p>
<br />

<p>
<img src="https://i.imgur.com/kMNBNy2.png"/>
</p>
<p>
Next, right click on folder and open properties.
</p>
<br />


<p>
<img src="https://i.imgur.com/J4hzMxK.png"/>
</p>
<p>
Select, Advanced.
</p>
<br />

<p>
<img src="https://i.imgur.com/NBzgSDn.png"/>
</p>
<p>
Select, Disable inheritance.
</p>
<br />

<p>
<img src="https://i.imgur.com/8kPyT70.png"/>
</p>
<p>
Select, remove all inherited permissions from this object.
</p>
<br />

<h2>Step 3: Now we will add permissions to allow all users access.</h2>

<p>
<img src="https://i.imgur.com/2vyi0JU.png"/>
</p>
<p>
Select Add, Located above enable inheritance 
</p>
<p>
<img src="https://i.imgur.com/pZXeJGb.png"height="80%" width="80%" alt=" Steps"/> 
</p>
<p>
Type, everyone in the object name box 
</p>
<p>
<img src="https://i.imgur.com/SznGEqw.png"/>
</p>
<p>
Check all Basic Permissions
</p>
<p>
<img src="https://i.imgur.com/BfZKELN.png"/>
</p>
<p>
Notice, that the permissions to allow all users access has now been added.
</p>
<p>
<img src="https://i.imgur.com/eEX5uG8.png"/>
</p>
<p>
Select, Apply
</p>
<br />

<p>
<img src="https://i.imgur.com/kkNUlaz.png"/>
</p>
<p>
Now that we have changed the settings, the osTicket extensions are enabled. The ones that are not enabled at this point are not needed at this time.
</p>
<br />

<h2>Step 4: Installation configuration of OS Ticket</h2>

<p>
<img src="https://i.imgur.com/tTdHZa6.png"/>
</p>
<p>
Open the osTicket file folder that was downloaded to your desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/2x9hxFm.png"/>
</p>
<p>
Open and install HEIDISQL .
</p>
<br />

<p>
<img src="https://i.imgur.com/AAvn85F.png"/>
</p>
<p>
Open HeidiSQL and Select create new.
</p>
<br />

<p>
<img src="https://i.imgur.com/Unq8fjJ.png"/>
</p>
<p>
Once, folder opens enter the password of ROOT and open.
</p>
<br />

<p>
<img src="https://i.imgur.com/YqmNwmz.png"/>
</p>
<p>
On the main page of SQL we will create a new data base.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZzQGmk2.png"/>
</p>
<p>
Next, name the new database Os-Ticket
</p>
<br />

<p>
<img src="https://i.imgur.com/TXtUUhf.png"/>
</p>
<p>
Once created, we can navigate back to the MySQL database connection tab, complete the form, and install.
</p>
<br />

<p>
<img src="https://i.imgur.com/6GEsLJO.png""/>
</p>
<p>
Congratulations, If everything was set up correctly, we will be able to navigate to the osTicket website.
</p>
<br />
