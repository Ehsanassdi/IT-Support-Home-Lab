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
