# Linux Command Line Cheat Sheet

## Ls Command

List the contents of the current working directory.

**Command:** `ls`

**Options:**
- `-a`: Show all files (including hidden).
- `-R`: Recursive list.
- `-r`: Reverse order.
- `-t`: Sort by last modified.
- `-S`: Sort by file size.
- `-l`: Long listing format.
- `-1`: One file per line.
- `-m`: Comma-separated output.
- `-Q`: Quoted output.

## Bash Commands

Automate software development tasks.

**Commands:**
- `username -a`: Show system and kernel.
- `head -n1 /etc/issue`: Show distribution.
- `mount`: Show mounted file systems.
- `date`: Show system date.
- `uptime`: Show uptime.
- `whoami`: Show your username.
- `man command`: Show manual for command.

## Pipes

Takes the standard output of one process and passes it as standard input into another process.

**Commands:**
- `cmd1 | cmd2`: Stdout of cmd1 to cmd2.
- `cmd1 | &cmd2`: Stderr to cmd2.

## File Permissions

Determine who can access files and directories on a system.

**Commands:**
- `chmod octal file`: 
   - `4`: Read (r).
   - `2`: Write (w).
   - `1`: Execute (x).
   - Order: user/group/others.
- `chmod 777 file`: rwx permission for everyone.
- `chmod 755 file`: rw for user, rx for group and others.
- `chown usr:grp file`: Change the file owner to user and group to group.

## Networking

Commands related to networks.

**Commands:**
- `ping host`: Ping host.
- `whois domain`: Get whois for domain.
- `dig domain`: Get DNS for domain.
- `dig -x host`: Reverse lookup host.
- `wget file`: Download file.
- `wget -c file`: Continue stopped download.
- `wget -r url`: Recursively download files from URL.
- `curl url`: Outputs the webpage from URL.
- `curl -o meg.html url`: Writes the page to meg.html.
- `ssh user@host`: Connect to host as user.
- `ssh -p port user@host`: Connect using port.
- `ssh -i path-to-pem-file ubuntu@ip-address`: Used to connect to Amazon EC2.

## I/O Redirection

Redirecting input/output.

**Command:**
- `cmd < file`: Input of cmd from file.
- `cmd1 < cmd2`: Output of cmd2 as file input to cmd1.
- `cmd > file`: Standard output (stdout) of cmd as input to file.
- `cmd`: Display standard output of cmd.
- `cmd >> file`: Append stdout to file.
- `cmd2 > file`: Error output (stderr) of cmd to file.
- `cmd > &2`: Stdout to the same place as stderr.
- `cmd 2 > &1`: Stderr to the same place as stdout.
- `cmd &> file`: Every output of cmd to file.

## Bash Variables

Temporary storage for strings or numbers.

**Commands:**
- `env`: Show environment variables.
- `echo $NAME`: Output value of $NAME variable.
- `$PATH`: Executable search path.
- `$HOME`: Home directory.
- `$SHELL`: Current shell.

## Directory

Commands for working with directories.

**Commands:**
- `pwd`: Show current working directory.
- `mkdir dir`: Make directory dir.
- `cd dir`: Change directory to dir.
- `cd ..`: Go up a directory.
- `ls`: List files.

## Search Files

Commands to search for files.

**Commands:**
- `grep pattern files`: Search for pattern in files.
- `grep -i`: Case-insensitive search.
- `grep -r`: Recursive search.
- `grep -v`: Inverted search.
- `grep -o`: Show matched part of the file only.
- `find /dir/ -user name`: Find files owned by name in dir.
- `find /dir/ -name name*`: Find files starting with name in dir.
- `find /dir/ -mmin num`: Find files modified less than num minutes ago in dir.
- `whereis command`: Find binary/source/manual for command.
- `locate file`: Find file (quick search of system index).

## File Operations

Commands for working with files.

**Commands:**
- `touch file1`: Create file1.
- `cat file1 file2`: Concatenate files and output.
- `less file1`: View and paginate file1 (one page at a time).
- `file file1`: Get the type of file1.
- `cp file1 file2`: Copy file1 to file2.
- `mv file1 file2`: Move file1 to file2.
- `rm file1`: Delete/remove file1.
- `head file1`: Show the first 10 lines of file1.
- `tail file1`: Show the last 10 lines of file1.
- `tail -f file1`: Output the last lines of file1 as it changes.

## Process

Viewing and managing processes.

**Commands:**
- `ps`: Show a snapshot of processes.
- `top`: Show real-time processes.
- `kill pid`: Kill process with ID pid.
- `pkill name`: Kill process with name "name".
- `killall name`: Kill all processes starting with name.
