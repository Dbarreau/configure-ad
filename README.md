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

<p align=center><img src="https://user-images.githubusercontent.com/121436228/220389039-b5401c5c-82d1-434c-8cf4-45c7d808a68c.jpg"></p>


<p>In the Barreau Hospital's VM, download the Active Directory Domain Services. The new domain service will be called Myhealthreport.com </p>

<p> The next step is to break down the firewalls between Barreau Hospital's VM and the Computer1 by going enabling all the ICMPv4's inbound rules. This step opens the communication between both virtual machines.</p>
<p align=center><img src="https://user-images.githubusercontent.com/121436228/220667270-655eced0-e537-4dc7-a3b4-3dd0e86dc76a.png"></p>

Change DC-1 IP Address from dynamic to static

Complete the AD Download

———————————


Create Client 1 (rename to Barreau Hospital)

Change Client 1 dns to DC-1’s dns server

Restart DC-1

Create Dr_Peters and make official



Create 
_employees to _doctors

_admins to _nurses

_users to  _patients

_accountant to _boardmembers

Then run script


Restart client1 - cmd - ping -t 10.0.0.4

Verify dc-1 is reachable on the network line

Right click start- system - change PC name

Restart client 1 sign in as Dr_Peters

Right click - start - system- Remote Desktop - access to pc - domain users - apply 
Restart client 

Pick a select user from Dc-1 sign in
On client (copy and paste on notepad)

