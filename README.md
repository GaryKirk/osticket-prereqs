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
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/da49890d-955c-4994-98e9-847d1ac1ff82" alt="Enable IIS with CGI"/ width="300" length="300"><br /><br />

<p>3. Go back to World Wide Web Services. Click Common HTTP Features and make sure that all features are turned on. </p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/abe28239-6d1f-4e9c-a0be-20a52fbaf55f" alt="Turn on HTTP Features"/ width="300" length="300"><br /><br />
