Overview

In this lab, I used Group Policy Management in Windows Server 2022 to deploy a security policy through Active Directory.

Instead of configuring security settings on every workstation individually, I created a Group Policy Object (GPO), configured the required settings, linked it to an Organizational Unit (OU), and verified that the policy was successfully applied to a domain user.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 1 – Create Group Policy Object (GPO)

    I created a new Group Policy Object named:
    
    Screen Lock Policy
    
    This policy will be used to enforce screen lock security settings for users in the IT Department.

<img width="800" height="400" alt="Screenshot 2026-07-04 at 18 02 03" src="https://github.com/user-attachments/assets/064c922e-7bef-4356-8662-8e358d3ef9c0" />

------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 2 – Configure Security Settings

I edited the Screen Lock Policy GPO and configured the following settings:

    Enable screen saver = Enabled
    Password protect the screen saver = Enabled
    Screen saver timeout = 600 seconds

These settings ensure that:

    A screen saver starts after 10 minutes of inactivity
    The workstation automatically locks
    A password is required to regain access

This helps protect company devices from unauthorised access.

------------------------------------------------------------------------------------------------------------------------------------------------------------

Task 3 – Link GPO to Organizational Unit

I linked the Screen Lock Policy GPO to the:

    IT Department OU

This tells Active Directory to automatically apply the policy to users and computers located inside that OU.

<img width="536" height="387" alt="Screenshot 2026-07-04 at 18 02 32" src="https://github.com/user-attachments/assets/6ce7078e-04f7-4ad4-ad9f-0a825ad831a4" />

------------------------------------------------------------------------------------------------------------------------------------------------------------


