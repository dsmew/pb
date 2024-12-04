This role is designed to automate the process of setting up encrypted storage volumes using Linux Unified Key Setup

Lines 3-6 Checks the status of the disks using the command lsblk -f to gather info about existing partitions and encryption status

Lines 8 and 38  If the disk is not encrypyted then block of tasks is executed

Lines 9-37 Automate the entire process of setting up the encrypted disk 

Lines 40-47 Execute the command lsblk -f again and show the output