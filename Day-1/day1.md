## What is Linux?
- Linux is an open-source operating system like Windows and macOS, but it is free.

## Why Linux is Important?
- Most of the cloud providers like Azure, GCP, AWS run Linux VMs.
- Automation tools like Ansible, Kubernetes, Docker mostly work on Linux.
- CI/CD servers like Jenkins mostly run on Linux.
- Bash scripting is easy in Linux.

## What is Networking?
- Networking means connecting one or more devices like containers, servers, computers so they can share information.
- There are 2 types:
  - **Private Networking:** Used for internal purposes.
  - **Public Networking:** Used for internet-facing applications.

## Core Network Concepts:
- **IP Address:** Unique address of a machine on a network.
- **Port:** Doorway to communicate with a machine.
- **Protocol:** Rules for communication like HTTPS, HTTP, UDP, TCP.
- **Subnet:** A small network within a big network.
- **Gateway:** Device that connects two different networks.

## Viewing Network Interface:
- `ip config` or `ip link show`

## Configuring Network Interface:

### Static IP Address:
- You need to add the network configuration:
  - `sudo nano /etc/network/interfaces`
- To restart and save:
  - `sudo systemctl restart networking`

### Dynamic IP Configuration:
- It can be done using DHCP.
- Configuration example under `/etc/network/interfaces`:
  auto eth0 iface eth0 inet dhcp
- To restart and save:
- `sudo systemctl restart networking`

## Network Configuration Files:
- `/etc/network/interfaces` location.
- This file is mostly used on Debian-based systems to configure the network interface.

## What is CIDR Block?
- CIDR means Classless Inter-Domain Routing blocks.

## IPv4 Address:
- It contains 32-bit numeric values written in 4 decimals.
- Example: `192.168.1.1`

### IPv4 Address Classes:
- **Class A:**  
`1.0.0.0` to `127.255.255.255` (Default subnet mask: `255.0.0.0` /8)
- **Class B:**  
`128.0.0.0` to `191.255.255.255` (Default subnet mask: `255.255.0.0` /16)
- **Class C:**  
`192.0.0.0` to `223.255.255.255` (Default subnet mask: `255.255.255.0` /24)

## Calculating CIDR Blocks:

- Common prefix lengths:
- `/8`: 8 bits for network and 24 bits for host.
- `/16`: 16 bits for network and 16 bits for host.
- `/24`: 24 bits for network and 8 bits for host.

- Example:
- IP: `192.168.1.0`
- 32 bits total, each number (octet) has 8 bits (192, 168, 1, 0).
- `/24` means:
  - First 24 bits = Network part (fixed) → `192.168.1`
  - Last 8 bits = Host part → `0` can be changed.

## How Many Hosts You Get for a Given CIDR Block:
- Formula:  
`Number of hosts = 2^(number of host bits) - 2`
- We subtract 2 because:
- 1 for broadcast address (all bits 1).
- 1 for network address (all bits 0).

### Examples:
- `/24`:  
- 32-24 = 8 host bits  
- Total IP addresses = 2^8 = 256  
- Usable IPs = 256 - 2 = 254 hosts
- `/16`:  
- 32-16 = 16 host bits  
- Total IP addresses = 2^16 = 65536  
- Usable IPs = 65536 - 2 = 65534 hosts
- `/8`:  
- 32-8 = 24 host bits  
- Total IP addresses = 2^24 = 16,777,216  
- Usable IPs = 16,777,216 - 2 = 16,777,214 hosts

