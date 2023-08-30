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

<p>8. Download <a href="https://www.linuxfromscratch.org/blfs/view/9.0/general/php.html">PHP for Windows (Version 7.3.8)</a>. Extract the contents to the PHP file on the C: Drive.</p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/f2f7abd1-6d2c-49c7-88e0-d19c07d92ba0" alt="PHP for Windows" width="400" length="400"/><br /><br />

<p>9. Download and install <a href="https://www.microsoft.com/en-US/download/details.aspx?id=48145">Visual C++ Redistributable for Visual Studio 2015</a></p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/5a8cb255-e782-4947-90a9-c75ecfeeedb5" alt="C++ Redistributable" width="400" length="400"/><br /><br />

<p>10. Download <a href="https://downloads.mysql.com/archives/get/p/23/file/mysql-5.5.62-win32.msi">MySQL Server (Version 5.5.62)</a>. Once downloaded, choose to complete a 'Typical' installation. When this is complete, launch the configuration wizard. Choose a 'Standard Configuration' and write a root password. Click 'Execute' to finish the setup. </p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/84ae9c13-6027-4959-9ef3-50bfa7bfc139)" alt="MySQL Server" width="400" length="400"/><br /><br />

<p>11. On your system, search for 'IIS'. Right-click on the program and click 'Run as Administrator'. On the following screen, double-click 'PHP Manager'. Click to 'Register new PHP version'. On the pop-up screen, navigate to C: Drive --> PHP --> php-cgi. When the path to this file has been selected, click 'Open". When you return to the IIS opening screen, click on the name of the server on the top-left and click to restart the server on the top-right.</p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/870fc7e1-a98a-4398-af22-c193880d99c3" alt="Register PHP" width="500" length="500"/><br /><br />

<p>12. Download <a href="https://osticketawesome.com/download/10398/?tmstv=1693419592">osTicket (Version 1.15.8)</a>. Once downloaded, navigate to the folder on your system. Click to open it and leave a window open with the 'upload' folder showing. In a seperate window, go to your C: Drive, open the 'inetpub' folder, and click to open 'wwwroot'. Drag the 'upload' folder from the osTicket download window to the 'wwwroot' folder. Rename this folder to "osTicket"</p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/dda5eecb-10e8-48be-90c5-1ff96d7721d3" alt="Rename folder to osTicket" width="500" length="500"/><br /><br />

<p>13. In IIS Manager, on the left sidebar, click Sites --> Default --> osTicket. After this, on the right sidebar, click 'Browse *:80'.This will load a screen that shows you have installed osTicket correctly. If the screen doesn't load, first troubleshoot by restarting the server and then by repeating the previous steps in the tutorial. If the screen opens correctly, leave the browser window open.</p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/5dde1c27-3d08-45cb-82c3-9f2baa924f12" alt="osTicket Installed Correctly" width="500" length="500"/><br /><br />

<p>14. Notice in the previous osTicket screenshot that there are some extensions with red crosses. These are currently not enabled. To enable them, go to IIS Manager, on the left sidebar, click Sites --> Default --> osTicket. After this, select PHP Manager and click 'Enable or diasble an extension. On the following screen, click to enable the following extensions:</p>
<ul>- Enable: php_imap.dll</ul>
<ul>- Enable: php_intl.dll</ul>
<ul>- Enable: php_opcache.dll</ul>
<p>Once this is complete, refresh the browser window that has the osTicket installation confirmation message and you should see that some other extensions are now available.</p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/0225e2c3-1fa7-4a3c-baf1-c229d5ed85ce" alt="osTicket Extensions Enabled" width="500" length="500"/><br /><br />

<p>15. Next, in your C: Drive, navigate to inetpub --> wwwroot --> osTicket --> include --> ost-sampleconfig.php. Right-click on this file and rename the file to "ost-config.php".</p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/cfc7562e-fa23-42e0-a5a1-764d3132f9b9" alt="Rename ost-sampleconfig.php" width="400" length="400"/><br /><br />

<p>16. Right-click on the 'ost-config.php' file and select 'Properties". Open the 'Security' tab and select 'Advanced'. On the following screen, click 'Disable Inheritance' and the click to 'Remove all permissions from this object'. Next, click 'Add', and select 'Add a principal'. In the following box, type "everyone', choose 'Check Names' and click 'OK'. On the following screen, choose the 'Full control' option and click 'Apply'. This setting is required by osTicket to ensure a smooth installation. It will be changed to a more secure setting later in the tutorial. </p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/b6e9e3f0-164a-4535-8dc5-35955b49038d" alt="Full control ost-config.php" width="400" length="400"/><br /><br />

<p>17. In the osTicket browser window, click 'Continue'. Complete the System Settings and Admin User details. </p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/367de891-578e-4bfa-9c74-df5100fccf8f" alt="Setup osTicket Account Details" width="400" length="400"/><br /><br />

<p>18. Download and install <a href="https://www.heidisql.com/download.php">HeidiSQL</a></p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/e4e4abd4-fbe2-4db6-afe2-8d9f84edfb2b" alt="HeidiSQL" width="400" length="400"/><br /><br />

<p>19. In HeidiSQL, click 'New'. Input the username and password that you setup for MySQL Server. Then click 'Open'. You should now have a connection to MySQL Server. You should then right-click 'Unnamed' on the left sidebar. Following this, click 'Create New' and then 'Database'. Name the database "osTicket" and click 'OK'.</p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/0da4e0b3-c77d-4711-a4ef-c9a3bb7584e1" alt="Setup a Database in HeidiSQL" width="400" length="400"/><br /><br />

<p>20. In the osTicket browser window, you can now continue the installation by adding the Database Settings details. Be sure to use 'osTicket' name for the MySQL Database part. Once all the information is complete, click to install. </p>
<img src="https://github.com/GaryKirk/osticket-prereqs/assets/137613637/8fb9c107-9aa5-483e-b8c4-b573fee6248d" alt="Setup a Database in HeidiSQL" width="400" length="400"/><br /><br />



