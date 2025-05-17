

## 🧪 Lab Walkthrough: Building a Virtual Lab Environment

This lab gives you a sandboxed environment to experiment with operating systems, networking, and cloud tools without affecting your main system.

---

### 🔧 Tools Needed

* **VirtualBox** (Free) or **VMware Workstation Player**
* **Linux ISO** (Ubuntu/Debian recommended)
* **Windows ISO** (e.g., Windows 10 Evaluation)
* At least **8GB RAM** and **30GB+ disk space** on your host machine

---

### 🧱 Lab Setup Steps

#### 1️⃣ Install Virtualization Software

* [Download VirtualBox](https://www.virtualbox.org/)




---

#### 2️⃣ Create VMs

* **Linux VM**:

  * Name: `LinuxLab`
  * Memory: 2048MB
  * Disk: 20GB (Dynamically allocated)
  * ISO: Ubuntu or Debian
* **Windows VM**:

  * Name: `WinLab`
  * Memory: 4096MB
  * Disk: 30GB
  * ISO: Windows 10

---

#### 3️⃣ Configure Virtual Network

Use **Host-Only** or **Internal Network** mode for VM-to-VM communication.

**Linux VM Static IP Example**:

```bash
sudo nano /etc/netplan/01-netcfg.yaml
```

```yaml
network:
  version: 2
  ethernets:
    enp0s3:
      dhcp4: no
      addresses: [192.168.56.101/24]
      gateway4: 192.168.56.1
      nameservers:
        addresses: [8.8.8.8, 1.1.1.1]
```

```bash
sudo netplan apply
```

---

#### 4️⃣ Enable SSH & RDP

* **Linux VM**:

  ```bash
  sudo apt update && sudo apt install openssh-server
  sudo systemctl enable ssh
  sudo systemctl start ssh
  ```

* **Windows VM**:

  * Enable **Remote Desktop**
  * Allow port 3389 through firewall

---

#### 5️⃣ Test Connectivity

From Linux:

```bash
ping 192.168.56.102  # Windows VM IP
ssh user@192.168.56.102
```

From Windows:

```powershell
ping 192.168.56.101  # Linux VM IP
```

---

### ✅ Success Criteria

* Both VMs can ping each other
* SSH from host to Linux VM works
* RDP from host to Windows VM works
* Internet access is optional (depending on NAT config)

---

Let me know if you want to go over the **Home Network Assignment Walkthrough** next or add screenshots and diagrams for this lab.
