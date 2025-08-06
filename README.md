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

- Windows 11 Pro</b> (24H2)

<h2>List of Prerequisites</h2>

- Azure account with active subscription
- Created a resource group
- Created a virtual network and subnet
- Created a virtual machine in Azure
- Connected to the virtual machine using remote desktop

<h2>Installation Steps</h2>


<p>
Step 1: Create your resource group and virtual machine
</p>
<p>The resource group will contain all the resources necessary for this project. The virtual machine is what we will use to deploy Windows 11 Pro, download all required files, and run osTicket.
</p>
<p>Action: </p>
<p>+ Go to Virtual Machines and click "Create".</p>
<p>+ Under the "Resource group" selection tab, click "Create new".</p>
<p>+ Name it "osticket" and click OK.</p>
<p>
<img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/step%201%20Create%20a%20resource%20group%20and%20virtual%20machine.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>+ Name your virtual machine "osticket-vm" and select your region.</p>
<p>
<img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/step%201b%20Create%20a%20resource%20group%20and%20virtual%20machine.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>+ In "Image", select Windows 11 Pro as your operating system.</p>
<p>+ For "Size", choose one with at least 2 vcpus and 8 GiB memory.</p>
<p>
<img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/step%201c%20Create%20a%20resource%20group%20and%20virtual%20machine.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>+ Your username will be "labuser" and your password will be "Cyberlab-123"</p>
<p>
<img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/step%201d%20Create%20a%20resource%20group%20and%20virtual%20machine.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>+ Make sure "RDP(3389)" is selected and check the Licensing Agreement</p>
<p>
<img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/step%201e%20Create%20a%20resource%20group%20and%20virtual%20machine.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>+ Click "Review + create"</p>
<p>
<img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/step%201f%20Create%20a%20resource%20group%20and%20virtual%20machine.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Step 2: Connect to your Virtual Machine
</p>
<p>
  You will log into the VM to install the prerequisites
</p>
<p>Action:</p>
<p>+ Once your VM is deployed, open Remote Desktop Connection</p>
<p>+ Enter the Public IP Address and Username for your VM</p>
<p>
  <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%202%20connect%20to%20the%20virtual%20machine.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>+ Enter your Password</p>
  <p><img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%202b%20connect%20to%20the%20virtual%20machine.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <p>+ Click "Yes" on the next prompt and wait for your VM to load</p>
<p>
  <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%202c%20connect%20to%20the%20virtual%20machine.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p> 
<p>
  <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%202d%20connect%20to%20the%20virtual%20machine.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
<br />

<p>
Step 3: Prepare the VM Desktop
</p>
<p>You will set up the environment before installing your files
</p>
<p>Action: </p>
<p>+ Open edge and download  [osTicket-Installation-Files.zip](https://docs.google.com/document/d/1DyjX8LeVU98LjhXO2t2K2F0aHywI2N9GD57T3taO5qo/edit?tab=t.0)(url)
<p>+ Extract to desktop and it will show up as "osTicket-Installation-Files" in File Explorer</p>
  <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%203%20prepare%20the%20vm%20desktop.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%203b%20prepare%20the%20vm%20desktop.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%203c%20prepare%20the%20vm%20desktop.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Step 4: Install IIS with CGI Enabled
</p>
<p>+ Go to your start menu, open Control Panel, and under "Programs", click "Uninstall a Program"</p>
</p>
  <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/step%204b%20install%20iis.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>+ Click "Turn Windows features on or off"</p>
<p>
  <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%204c%20install%20iis.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>+ Enable Internet Information Services</p>
<p>+ Expand Internet Information Services</p>
<p>+ Expand World Wide Web Services</p>
<p>+ Expand Application Development Features</p>
<p>+ Enable CGI and click OK</p>
  <p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%204d%20install%20iis.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%204e.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%204f.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Step 5: Install IIS Extensions
</p>
<p>From osTicket-Installation-Files folder:</p>
<p> + Install PHP Manager for IIS: PHPManagerForIIS_V1.5.0.msi</p>
<p> + Install IIS Rewrite Module: rewrite_amd64_en-US.msi</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205b.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205c.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205d.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205e.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205f.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205g%20create%20file%20PHP.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205h%20create%20new%20file%20PHP.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> + Extract all PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205i%20extractall%20from%20php-7.3.8.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205j.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205k.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%205l.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Step 6: Install VC_redist.x86.exe (Microsoft Visual ++)
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%206.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%206b.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Step 7: Install MySQL Server
</p>
<p> + Run mysql-5.5.62-win32.msi </p>
<p> + Choose Typical Setup </p>
<p> + After install, launch MySQL Configuration Wizard </p>
<p> + Choose Standard Configuration </p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%207.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%207b.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%207c.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%207d.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%207e.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%207f.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p> + Set username: root, password: root </p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%207g.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%207h.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%207i.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Step 8: Register PHP with IIS
</p>
<p> + Open IIS as Administrator</p>
<p> + Click your computer name, then click PHP Manager</p>
<p> + For Path, select your PHP file</p>
<p> + Restart IIS (Stop/Start from within IIS Manager)</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%208.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%208b.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%208c.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%208d.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%208e.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%208f.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%208g.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%208h.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%208i.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
  Step 9: Unzip and Move osTicket Files
</p>
<p>From osTicket-Installation-Files folder:</p>
<p> + Extract All osTicket-v1.15.8.zip</p>
<p> + Copy the upload folder into C:\inetpub\wwwroot</p>
<p> + Rename upload to osTicket</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%209.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%209b.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%209c.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%209d.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%209e.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> + Open IIS, Stop and Start the server just like before</p>
<br />

<p>
Step 10: Browse to osTicket
</p>
<p>In IIS:</p>
<p> + Expand "Sites", expand "Default Website", and open "osTicket"</p>
<p> + On the right, click “Browse *:80”</p>
<p> + The osTicket Installer will open in your browser</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%2010.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%2010b.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%2010c.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
Step 11: Enable PHP Extensions
</p>
<p> + Go back to IIS, Sites, Default, osTicket</p>
<p> + Double-click PHP Manager</p>
<p> + Click “Enable or disable an extension”</p>
<p> + Enable:</p>
<p>php_imap.dll</p>
<p>php_intl.dll</p>
<p>php_opcache.dll</p>
<p> + Refresh the osTicket site in your browser and observe the changes</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%2011.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%2011b.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%2011c.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%2011d.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Step 12: Rename ost-sampleconfig.php
</p>
<p> + From C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php</p>
<p> + To C:\inetpub\wwwroot\osTicket\include\ost-config.php</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%2012.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <img src="https://github.com/bigbearbunkie/osticket-prereqs/blob/main/Step%2012b.PNG?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<Step 13: 
