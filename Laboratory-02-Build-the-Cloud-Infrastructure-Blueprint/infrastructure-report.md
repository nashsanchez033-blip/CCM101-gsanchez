# Cloud Infrastructure Report

## Investigation Date
August 30, 2026

## Investigator
[Your Name]

---

## Server Specifications

### 1. Operating System
- **Distribution**: Ubuntu 24.04.4 LTS
- **Codename**: Noble Numbat
- **Kernel Version**: 6.8.0-138-generic
- **Architecture**: x86_64

---

### 2. Kernel Information
- **Version**: 6.8.0-138-generic
- **Build Date**: Fri Jul 31 22:41:49 UTC 2026

---

### 3. CPU Specifications
- **Model**: Intel Xeon E312xx (Sandy Bridge, IBRS update)
- **CPU Cores**: 1
- **Threads**: 1
- **Cache**: L1d=32 KiB, L1i=32 KiB, L2=4 MiB, L3=16 MiB
- **CPU Frequency**: 2.0 GHz

---

### 4. Memory (RAM)
- **Total RAM**: 1.9 GiB
- **Used RAM**: 418 MiB
- **Free RAM**: 822 MiB
- **Available RAM**: 1.4 GiB
- **Swap**: 1.0 GiB

---

### 5. Storage (Disk)
- **Main Disk**: 19 GiB (5.4 GiB used, 13 GiB available)
- **Boot Partition**: 881 MiB (117 MiB used, 703 MiB available)
- **EFI Partition**: 105 MiB (6.2 MiB used, 99 MiB available)

---

### 6. Mounted File Systems
- **tmpfs**: 191 MiB - `/run`
- **/dev/vda1**: 19 GiB - `/`
- **tmpfs**: 952 MiB - `/dev/shm`
- **tmpfs**: 5.0 MiB - `/run/lock`
- **/dev/vda16**: 881 MiB - `/boot`
- **/dev/vda15**: 105 MiB - `/boot/efi`

---

### 7. Network Configuration
- **Hostname**: ubuntu
- **Primary Network Interface**: enp1s0
- **Primary IP**: 172.30.1.2
- **Secondary IP**: 172.17.0.1 (Docker)

---

### 8. Virtualization
- **Hypervisor Vendor**: KVM
- **Virtualization Type**: Full

---

## Investigation Commands

The following commands were used to investigate the cloud server:

```bash
uname -a
uname -r
cat /etc/os-release
lscpu
free -h
df -h
hostname
ip a
hostname -I
