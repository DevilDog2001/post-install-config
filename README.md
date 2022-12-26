<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation</h1>
This tutorial outlines the installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation requirements</h2>

- VM (Virtual Machine)
- RDP (Remote Desktop Connection)
- Google Drive file (<a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a>)
- Internet Information Service (IIS) set up
- Most importantly a Wifi connection

<h2>Installation Steps</h2>

<p>
This is the installation portion of the osTicket Lab. If you missed the previous steps here is the <a href="https://github.com/DevilDog2001/osticket-prereqs">Link.</a>
</p>
<p>
<img src="https://i.imgur.com/rdVp6Sn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continuing from where we left off within the VM. We want to now open a windows control panel and head to programs, form programs select program and feature. Now within the program and features there will be a selection called Turn windows features on or off on the left hand side, select that button. And the following will be prompted on your screen, from there we will select the IIS(Information Internet Services) and let the IIS install.
</p>
<br />

<p>
<img src="https://i.imgur.com/xyCY5M7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now after we have the IIS finish, we will go to the google doc and download the WebPlatformInstaller file. The file will download this launcher as shown above, go through the installation when complete the following will appear.
</p>
<br />

<p>
<img src="https://i.imgur.com/93ejQfx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we select finish we will then head over to the windows search and type in platform. The Web Platform Installer 5.1 should appear. moving to the search bar at the top right we will type in MySQL and select the MySQL Windows 5.5 released 9/9/2015.
</p>
<br />
<p>
<img src="https://i.imgur.com/j7Q72F4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
Next after adding MySQL go back to the search bar and type PHP. From there filter the names by pressing name and locate the PHP ....(x86) files you want to add them up until you reach PHP 7.4.13 (x86). The image above from the lab shows the exact files, there should be exactly 12 items to be installed after selecting the files.
</p>
<br />
<p>
<img src="https://i.imgur.com/g209LMw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next press the install button and you should recieve a prompt on a new username for MySQL as root and to create the password(Document these 2 pieces of information they will be used later in the lab). Once you do press next and go through the installation, the installation should fail and prompt the page above.
</p>
<br />
<p>
<img src="https://i.imgur.com/j1MGLmo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we are going to install the PHP Manger and vcredist located within the <a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a> to are google Drive for the lab. These 2 files can be found in your file explorer within the downloads as shown above.
</p>
<br />
<p>
<img src="https://i.imgur.com/4ViV05z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After that we head back into are <a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a> to are google Drive for the lab and download the osTicket file. Once downloaded extract the zipped folder from the downloads into the downloads, doing this makes the zip folder create a regular folder with the same contents.
</p>
<br />
<p>
<img src="https://i.imgur.com/Q3LUJgA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next head into the new and unzip folder from the osTicket download and copy the upload folder. Go to <strong>This PC--> then windows(C:)--> then inetpub--> and finally open wwwroot</strong> and paste the upload folder within. Rename that folder to osTicket.
</p>
<br />
<p>
<img src="https://i.imgur.com/PlitxOI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we are done with the last step we want to head to are windows search bar and type in IIS. Select IIS and restart IIS with the panel on the right side, after that select the drop down arrow key for VM-osTicket or whatever name you selected earlier in the lab on the <strong>left hand panel--> then select sites--> Defualt Website--> and are osTicket folder</strong> should be there.
</p>
<br />
<p>
<img src="https://i.imgur.com/KIGAyir.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After we are going to select the PHP Manager within the osTicket Home located in the center. From there <strong>select Enable or disable an extension, look for php_imap.dll is enable along with php_intl.dll and php_opcache.dll.</strong>
</p>
<br />
<p>
<img src="https://i.imgur.com/dRGPdWI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we head back to are wwwroot folder within file explorer, from there we select <strong>osTicket--> Then include</strong>. When inside the include folder scroll down to the ost-sampleconfig.php to ost-config.php as shown above.
</p>
<br />
<p>
<img src="https://i.imgur.com/cHBdPn3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After we changed the ost-sampleconfig.php to ost-config.php we will <strong>open its properties then --> open security --> click on advance --> then disable inheritance --> add permission --> select principle at the top left --> from there within the open box below for objects type everyone --> select Check Names --> and select ok --> on the following page select full control to give all basic permissions besides Special permissions for everyone</strong>. Your security panel should display whats above with everyone and full control under access.
</p>
<br />
<p>
<img src="https://i.imgur.com/vCXWto2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If you've reached this page all the following steps have been completed successfully. Now simple fill out all the information as shown<strong>(Document The Admin User portion as well as the Database setting username and password will be needed for the lab).</strong>
</p>
<br />
<p>
<img src="https://i.imgur.com/mQPzPDm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we head back into are <a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a> to are google Drive for the lab and download the HeidiSQL. Go through the complete download until the finish button is prompt, after you select finish the application will open as shown above.
</p>
<br />
<p>
<img src="https://i.imgur.com/GhJrKSP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select the add button on the button left, Heidi will prompt you to put in the password you create earlier when downloading the php files within WebPlatformInstaller 5.1. Enter the password and you will be sent to the page shown.Next <strong>rightclick unnamed --> then hover over create new --> and select Database</strong>. Name that dataase osTicket<strong>(it is important the spelling is correct)</strong>.
</p>
<br />
<p>
<img src="https://i.imgur.com/wvurZnY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now go back to the osTicket web browser as shown above and enter the new database name along with the respected credentials. Press install and wait for the page to load.
</p>
<br />
<p>
<img src="https://i.imgur.com/aCKlFCn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once complete you will have this page appear letting you know that you've successfully created the osTicket system. The links below are for the user end and the staff as well.
</p>
<br />
<p>
<img src="https://i.imgur.com/cWrNy3w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Final step, head back to the folder where we were in the include folder. From there <strong>Rightclick properties--> head to security tab --> then advance --> and double click on everyone --> once you are back in permissions change every user to read and execute</strong> press ok and close out the tabs for the properties.
</p>
<br />
<p>
<img src="https://i.imgur.com/2kYWhCm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To end off the installation for osTicket. Head into the osTicket folder by <strong>clicking on This PC --> then windows (C:) --> select inetpub --> wwwroot --> and finally select osTicket.</strong> There we must delete the setup folder, in order to do so we must delete the contents with the folder. After deleting the contents within the setup folder we can move onto deleting the setup folder from osTicket. And congradulations you have completed the osTicket Installation.
</p>
<br />
<p>
This will conclude the Installation for the osTicket Lab. The next section we will begin to use osTicket and begin with the configurations. Next section <a href='https://github.com/DevilDog2001/osTicket-configurations'>Configurations</a> .
</p>
