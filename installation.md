
<h1>How to use</h1>

STEP 1, Create Bootable Device (Instruction for Mac users; For Windows and Linux, GL)
1. Format your drive to GPT

2. Create regular MacOS installer on USB, https://support.apple.com/en-us/101578

3. Mount EFI partition of MacOS installer.

    a.) Go to terminal and run `diskutil list` to see all partitions(mounted and unmounted)
    
    b.) Copy your MacOS installer's EFI partition IDENTIFIER. First find your USB stick under `/dev/diskxx`, then locate the partition with TYPE NAME `EFI` and copy IDENTIFIER `diskxxsyy`
   <br>
        <img width="561" alt="image" src="https://github.com/alders-lakes/MacOS-on-Latitude-5320/assets/101434885/cd760e55-6e8d-4cca-98d9-4b1e3f886ab6">
        <br>
        For example, In this image, the USB Installer is mounted at `/dev/disk4`, and the EFI PARTITION IDENTIFIER is `disk4s1`. The `(external, physical)` label helps avoid accidently mounting an internal SSD's EFI partition.
    c.) Run command `sudo diskutil mount <YOUR USB INSTALLER'S EFI PARTITION IDENTIFIER>`
    
4. Locate EFI partition in Finder app, drag the EFI folder into the EFI partition

Alternatively, you can use MBR and MS-DOS. Just put the EFI partition and the [`BaseSystem` folder](https://github.com/JustinJiangNext/BaseSystem) in the partition

STEP 2, Configuring Dell BIOS

1. Disable Secure Boot in Boot Configuration

2. Switch to AHCI/NVMe mode in Storage, SATA/NVMe Operation

3. Enable USB Boot Support under Integrated Devices, USB/Thunderbolt Configuration

STEP 3, BOOTING

1. Stick your installer USB into dell laptop once SHUTDOWN

2. Press power button and click `F12` continously immediatly

3. Locate your USB in the Boot Menu(will be the USB vendor's' name) and hit `ENTER`
    
    
STEP 4,
 Install MacOS in recoverymode just as any regular Mac
     
    
    
