# Linux User Space vs. Kernel Space

Linux separates its operations into two distinct areas: **user space** and **kernel space**. This design enhances security, stability, and performance.

## Diagram

```plaintext
                +-------------------------------------------+
                |               User Space                |
                |-------------------------------------------|
                |  Applications, Libraries, Shells         |
                |  (word processors, browsers, etc.)        |
                +-------------------------------------------+
                              │
                              │   System Calls
                              ▼
                +-------------------------------------------+
                |             Kernel Space                |
                |            (System Space)               |
                |-------------------------------------------|
                |  Core Kernel, Device Drivers,             |
                |  Memory Management, Scheduling            |
                +-------------------------------------------+
                              │
                              │   Direct Hardware Access
                              ▼
                +--------------------------------------------+
                |                Hardware                  |
                |  (CPU, Memory, Storage, I/O Devices)        |
                +--------------------------------------------+
