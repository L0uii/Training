
## 🏡 Home Network Assignment Walkthrough

Design, document, and secure your own home network using real devices or a simulated environment.

---

### 🎯 Objective

Configure a secure network at home with static IPs, firewall rules, and proper segmentation where possible.

---

### 📦 Requirements

* 3 or more networked devices (PC, smartphone, printer, smart device)
* Home router (or emulator if simulating)
* Screenshot evidence + config summary

---

### 🛠️ Step-by-Step

#### 1️⃣ Map Your Devices

| Device     | Example IP   | Purpose     |
| ---------- | ------------ | ----------- |
| PC/Laptop  | 192.168.0.10 | Admin / Dev |
| Smartphone | 192.168.0.11 | Internet    |
| Smart TV   | 192.168.0.12 | Media       |

---

#### 2️⃣ Assign Static IPs

* Log into your router (typically 192.168.0.1)
* Find **DHCP settings** → **Static IP Mapping**
* Assign MAC address to a specific IP for each device

---

#### 3️⃣ Secure the Network

* **Change default admin credentials** on your router
* **Enable WPA2 or WPA3 encryption** on Wi-Fi
* **Disable WPS**
* **Restrict port forwarding** (disable unless needed)
* Enable **firewall** (built-in or external)
* Optional: Separate IoT devices on guest/VLAN network

---

#### 4️⃣ Test & Document

* Use `ping`, `tracert`, or `ipconfig` to confirm static IPs
* Take screenshots of:

  * Router admin interface (with MAC/IP bindings)
  * Device IP configuration screen
* Summarize security settings applied

---

### ✅ Submission Checklist

* [ ] IP address table for each device
* [ ] Screenshots of router config
* [ ] Security actions taken (in bullet points)
* [ ] Any tools used for testing

---

