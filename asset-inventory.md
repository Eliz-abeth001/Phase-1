# Asset Inventory
## 1. System Identification
- System Manufacturer: Dell Inc.
- System Model: Latitude 3330
- System Type: x64-based PC

   The system manufacturer identifies the company that produced the computer which in this case is Dell Inc. The system model identifies the specific computer model as a Dell Latitude 3330. The system type is x64-based PC, meaning the computer uses a 64-bit architecture and is capable of running a 64-bit operating system.
## 2. CPU
- Processor: Intel(R) Core(TM) i5-3337U CPU @ 1.80GHz, 1801 MHz
- Physical Cores: 2
- Logical Processors: 4

The CPU(Central Processing Unit) is responsible for processing instructions and performing calculations required by the operating system and applications. My computer uses an Intel Core i5-3337U processor with a clock speed of approximately 1.80 GHz.

The CPU has 2 physical cores and 4 logical processors. Because the computer has only 2 physical cores, I considered this limitation when allocating CPU resources to my virtual machines. I allocated 1 virtual processor to each VM so that the host computer would still have processing resources available.

## 3. Memory
- Installed RAM: 4.0 GB DDR3

RAM (Random Access Memory) is volatile memory that temporarily holds data and programs that the computer is actively using. Its contents are normally lost when the computer is powered off.

My computer has 4.0 GB of RAM which is a limited amount for running multiple demanding applications or virtual machines at the same time. I therefore considered this limitation when configuring my virtual machines and allocated resources carefully so that the host computer would still have enough memory to operate.

## 4. Storage
- Storage Device: Toshiba MQ01ACF050 (HDD)
- Storage Capacity: 466 GB
- Available Storage: 296 GB

Storage is different from RAM because it is non-volatile. It stores data permanently, meaning the data remains available even when the computer is powered off.

My computer uses a Hard Disk Drive (HDD), which stores data on spinning magnetic platters and uses a read/write head to access the data. HDDs are generally slower than solid-state drives (SSDs) because they contain moving mechanical parts.

I considered my available storage when configuring my virtual machines. Since I had 296 GB available, I allocated storage to the VMs without using an unnecessarily large amount of the host computer's available space.

## 5. Operating System
- Operating System: Windows 10 Pro
- OS Version: 22H2
- OS Architecture: 64-bit

My computer uses Windows 10 Pro, version 22H2, with a 64-bit operating system. The operating system manages the computer's hardware and provides the environment needed for applications and other software to run.

The 64-bit architecture allows the operating system to work with modern 64-bit software and hardware.
## 6. Graphics
- Graphics Adapter: Intel(R) HD Graphics 4000

The graphics adapter is responsible for processing and displaying visual information on the computer, such as the desktop, applications, images and videos.

My computer uses Intel HD Graphics 4000, which is an integrated graphics solution. This means the graphics processing is built into the computer's processor/platform rather than using a separate dedicated graphics card.
## 7. Network Adapters
- Wi-Fi Adapter: Broadcom 802.11n Network Adapter
- Ethernet Adapter: Intel(R) 82579LM Gigabit Network Connection

Wi-Fi IP Configuration includes;
- MAC Address: 70-XX-XX-XX-XX-XX
- IPv4 Address: 192.168.X.X
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.X.X
- DHCP Server: 192.168.X.X
- DNS Server: 192.168.X.X

The Wi-Fi adapter allows the computer to connect to a wireless network. The Ethernet adapter provides a wired network connection when an Ethernet cable is used.

The MAC address is a hardware-level identifier for the network adapter. The IPv4 address identifies the computer on its current network. The subnet mask helps determine which devices are on the local network, while the default gateway provides a path to other networks. DHCP automatically provides network configuration information and DNS helps translate domain names into IP addresses.
## 8. BIOS/UEFI
- BIOS Version/Date: Dell Inc. A01, 5/9/2013
- BIOS Mode: Legacy

The BIOS is firmware that initializes and checks the computer's hardware during the startup process and helps begin the operating system boot process.

My computer uses Dell BIOS version A01, dated 5/9/2013, and is configured to use Legacy BIOS mode rather than UEFI mode.
## 9. Connected Peripherals

No external peripherals are currently connected to the computer.

The computer's built-in keyboard, touchpad, and display are integrated into the laptop and are not considered externally connected peripherals for this inventory.
