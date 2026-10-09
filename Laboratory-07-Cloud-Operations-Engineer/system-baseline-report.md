# System Baseline Report

## Host System Information

This report documents the baseline health of the Ubuntu server before deploying and monitoring the client website container.

## Memory Usage

Command executed:

```bash
free -h
```

* Total RAM: **1.9 GiB**
* Used RAM: **419 MiB**
* Free RAM: **1.1 GiB**
* Available RAM: **1.4 GiB**

## Root Disk Storage

Command executed:

```bash
df -h /
```

* Root filesystem: **/dev/vda1**
* Total storage capacity: **19G**
* Used storage: **5.5G**
* Available storage: **13G**
* Disk usage: **30%**
* Mount point: **/**

## Why Disk Space Monitoring Is Important

Checking available disk space before a major traffic surge is important because insufficient storage can prevent applications from writing logs, saving data, or operating reliably.
