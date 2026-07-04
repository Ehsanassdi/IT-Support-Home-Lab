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

------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 4 – Verify the Link

I verified that the Screen Lock Policy was successfully linked to the IT Department OU.

    The Linked Group Policy Objects section showed the policy as enabled.

<img width="800" height="400" alt="Screenshot 2026-07-04 at 18 02 44" src="https://github.com/user-attachments/assets/fdf3b99d-11e7-4612-aba0-42764196904b" />

------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 5 – Force Policy Update

On the Windows 11 domain workstation (WIN11-PC), I forced an immediate policy update using:

    gpupdate /force

This command makes the workstation retrieve the latest Group Policy settings from Active Directory immediately rather than waiting for the next automatic refresh.

<img width="800" height="400" alt="Screenshot 2026-07-04 at 18 02 59" src="https://github.com/user-attachments/assets/7ccf4f1d-196c-419d-8377-d85c5bc8963c" />

------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 6 – Verify Policy Application

I logged in using the domain user account:

    John Smith

and verified policy deployment using:

    gpresult /r

The output confirmed that:

    Screen Lock Policy

was successfully applied to the user account.

<img width="800" height="400" alt="Screenshot 2026-07-04 at 18 03 12" src="https://github.com/user-attachments/assets/7fbd5e3c-a21b-4eb1-86e8-b65fccbf98b7" />

------------------------------------------------------------------------------------------------------------------------------------------------------------

Skills Demonstrated:

    Windows Server 2022
    Active Directory
    Group Policy Management
    Organizational Units (OU)
    Security Policy Deployment
    Domain Administration
    Windows 11 Domain Workstation Management
    Policy Verification and Troubleshooting

------------------------------------------------------------------------------------------------------------------------------------------------------------
Key Learning

    Group Policy allows administrators to centrally manage and enforce security settings across multiple users and computers.

    By creating a Group Policy Object and linking it to an Organizational Unit, security settings can be automatically distributed without manually configuring every workstation.
