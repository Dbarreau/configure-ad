<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory step-by-step tutorial</h1>
This tutorial displays the steps on implementing the Active Directory Domain Services within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: Active Directory Tutorial (https://www.youtube.com/watch?v=VhZrN8monh0)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- Active Directory Domain Services
- PowerShell ISE (x86)

<h2>Operating Systems Used </h2>

- Windows Server 2022 Datacenter 
- Windows 10 PRO (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create 2 Virtual Machines (Domain Controller and Client VM)
- Enable ICMPv4 inbound rules
- Change DNS server's address assignment
- Download Active Directory Domain Services
- Stabilize the Domain Controller's Private IP address
- Change the Client's DNS server to the Domain Controller's DNS server
- Create an Admin and some users

On Microsoft Azure, create two virtual machines, one is a Domain Controller and the other is the Client.
In this tutorial, the Domain Controller is called Barreau Hospital. Barreau Hospital's  dns server private IP address is 10.0.0.4.
The Client is Computer 1. The Computer 1's DNS server private IP address is 10.0.0.5.

<p align=center><img src="https://user-images.githubusercontent.com/121436228/220669251-4a2e9638-a2be-4714-a45d-294a55199111.png"></p>


<p>In the Barreau Hospital's VM, download the Active Directory Domain Services. The new domain service will be called Myhealthreport.com </p>

<p> The next step is to break down the firewalls between Barreau Hospital's VM and the Computer1 by going enabling all the ICMPv4's inbound rules. This step opens the communication between both virtual machines.</p>
<p align=center><img src="https://user-images.githubusercontent.com/121436228/220667270-655eced0-e537-4dc7-a3b4-3dd0e86dc76a.png"></p>

<p> Go to Microsoft Azure and change Domain Controller's IP Address from dynamic to static. This action will prevent the Private IP address from changing everyday and maintain stability for the other computers.</p>
<p align=center><img src="https://user-images.githubusercontent.com/121436228/220678460-9048710f-c167-45d2-aa17-2e803cb62915.png"></p>  

<p> On Barreau Hospital's VM, go to the Server Manager and create an admin and new users. Go to the tool tab, to make two organizational units (_Doctors and _Patients) through the Active Directory Users and Computer's program. As a adminstrator for PowerShell ISE, run the script for both _Doctors and _Patients codes to create random users. Then, go to _Doctor folder and select a user to become an admin. Finally, restart Barreau Hospital's VM and log back in with the Admin.</p>
<p> New username: Myhealthreport.com\Pub.manaje ||||||||||||||||| Password: Password1 </p>
<p align=center><img src="https://user-images.githubusercontent.com/121436228/220687385-63a3e502-ae04-4be2-ba66-7a8d7c7a202d.png"></p>


<p> Go to Microsoft Azure, and change Computer 1 dns private IP address to Barreau Hospital’s dns server. Then restart Computer1's VM.</p>
<p align=center><img src="https://user-images.githubusercontent.com/121436228/220696740-b6b764b1-e872-4da8-9221-092fb91ce3d8.png"></p>

<p> Let's add the domain (myhealthreport.com) and the Admin to the Computer1's VM.  Log back in the computer1, right-click start, go system, and go to change PC name. Select Change then type in myhealthreport.com, plug in Pub.manaje username and password, finally restart Computer1.</p>
<p align=center><img src="https://user-images.githubusercontent.com/121436228/220700824-46b37bf6-840d-4cd3-acad-65e6dfb2e483.png"></p>


<p> Next step is to add the Domain users. So, log back into Computer 1 as the Admin full username (myhealthreport.com\Pub.manaje) then right-click on the start button. Scroll up to System, go to Remote Desktop, then go to users that can access this pc, then add domain users.</p>
<p align=center> <img src="https://user-images.githubusercontent.com/121436228/220702838-6efdddc3-36e3-4a1e-9ba2-82bb488db35e.png"></p>

Right click - start - system- Remote Desktop - access to pc - domain users - apply 
Restart client 

Pick a select user from Dc-1 sign in
On client (copy and paste on notepad)

