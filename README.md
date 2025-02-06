# Best Practices for Working on a Windows-Based Workstation

## Table of Contents
- [Introduction](#introduction)
- [Understanding Your Hardware](#understanding-your-hardware)
  - [CPU (Central Processing Unit)](#cpu-central-processing-unit)
  - [GPU (Graphics Processing Unit)](#gpu-graphics-processing-unit)
  - [RAM (Random Access Memory)](#ram-random-access-memory)
  - [Storage (SSD vs HDD)](#storage-ssd-vs-hdd)
- [File Management](#file-management)
  - [Avoid Saving Files on the C: Drive](#avoid-saving-files-on-the-c-drive)
  - [Use a Dedicated Storage Drive](#use-a-dedicated-storage-drive)
  - [Cloud Storage and Backups](#cloud-storage-and-backups)
- [Performance Optimization](#performance-optimization)
  - [Close Unused Programs](#close-unused-programs)
  - [Clean Out Temporary Files](#clean-out-temporary-files)
  - [Keep Software Updated](#keep-software-updated)
- [Network Shares](#network-shares)
- [Conclusion](#conclusion)

## Introduction
This document provides **best practices** for efficiently using Windows-based workstations in the IRSS. These practices help ensure smooth operation and prevent conflicts with IT.

---

## Understanding Your Hardware

### CPU (Central Processing Unit)
The CPU is the **brain of your computer**, responsible for executing instructions and performing calculations. Higher **clock speeds** (GHz) and more **cores** improve performance in computationally intensive tasks. More cores allow for parallel processing, enabling multiple computations to run simultaneously.

### GPU (Graphics Processing Unit)
A GPU is uniquely designed for **parallel processing** and is essential for tasks such as **machine learning, simulations, and graphics rendering**. Utilizing the GPU is crucial for complex mathematical computations, such as deep learning, but it must be balanced with graphics rendering based on GPU allocation.

### RAM (Random Access Memory)
RAM provides **temporary storage** for running programs. The more RAM available, the more applications and processes can run simultaneously **without performance slowdowns**.

### Storage (SSD vs HDD)
- **SSD (Solid State Drive):** Faster read/write speeds, significantly improving system performance.
- **HDD (Hard Disk Drive):** Higher capacity at a lower cost but slower than SSDs.

**Recommendation:** Use an **SSD for system files** and an **HDD for long-term storage** of large datasets (if available).

---

## File Management

### Avoid Saving Files on the C: Drive
- The **C:\ drive** is primarily for the **Windows operating system and essential software**.
- Storing large files here can lead to **slow performance and system instability**.
- Avoid having your cloud storage (OneDrive, Sync) save to your C:\ drive.

### Use a Dedicated Storage Drive
- Save research data and models on a **separate partition** (e.g., **D:\ or E:\ drive**).
- This prevents data loss in case of system failure or OS reinstallation.

### Cloud Storage and Backups
- Always **back up** important files to a **cloud service** (e.g., OneDrive, Sync).
- Store **local backups** on an external drive separate from your working system.
- Maintain a **consistent backup schedule** to prevent data loss.
- IRSS provides a **network share** for backing up and sharing data (more details below).

---

## Performance Optimization

### Close Unused Programs
- Running multiple background applications **consumes RAM and CPU resources**.
- Use **Task Manager (Ctrl + Shift + Esc)** to monitor and close unnecessary processes.
- Excessive GIF usage in Slack consumes GPU resources, slowing down GPU-based processing. If this is an issue, disable animations in Slack:
  - **File > Accessibility > Animation > Uncheck 'Automatically play animations in Slack'**

### Clean Out Temporary Files
- Empty the **Recycle Bin** regularly, preferably before restarting your computer.
- Clear the **temporary files folder**:
  - **Search `%tmp%` > Select All (Ctrl + A) > Delete**.
  - Some files may be in use or cannot be deleted—skip them when prompted.

### Keep Software Updated
- Install updates for **Windows, drivers, and essential software** (often handled by IT).
- Updates include **performance improvements and security patches**. Ensure you update when possible to avoid forced restarts.

---

## Network Shares
IRSS provides access to **network shares** (**ByUser** and **ByProject**) for data backup and sharing. However, note the following:
- These shares are **not secure**, meaning anyone in the lab can access stored data.
- **Do not store personal or sensitive information** (e.g., passport numbers, student information).
- These shares are meant for **storage, not active processing**. Copy data to a local machine before performing any computations.

---

## Conclusion
By following these best practices, you can ensure your workstation runs efficiently and remains secure while handling large-scale **data analysis and modeling tasks**.

For specific issues, contact IT via the ticketing system: [forestry.ithelp@ubc.ca](mailto:forestry.ithelp@ubc.ca)
