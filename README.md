<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Configuration Steps</h2>

<p>
This is the configuration portion of the osTicket Lab. If you missed the previous steps here is the <a href="https://github.com/DevilDog2001/osticket-prereqs">Link.</a>
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
<img src="https://i.imgur.com/g209LMw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next press the install button and you should recieve a prompt on a new username for MySQL as root and to create the password<strong>(Document these 2 pieces of information they will be used later in the lab)</strong>. Once you do press next and go through the installation, the installation should fail and prompt the page above.
</p>
<br />
<p>
<img src="https://i.imgur.com/j1MGLmo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we are going to install the PHP Manger and vcredist located within the <a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a> to are google Drive for the lab. These 2 files can be found in your file explorer within the downloads as showen above.
</p>
<br />
<p>
<img src="https://i.imgur.com/4ViV05z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After that we head back into are <a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a> to are google Drive for the lab and download the osTicket file. Once downloaded extract the zipped folder from the downloads into the downloads, doing this makes the zip folder create a regular folder with the same contents.
</p>
<br />
