# System-Level Commands

These are commands that give you information about the system itself, and the tools used to install/manage software.

## Getting system information

`uname` shows information about the Linux system and kernel.

`uptime` shows how long the system has been running.

`date` displays the current date and time.

`who` and `whoami` show which users are currently logged into the system, and which user you are, respectively.

`which` shows the location/path of a command (which command is actually being run when you type it).

`id` displays information about a user, including their UID, GID, and group memberships.

`hostname` shows the system's hostname.

## Process states in Linux

Every running process is in one of these states:

**R — Running.** The process is currently executing.

**S — Sleeping.** The process is waiting for an event to happen.

**D — Uninterruptible sleep.** The process is usually waiting on I/O and can't be interrupted normally while in this state.

**T — Stopped.**

**Z — Zombie.** The process has finished executing, but its parent process hasn't yet collected its exit status.

## sudo

`sudo` allows a user to run commands with root privileges.

## Package managers

Different Linux distributions use different package managers to install, update, and remove software.

`apt` is used on Ubuntu and other Debian-based distributions.

`yum` is used on RedHat, and specifically on CentOS/RHEL.

`dnf` is the modern replacement for yum, used on newer RedHat-family systems like Fedora and RHEL.

`pacman` is used on Arch Linux and Arch-based distributions.

## System monitoring commands

`df -h` shows disk usage.

`free -h` shows RAM/memory usage.

`du` shows disk usage of files and directories, `du -sh` gives a summarized human-readable size.

`vmstat` and `vmstat -a` give information about RAM and overall system performance.

## Shutdown / reboot

`shutdown` and `reboot` are used to shut down or restart the system.
