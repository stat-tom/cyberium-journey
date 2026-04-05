# Lesson 3 - Searching in Linux

## Status
- Completed

## Overview
- Notes and examples for searching files, text, and system information in Linux.

## Notes
- `find` searches the filesystem in real time and is useful when you know where to start looking. It can filter by name, type, size, owner, or permissions.
- `find / ... 2>/dev/null` is commonly used when searching from the root directory so permission errors are hidden and only useful results are shown.
- `locate` searches a prebuilt file index, so it is usually faster than `find`, but the results depend on the index being up to date.
- `which` shows the full path of a command that will run in the current shell based on the `PATH` environment variable.
- `whereis` looks for a command's binary, source files, and manual page locations.
- `grep` searches inside text for matching words or patterns and is one of the most important tools for filtering command output.
- `grep` is commonly combined with pipes so you can search through the output of another command instead of searching a file directly.
- Searching `/etc/passwd` with `grep` is useful for checking login shells, counting matching accounts, or showing exact line numbers for entries.
- `ps aux` lists running processes for all users with detailed information such as the user, PID, CPU usage, memory usage, and command.
- `ps aux | grep kali` is a common way to filter the process list to only entries related to `kali`.

## Commands Practiced
- `find`
	- Search for files and directories starting from the current location.
	- Example: `find . -name "*.log"`
- `find / -type d -name apache2 2>/dev/null`
	- Search the whole system for directories named `apache2` and hide permission denied errors.
- `find / -type f -size +20M 2>/dev/null`
	- Search the whole system for files larger than 20 MB and hide permission denied errors.
- `locate`
	- Search the indexed file database for matching paths.
	- Example: `locate passwd`
- `which`
	- Show the executable path for a command.
	- Example: `which grep`
- `whereis`
	- Show binary, source, and manual page locations for a command.
	- Example: `whereis grep`
- `grep`
	- Search for matching text in a file or command output.
	- Example: `grep root /etc/passwd`
- `sudo grep nologin /etc/passwd`
	- Show all `/etc/passwd` lines containing `nologin`.
- `sudo grep -c nologin /etc/passwd`
	- Count how many lines in `/etc/passwd` contain `nologin`.
- `sudo grep -n kali /etc/passwd`
	- Show matching `kali` lines and include their line numbers.
- `ps aux`
	- List all active processes in a detailed format.
- `ps aux | grep kali`
	- Filter the process list to lines that contain `kali`.
