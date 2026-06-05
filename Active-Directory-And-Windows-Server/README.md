Windows Server & Active Directory Setup

Overview:

In this lab, I deployed a Windows Server 2022 Domain Controller, configured Active Directory, assigned static IP addresses, verified network connectivity, and joined a Windows 10 client to the domain.

Objectives:

        Install Active Directory Domain Services (AD DS)
        Create an Active Directory domain
        Configure static IP addressing
        Verify connectivity and DNS resolution
        Join a Windows 10 client to the domain

Environment:

Device	                        Role	                                 IP Address
DC01	                          Domain Controller	                     192.168.10.10
Windows10-Lab2	                Domain Client	                         192.168.10.20

Domain:

        ehsan.local

Step 1 – Install Active Directory Domain Services

Opened PowerShell and installed Active Directory Domain Services.

Command used:

        Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
        <img width="300" height="300" alt="Screenshot 2026-06-03 at 22 36 30" src="https://github.com/user-attachments/assets/2f6df296-a37e-4ed4-81d6-0a314a9d6c05" />
