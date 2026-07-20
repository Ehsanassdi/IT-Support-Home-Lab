Scenario

A user was unable to access the company's shared drive.

The objective was to configure a shared folder on Windows Server, manage SMB sharing and NTFS permissions, troubleshoot access issues, and map the shared folder as a network drive for end users.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Technologies Used:

    - Windows Server 2022
    - Windows 11
    - Active Directory
    - SMB (Server Message Block)
    - NTFS Permissions
    - UNC Paths
    - Network Drives
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Tasks Completed:

1. Created a Shared Folder

Created a central folder named CompanyShare on the Windows Server.

This folder acts as a shared location where users can store and access company files across the network.
<img width="400" height="800" alt="Create Shared Folder " src="https://github.com/user-attachments/assets/0fbf0669-1f35-457e-b80c-f1bc3f787af7" />

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
2. Configured an SMB Share

Configured CompanyShare as an SMB shared folder using Advanced Sharing.

Granted appropriate share permissions to allow network access from client computers.

SMB (Server Message Block) is the protocol Windows uses to share files and folders across a network.
<img width="400" height="800" alt="Create SMB Share " src="https://github.com/user-attachments/assets/bc989182-45d2-4813-a9d6-8bc283339393" />

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
3. Accessed the Shared Folder from a Client

Verified that the Windows 11 client could successfully access the shared folder using the UNC path:

    \\WIN-ULD00FLHOUL\CompanyShare

This confirmed that:

    - SMB sharing was configured correctly.
    - Network connectivity was working.
    - The shared folder was reachable from another computer.
<img width="400" height="800" alt="Access Shared Folder " src="https://github.com/user-attachments/assets/2fd3e6a0-c9ed-4aec-9aaf-3bb36d9696fe" />

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
4. Reviewed NTFS Permissions

Reviewed the Security settings of the shared folder to understand how Windows controls access to files and folders.

Learned the relationship between:

    - Read
    - Modify
    - Full Control

permissions.
<img width="400" height="800" alt="4" src="https://github.com/user-attachments/assets/c7777975-dff5-473b-9dd0-431e62353b32" />

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
5. Assigned Read Permissions to a Domain User

Created a test Active Directory user and granted Read-only access to the shared folder.

Verified that the user could:

    ✅ Open files
    ✅ Read files
    ❌ Modify files
    ❌ Delete files
    ❌ Create new files

This demonstrated how NTFS permissions enforce different levels of access.
<img width="400" height="800" alt="5" src="https://github.com/user-attachments/assets/04790bd2-f071-4f81-85ce-698657db7c3a" />

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
6. Troubleshot an "Access Denied" Issue

Simulated an Access Denied scenario and followed a structured troubleshooting process.

Checked:

    - NTFS Permissions
    - Share Permissions
    - User Membership
    - Access after permission changes

This mirrors a common Help Desk task when users cannot access department folders.
<img width="400" height="800" alt="6" src="https://github.com/user-attachments/assets/5127a9fc-2047-4d35-84b9-987840603c1e" />

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
7. Mapped the Shared Folder as a Network Drive

Mapped the shared folder as drive Z: on the Windows 11 client.

This allows users to access the shared company folder directly from File Explorer instead of typing the UNC path every time.
<img width="400" height="800" alt="7" src="https://github.com/user-attachments/assets/032e01fa-b576-4271-8e41-ad543fe781a2" />

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Key Skills Demonstrated:

    - Windows Server File Sharing
    - SMB Configuration
    - NTFS Permission Management
    - Active Directory User Management
    - UNC Paths
    - Network Drive Mapping
    - Access Denied Troubleshooting
    - Windows File Server Administration
    
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
What I Learned:

    - How SMB shares are created and accessed across a network.
    - How NTFS permissions control user access to files and folders.
    - The difference between Share Permissions and NTFS Permissions.
    - How to diagnose and resolve common file access issues.
    - How to map shared folders as network drives for easier access in a business environment.
    
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Outcome

Successfully configured a Windows file server, secured it using NTFS permissions, validated client access from Windows 11, resolved permission-related issues, and deployed the shared folder as a mapped network drive.
