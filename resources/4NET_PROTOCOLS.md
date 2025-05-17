
## 🔗 Network Protocols

Network protocols define the rules and formats for data exchange over a network. Below are some of the most important ones for IT professionals.

---

### 🌐 **HTTP / HTTPS**

* **HyperText Transfer Protocol** (Port 80)
* **HTTPS** (Port 443): Encrypted using TLS/SSL.
* Used by web browsers and APIs to request and serve content.

> 🛡️ Always use HTTPS to ensure confidentiality and data integrity.

---

### 🔐 **SSH (Secure Shell)**

* **Port 22**
* Secure remote login and command execution over encrypted channels.
* Replaces insecure protocols like Telnet.

#### Example usage:

```bash
ssh user@192.168.1.10
```

> ✅ Common for server management, file transfers (via SCP or SFTP), tunneling.

---

### 📁 **FTP (File Transfer Protocol)**

* **Ports 20/21**
* Used for transferring files between systems.
* Lacks encryption by default – not secure.

> ❗ Use **SFTP** (SSH File Transfer Protocol) or **FTPS** (FTP over SSL/TLS) for secure alternatives.

---

### 🌍 **DNS (Domain Name System)**

* **Port 53**
* Translates human-readable domains into IP addresses.
* e.g., `google.com` → `142.250.190.14`

#### Test DNS resolution:

```bash
nslookup github.com
dig github.com
```

> 📌 Critical for almost all internet-based communications.

---

### 🧰 **Other Useful Protocols (Mention-Worthy)**

| Protocol | Port  | Purpose                       |
| -------: | ----- | ----------------------------- |
|     DHCP | 67/68 | Dynamic IP address assignment |
|     ICMP | N/A   | Ping, traceroute diagnostics  |
|      NTP | 123   | Network time synchronization  |

---

> 🔧 Mastering these protocols helps in debugging, securing, and optimizing networks.

---

