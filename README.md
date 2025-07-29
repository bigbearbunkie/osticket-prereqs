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
<p>
Step 3: Prepare the VM Desktop
</p>
<p>You will set up the environment before installing your files
</p>
<p>Action: </p>
<p>+ Open edge and download  [osTicket-Installation-Files.zip](https://docs.google.com/document/d/1DyjX8LeVU98LjhXO2t2K2F0aHywI2N9GD57T3taO5qo/edit?tab=t.0)(url)
<p>
<p>+ Extract to desktop and it will show up as "osTicket-Installation-Files" in File Explorer</p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
