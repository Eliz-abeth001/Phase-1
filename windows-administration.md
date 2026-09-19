# Operating System Administration
On Windows Virtual Machine demonstrate that you can;
## Identify running processes
The first thing to do is to open Task Manager. I opened Task Manager on the Windows virtual machine and inspected the Processes tab. Under the Apps section, I observed VirtualBox Virtual Machine as a running process.

At the time of observation, it was using approximately 30% CPU, although the percentage continued to change while I was observing it. It was also using approximately 38.4 MB of memory.

A process is a program or task that is currently being executed by the operating system. The CPU and memory usage of a process can change depending on what the program is doing at a particular time.

## identify resource utilisation;
I used Task Manager to inspect the resource utilisation of the Windows virtual machine. At the time of observation, the overall utilisation was:

* CPU: 100%
* Memory: 87%
* Disk: 100%
* Network: 0%

The CPU and disk were under heavy activity at the time of observation, while memory usage was also high. Network activity was at 0%, indicating that there was little or no network activity at that particular moment.

Resource utilisation changes depending on what the computer is doing. High CPU, memory, or disk utilisation over an extended period can contribute to poor system performance. This observation also demonstrates why the resources allocated to a virtual machine need to be considered carefully.

## inspect services;
I inspected several Windows services using the Services management console. I observed services with different startup types, including Automatic, Manual, and Disabled.

An Automatic service is configured to start automatically when Windows starts. A Manual service does not normally start automatically during system startup, but it can be started when Windows, an application, or an administrator requires it. A Disabled service is prevented from starting normally until its startup type is changed.

Inspecting services helps me understand which services are running in the background and how Windows controls them. It also helps with troubleshooting because an administrator can determine whether a required service is running and when appropriate, stop or start a service.

## stop and start an appropriate test service;
I opened the Windows Services management console using services.msc and inspected the Print Spooler service.

The Print Spooler service was initially Running, with its startup type set to Automatic. The service manages print jobs and communication with printers.

I stopped the Print Spooler service as a test, and its status changed to Stopped. I then started the service again, and its status returned to Running.

This demonstrated how Windows services can be inspected, stopped, and started when performing system administration and troubleshooting.

## inspect disk utilisation;
I inspected the Windows VM's disk utilisation using Task Manager. At the time of observation, the disk usage was approximately 64%, although the value continued to change.

Disk Capacity: 50.0 GB
Disk Type: SSD

The disk usage percentage represents the level of disk activity at that moment. It does not mean that 64% of the 50 GB storage capacity has been filled. The 50 GB represents the storage capacity allocated to the virtual machine.

Monitoring disk utilisation can help identify situations where high disk activity may contribute to slow system performance.

## create a local user;
I used the Windows User Accounts management tool to create a local test user account named TestUser.

A local user account is managed directly by the Windows computer and provides an individual identity that can be assigned specific permissions. I created the account as a standard user rather than an administrator because normal users should not have unnecessary administrative privileges.

## create a local group where supported;
I created a local group named LabUsers using the Local Users and Groups management console. I then added TestUser as a member of the group.

A local group allows multiple user accounts to be managed together. Instead of assigning the same permissions to each user individually, permissions can be assigned to the group, and its members can receive those permissions. 

## modify permissions;
I created a test folder named LabFolder and added the LabUsers group to its Security permissions. I assigned the Modify permission to the group doing this would give certain pemissions like read,write to the group.

This demonstrated how Windows permissions can be assigned to a group to control access to a resource. Members of LabUsers, such as TestUser, can receive the permissions assigned to the group.

## identify network configuration;
I used the ipconfig command in Command Prompt to inspect the network configuration of the Windows virtual machine.

The active network adapter was Ethernet. It had an IPv4 address, subnet mask, and default gateway.

The IPv4 address identifies the virtual machine on its network. The subnet mask determines which part of the IP address represents the network and which part identifies the host. The default gateway provides a path for the virtual machine to communicate with networks outside its local network.

The VM is configured to use NAT networking in VirtualBox, which allows the virtual machine to access external networks through the host computer's network connection.

## inspect Windows Update;
I opened Windows Update in the Windows VM and inspected its current update status.

Windows reported that the device was missing important security and quality fixes. The last update check was recorded as today at 6:40 PM, and an update was pending download.

Windows Update is used to deliver operating system updates, including security fixes, quality improvements, and other updates. Regularly checking Windows Update helps ensure that the operating system receives important security fixes and remains maintained

## inspect Windows Defender;
I opened Windows Security and inspected the Virus & threat protection section.

Windows Defender reported "No current threats." I also checked the Virus & threat protection settings and confirmed that Real-time protection was turned on.

Windows Defender helps protect the computer against malware and other security threats. Real-time protection continuously monitors the system for potential threats, while the threat status provides information about threats detected by Windows Security.

## locate relevant system logs.
I opened Event Viewer and navigated to Windows Logs > System to inspect system events.

I selected a recent event with the following details:

* Source: FilterManager
* Event ID: 6
* Level: Information

The System log records events related to Windows system components, services, drivers, and other system activities. Event Viewer allows an administrator to review these events when monitoring or troubleshooting a Windows system.

The selected event had an Information level, meaning it was recorded as informational rather than being classified as a warning or error. 