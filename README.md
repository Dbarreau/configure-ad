<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory step-by-step tutorial</h1>
This tutorial displays the steps on implementing the Active Directory Domain Services within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: Active Directory Tutorial (https://youtu.be/RjjP7qcFxCQ)

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
