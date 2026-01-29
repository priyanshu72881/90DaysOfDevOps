Kernel – The central core that directly manages hardware, processes, memory, and device drivers, acting as an interface between hardware and software.
•	CPU Management:
The kernel decides which process uses the CPU and for how long (CPU scheduling).
•	Memory Management:
It allocates RAM to processes and prevents them from accessing each other’s memory.
•	Device Control:
The kernel manages communication between software and hardware using device drivers.
•	Process Management:
It creates, runs, and terminates processes, allowing multiple programs to run at the same time.
•	Security and Permissions:
The kernel controls access to files and resources based on user permissions.
  
USER SPACE
-----------
User Space is the part of the operating system where user programs and applications run.

SHELL - A shell is a program that understands the commands you type and tells the operating system (kernel) what task needs to be performed. (Shell ek bridge hai between User ↔ Operating System)
•	Shell Interpreters - A shell interpreter is a command-line program that takes user commands and executes them by communicating with the operating system.
Example: bash, sh, zsh, ksh, fish.
System libraries - System libraries are ready-made helper code that programs use to do basic tasks and talk to the Linux kernel.
•	glibc (libc.so.6) – Basic functions like input/output, memory, files
•	libm – Math functions like square root, power, sin, cos

System utilities = daily-use Linux commands that help you manage files, processes, and the system.
Daemons - A daemon is a background program that runs continuously to provide services to the system or other programs, without direct user interaction. Eg: Nginx, mySql etc.
init/system – init/systemd is the first process started by the Linux kernel at boot and is responsible for initializing the system, starting services, managing dependencies, and controlling background daemons.
What Is a Process?
A process is a running instance of a program.
A process contains:
•	Program code
•	Memory (heap, stack)
•	File descriptors
•	Process ID (PID)
•	User and permissions

Process Creation Flow
1.	A user runs a command (e.g., nginx)
2.	Shell requests the kernel to create a process
3.	Kernel:
o	Allocates memory
o	Assigns a PID
o	Schedules it on the CPU
4.	Process runs in user space
   
Process Managed
----------------
The Linux kernel manages processes by giving them CPU time, allocating memory, controlling their states, handling priorities, tracking parent–child relationships, and cleaning them up when they finish.

What systemd Does
•	Starts the system at boot
It launches all necessary services when Linux starts.
•	Manages background services
It can start, stop, restart, and check the status of services like SSH, nginx, and MySQL.
•	Handles service dependencies
It makes sure services start in the correct order.
•	Restarts failed services
If a service crashes, systemd can automatically restart it.
•	Controls system states
It manages shutdown, reboot, and different system modes.
•	Collects system logs
It stores logs for the system and services, which can be viewed using journalctl.

List 5 Commands You Would Use Daily
1.	ps
View running processes and their states.
Example: ps aux
Use ps aux to quickly identify zombie (Z) or stuck (D) processes.
2.	top / htop
Real-time monitoring of CPU, memory, and process states.
Real-time system and process monitoring.
3.	ls
List files and directories.
Example: ls -l
4.	systemctl
Manage services.
Example: systemctl status nginx
5.	df
Check disk usage.
Example: df -h

