# linux_for-devops

# Linux Fundamentals

Step 1 of my DevOps learning journey. This covers core Linux concepts, system commands, user and permission management, file/process handling, networking commands, and file transfer tools — all written up and practiced from my own notes.

## Structure

```
01-linux-basics/
├── notes/        topic-wise notes, written in my own words
├── practice/      hands-on exercises with real commands and their output
```

## Topics covered

- Kernel, bootloader, shell, and desktop environment
- Linux system architecture, Linux vs Windows, Linux vs Unix
- The Linux file system layout
- System-level commands (uname, uptime, who, id, package managers)
- Process states (running, sleeping, stopped, zombie)
- User and group management
- File permissions — both the numeric and symbolic methods
- File, directory, and process handling commands
- Networking commands — ping, traceroute, dig, nc, ip, ss, arp, whois, and more
- Compression tools and file transfer with scp and rsync
- Text processing with awk, sed, and grep
- LVM — physical volumes, volume groups, logical volumes, and live resizing

## What stood out the most

The networking commands section ended up being the biggest one by far — there's a lot of overlap between tools (ss vs netstat, arp vs ip neigh, traceroute vs tracepath vs mtr), and figuring out which one is the "modern" replacement for which older command was as useful as learning the commands themselves.

LVM was the other big one — resizing a mounted, live filesystem without downtime is the kind of thing that doesn't fully make sense until you actually run through it once.


