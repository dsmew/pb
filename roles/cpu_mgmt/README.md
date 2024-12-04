This role is designed to optimize the CPU performance on Linux

Line 1-4 Runs the nproc command which returns the number of CPU and store the result

Line 6-9 Prevent all CPUs from entering to the idle state 

Line 11-14 The loop will run for each CPU executing the command to set its governor to "performance"