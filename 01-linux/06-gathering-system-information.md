# Lesson 6 - Gathering System Information

## Status
- Completed

## Overview
- Notes and examples for collecting system information in Linux.

## Notes
- User information commands help identify the current account, groups, and logged-in users.
- System information commands show host details, environment variables, and running processes.
- Network information commands help inspect interfaces, IP addresses, and active connections.
- Device information commands show storage usage and connected hardware.

## Commands Practiced
- User Information:
	- `whoami` - displays the name of the current user
	- `id` - shows detailed information about the user and groups
	- `who` - lists logged-in users
- System Information:
	- `hostname` - shows the host name
	- `uname -a` - displays operating system information
	- `env` - prints environment variables
	- `ps aux` - lists running processes
	- `top` - monitors processes in real time
- Network Information:
	- `ifconfig` - shows network interface configuration
	- `ip addr` - displays IP addresses
	- `netstat` - shows network connections
	- `ss` - displays socket statistics
- Device Information:
	- `df -h` - shows disk space usage in a human-readable format
	- `lsblk` - lists block devices
	- `lsusb` - lists USB devices
	- `lspci` - lists PCI devices
