# MacOS-on-Latitude-5320
MacOS, an user friendly posix operating system, now works on the Dell Latitude 5320. 

For MacOS Sonoma 14.2 or later<br>
Processor: i3-1125G4 (Tigerlake)<br>
Find more info at [Detailed hardware and software information](SPECIFICATIONS.md)

<br>
Graphics won't work until someone builds the Xe/UHD 500 series drivers...<br>
https://github.com/lshbluesky/Samsung-NT750XDA-KF59U-Hackintosh/issues/2

<h4>Current Status</h4>
Boots into MacOS Recovery Mode 

<h3>How to use</h3>

STEP 1, Create Bootable Device (Instruction for Mac users; For Windows and Linux, GL)

1. Create regular MacOS installer on USB, https://support.apple.com/en-us/101578

2. Mount EFI partition of MacOS installer.

    a.) Go to terminal and run `diskutil list` to see all partitions(mounted and unmounted)
    
    b.) Copy your MacOS installer's EFI partition IDENTIFIER. First find your USB stick under `/dev/diskxx`, then locate the partition with TYPE NAME `EFI` and copy IDENTIFIER `diskxxsyy`
   <br>
        <img width="561" alt="image" src="https://github.com/alders-lakes/MacOS-on-Latitude-5320/assets/101434885/cd760e55-6e8d-4cca-98d9-4b1e3f886ab6">
        <br>
        For example, In this image, the USB Installer is mounted at `/dev/disk4`, and the EFI PARTITION IDENTIFIER is `disk4s1`. The `(external, physical)` label helps avoid accidently mounting an internal SSD's EFI partition.
    c.) Run command `sudo diskutil mount <YOUR USB INSTALLER'S EFI PARTITION IDENTIFIER>`
    
4. Locate EFI partition in Finder app, drag the EFI folder into the EFI partition

STEP 2, Configuring Dell BIOS

1. Disable Secure Boot in Boot Configuration

2. Switch to AHCI/NVMe mode in Storage, SATA/NVMe Operation

3. Enable USB Boot Support under Integrated Devices, USB/Thunderbolt Configuration

STEP 3, BOOTING

1. Stick your installer USB into dell laptop once SHUTDOWN

2. Press power button and click `F12` continously immediatly

3. Locate your USB in the Boot Menu(will be the USB vendor's' name) and hit `ENTER`
    
    
STEP 4,
 Boots into MacOS recovery mode, its possible to install with mouse and keyboard and update EFI folder later. <br>
 Still working on trackpad and keyboard, so check back on this project later.....
     
    
    
