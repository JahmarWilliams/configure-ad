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
<img width="772" height="463" alt="image" src="https://github.com/user-attachments/assets/0fe19388-4aef-496f-a966-9c8abcd9a406" />

</p>
<p>
Now that the client account is locked, open another instance of remote desktop and sign into the domain controller VM with the admin account. Once in the VM, open "Active Directory Users and Computers" and navigate to the client account using the "Find" feature or navigate normally through the files to whichever group they're in. 
</p>
<br />

<p>
<img width="425" height="534" alt="image" src="https://github.com/user-attachments/assets/91e10c22-cf3c-4adb-94d8-ec77b3a43b97" />
<img width="358" height="241" alt="image" src="https://github.com/user-attachments/assets/9174b314-2196-4149-89ed-b9e291f3e829" />

</p>
<p>
Double click on the client name to open the properties panel. Once there, navigate to the "account" tab and select unlock account. This will unlock the account and allow another login attempt. If a password reset is needed, you can also go back to the user account in the find tab and right click to bring up a list of options. Once there, you can select reset password to wipe their current password and assign them a new one. 
</p>
<br />

<p>
<img width="1324" height="817" alt="image" src="https://github.com/user-attachments/assets/4d4b0776-8fce-423a-9396-1f73ca4be5dd" />
  
</p>
<p>
Now that the account has been unlocked, go back to the client VM login and attempt to login with the correct password. Observe the success now that the account has been unlocked. 
</p>
<br />

<p>
<img width="492" height="545" alt="image" src="https://github.com/user-attachments/assets/74cc8c33-a8a7-4cfd-b2f6-8f0f6e1bf98f" />

</p>
<p>
Open the Domain Controller VM where AD Users and Computers should still be open, along with the find users window. Right click the client account and select "disable account". 
</p>
<br />

<p>
<img width="241" height="251" alt="image" src="https://github.com/user-attachments/assets/20543992-0053-4b98-8296-1c236713b023" />
  
</p>
<p>
Go to the client VM and logout then attempt to log back in. You will observe that the account is now disabled and login is not possible. 
</p>
<br />

<p>
<img width="509" height="538" alt="image" src="https://github.com/user-attachments/assets/df1f1b79-9df6-4a16-b679-a5541c8d2d1c" />

</p>
<p>
Go back to the Domain Controller VM and re-enable the account from the same window we had open previously. 
</p>
<br />

<p>
<img width="689" height="479" alt="image" src="https://github.com/user-attachments/assets/34677f2a-0c29-4ac4-8131-88d758265d4b" />

</p>
<p>
Proceed to the Client-side VM and attempt login. The system should let you in this time now that the account has been re-enabled. 
</p>
<br />
