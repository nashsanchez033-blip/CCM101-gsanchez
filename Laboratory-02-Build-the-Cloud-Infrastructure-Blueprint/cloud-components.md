# Cloud Infrastructure Components

## Checkpoint 3 – Identify Cloud Infrastructure Components

Based on the investigation of the Linux cloud server in KillerCoda, the following cloud infrastructure components were identified.

---

## 1. Compute Resources

### Example
- **CPU:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
- **CPU Cores:** 1
- **CPU Threads:** 1
- **CPU Speed:** 2.0 GHz
- **Architecture:** x86_64
- **Virtualization:** KVM

### Purpose

Compute resources provide the processing power needed to run applications, execute commands, process data, and perform tasks on the cloud server.

### Importance in Cloud Computing

Compute resources are important because cloud applications and services require processing power to operate. CPU resources allow servers to execute programs, handle requests, and perform different workloads. Cloud environments can provide virtualized CPU resources based on the requirements of the workload.

### Relation to the KillerCoda Linux Environment

The KillerCoda environment provides a virtual cloud server with an Intel Xeon E312xx processor and 1 CPU core. According to the investigation, the system is running under KVM full virtualization. The CPU and virtualization information was identified using the `lscpu` command.

---

## 2. Storage Resources

### Example
- **Main Disk:** 19 GiB
- **Used Storage:** 5.4 GiB
- **Available Storage:** 13 GiB
- **Boot Partition:** 881 MiB
- **EFI Partition:** 105 MiB
- **Main Mount Point:** `/`

### Purpose

Storage resources are used to store the operating system, applications, configuration files, user files, logs, and other data required by the cloud server.

### Importance in Cloud Computing

Storage is important because cloud servers need persistent space for operating system files, applications, databases, logs, and other information. Sufficient storage allows applications and services to operate properly and provides space for storing important data.

### Relation to the KillerCoda Linux Environment

The KillerCoda server has a 19 GiB main disk represented by `/dev/vda1` and mounted at `/`. The investigation also identified a `/boot` partition using `/dev/vda16` with a size of 881 MiB and an EFI partition using `/dev/vda15` with a size of 105 MiB. The `df -h` command was used to inspect the storage capacity and mounted file systems.

---

## 3. Networking Resources

### Example
- **Hostname:** ubuntu
- **Primary Network Interface:** enp1s0
- **Primary IP Address:** 172.30.1.2
- **Docker Network Interface:** docker0
- **Docker IP Address:** 172.17.0.1
- **Loopback Address:** 127.0.0.1

### Purpose

Networking resources allow the cloud server to communicate with other systems, services, applications, and networks. Network interfaces and IP addresses provide the connectivity needed for data to move between systems.

### Importance in Cloud Computing

Networking is important because cloud servers need to communicate with users, applications, databases, and other cloud resources. Network interfaces and IP addresses allow services to communicate within a network and enable cloud resources to interact with each other.

### Relation to the KillerCoda Linux Environment

The KillerCoda Linux server uses the `enp1s0` network interface as its primary network interface. It has the IP address `172.30.1.2`. The investigation also identified the `docker0` interface with the IP address `172.17.0.1`, which is used as a Docker bridge network. The loopback interface uses `127.0.0.1`.

The networking information was identified using the `ip a`, `hostname`, and `hostname -I` commands.

---

## 4. Operating System

### Example
- **Operating System:** Ubuntu 24.04.4 LTS
- **Codename:** Noble Numbat
- **Kernel:** 6.8.0-138-generic
- **Architecture:** x86_64

### Purpose

The operating system manages the server's hardware and software resources. It provides the environment needed to run applications, execute commands, manage files, configure networking, and control system processes.

### Importance in Cloud Computing

The operating system is important because cloud applications and services need an operating environment where they can run. It manages CPU, memory, storage, networking, users, processes, and other system resources.

### Relation to the KillerCoda Linux Environment

The KillerCoda cloud server runs Ubuntu 24.04.4 LTS, also known as Noble Numbat. The system uses the 6.8.0-138-generic Linux kernel and an x86_64 architecture. The operating system information was identified using the `cat /etc/os-release`, `uname -r`, and `uname -a` commands.

---

## Summary

| Cloud Component | KillerCoda Example | Purpose |
|---|---|---|
| Compute Resources | Intel Xeon E312xx, 1 CPU Core | Provides processing power |
| Storage Resources | 19 GiB Main Disk | Stores the OS, applications, and data |
| Networking Resources | 172.30.1.2, enp1s0 | Provides network communication |
| Operating System | Ubuntu 24.04.4 LTS | Manages hardware and software resources |

---

## Conclusion

The investigation of the KillerCoda Linux environment demonstrates the main components of cloud infrastructure. The server uses compute resources through an Intel Xeon E312xx processor with 1 CPU core, storage resources through a 19 GiB main disk, networking resources through the `enp1s0` network interface and IP address `172.30.1.2`, and Ubuntu 24.04.4 LTS as its operating system.

The investigation also confirmed that the cloud environment is running under KVM full virtualization. These components work together to provide a functional virtual cloud computing environment where applications, commands, and services can run.
