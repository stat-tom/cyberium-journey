# 01 – Linux

Notes and exercises covering Linux fundamentals for cybersecurity.

## Topics
- File system navigation and permissions
- User and group management
- Process management
- Networking tools (`netstat`, `ss`, `nmap`, `tcpdump`)
- Shell scripting basics
- Log analysis

## Progress
- Deployed Kali Linux on Oracle VirtualBox

## Commands Practiced
- `echo $SHELL` - Displays the current default shell for the logged-in user, which in this case returned `/usr/bin/zsh`.
- `sudo su` - Switches from the current user to the root user with elevated privileges.
- `exit` - Leaves the current shell session, which here was used to exit the root shell and return to the `kali` user.
- `tree -L 1 /` - Shows the top-level directory structure of the root filesystem, limited to one level deep.
- `ls -la /etc` - Lists all files in `/etc` in long format, including hidden entries, and shows permissions, owner, group, size, and modification date.

## Permission Format
- `d` - Entry is a directory.
- `-` - Entry is a regular file.
- `r` - Read permission.
- `w` - Write permission.
- `x` - Execute permission.
- The first character shows the file type, for example `d` for directory or `-` for file.
- The next 9 characters are grouped as `rwxrwxrwx` for user, group, and others.
- Example: `drwxr-xr-x` means a directory where the owner has full access, and group and others can read and enter it.

## Linux Structure
- `/bin` - Essential user command binaries. On this system it links to `/usr/bin`.
- `/boot` - Bootloader files, kernel files, and other data needed during system startup.
- `/dev` - Device files that represent hardware and virtual devices.
- `/etc` - System-wide configuration files.
- `/home` - Home directories for regular users.
- `/lib` - Essential shared libraries and kernel modules. On this system it links to `/usr/lib`.
- `/media` - Mount point for removable media such as USB drives.
- `/mnt` - Temporary mount point for manually mounted filesystems.
- `/opt` - Optional third-party software packages.
- `/proc` - Virtual filesystem exposing process and kernel information.
- `/root` - Home directory of the root user.
- `/run` - Runtime data created after the system boots.
- `/sbin` - Essential system administration binaries. On this system it links to `/usr/sbin`.
- `/srv` - Data served by system services.
- `/sys` - Virtual filesystem providing access to kernel and hardware information.
- `/tmp` - Temporary files used by applications and the system.
- `/usr` - User-space applications, libraries, and shared resources.
- `/var` - Variable data such as logs, cache, and spool files.
