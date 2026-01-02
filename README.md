<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Microsoft Azure: Managing Accounts (Lockouts and Disabled Accounts)</h1>
This tutorial explains the process of unlocking a locked user account and re-enabling disabled accounts in Active Directory. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Account Lockout and Unlock/Account Disable and Re-Enable Process</h2>

- Lockout the client account by using the wrong password 10+ times on the Client-VM
- Login to the Domain Controller VM and open Active Directory Users and Computers
- Unlock the Account and Reset the Password
- Login with new password on Client-VM and observe successs
- Open DC-VM again and disable the same account you just unlocked
- Attempt to login on the Client-VM and observe that it is locked
- Reopen the DC-VM and Re-enable the account
- Login to Client-VM with same account and observe success

<h2>Account Lockout and Unlock/Account Disable and Re-Enable Steps</h2>

<p>
<img width="241" height="291" alt="image" src="https://github.com/user-attachments/assets/145c11ae-d2f6-4cec-844a-6e753937bca0" />

</p>
<p>
Open remote desktop and attempt to login to the client-side Virtual Machine running Windows 10. Be sure to use the wrong password and attempt the login 10+ times until you get the notification that the account has been locked. 
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
