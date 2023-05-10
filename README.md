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
Next, create a new folder named "PHP" in your C drive. To do this go to File Explorer > This PC > (C:) > New Folder > Name folder "PHP".
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/19626d06-8e56-4ff2-b44d-5c586b69c9f1" height="80%" width="80%" alt="Extact Files"/>
</p>
<p>
Once the file is created, download and install php-7.3.8-nts-Win32-VC15-x86.zip and then extract all the contents into C:\PHP.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/8861eba6-27ce-4975-8cac-f079980b12fb" height="80%" width="80%" alt="Installation File"/>
</p>
<p>
Download and install VC_redist.x86.exe.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/2d0e0617-1b9b-401c-b2ed-0730dd35f7a1" height="80%" width="80%" alt="Installation FIle"/>
</p>
<p>
Download and install Download and install mysql-5.5.62-win32.msi. To install this properly Select Next > Accept Agreement > Next > Typical Setup > Install > Finish > Next > Standard Configuration > Next > Next.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/67cd5db1-3b75-47d0-a384-57b49a633cd7" height="80%" width="80%" alt="Password Setup"/>
</p>
<p>
Once you arrive to the password setup, make sure to create a password that you will remember. After creating a password Select Next > Execute.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/e3158129-bfc9-43c9-8e4d-e9363bbc0dc3" height="80%" width="80%" alt="Administrator"/>
</p>
<p>
In the Windows search bar search for "IIS" and run it as administrator.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/939b0e86-80ef-450b-8aea-95b1e68c09c7" height="80%" width="80%" alt="Register"/>
</p>
<p>
Once the IIS Manager is open, select PHP Manager > Select Register new PHP version > Browse Files > PHP > Open php-cgi
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/ed84c1c5-c133-4799-8d2f-81c056cd4e1b" height="80%" width="80%" alt="Restart"/>
</p>
<p>
Restart IIS Manager
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/c7f9079b-747c-409d-9f6c-b6c162d2bb1e" height="80%" width="80%" alt="Folder Allocation"/>
</p>
<p>
Download the file osTicket-v1.15.8 from the google doc. Once it is finished downloading, open two file explorer windows and navigate to the osTicket-v1.15.8.zip folder and "inetpup". In the inetpup folder, go to "wwwroot" and transfer the "upload" folder in from the osTicket zip. After it finishes, rename the "upload" folder to "osTicket".
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/02765eb7-7359-4227-9803-77ae27e86808" height="80%" width="80%" alt="Restart"/>
</p>
<p>
Restart IIS Manager
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/240891fc-e218-4f72-a1e6-39b4d50e1e81" height="80%" width="80%" alt="osTicket"/>
</p>
<p>
Expand osTicket on the left menus > Sites > Default Web Sites > Click osTicket. Click on "Browse *.80. This will take you to the osTicket installer.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/f666448e-75b2-44a8-ae98-9a6ee5949f61" height="80%" width="80%" alt="PHP Manager"/>
</p>
<p>
Head back to IIS Manager and into osTicket. Select "PHP Manager" then select "Enable or disable extension" under PHP Extensions.
  
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/1d51e9ec-4776-48f7-b4f7-91017790d8e5" height="80%" width="80%" alt="Enable"/>
</p>
<p>
Next, go ahead and enable "php_imap.dll", "php_intl.dll", and "php_opcache.dll" by selecting "Enable" 
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/3b59f90f-d29f-4260-bfa3-e999b8700f23" height="80%" width="80%" alt="Check"/>
</p>
<p>
Now head back to osTicket Installer on the web browser, refresh and see if the changes were made to match the screenshot above.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/d49c56b6-72a8-4c46-ae73-ca6844e0a794" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the correct changes are made, open file explorer and navigate back to osTicket inside of inetpub. Select include and locate "ost-sampleconfig.php" and rename it to "ost-config.php".
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/3aba583c-80ef-4659-ad07-97f4f1d3527d" height="80%" width="80%" alt="Disable"/>
</p>
<p>
Once the name has been changed, right click and select Properties > Security > Advanced > Disable Inheritance > Remove all.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/89049d38-e52b-48db-8a00-a285bfd194bd" height="80%" width="80%" alt="Add"/>
</p>
<p>
Select Add > Select a principle > type "everyone" in the object box > Check name > Press Ok.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/5cf7eb82-9b84-437c-bd5a-16d2b8fba5b1" height="80%" width="80%" alt="Check
</p>
<p>
Check "Full Control" > Select Apply > Select OK
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/098bace1-cd1c-4085-a6eb-b36fc5100332" height="80%" width="80%" alt="Information
</p>
<p>
Next, go back to the osTicket Installer and select "Continue". In the first red box above, copy exactly as it. In the red box below. you can create your own Admin user credentials. I wrote down a random email and created a password. Make sure to write down the email, username, and password in a notepad to help you login later. (Note: Writing important information down in a notepad is only specifically used for training or tutorials and is not best practice in a professional environment.)
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/3fc84e26-4239-4f0c-a583-02085a79d346" height="80%" width="80%" alt="heidi"/>
</p>
<p>
  Download HeidiSQL from the google doc which contains a word doc with a link to the actual download. Just select continue all the way through and install.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/a1c9581e-6653-40dc-a822-4698d16b4266" height="80%" width="80%" alt="New"/>
</p>
<p>
Once HeidiSQL has been installed, Select New > Enter the password that was created earlier in the tutorial "Password1" > Select Open.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/65ec56c7-1698-4531-acc2-0949148a515f" height="80%" width="80%" alt="Database"/>
</p>
<p>
Inside of HeidiSQL, right click "Unnamed" > Create new > Database > Name it "osTicket"> Select OK.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/72599e7e-0b06-42c1-981d-144b6bbf8ba0" height="80%" width="80%" alt="Apply"/>
</p>
<p>
Now go back to the osTicket Installer and enter the username and password. MySQL Database should be "osTicket. The username and password should be "root" and "Password1". Select Install Now
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/6b8a0879-1af1-44e6-bd25-9c728e3f8082" height="80%" width="80%" alt="Clean Up"/>
</p>
<p>
To finish off the tutorial we will be cleaning some stuff up that is not needed anymore. Go back to the file explorer > C:\inetpub > wwwroot > osTicket > delete the "setup" folder.
</p>
<br />

<p>
<img src="https://github.com/sebbec31/osticket-prereqs/assets/125160491/452b9d82-5788-40fa-a11b-4b8af0191b58" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Stay in the osTicket folder > include > fine "ost-config.php" > right click for properties > Security > Advanced > Select Everyone > Edit > set permissions to only "Read" and "Read and execute" only > OK > Apply > OK
</p>
<br />

