This role is designed to optimize the CPU performance on Linux

Lines 3-6 Run grep command to search the line and save in variable grub_line

Lines 8-10 Trim whitespace and newline characters

Lines 13-23 Disable C-states and set CPU to perfomance mode 

Line 25-26 Apply GRUB configuration changes 

Line 27-29 Conditions for any changes

Line 30 Notify handlers to reboot server when the configuration is changed 