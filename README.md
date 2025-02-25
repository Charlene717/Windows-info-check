# Windows Guide for Checking Hardware and Network Information

This guide compiles methods to quickly check **IP addresses (internal and external)**, **hardware information (system and resources)**, **graphics card (GPU)**, and **hard drives (HDD/SSD)** on Windows systems. It is useful for basic system diagnostics and configuration.

## What are Internal and External Networks?
- **Internal IP** (Local IP): The IP address assigned within a **Local Area Network (LAN)** by a router or DHCP server, typically starting with `192.168.x.x` or `10.x.x.x`, visible only within the same network.
- **External IP** (Public IP): The IP address assigned to a device for accessing the **Internet**, usually provided by an Internet Service Provider (ISP), allowing global network identification.

---

## 1. Checking IP Addresses

### 1.1 Checking Internal IP (Local Network)
In **Command Prompt (CMD)** or **PowerShell**, enter:
```powershell
ipconfig
```
This command will display detailed network information, including:
- **IPv4 Address** (Local IP)
- **Subnet Mask**
- **Default Gateway (Router IP)**

### 1.2 Checking External IP (Public Network)
In **PowerShell** or **CMD**, enter:
```powershell
curl ifconfig.me
```
Alternatively, visit [ifconfig.me](https://ifconfig.me) in a browser to retrieve the **public IP**.

---

## 2. Checking Hardware Information
Windows includes a built-in **System Information tool (msinfo32)** to view detailed hardware and software information.

### Steps:
1. Press <kbd>Win + R</kbd> to open the "Run" dialog.
2. Type:
   ```
   msinfo32
   ```
3. Press <kbd>Enter</kbd> to open the **System Information** window.

This tool provides:
- **System Summary** (Processor, Memory, OS Version)
- **Hardware Resources** (IRQ, Memory Usage)
- **Components** (Graphics Card, Disk, Network Devices)
- **Software Environment** (Drivers, System Services)

---

## 3. Checking Graphics Card (GPU)
1. Right-click the "Start" button or press <kbd>Win + X</kbd> → Select **"Device Manager"**.
2. Expand **"Display adapters"**, where the GPU name and model will be listed.

---

## 4. Checking Hard Drive (HDD/SSD)
1. Right-click the "Start" button → Select **"Disk Management"**.
2. View all installed drives, partitions, unallocated space, and health status.
3. To differentiate HDD from SSD:
   - Check the **model name** and search for specifications.
   - Use third-party tools like **CrystalDiskInfo** for detailed analysis.

---

## Summary
| Query | Method |
|----------|----------|
| **Internal IP** | `ipconfig` |
| **External IP** | `curl ifconfig.me` or visit ifconfig.me |
| **Hardware Information** | <kbd>Win + R</kbd> → `msinfo32` |
| **Graphics Card** | Device Manager → "Display adapters" |
| **Hard Drive Information** | Disk Management to view installed disks |

By following these steps, you can quickly obtain **network locations** and **hardware specifications** on Windows, making it easier for system diagnostics and maintenance.
