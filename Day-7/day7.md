# Process and Network Management

This repository contains information on basic process and network management tasks in Linux. It provides commands and their explanations for managing processes, network connections, and useful system tools.

## Process Management

Every task in Linux has a process ID (PID).

### Common Commands:

- `ps`  
  To check the process ID.

- `ps -ef`  
  Shows all currently running process IDs.

  - `-e`: Shows all processes running on the system.
  - `-f`: Displays the full formatting list.

### Key Terms:

- **PPID**: Parent process ID. This is the starting point of a process.
- **PID**: Process ID.
- **UID**: Owner of the process.
- **C**: CPU usage.

- `ps -ef | grep <processname>`  
  Shows the process ID for a particular service name.

### Types of Processes:

1. **Foreground Processes**:  
   - These processes run directly on the terminal.
   - You can see the output in the terminal and it blocks your terminal until it finishes.
   - You must wait for it to finish before running the next command.

2. **Background Processes**:  
   - Multiple applications can run in the background.
   - If any process blocks you, you can kill it using the process ID.

   Command to kill a process:
   ```bash
   kill <PID>
dnf install htop
Network Management
netstat -lntp
Displays open ports in Linux.

-l: List only listening sockets.

-n: Show numerical port numbers.

-t: Show TCP connections (e.g., ssh, http, https).

-p: Display the process ID using the port.
Key Terms:
l: List

n: Port number

t: TCP (ports like SSH, HTTP, HTTPS)

p: Process ID
