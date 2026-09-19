# Virtual Lab Build
## 1 Host computer informations

- According to Task 1.1, the technical laboratory should have three minimum environments: my host computer, a Windows virtual machine, and an Ubuntu Linux virtual machine.
- The first thing I did was investigate my host computer's resources so I could determine what it could safely support and make appropriate resource allocations for the virtual machines.
- I checked the CPU and found that my host computer has an Intel(R) Core(TM) i5-3337U CPU with 2 physical cores and 4 logical processors.
 - I also confirmed that virtualization is enabled. This was important because I needed to know whether my computer could support running virtual machines.
- I then checked the memory and storage. The host computer has 4.0 GB of DDR3 RAM and a 466 GB HDD, with approximately 296 GB of storage available. These resources helped me determine how much CPU, memory, and storage I could allocate to the virtual machines without unnecessarily too much load on my host machine.
- After confirming the capabilities and limitations of my host computer, I proceeded to configure the two virtual machines.
- Snapshots was takeen on the two virtual machines but i took it after the configuration.
## 2 Window Virtual Machine build Up

- CPU: 1 Processor
- RAM: 1.5GB
- Disk:50 GB
- Network: NAT
## 3 Ubuntu Virtual Machine build up
- CPU: 1 Processor
- RAM: 1.5GB
- Disk: 25GB
- Network: NAT
## 4 Resource Allocations
- I mentioned thatmy host computer has only 4 GB of RAM and 2 physical CPU cores so I had to allocate resources accordingly.
-  I allocated 1 processor to each Virtual Machine rather than assigning all available processing resources to one Virtual machine which is not wise to do.
-  I also allocated 1.5 GB RAM to each Virtuaal Machines because assigning excessive memory could leave insufficient RAM for the host operating system which is also not advisable. It can cause the host machine to proceses it operating system slowly. 
- I used my host computer available storage which is about 296GB to assign the amount of storage each virtual machines would use because i won't want it to be excessively which can put uncessary pressure on my host computer so i decided to allocate 50GB of storage to my windows virtual machine and 25GB to Ubuntu Virtual Machine which supports my host computer.
## 5 Network Configuration
- I used NAT (Network Address Translation) for the virtual machines in my technical laboratory.
-  I used NAT because it allows the virtual machines to access the network through the host computer's network connection while keeping the virtual machines on a private virtual network behind the host.
- This configuration is suitable for my project because I need the virtual machines to perform basic network and administration activities without making them directly accessible as separate devices on the external network which bridged network would have done but i decided to use NAT which flows well with my project.
- The NAT configuration also means that if my host computer is not connected to the internet the virtual machines will not have internet access through NAT.
## 6 Snapshots
- I took a snapshot after completing the initial configurations on both virtual machines and named the snapshots "Phase 1 - Initial Configuration."
- The purpose of the snapshots is to provide a restore point for the virtual machines. If a virtual machine becomes unstable, crashes or I need to return to an earlier state, I can use the snapshot to restore the VM to the state captured by the snapshot.
