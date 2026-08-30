# CCM101 – Cloud Computing Laboratory

#  Welcome to the Cloud

## Mission Overview

This laboratory activity focused on investigating a Linux-based cloud environment using the KillerCoda terminal. The investigation involved checking the operating system, kernel, CPU, memory, storage, hostname, network interfaces, and IP addresses available in the virtual server.

The investigation showed that the environment is running Ubuntu 24.04.4 LTS with the Linux kernel version 6.8.0-138-generic. The server is a virtualized environment using KVM and provides basic computing, memory, storage, and networking resources that can be observed directly through Linux commands.

---

# Objectives

The objectives of this laboratory activity were:

- Investigate the Linux environment provided by KillerCoda.
- Identify the operating system installed on the server.
- Determine the Linux kernel version.
- Identify the CPU model and available CPU resources.
- Determine the total available RAM and swap memory.
- Check the available disk capacity and mounted file systems.
- Identify the hostname of the server.
- Examine the network interfaces and IP addresses.
- Identify the major cloud infrastructure components present in the environment.
- Compare basic infrastructure services offered by major cloud providers.
- Document the investigation using Markdown.

---

# Cloud Infrastructure Components

The investigation of the KillerCoda server identified several infrastructure components.

## 1. Compute Resource

The CPU information obtained using `lscpu` showed the following:

- **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
- **CPU(s):** 1
- **CPU Core(s):** 1
- **Thread(s) per Core:** 1
- **CPU Speed:** 2.0 GHz
- **Architecture:** x86_64
- **Hypervisor:** KVM
- **Virtualization Type:** Full

The CPU provides the processing capability used by the Linux server to execute commands and run processes. The investigation also confirmed that the server is running in a KVM virtualized environment.

---

## 2. Memory Resource

The `free -h` command showed:

| Memory | Amount |
|---|---:|
| Total RAM | 1.9 GiB |
| Used RAM | 418 MiB |
| Free RAM | 822 MiB |
| Available RAM | 1.4 GiB |
| Total Swap | 1.0 GiB |
| Used Swap | 0 B |

RAM provides temporary working space for the operating system and running processes. The available memory allows the virtual server to execute commands and operate its services.

---

## 3. Storage Resource

The `df -h` command identified the following mounted file systems:

| Filesystem | Size | Used | Available | Mounted On |
|---|---:|---:|---:|---|
| `/dev/vda1` | 19G | 5.4G | 13G | `/` |
| `/dev/vda16` | 881M | 117M | 703M | `/boot` |
| `/dev/vda15` | 105M | 6.2M | 99M | `/boot/efi` |

The main file system is `/dev/vda1`, with a total capacity of 19 GB. Storage is used by the operating system and for keeping files required by the Linux environment.

---

## 4. Networking Resource

The networking investigation using `ip a` showed three network interfaces:

| Interface | IP Address | Description |
|---|---|---|
| `lo` | 127.0.0.1 | Loopback interface |
| `enp1s0` | 172.30.1.2 | Main network interface |
| `docker0` | 172.17.0.1 | Docker bridge interface |

The hostname of the server was identified as:

**ubuntu**

The primary IP address reported by the investigation was:

**172.30.1.2**

The `hostname -I` command also showed:

**172.17.0.1**

Networking allows the Linux server and its services to communicate through the available network interfaces.

---

## 5. Operating System

The `/etc/os-release` file identified the operating system as:

- **Operating System:** Ubuntu 24.04.4 LTS
- **Codename:** Noble Numbat
- **Kernel:** 6.8.0-138-generic
- **Architecture:** x86_64

The operating system provides the environment in which the server commands and processes are executed.

---

# Tools Used

The following tools and utilities were used during the investigation:

## KillerCoda

KillerCoda provided the virtual Linux server environment used for the laboratory activity.

## Linux Terminal

The terminal was the main environment used to investigate the server and execute Linux commands.

## Linux System Utilities

The following built-in Linux utilities were used to gather information:

- `uname`
- `cat`
- `lscpu`
- `free`
- `df`
- `hostname`
- `ip`

## Markdown

Markdown was used to organize and document the results of the investigation.

---

# Linux Commands Executed

The following commands were executed during the investigation.

## System and Kernel Information

```bash
uname -a
