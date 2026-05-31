Windows Troubleshooting Foundations

Overview
As part of my IT Support Home Lab, I practised common Windows troubleshooting tasks that are frequently encountered in Helpdesk and IT Support roles.
The focus of this lab was understanding how Windows components work, identifying common issues, and following a structured troubleshooting process.



Task Manager & Performance Troubleshooting

Skills Practised:

        Opened and navigated Task Manager
        Monitored CPU, Memory, Disk and Network usage
        Identified running applications and background processes
        Observed resource utilisation during normal system activity


Key Learning:

        High CPU, Memory or Disk usage can affect system performance
        Performance graphs help identify resource spikes
        Not every high-usage process is a problem
        Core Windows processes should not be terminated without investigation


Troubleshooting Approach:

When a system is slow:

        Open Task Manager
        Check CPU, Memory and Disk utilisation
        Identify the process responsible
        Determine whether the process is expected or abnormal
        Apply corrective action if required



Windows Services Troubleshooting
Skills Practised:

        Opened Services Manager (services.msc)
        Located Print Spooler service
        Restarted services
        Reviewed service properties
        Modified startup types


Key Learning:
        Windows services run in the background and support many operating system functions.

Examples:

        Service	                                                               Function

        Print Spooler	                                                         Printing
        Windows Audio	                                                         Sound
        Bluetooth Support Service	                                             Bluetooth
        DHCP Client	                                                           Network configuration


Troubleshooting Approach:

When a Windows feature stops working:

        Identify the related service
        Verify service status
        Restart the service
        Confirm functionality has been restored



Startup Application Troubleshooting

Skills Practised:

        Reviewed Startup applications
        Disabled and re-enabled startup programs
        Investigated startup impact ratings
        Used shell:startup
        Added a startup item manually
        Verified automatic launch after login


Key Learning:

        Too many startup applications can increase boot times and reduce performance.
        Disabling a startup application does not uninstall it; it only prevents it from launching automatically.



Network Troubleshooting Practice

Scenario

I intentionally disabled the Ethernet adapter and then diagnosed and resolved the connectivity issue.

Steps Performed

        Disabled Ethernet adapter
        Verified internet connectivity failed
        Used Windows Troubleshooter
        Identified the root cause
        Re-enabled the adapter
        Confirmed internet access was restored


Key Learning:

        A structured troubleshooting process is important:

        Identify the problem
        Investigate the cause
        Apply a fix
        Verify the solution



Outcome

This lab improved my confidence using Windows troubleshooting tools including:

        Task Manager
        Services Manager
        Startup Management
        Windows Network Diagnostics

It also reinforced the importance of following a logical troubleshooting process rather than making random changes.
