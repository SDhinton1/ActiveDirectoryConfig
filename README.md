<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- 1:Install Active Directory Domain Services and Create your Myforest.
- 2:Create Folders for your employees and admins to stay
- 3:Connect The Domain Controller to Your Client RD
- 4:Login As one of your created admins, create emplyees and try to log in to your Client's RD to see results.

<h2>Deployment and Configuration Steps</h2>

Make sure the Client VM is connected to the Domain Controllers V-Net and set the DC's ip to static. Open the Client VM and ping the Domain Controller it isn't able to ping the Domain Controller so inside the DC Enable icmpv4 on the local windows firewall and obersve their is now a ping. 

<p>
<img src="https://i.imgur.com/htwx4q8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>
When Starting active directory enable icmpv4 traffic from the domain controller to Client-1 and proceed to download Active Directory Domain Services on the domain controller and set up your domain services
</p>
<br />

<p>
<img src="https://i.imgur.com/bq5ukth.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>
After making The Organizational units Logout and log back in as your created user to make sure it is correct, then set the Client's DNS settings to DC's Private ip address, restart Client-1 in the azure portal and log back in then proceed to connect DC-1 to Client-1 through the windows system.
</p>
<br />

<p>
<img src="https://i.imgur.com/kzUzKDI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p>
When you connect the DC-1 to Client-1 you can now load any account in the domain users catagory to the Client-1 with that user account successfully connecting the two VM's. using Powershell.ise as an administrator (not necessary but can help) make many user accounts and attempt to log in with one of those accounts
<br />
