# CCM101 – Cloud Computing Laboratory

## Laboratory 01 – Welcome to the Cloud

> **Cloud Infrastructure Investigation and Documentation**
>
> A hands-on exploration of a Linux-based virtual cloud environment using KillerCoda.

---

## Mission Overview

This laboratory activity served as an introduction to working with cloud infrastructure through a Linux-based virtual server. Instead of only studying cloud computing concepts theoretically, the activity provided an opportunity to investigate an actual running environment and identify the resources available to it.

The laboratory started with accessing a Linux cloud server through KillerCoda and continued with system investigation, infrastructure identification, cloud provider comparison, and basic cloud architecture design.

During the investigation, the server was identified as an **Ubuntu 24.04.4 LTS** environment running on **KVM virtualization**. The available compute, memory, storage, and networking resources were examined using Linux command-line tools.

The activities helped connect theoretical cloud computing concepts with the actual components found inside a virtual cloud environment.

---

# Objectives

The laboratory was completed with the following objectives:

- Access and navigate a Linux-based cloud environment.
- Create and manage files and directories using Linux commands.
- Investigate the operating system and Linux kernel.
- Identify the available CPU and memory resources.
- Examine disk capacity and mounted file systems.
- Identify the hostname, network interfaces, and IP addresses.
- Recognize compute, storage, networking, and operating system components.
- Compare equivalent infrastructure services from AWS, Microsoft Azure, and Google Cloud.
- Design a simple cloud infrastructure for a fictional company.
- Practice writing technical documentation using Markdown.
- Develop basic skills required for cloud infrastructure and system administration.

---

# Cloud Infrastructure Components

The investigation of the KillerCoda server revealed several important cloud infrastructure components.

## 1. Compute Resource

The virtual server is equipped with an:

**Intel Xeon E312xx (Sandy Bridge, IBRS update)**

The investigation showed:

- CPU Cores: **1**
- Threads: **1**
- Architecture: **x86_64**
- CPU Speed: **2.0 GHz**
- Hypervisor: **KVM**
- Virtualization Type: **Full**

The compute resource provides the processing power required to execute commands, run applications, and perform workloads on the virtual server.

---

## 2. Memory Resource

The server has:

- Total RAM: **1.9 GiB**
- Used RAM: **418 MiB**
- Free RAM: **822 MiB**
- Available RAM: **1.4 GiB**
- Swap: **1.0 GiB**

Memory allows the operating system and applications to temporarily store information while processes are running.

---

## 3. Storage Resource

The primary storage device is:

**`/dev/vda1` – 19 GiB**

Storage information from the investigation:

| Storage | Capacity | Used | Available | Mount Point |
|---|---:|---:|---:|---|
| `/dev/vda1` | 19 GiB | 5.4 GiB | 13 GiB | `/` |
| `/dev/vda16` | 881 MiB | 117 MiB | 703 MiB | `/boot` |
| `/dev/vda15` | 105 MiB | 6.2 MiB | 99 MiB | `/boot/efi` |

Storage is responsible for keeping the operating system, applications, configuration files, and other server data.

---

## 4. Networking Resource

The primary network interface identified during the investigation was:

**Interface:** `enp1s0`  
**Primary IP Address:** `172.30.1.2`

The server also contained:

| Interface | Address | Purpose |
|---|---|---|
| `enp1s0` | `172.30.1.2` | Primary network interface |
| `docker0` | `172.17.0.1` | Docker bridge network |
| `lo` | `127.0.0.1` | Local loopback interface |

The server hostname is:

**`ubuntu`**

Networking resources allow the cloud server to communicate with other systems, services, and networks.

---

## 5. Operating System

The cloud server runs:

**Ubuntu 24.04.4 LTS – Noble Numbat**

System details:

- Kernel: **6.8.0-138-generic**
- Architecture: **x86_64**
- Distribution: **Ubuntu**
- Version: **24.04.4 LTS**

The operating system manages the server's hardware and software resources and provides the environment where applications and services operate.

---

# Cloud Provider Comparison

During the laboratory, three major public cloud providers were examined:

- Amazon Web Services (AWS)
- Microsoft Azure
- Google Cloud Platform (GCP)

Although the providers use different product names, many of their services perform similar infrastructure functions.

| Infrastructure | AWS | Microsoft Azure | Google Cloud |
|---|---|---|---|
| **Compute** | Amazon EC2 | Azure Virtual Machines | Compute Engine |
| **Storage** | Amazon S3 | Azure Blob Storage | Cloud Storage |
| **Networking** | Amazon VPC | Azure Virtual Network | Google Cloud VPC |
| **IAM** | AWS IAM | Microsoft Entra ID + Azure RBAC | Google Cloud IAM |

### Key Observation

The biggest lesson from the comparison is that cloud providers may use different terminology for similar technologies.

For example:

> **Virtual Machine → EC2 → Azure VM → Compute Engine**

The product names change, but the basic concept remains the same: providing virtual computing resources that can run applications and workloads.

---

# Simple Cloud Architecture

A simple cloud infrastructure was designed for a fictional company named **TechNova Solutions**.

The architecture contains the following major components:

```text
                         INTERNET
                             |
                             |
                     Internet Connection
                             |
                             v
                    +----------------+
                    |      VPC       |
                    |  Virtual Cloud |
                    +-------+--------+
                            |
                     Public Subnet
                            |
             +--------------+--------------+
             |                             |
             v                             v
      +-------------+              +---------------+
      |   COMPUTE   |              |    STORAGE    |
      |   INSTANCE  |<------------>|  Object Data  |
      | Ubuntu 24.04|              |     / Files   |
      +------+------+              +---------------+
             |
             |
             v
           USER
      Web Application
