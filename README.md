<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>Lab - osTicket Setup and Configuration</h1>

- Simple Steps and Description:
  
We'll set up a help desk ticketing system using osTicket on a cloud Windows computer. This system helps manage IT support requests.

- Create a Virtual Machine: Make a Windows 10 computer in the cloud.
- Install Necessary Software: Set up web server software and a database.
- Install osTicket: Put osTicket on the computer.
- Configure the Help Desk: Set up user roles, departments, and support teams.
- Practice Using the Help Desk: Create and manage support tickets.
  
This lab guides you through setting up a help desk ticketing system using osTicket on an Azure virtual machine. You'll install the necessary software, configure a MySQL database, and set up osTicket to manage help desk operations. This project provides hands-on experience in deploying web-based applications and managing IT support systems.<br />

<h2>Environments and Technologies Used</h2>

- Azure Portal
- Windows 10 VM
- osTicket
- IIS (Internet Information Services)
- PHP
- MySQL
- HeidiSQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

- Part 1: Create a Virtual Machine in Azure
Create a Resource Group and VM:
Navigate to the Azure Portal.
Create a new Resource Group (e.g., OSTicketLab).
Create a Windows 10 VM in this Resource Group with 2-4 Virtual CPUs.
Allow the VM to create a new Virtual Network (Vnet).
<img src="https://i.imgur.com/ui6mnSa.png" alt="VM Creation"/>

- Part 2: Installation
Set up the VM:
Name the VM 'Vm-osticket'.
Set up a username (e.g., labuser) and password (e.g., osTicketPassword1!).
<img src="https://i.imgur.com/4ocYzi6.png" alt="VM Installation"/>

- Install IIS and Prerequisites:

- Log into the VM using Remote Desktop.
- Open "Server Manager" and select "Add roles and features".
- Install the Web Server (IIS) role with the following features:
- Web Server -> Common HTTP Features -> [X] CGI
- Web Server -> Application Development -> [X] CGI
- Management Tools -> [X] IIS Management Console
- Download and install PHP Manager for IIS and the Rewrite Module from the provided links.
- Create a directory C:\PHP and download PHP 7.3.8. Unzip it into C:\PHP.
- Install VC_redist.x86.exe and MySQL 5.5.62.
<img src="https://i.imgur.com/nBMRQQf.png" alt="Install ISS"/>
<img src="https://i.imgur.com/jbG4cD6.png" alt="Install ISS"/>

- Install osTicket:

Download osTicket from the provided link.
Extract the "upload" folder to C:\inetpub\wwwroot and rename it to "osTicket".
Open IIS Manager, stop and start the server, and browse to http://localhost/osTicket.
<img src="https://i.imgur.com/k91kEqu.png" alt="Install osTicket"/>
<img src="https://i.imgur.com/KYj1eVf.png" alt="Install osTicket"/>

- Configure Database:

Download and install HeidiSQL.
Create a new session with root/Password1 and create a database called osTicket.
Complete the osTicket setup in the browser using the database details.

<img src="https://i.imgur.com/KYj1eVf.png" alt="Install HeidiSQL"/>
<img src="https://i.imgur.com/ZbQ0uNU.png" alt="Install HeidiSQL"/>
<img src="https://i.imgur.com/jPFkABR.png" alt="Install HeidiSQL"/>


- Part 3: Post Installation Setup
Configure Roles and Departments:

In the osTicket Admin Panel, go to Agents -> Roles and create roles such as "Supreme Admin".
Go to Agents -> Departments and create departments like "System Administrators".
<img src="https://i.imgur.com/CGyWMB5.png" alt="Configure Roles and Department"/>

- Allow Ticket Creation:

Go to Settings -> User Settings and configure it to allow anyone to create tickets.
<img src="https://i.imgur.com/38huFkb.png" alt="Ticket Creation"/>

- Add Agents and Users:

Add agents (e.g., Jane, John) in the Agents section.
Add users (e.g., Karen, Ken) in the Users section.
Configure SLA and Help Topics as needed.
<img src="https://i.imgur.com/2zWkvTk.png" alt="Add Agents"/>
<img src="https://i.imgur.com/KhnnQfn.png" alt="Add Agents"/>
<img src="https://i.imgur.com/OzhLvXT.png" alt="Add Users"/>
