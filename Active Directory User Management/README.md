Overview:

In this lab, I practised common Active Directory administration tasks including user creation, group management, password resets, and locked account recovery. These are common tasks performed by IT Support and Helpdesk technicians in enterprise environments.

Objectives:

        Create an Organizational Unit (OU)
        Create a user account
        Create a security group
        Add a user to a group
        Reset a user's password
        Enable a disabled account
        Configure account lockout policy
        Investigate locked accounts
        Unlock user accounts
        Verify successful user login

Environment:

Device  ------------------------------> Role

DC01	------------------------------> Domain Controller

Windows10-Lab2	----------------------> Domain Client

Domain	------------------------------> ehsan.local


Step 1 – Create Organizational Unit:

Created an Organizational Unit called IT Support Lab to organize users and groups.

Command used:

        New-ADOrganizationalUnit -Name "IT Support Lab" -Path "DC=ehsan,DC=local"
        Get-ADOrganizationalUnit -Filter *
<img width="800" height="300" alt="Screenshot 2026-06-06 at 22 19 52" src="https://github.com/user-attachments/assets/fcc18059-84e3-42aa-8e71-2eb199917d46" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 2 – Create User Account:

Created a new Active Directory user called john.smith.

Command used:

        New-ADUser -Name "John Smith" -GivenName "John" -Surname "Smith" -SamAccountName "john.smith" -Path          "OU=IT Support Lab,DC=ehsan,DC=local"
        
        Get-ADUser john.smith
<img width="800" height="300" alt="Screenshot 2026-06-07 at 13 23 10" src="https://github.com/user-attachments/assets/5e953d12-4dd2-4c94-a3cb-45b2bde035e9" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 3 – Create Security Group:

Created the IT Support Users security group.

Command used:

        New-ADGroup -Name "IT Support Users" -GroupScope Global -GroupCategory Security -Path "OU=IT Support         Lab,DC=ehsan,DC=local"
        
        Get-ADGroup "IT Support Users"
<img width="800" height="300" alt="Screenshot 2026-06-07 at 13 34 07" src="https://github.com/user-attachments/assets/64fd73a8-c606-4551-9f72-96f7c880b66c" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 4 – Add User to Group:

Added john.smith to the IT Support Users group.

Command used:

        Add-ADGroupMember -Identity "IT Support Users" -Members "john.smith"
        
        Get-ADGroupMember "IT Support Users"
<img width="800" height="300" alt="Screenshot 2026-06-07 at 13 40 31" src="https://github.com/user-attachments/assets/4991cacf-7a90-46a8-a1b5-36c19991c364" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 5 – Password Reset & Account Enable:

Reset the user's password and re-enabled the account using PowerShell.

Command used:

        Set-ADAccountPassword -Identity john.smith -Reset -NewPassword (ConvertTo-SecureString "Welcome123"          -AsPlainText -Force)
        
        Enable-ADAccount -Identity john.smith
        
        Get-ADUser john.smith -Properties Enabled
<img width="800" height="300" alt="Screenshot 2026-06-10 at 22 03 15" src="https://github.com/user-attachments/assets/e9148962-abdc-4785-a73b-b867f28154c2" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 6 – Successful Login:

Verified successful domain login using the reset password.

        EHSAN\john.smith
        
        Password:
        Welcome123
<img width="800" height="300" alt="Screenshot 2026-06-10 at 22 23 15" src="https://github.com/user-attachments/assets/a3966354-3bec-4819-adb9-8a35d5cabd08" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 7 – Configure Lockout Policy:

Configured an account lockout policy to lock accounts after three failed login attempts:

        net accounts /lockoutthreshold:3
        
        net accounts
<img width="800" height="300" alt="Screenshot 2026-06-12 at 23 56 40" src="https://github.com/user-attachments/assets/229cde31-1d1e-44b8-bb27-79e75d6519d1" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 8 – Simulate Account Lockout:

Entered an incorrect password multiple times to trigger the account lockout policy.

Reason:
Simulates a common Helpdesk scenario where a user repeatedly enters an incorrect password and their account becomes locked.
<img width="800" height="300" alt="Screenshot 2026-06-12 at 23 57 40" src="https://github.com/user-attachments/assets/898fb6a3-203e-47d8-a43d-9b6322b6698a" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 9 – Investigate Locked Account:

Used PowerShell to identify locked user accounts in Active Directory and confirm that john.smith was locked.

Command used:

        Search-ADAccount -LockedOut
<img width="800" height="300" alt="Screenshot 2026-06-12 at 23 58 49" src="https://github.com/user-attachments/assets/e28d344c-135f-4933-a5c1-f5980b13bfed" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 10 – Recover Locked Account:

Unlocked the user account to restore access after the lockout event.

This is a common IT Support task performed when users are locked out of their accounts.

Command used:

        Unlock-ADAccount -Identity john.smith
<img width="800" height="300" alt="Screenshot 2026-06-13 at 00 02 00" src="https://github.com/user-attachments/assets/c3bcdd80-7c37-4c53-9312-66517ae34e0c" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 11 – Verify Successful Login:

Logged into the Windows 10 workstation using:

        EHSAN\john.smith
        
        Password:
        Welcome123
<img width="800" height="300" alt="Screenshot 2026-06-13 at 00 02 54" src="https://github.com/user-attachments/assets/bde23b82-3aff-43af-8f82-4cbd3b4c9582" />
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Skills Practised:

        Active Directory User Management
        Security Group Administration
        Password Resets
        Account Enablement
        Account Lockout Policies
        Account Recovery
        PowerShell Administration
        Windows Authentication
        IT Support Helpdesk Tasks
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Outcome:

Successfully:

        Created an Organizational Unit
        Created a user account
        Created a security group
        Added user to a security group
        Reset a user password
        Enabled a disabled account
        Configured account lockout policy
        Detected a locked account
        Unlocked the account
        Verified successful login after recovery
