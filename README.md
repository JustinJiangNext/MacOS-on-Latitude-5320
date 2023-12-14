# MacOS-on-Latitude-5320
MacOS, an user friendly posix operating system, now works on the Dell Latitude 5320. 

For MacOS Sonoma 14.2 or later
Processor: i3-1125G4 (Tigerlake)
Audio Controller: ALC3254
Wi-Fi Device: Intel Wireless

##How to use##
STEP 1, Create Bootable Device (Instruction for Mac users; For Windows and Linux, GL)
    1. Create regular MacOS installer on USB, https://support.apple.com/en-us/101578
    
    2. Mount EFI partition of MacOS installer.
    
        a.) Go to terminal and run `diskutil list` to see all partitions(mounted and unmounted)
        
        b.) Copy your MacOS installer's EFI partition IDENTIFIER. First find your USB stick under `/dev/diskxx`, then locate the partition with TYPE NAME `EFI` and copy IDENTIFIER `diskxxsyy`
        
        c.) Run command `sudo diskutil mount <YOUR USB INSTALLER'S EFI PARTITION IDENTIFIER>`
        
    3. Locate EFI partition in Finder app, drag the EFI folder into the EFI partition


STEP 2, Configuring Dell BIOS

    1. Disable Secure Boot in Boot Configuration
    
    2. Switch to AHCI/NVMe mode in Storage, SATA/NVMe Operation
    
    3. Enable USB Boot Support under Integrated Devices, USB/Thunderbolt Configuration
    
    4. Enable Thunderbolt Boot Support under Integrated Devices


STEP 3, BOOTING

    1. Stick your installer USB into dell laptop once SHUTDOWN
    
    2. Press power button and click `F12` continously immediatly
    
    3. Locate your USB in the Boot Menu(will be the USB vendor's' name) and hit `ENTER`
    
    
STEP 4,

     Still working on trackpad and keyboard, so check back on this project later.....
     
    
    
