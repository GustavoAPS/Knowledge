| **Command**            | **Description**                                                                 | **Example**                                            |
|------------------------|---------------------------------------------------------------------------------|--------------------------------------------------------|
| `pwd`                  | Prints the current working directory                                            | `pwd`                                                  |
| `ls`                   | Lists files and directories in the current directory                           | `ls`                                                    |
| `cd <directory>`       | Changes the current directory to `<directory>`                                  | `cd /home/user`                                        |
| `mkdir <dir>`          | Creates a new directory named `<dir>`                                           | `mkdir new_folder`                                     |
| `rmdir <dir>`          | Removes an empty directory `<dir>`                                              | `rmdir old_folder`                                     |
| `rm <file>`            | Removes the file `<file>`                                                       | `rm file.txt`                                          |
| `rm -r <dir>`          | Removes a directory and its contents recursively                                | `rm -r old_folder`                                     |
| `cp <source> <dest>`   | Copies a file or directory from `<source>` to `<dest>`                          | `cp file.txt /home/user/new_file.txt`                  |
| `mv <source> <dest>`   | Moves or renames a file or directory from `<source>` to `<dest>`                | `mv file.txt /home/user/new_location/`                 |
| `touch <file>`         | Creates an empty file or updates the timestamp of an existing file `<file>`     | `touch newfile.txt`                                    |
| `cat <file>`           | Displays the content of `<file>`                                                | `cat file.txt`                                         |
| `less <file>`          | Displays the content of `<file>` one screen at a time                           | `less file.txt`                                        |
| `head <file>`          | Displays the first 10 lines of `<file>`                                         | `head file.txt`                                        |
| `tail <file>`          | Displays the last 10 lines of `<file>`                                          | `tail file.txt`                                        |
| `grep <pattern> <file>`| Searches for a pattern in a file and outputs matching lines                    | `grep "error" log.txt`                                |
| `find <dir> -name <name>` | Finds files and directories by name within `<dir>`                            | `find /home/user -name "*.txt"`                        |
| `ps`                   | Displays a list of currently running processes                                  | `ps`                                                    |
| `top`                  | Displays a dynamic view of system processes and resource usage                  | `top`                                                   |
| `kill <pid>`           | Terminates the process with the given `<pid>`                                   | `kill 1234`                                            |
| `chmod <permissions> <file>` | Changes the permissions of `<file>`                                          | `chmod 755 script.sh`                                  |
| `chown <user>:<group> <file>` | Changes the owner and group of `<file>`                                     | `chown user:group file.txt`                            |
| `df`                   | Displays information about disk space usage                                     | `df -h`                                                |
| `du`                   | Displays disk usage of files and directories                                    | `du -sh /home/user`                                    |
| `free`                 | Displays memory usage (RAM and swap)                                            | `free -h`                                              |
| `uname -a`             | Displays system information (kernel version, architecture, etc.)                | `uname -a`                                             |
| `man <command>`        | Displays the manual page for `<command>`                                        | `man ls`                                               |
| `history`              | Shows the list of previously used commands                                       | `history`                                              |
| `clear`                | Clears the terminal screen                                                      | `clear`                                                |
| `sudo <command>`       | Executes a command as the superuser or with elevated privileges                 | `sudo apt-get update`                                  |
| `apt-get update`       | Updates the list of available packages (Debian-based systems)                  | `sudo apt-get update`                                  |
| `apt-get install <package>` | Installs a package `<package>` (Debian-based systems)                       | `sudo apt-get install vim`                             |
| `yum install <package>` | Installs a package `<package>` (RedHat-based systems)                         | `sudo yum install wget`                                |
| `tar -czvf <archive.tar.gz> <dir>` | Compresses `<dir>` into a `.tar.gz` archive                            | `tar -czvf backup.tar.gz /home/user`                   |
| `tar -xzvf <archive.tar.gz>` | Extracts a `.tar.gz` archive                                                 | `tar -xzvf backup.tar.gz`                              |
| `wget <url>`           | Downloads a file from the given URL                                             | `wget http://example.com/file.zip`                     |
| `curl <url>`           | Transfers data from or to a server using various protocols (HTTP, FTP, etc.)    | `curl http://example.com`                              |
| `ssh <user>@<host>`     | Connects to a remote machine via SSH                                            | `ssh user@192.168.1.10`                                |
| `scp <source> <user>@<host>:<destination>` | Copies a file from `<source>` to a remote machine via SCP            | `scp file.txt user@192.168.1.10:/home/user/`           |
| `exit`                 | Exits the terminal session                                                      | `exit`                                                 |
