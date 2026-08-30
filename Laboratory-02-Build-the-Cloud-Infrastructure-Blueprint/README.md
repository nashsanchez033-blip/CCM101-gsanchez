# CCM101 – Cloud Computing Laboratory

## Technical Documentation

This README documents the activities, observations, and skills developed while investigating and working with a Linux-based cloud environment using KillerCoda.

---

# Mission Overview

This laboratory activity introduced the basic concepts and practical aspects of cloud infrastructure. The activities involved accessing a Linux cloud server, investigating its system resources, identifying important cloud infrastructure components, researching major cloud providers, and designing a simple cloud architecture.

The laboratory used the KillerCoda Linux environment to provide hands-on experience with a virtualized cloud server. Through the different checkpoints, the server's operating system, compute resources, memory, storage, networking configuration, and virtualization environment were examined and documented.

The activity also introduced Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP) and compared their equivalent infrastructure services.

---

# Objectives

The main objectives of this laboratory activity were:

- Understand the basic concepts of cloud computing infrastructure.
- Access and investigate a Linux-based cloud environment.
- Identify the operating system and Linux kernel version.
- Examine CPU, memory, storage, and networking resources.
- Identify examples of compute, storage, networking, and operating system components.
- Compare equivalent services offered by AWS, Microsoft Azure, and Google Cloud.
- Understand how different cloud infrastructure components work together.
- Create a simple cloud infrastructure architecture diagram.
- Practice documenting technical information using Markdown.
- Develop basic Linux command-line and cloud infrastructure skills.

---

# Cloud Infrastructure Components

The following major cloud infrastructure components were identified during the laboratory activities.

## 1. Compute Resources

The KillerCoda server uses an **Intel Xeon E312xx** processor with **1 CPU core and 1 thread**. The CPU information also showed that the environment is running under **KVM full virtualization**.

Compute resources provide the processing power required to execute commands, run applications, and handle workloads on a cloud server.

---

## 2. Storage Resources

The main storage device identified was **`/dev/vda1`**, with a capacity of approximately **19 GiB**.

The investigation also identified:

- `/dev/vda16` – 881 MiB mounted on `/boot`
- `/dev/vda15` – 105 MiB mounted on `/boot/efi`

Storage resources are responsible for keeping the operating system, applications, configuration files, and other data.

---

## 3. Networking Resources

The primary network interface identified was **`enp1s0`**, which was assigned the IP address:

`172.30.1.2`

The investigation also identified a Docker bridge interface:

`docker0` – `172.17.0.1`

The hostname of the server was:

`ubuntu`

Networking resources allow the cloud server to communicate with other systems and services.

---

## 4. Operating System

The server is running:

**Ubuntu 24.04.4 LTS (Noble Numbat)**

The system uses:

- **Kernel:** 6.8.0-138-generic
- **Architecture:** x86_64

The operating system manages the server's hardware and software resources and provides the environment where applications, commands, and services can operate.

---

# Tools Used

The following tools were used during the laboratory activity:

### KillerCoda

KillerCoda was used to provide the Linux-based cloud server environment. It allowed the investigation and execution of Linux commands through a terminal.

### Linux Terminal

The terminal was used to inspect the operating system, CPU, memory, storage, hostname, network interfaces, and IP addresses.

### GitHub

GitHub was used to store and organize the laboratory documentation and related files in a cloud-based repository.

### Draw.io

Draw.io was used to design the simple cloud infrastructure architecture diagram created during the laboratory activity.

### Markdown

Markdown was used to create and format the technical documentation files such as:

- `README.md`
- `infrastructure-report.md`
- `cloud-components.md`
- `cloud-provider-comparison.md`

---

# Linux Commands Executed

The following Linux commands were executed during the investigation.

## System Information

```bash
uname -a
