# Practice Questions: Kernel, Bootloader, Shell & Desktop Environment

1. In your own words, explain what the kernel does and why applications can't talk to hardware directly without it.
:- The kernel is the core part of the operating system. It acts as a bridge between applications 
   and computer hardware.
   Applications cannot directly access hardware because this could cause security problems, resource conflicts,
   and system crashes. The kernel provides controlled and safe access to hardware.

2. Write out the full boot flow from power-on to the login screen, naming each stage in order.
  1 Power On – The computer is switched on.
  2 BIOS/UEFI – Initializes basic hardware and looks for something to boot.
  3 POST – Performs basic hardware checks.
  4 GRUB – Bootloader selects and loads the Linux kernel.
  5 Linux Kernel – Initializes hardware, drivers, memory, and other core components.
  6 initramfs – Provides the temporary filesystem needed during early boot and helps locate the real root filesystem.
  7 systemd – Starts as PID 1 and manages the rest of the system.
  8 System Services – Services such as networking and other required services are started.
  9 Display Manager – On a GUI system, it provides the graphical login interface.
  10 Login Screen – The user can log into the system.

3. What is GRUB, and where does it sit in the boot flow?
:-    GRUB stands for GRand Unified Bootloader.

   GRUB is a bootloader commonly used by Linux systems. Its main job is to load the Linux kernel and pass the required boot parameters to it.

   GRUB comes after BIOS/UEFI and before the Linux kernel.

4. Run `echo $SHELL` and `echo $0` on your machine. What shell are you currently using? How would you switch to 
   a different one (e.g. from bash to zsh) temporarily?
:-   echo $SHELL
     echo $0
output:-
     /bin/bash
     bash     
   

5. List three different shells and one difference between any two of them.
:- Three common Linux shells are:
   Bash – Bourne Again Shell
   Zsh – Z Shell
   Fish – Friendly Interactive Shell
   Difference between Bash and Zsh

   Zsh provides additional interactive features and more powerful customization and completion capabilities compared with traditional Bash usage.   

6. What's the difference between a shell and a desktop environment? Give an example of something each one is responsible for.
:- A shell is a command-line interface that allows users to interact with the operating system using commands.
   A desktop environment (DE) provides a graphical interface for interacting with the operating system.


7. If you're working entirely over SSH on a headless server, which of the two (shell or desktop environment) do you still have access to, and why?
:- A headless server normally does not have a graphical desktop environment installed because it is managed remotely through the command line.

8. Name four components that make up a typical desktop environment.
:- Window Manager – Manages application windows.
File Manager – Allows users to browse and manage files.
Panel/Taskbar – Provides menus, application shortcuts, notifications, etc.
Settings/Control Center – Allows users to configure system settings.

9. Task: check what desktop environment (if any) is installed on your machine, using a command of your choice. If you're on a cloud server with no GUI, explain what you'd expect to find instead.
:- A simple command to check the current desktop environment is: echo $XDG_CURRENT_DESKTOP
   Another command is: echo $DESKTOP_SESSION
   We can also check available desktop sessions: ls /usr/share/xsessions/

10. Task: find out which bootloader your machine uses. Hint — look for a config file under `/boot/`.
:- ls /boot/grub/grub.cfg
