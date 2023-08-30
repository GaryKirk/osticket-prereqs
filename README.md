<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In order to improve my technical skills, I wanted to gain some experience using a professional ticketing system. This lab explains how to install the prerequisite software required to use osTicket, an open-source support ticketing system.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8

<h2>Required Setup of Preqrequisites to Ensure a Successful Installation of osTicket</h2>

<p>1. In Microsoft Azure, create a new Resource group. After this, in the new resource group, create a new virtual machine (VM) with 2-4 virtual CPUs. Make sure to also create a new virtual network. Connect to the VM using a Remote Desktop program on your device. <br /></p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/afdf7df5-0b36-4ca7-8142-f95dbb57b113" alt="Create VM"/><br /><br />

<p>2. Once connected to the the VM, find Control Panel --> Programs --> Turn Windows Features On or Off --> Internet Information Services --> World Wide Web Services --> Application Development Features --> Turn CGI on </p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/da49890d-955c-4994-98e9-847d1ac1ff82" alt="Enable IIS with CGI" width="300" length="300/"><br /><br />

<p>3. Go back to World Wide Web Services. Click Common HTTP Features and make sure that all features are turned on. Click OK to confirm all of the changes and the features will be installed. </p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/abe28239-6d1f-4e9c-a0be-20a52fbaf55f" alt="Turn on HTTP Features" width="300" length="300"/><br /><br />

<p>4. Once the changes have been applied, open a web browser and type a local host address "127.0.0.1". Click enter and you will see that IIS is working correctly. </p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/6bb42223-f518-4693-8114-b09c6915134f" alt="IIS Check"/ width="500" length="500"><br /><br />

<p>5. Download and install <a href="https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10">PHP Manager for IIS</a></p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/e3ee113d-07a1-437e-84d7-05384a8f0bdb" alt="PHP Manager for IIS" width="300" length="300"/><br /><br />

<p>6. Download and install <a href="https://www.iis.net/downloads/microsoft/url-rewrite">URL Rewrite</a></p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/f6f1a919-7931-4cd4-81a3-5600368e66c0" alt="URL Rewrite" width="300" length="300"/><br /><br />

<p>7. Navigate to the C: Drive. Right-click --> New --> Folder --> Name the folder "PHP" </p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/e7e94008-6ea4-47ef-96e6-d246258f2854" alt="Add PHP folder to C: Drive" width="400" length="400"/><br /><br />

<p>8. Download <a href="https://www.linuxfromscratch.org/blfs/view/9.0/general/php.html">PHP for Windows (Version 7.3.8)</a>. Unzip the contents to the new PHP file on the C: Drive.</p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/f2f7abd1-6d2c-49c7-88e0-d19c07d92ba0" alt="PHP for Windows" width="400" length="400"/><br /><br />

<p>9. Download and install <a href="https://www.microsoft.com/en-US/download/details.aspx?id=48145">Visual C++ Redistributable for Visual Studio 2015</a></p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/5a8cb255-e782-4947-90a9-c75ecfeeedb5" alt="C++ Redistributable" width="400" length="400"/><br /><br />
