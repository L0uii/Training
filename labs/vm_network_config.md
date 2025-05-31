
* **Vagrant**
* **VirtualBox**
* **Alpine (lightweight Linux box)**
* **A lightweight Windows box (which isn't as light as Linux, but I’ll pick a relatively small one)**

---

## FOR WINDOWS

### 1️⃣ Install VirtualBox

* Go to:
  [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
* Download **Windows hosts** version.
* Install it (next-next-finish).

### 2️⃣ Install Vagrant

* Go to:
  [https://developer.hashicorp.com/vagrant/downloads](https://developer.hashicorp.com/vagrant/downloads)
* Download Windows version.
* Install it (next-next-finish).

### 3️⃣ Verify Install

Open **Command Prompt** or **PowerShell**:

```bash
vagrant --version #This shows if vagrant was properly installed
vboxmanage --version #This shows if virtualbox was properly installed
```

Both should output versions.

---

## FOR MACOS

### 1️⃣ Install VirtualBox

* Same link:
  [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
* Download **macOS hosts** version.
* Install it (might require allowing extensions in `System Settings > Privacy & Security`).

### 2️⃣ Install Vagrant

* Same link:
  [https://developer.hashicorp.com/vagrant/downloads](https://developer.hashicorp.com/vagrant/downloads)
* Download macOS version.
* Install it.

### 3️⃣ Verify Install

Open **Terminal**:

```bash
vagrant --version
vboxmanage --version
```

---

### 4️⃣ Install Alpine Linux Vagrant Box (Clean Config with Private Network)
## Step 1 — Create directory
```bash
mkdir alpine38
cd alpine38
```

## Step 2 — Create minimal Vagrantfile

Instead of using vagrant init, manually create a minimal Vagrantfile:

```bash
cat <<EOF > Vagrantfile
Vagrant.configure("2") do |config|
  config.vm.box = "generic/alpine38"
  config.vm.network "private_network", ip: "192.168.56.10"
end
EOF
```

### (On Windows, create the file manually by copying from Vagrant.configure to  ip: "192.168.56.10" or use PowerShell's Set-Content.)

## Step 3 — Bring up the VM
```bash
vagrant up
```

### Step 4 — Verify
**SSH into the VM**:

```bash
vagrant ssh
```

**From host, verify ping works**:

```bash
ping 192.168.56.10
```
✅ Done. You now have Alpine running with direct IP access from your host.

---

## 5️⃣ Spin up Lightweight Windows 11 VM
We're using the community-maintained gusztavvargadr/windows-11 box (version 2402.0.2503).

Create a directory:
```bash

mkdir win11lite
cd win11lite
```

Initialize **Vagrant with Windows 11 box**:
```bash

vagrant init gusztavvargadr/windows-11 --box-version 2402.0.2503
```

(Optional) **Pre-download the box**:
```bash
vagrant box add gusztavvargadr/windows-11 --box-version 2402.0.2503
```

**Start the VM**:
```bash
vagrant up
```

**Access the Windows VM**

**Use RDP client to connect to:**
```bash
127.0.0.1:3389
```

**Default credentials (usually)**:
```bash
vagrant / vagrant
```

## ⚠ You are responsible for Windows licensing after installation.

## 6️⃣ Vagrant Global Status
**List all Vagrant VMs**:

```bash
vagrant global-status
```

## 7️⃣ Shutdown / Destroy VMs
**Shutdown VM**:

```bash
vagrant halt
```

**Destroy VM**:

```bash
vagrant destroy
```