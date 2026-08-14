# Laboratory 2: Build the Cloud Infrastructure Blueprint

## Mission Overview

This lab put me in the role of a newly onboarded cloud engineer tasked with investigating and documenting cloud infrastructure fundamentals. Using a Linux server running in the KillerCoda playground, I explored what actually makes up a cloud environment, compute, storage, networking, and the operating system, then connected those observations to how real providers like AWS, Azure, and GCP structure their services. The end goal was to produce documentation clear enough that someone else could read it and understand exactly what was investigated and why it matters.

## Objectives

- Investigate a Linux server's hardware and software specs using command-line tools
- Identify and categorize the core components of cloud infrastructure
- Compare equivalent services across AWS, Azure, and Google Cloud Platform
- Design a simple cloud architecture diagram
- Produce organized, properly formatted Markdown documentation
- Build a structured, professional GitHub repository through meaningful commits

## Cloud Infrastructure Components

A full breakdown is available in `cloud-components.md`, but the short version:

- **Compute** is the CPU and RAM that actually run everything, this VM had a single virtual CPU and 1.9Gi of RAM.
- **Storage** is where data persists, this environment had a 19G disk split across several mount points.
- **Networking** connects the machine to everything else, identified through its hostname and IP address.
- **Operating System** manages the hardware underneath and provides the foundation everything else runs on, in this case Ubuntu 24.04.4 LTS.

## Tools Used

- KillerCoda Playground (Ubuntu 24.04 environment)
- Linux terminal
- GitHub (repository hosting and version control)
- Mermaid.js (cloud architecture diagram)
- Markdown (all documentation)

## Linux Commands Executed

- `cat /etc/os-release` — identified the operating system
- `uname -r` — identified the kernel version
- `lscpu` — identified the CPU model and core count
- `free -h` — identified total RAM
- `df -h` — identified disk capacity and mounted filesystems
- `hostname` — identified the hostname
- `ip a` / `hostname -I` — identified the IP address

## Skills Learned

Going into this lab, I hadn't spent much time in a raw Linux terminal, by the end I was comfortable pulling real system information straight from the command line instead of relying on a GUI. I also got a much clearer picture of how cloud infrastructure concepts map to actual hardware and software, rather than just abstract definitions. On the GitHub side, I learned how file and folder creation works through the web interface, including how to structure a repository the way a real engineering team would, with meaningful commits instead of one giant upload at the end.

## Challenges Encountered

The biggest challenge honestly wasn't the Linux side, it was GitHub. Creating folders through the web interface isn't obvious at first, typing a folder name without the trailing filename just creates an empty file instead of an actual folder, and I ran into that more than once. Once I understood the `foldername/filename.md` pattern, everything else moved a lot faster. Interpreting raw command output and turning it into something readable also took a bit of trial and error, especially figuring out which numbers actually mattered versus which were just noise.
