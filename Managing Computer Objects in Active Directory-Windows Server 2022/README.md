Real Ticket:

A company laptop is being reassigned to another department and must be managed in Active Directory before it can be used again.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
What I Practiced:

        - Located a computer object in Active Directory Users and Computers (ADUC)
        - Disabled a computer account
        - Re-enabled the computer account
        - Moved the computer object between Organizational Units (OUs)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
Steps Performed:
1. Find the Computer in ADUC
   
        - Open Active Directory Users and Computers
        - Navigate to the correct Organizational Unit
        - Locate the computer object (WIN11-PC)

<img width="800" height="400" alt="Screenshot 2026-07-08 at 16 55 29" src="https://github.com/user-attachments/assets/a37efbab-a7f1-439c-b11b-7b35425ef867" />

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
2. Disable the Computer Account
   
        - Right-click WIN11-PC
        - Select Disable Account
        - Confirm the action

<img width="800" height="400" alt="Screenshot 2026-07-08 at 17 04 44" src="https://github.com/user-attachments/assets/333be77e-cd72-4d55-943e-11cca88a3eb1" />

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
3. Enable the Computer Account
   
        - Right-click WIN11-PC
        - Select Enable Account
        - Confirm the action
   
   <img width="800" height="400" alt="Screenshot 2026-07-08 at 17 05 45" src="https://github.com/user-attachments/assets/937d9592-6ba0-45fc-b4e8-32122aeb988a" />

   -----------------------------------------------------------------------------------------------------------------------------------------------------------------------
   4. Move the Computer to Another OU

        To simulate a device being reassigned to another department:

                - Right-click WIN11-PC
                - Select Move
                - Choose the destination OU
                - Confirm the move
   <img width="800" height="400" alt="Screenshot 2026-07-08 at 17 13 58" src="https://github.com/user-attachments/assets/696ae2c2-9859-4db5-9dca-f1ed16c7647a" />

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
   Why This Matters

        In many organisations, computers are managed in Active Directory just like user accounts.

IT Support engineers may:

        - Disable a computer if it is lost, stolen, or being investigated.
        - Re-enable it when it is ready to be used again.
        - Move the computer to another Organizational Unit when it is reassigned to a different department so that the correct Group Policies and security settings are                applied automatically.
        
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
Skills Demonstrated:

        - Windows Server 2022
        - Active Directory Users and Computers (ADUC)
        - Computer Object Management
        - Organizational Units (OUs)
        - Active Directory Administration
        - Help Desk / IT Support
