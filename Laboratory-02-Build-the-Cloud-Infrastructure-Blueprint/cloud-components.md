# Cloud Infrastructure Components

This document breaks down the four core categories of cloud infrastructure and connects each one to what I actually found while investigating the KillerCoda Ubuntu environment.

## Compute Resources

### Purpose
Compute resources are the CPU and RAM that do the actual work, running programs, processing requests, executing code. Nothing happens without compute.

### Why It Matters in Cloud Computing
Compute is basically the product cloud providers are selling. Businesses don't want to buy and maintain physical servers, so they rent compute power instead and scale it up or down depending on how much traffic or workload they're dealing with. This is the whole reason "the cloud" makes sense as a business model in the first place.

### In the KillerCoda Environment
Running `lscpu` showed a single virtual CPU (Intel Xeon E312xx, Sandy Bridge), and `free -h` showed 1.9Gi of RAM. That's not a lot of horsepower, but it's a real example of a compute resource, small-scale, but functionally the same thing an AWS EC2 instance or Azure VM provides on a much bigger level.

## Storage Resources

### Purpose
Storage is where data actually lives, the OS files, logs, user data, all of it, persisting even after the machine restarts or shuts down.

### Why It Matters in Cloud Computing
Companies need somewhere reliable to keep their data, and they need that storage to grow without having to physically install a new hard drive every time they run low on space. Cloud storage solves that by letting you resize on demand.

### In the KillerCoda Environment
Running `df -h` showed a 19G disk on `/dev/vda1`, split across mount points like `/`, `/boot`, and `/boot/efi`. Even in a small VM like this, you can see the same logic real cloud storage uses, dividing storage into partitions with specific jobs.

## Networking Resources

### Purpose
Networking is what connects a machine to everything else, other servers, the internet, and end users trying to reach it.

### Why It Matters in Cloud Computing
Without networking, a cloud server is useless, it would just sit there completely unreachable. Networking is what actually lets applications get delivered to real people, and it's what lets different parts of a system (like a web server and a database) talk to each other.

### In the KillerCoda Environment
Running `hostname` and `ip a` showed this machine's hostname (ubuntu) and its network interfaces, including an IP address of 172.30.1.2 on the primary interface. That's the machine's identity on the network, the exact same concept behind how cloud providers assign IPs to every VM they spin up.

## Operating System

### Purpose
The operating system manages the hardware underneath and gives every other piece of software a place to actually run.

### Why It Matters in Cloud Computing
The OS you pick affects what software will run, how security updates get handled, and how efficiently the hardware gets used. This is exactly why cloud providers let you choose your OS image before launching a server, it's not a minor detail, it shapes everything else you do afterward.

### In the KillerCoda Environment
Running `cat /etc/os-release` and `uname -r` confirmed this machine is running Ubuntu 24.04.4 LTS with kernel version 6.8.0-136-generic. Everything else I found, the compute specs, the storage layout, the network config, is all sitting on top of this OS layer. It's the foundation the rest of the system depends on.
