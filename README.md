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
<img src="blob:chrome-untrusted://media-app/89b6410d-c04c-4b82-8353-2eaf70348c47" alt="Screenshot 2023-09-04 12.56.47 PM.png"/>![image](https://github.com/SDhinton1/ActiveDirectoryConfig/assets/143854836/27c90ebc-46c4-43aa-ad37-d47bb8e90cc0)
</p>
<p>
When Starting active directory enable icmpv4 traffic from the domain controller to Client-1 and proceed to download Active Directory Domain Services on the domain controller and set up your domain services
</p>
<br />

<p>
<img src="blob:chrome-untrusted://media-app/0d082312-41bd-4642-a6af-603d0fd70ee6" alt="Screenshot 2023-09-09 4.28.17 PM.png"/>![image](https://github.com/SDhinton1/ActiveDirectoryConfig/assets/143854836/f7efef88-508c-40c0-b3d3-0a964e66b873)
</p>
<p>
After making The Organizational units Logout and log back in as your created user to make sure it is correct, then set the Client's DNS settings to DC's Private ip address, restart Client-1 in the azure portal and log back in then proceed to connect DC-1 to Client-1 through the windows system.
</p>
<br />

<p>
<img src="blob:chrome-untrusted://media-app/51e34270-1e35-4fc6-82a4-c6a76a2921b7" alt="Screenshot 2023-09-09 4.54.15 PM.png"/>![image](https://github.com/SDhinton1/ActiveDirectoryConfig/assets/143854836/4bd60eb0-4cd0-4883-9c79-478b79093dd0)
<p>
When you connect the DC-1 to Client-1 you can now load any account in the domain users catagory to the Client-1 with that user account successfully connecting the two VM's. using Powershell.ise as an administrator (not necessary but can help) make many user accounts and attempt to log in with one of those accounts
<br />
