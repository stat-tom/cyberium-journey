# Lesson 2 - Basic Commands

## Status
- Completed

## Overview
- This lesson covers basic terminal navigation, finding help for commands, and discovering related tools from the command line.
- The examples show the difference between relative paths and absolute paths when moving between directories.

## Notes
- `pwd` prints the current working directory so you can confirm where you are.
- `cd ..` moves up one directory level, while a longer relative path such as `cd ../../` moves up multiple levels.
- Absolute paths start from `/`, so `/etc/apache2/mods-enabled` works from any location.
- Relative paths depend on the current directory. For example, running `cd etc` while already inside `/etc` fails because there is no nested `etc` directory there.
- Some system files are protected. Reading `/etc/shadow` as a normal user returns `Permission denied`, so administrative access is required.
- Built-in help is often the fastest starting point. Short help flags such as `ping -h` give a quick summary, while `man ping` provides the full manual page.
- `apropos compress` searches manual page descriptions for related commands, which is useful when you know the task but not the exact command name.
- `https://explainshell.com/` is useful for breaking down command syntax and options when a command line looks unfamiliar.

## Commands Practiced
- `pwd`
- `cd ..`
- `cd ../../`
- `cd /etc/apache2/mods-enabled`
- `cat /etc/shadow`
- `sudo cat /etc/shadow`
- `ping -h`
- `man ping`
- `apropos compress`

## Sample Commands
- `ls`
- `cd /etc`
- `cd /var/log`
- `whoami`
- `uname -a`
- `man ls`
- `apropos network`
