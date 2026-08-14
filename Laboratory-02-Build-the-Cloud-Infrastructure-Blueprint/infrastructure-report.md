# Infrastructure Report

### Summary Table

| Item | Value |
|---|---|
| Operating System | Ubuntu 24.04.4 LTS (Noble Numbat) |
| Kernel Version | 6.8.0-136-generic |
| CPU Model | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| Number of CPU Cores | 1 |
| Total RAM | 1.9Gi |
| Disk Capacity | 19G (`/dev/vda1`, mounted at `/`) |
| Mounted File Systems | `/run`, `/`, `/dev/shm`, `/run/lock`, `/boot`, `/boot/efi` |
| Hostname | ubuntu |
| IP Address | 172.30.1.2 (enp1s0), 172.17.0.1 (docker0) |

### Commands

**Operating System**
Command used: `cat /etc/os-release`
The server is running Ubuntu 24.04.4 LTS, codenamed "Noble Numbat."

**Kernel Version**
Command used: `uname -r`
The kernel version is 6.8.0-136-generic.

**CPU Model and Core Count**
Command used: `lscpu`
The processor is an Intel Xeon E312xx (Sandy Bridge, IBRS update), reported with 1 CPU, 1 socket, 1 core per socket, and 1 thread per core, indicating a single virtual CPU.

**Total RAM**
Command used: `free -h`
Total memory available is 1.9Gi, with 420Mi used and 864Mi free at the time of inspection.

**Disk Capacity and Mounted File Systems**
Command used: `df -h`
The main disk (`/dev/vda1`) has a total capacity of 19G, with 5.4G used and 13G available (30% used), mounted at `/`. Other mounted filesystems include `/run`, `/dev/shm`, `/run/lock`, `/boot` (on `/dev/vda16`), and `/boot/efi` (on `/dev/vda15`).

**Hostname**
Command used: `hostname`
The hostname of the machine is `ubuntu`.

**IP Address**
Commands used: `ip a`, `hostname -I`
The machine has two network interfaces: `enp1s0` with IP address 172.30.1.2, and `docker0` with IP address 172.17.0.1.


