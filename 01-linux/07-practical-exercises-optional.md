# Lesson 7 - Practical Exercises (Optional)

## Status
- Completed

## Overview
- Optional exercises for system information and related Linux tasks.

## Tasks
- Task 1:
	- Create a file named `users.txt` in your home directory.
	- Display the contents of `/etc/passwd` and filter only the lines containing `home`.
	- Save the result to the `users.txt` file.
	- Append the current date to the end of the `users.txt` file.
	- Display the contents of `users.txt` together with line numbers.
- Task 2:
	- Find all processes that belong to your user.
	- Check which groups the `root` user belongs to.
	- Check your IP address.
- Task 3:
	- Create the directory structure `project/data/2024/backup`.
	- In the `backup` directory, create 3 files with the date in their names.
	- Copy the entire structure to a new location named `project_backup`.
	- Display the directory tree for both structures.

## Notes
- Solutions:
	- Task 1:
		- `touch ~/users.txt`
		- `grep home /etc/passwd > ~/users.txt`
		- `date >> ~/users.txt`
		- `nl ~/users.txt`
	- Task 2:
		- `ps -u $(whoami)`
		- `groups root`
		- `ip addr show`
	- Task 3:
		- `mkdir -p ~/project/data/2024/backup`
		- `touch ~/project/data/2024/backup/backup-$(date +%F)-1.txt ~/project/data/2024/backup/backup-$(date +%F)-2.txt ~/project/data/2024/backup/backup-$(date +%F)-3.txt`
		- `cp -r ~/project ~/project_backup`
		- `tree ~/project ~/project_backup`
