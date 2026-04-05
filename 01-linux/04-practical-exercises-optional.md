# Lesson 4 - Practical Exercises (Optional)

## Status
- Not started

## Overview
- Optional exercises related to the previous Linux topics.

## Tasks
- Task 1:
	- Find all configuration files (`.conf`) in the `/etc` directory using the `find` command.
	- Save the result in your home directory to a file named `~/conf_files.txt`.
	- Filter the results using `grep` to find entries containing the word `network`.
- Task 2:
	- Find all files larger than 100 MB.
	- Find files modified within the last 7 days.
	- Search for files owned by your current user.
	- Combine all of the above conditions into one `find` command.
- Task 3:
	- Find all `.log` files in the system.
	- Find files with the word `backup` in their name.
	- Find files in the `/etc` directory with the word `conf` in their name.

## Notes
- When searching the whole system, it is useful to add `2>/dev/null` to hide permission denied messages.
- Solutions:
	- Task 1:
		- `find /etc -type f -name "*.conf" > ~/conf_files.txt`
		- `grep network ~/conf_files.txt`
	- Task 2:
		- `find / -type f -size +100M 2>/dev/null`
		- `find / -type f -mtime -7 2>/dev/null`
		- `find / -type f -user $(whoami) 2>/dev/null`
		- `find / -type f -size +100M -mtime -7 -user $(whoami) 2>/dev/null`
	- Task 3:
		- `find / -type f -name "*.log" 2>/dev/null`
		- `find / -type f -name "*backup*" 2>/dev/null`
		- `find /etc -type f -name "*conf*"`
