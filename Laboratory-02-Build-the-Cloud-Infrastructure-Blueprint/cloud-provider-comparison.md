# Cloud Infrastructure Components

## Checkpoint 3 – Identify Cloud Infrastructure Components

This document identifies the cloud infrastructure components found in the Linux environment provided by KillerCoda. The components are based on the observations and system information gathered during the server investigation.

---

## 1. Compute Resources

### Example
**Intel Xeon E312xx (Sandy Bridge, IBRS update)**

The Linux environment is provided with an Intel Xeon E312xx processor running at 2.0 GHz. The virtual server has 1 CPU core and 1 thread available.

### Purpose

Compute resources provide the processing power needed to run applications, execute Linux commands, manage services, and perform tasks on the cloud server.

### Importance in Cloud Computing

Compute resources are one of the main components of cloud computing because they allow users to run applications and workloads without needing to own and maintain physical servers. Cloud platforms can allocate CPU resources depending on the requirements of the workload.

### Relation to the KillerCoda Linux Environment

The KillerCoda environment provides a virtual Linux server with 1 CPU core. The CPU information was identified using the `lscpu` command.

---

## 2. Storage Resources

### Example
**/dev/vda1 – 19 GiB**

The main storage device of the Linux environment is `/dev/vda1`, which has a total capacity of 19 GiB. Approximately 5.4 GiB is used and 13 GiB is available.

Other storage partitions found include:

- `/dev/vda16` – 881 MiB mounted on `/boot`
- `/dev/vda15` – 105 MiB mounted on `/boot/efi`

### Purpose

Storage resources are used to store the operating system, applications, configuration files, user files, and other data required by the server.

### Importance in Cloud Computing

Storage is important in cloud computing because applications and operating systems need a place to store data. Cloud storage allows data to remain available to applications and users while providing scalable and manageable storage resources.

### Relation to the KillerCoda Linux Environment

The KillerCoda server provides a virtual disk that is represented by `/dev/vda1`. The disk capacity and usage were identified using the `df -h` command.

---

## 3. Networking Resources

### Example
**enp1s0 Network Interface – 172.30.1.2**

The primary network interface found in the Linux environment is `enp1s0`. It is assigned the IP address `172.30.1.2`.

A Docker bridge interface was also found:

- **Interface:** docker0
- **IP Address:** 172.17.0.1

### Purpose

Networking resources allow the cloud server to communicate with other systems, services, and networks. Network interfaces and IP addresses are used to identify and connect the server within a network.

### Importance in Cloud Computing

Networking is essential in cloud computing because cloud servers need to communicate with users, applications, databases, and other cloud resources. Proper networking enables connectivity, service access, and communication between different systems.

### Relation to the KillerCoda Linux Environment

The KillerCoda Linux environment uses the `enp1s0` interface for its primary network connection. The IP address `172.30.1.2` was identified using the `ip a` and `hostname -I` commands. The environment also contains a Docker bridge network with the IP address `172.17.0.1`.

---

## 4. Operating System

### Example
**Ubuntu 24.04.4 LTS (Noble Numbat)**

The cloud server is running Ubuntu 24.04.4 LTS, also known as Noble Numbat. The system uses the Linux kernel version `6.8.0-138-generic` and an x86_64 architecture.

### Purpose

The operating system manages the computer's hardware and software resources. It provides the environment where applications, commands, services, and other processes can run.

### Importance in Cloud Computing

The operating system is important in cloud computing because it provides the software environment needed to operate and manage virtual servers. It allows administrators and users to interact with computing, storage, networking, and application resources.

### Relation to the KillerCoda Linux Environment

KillerCoda provides an Ubuntu 24.04.4 LTS Linux environment that can be accessed through a terminal. The operating system information was identified using the following commands:

```bash
cat /etc/os-release
uname -r
uname -a
