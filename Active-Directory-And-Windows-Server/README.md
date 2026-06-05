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

Step 1 – Install Active Directory Domain Services:

Opened PowerShell and installed Active Directory Domain Services.

Command used:

        Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
        
<img width="700" height="300" alt="Screenshot 2026-06-03 at 22 36 30" src="https://github.com/user-attachments/assets/2f6df296-a37e-4ed4-81d6-0a314a9d6c05" />


Step 2 – Create Active Directory Domain:

Created a new Active Directory forest and domain.

Command used:

        Install-ADDSForest -DomainName "ehsan.local"

Domain created:

        ehsan.local

<img width="800" height="300" alt="Screenshot 2026-06-03 at 22 49 20" src="https://github.com/user-attachments/assets/40e5f906-6955-4efd-a76a-82360b04a7b4" />




Step 3 – Verify Domain Controller:

After promotion, the server became a Domain Controller.

Server details:

        Computer Name: DC01
        Domain: ehsan.local

<img width="700" height="400" alt="Screenshot 2026-06-03 at 22 52 27" src="https://github.com/user-attachments/assets/b3493d6b-a7da-4a85-9358-10b9d9f9b9a2" />



Step 4 – Configure Static IP on DC01:

Configured a static IP address using SConfig.

Settings:

        IP Address: 192.168.10.10
        Subnet Mask: 255.255.255.0
        Gateway: 192.168.10.1

Reason:

        Domain Controllers should use static IP addresses.
        Clients must always be able to locate the Domain Controller.

<img width="700" height="400" alt="Screenshot 2026-06-05 at 18 37 01" src="https://github.com/user-attachments/assets/7907b384-6253-4467-b4d0-4715d3cb714f" />



Step 5 – Configure Static IP on Windows 10 Client:

Configured a static IP address on the Windows 10 client.

Settings:

        IP Address: 192.168.10.20
        Subnet Mask: 255.255.255.0
        Gateway: 192.168.10.1
        DNS Server: 192.168.10.10

Reason:

        Enables reliable communication with the Domain Controller.
        Allows DNS resolution for Active Directory services.

Screenshot 5: Windows 10 network configuration


Step 6 – Test Connectivity:

Verified communication between the client and Domain Controller.

Command:

        ping 192.168.10.10

Result:

        Reply from 192.168.10.10

Screenshot 6: Successful ping test


Step 7 – Verify DNS Resolution:

Verified DNS functionality.

Command:

        nslookup ehsan.local

Result:

        Name: ehsan.local
        Address: 192.168.10.10

Screenshot 7: Successful DNS resolution


Step 8 – Join Windows 10 to the Domain:

Opened:

        sysdm.cpl

Then:

        Computer Name
        Change
        Domain
        ehsan.local

Authenticated using domain administrator credentials.

Received confirmation:

        Welcome to the ehsan.local domain.

Screenshot 8: Successful domain join


Step 9 – Restart and Verify Domain Membership:

Restarted Windows 10.

The login screen now displays the option to sign in using domain credentials.

Screenshot 9: Domain-joined login screen


Skills Practiced:

        Windows Server 2022
        Active Directory
        Domain Controller Deployment
        DNS Configuration
        Static IP Configuration
        Domain Joining
        Windows Administration
        IT Support Fundamentals
        Network Troubleshooting
        
Outcome:

Successfully:

        Installed AD DS
        Created Active Directory domain
        Promoted DC01 to Domain Controller
        Assigned static IP addresses
        Verified connectivity and DNS
        Joined Windows 10 to the domain
        Confirmed successful Active Directory integration
