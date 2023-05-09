<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation Files
- Heidi SQL

<h2>Installation Steps</h2>

<p>
Welcome to my first tutorial! this is the first part of a 3 part tutorial on how to install, setup, and run your own in house Help Desk Ticketing system through osTicket. In this tutorial we will be using a virtual machine with 2-4 Virtual CPU's on Azure and installing all the necessary files in order to run osTicket properly.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/125160491/236000735-6fddc58f-4594-4214-8f30-829bcd0d4740.png" height="80%" width="80%" alt="Virtual Machine"/>
</p>
<p>
The first step is to connect to the Virtaul Machine that you created through Azure to Remote Desktop Connection(RDC). To do this, go to your VM on the Azure portal > Copy Public IP Address > Connect with RDC
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/125160491/236275103-ad9c34bb-6ff3-442f-b950-1ce8b08a6565.png" height="80%" width="80%" alt="Installation Files"/>
</p>

<p>
Make sure to use this link  below that will take you to the installation files needed to properly install osTicket. You should have this window open in your VM since all the downloads will be happening inside there.
</p>
<ul>
  <li><a href="https://docs.google.com/document/d/16Qxd2kooP5vsWpHshRSUSVaLnr5Sor9YDxFiZt21CFI/edit?usp=sharing">Installation Files needed to install osTicket</a>
</ul>
<br />

<p>
<img src="https://user-images.githubusercontent.com/125160491/236276419-90a412c5-56d9-4348-a810-e68ccc582a0e.png" alt="Control Panel"/>
</p>
<p>
In the Control Panel go to the Programs section and select "Turn Windows features on or off".</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/7a944abe-e142-4ef3-90c2-c8fa920b5bd7" height="80%" width="80%" alt="Windows Features"/>
</p>
<p>
Next, enable and install IIS in Windows with CGI. To do this enable Internet Information Services > Expand World Wide Web Services > Expand Development Features > Check CGI > Select OK
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/3c9961fd-30b3-4498-9781-906981d835c7" height="80%" width="80%" alt="Installation Software"/>
</p>
<p>
Once you have installed IIS go ahead and type "127.0.0.1" in a new tab to make sure that it was installed properly. If it was then it should look like it does in the screen shot. Once that is done, download and install PHPManagerForIIS_V1.5.0.msi and rewrite_amd64_en-US.msi from the google doc. 
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/98ee5d62-e0f8-418a-8cb6-6d8d7b40e333" height="80%" width="80%" alt="New Folder"/>
</p>
<p>
Next, create a new folder named "PHP" in the C drive. To do this go to File Explorer > This PC > (C:) > New Folder > Name folder "PHP".
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
