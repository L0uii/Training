

## 🌐 IP Addressing & Subnetting

Understanding how IP addressing and subnetting work is essential for designing, configuring, and troubleshooting networks.

---

### 📌 **IP Addressing Basics**

* **IPv4 Format**: Four octets separated by dots (e.g., `192.168.1.1`).
* **Each octet**: 8 bits → full IP = 32 bits.
* **Classes (historical)**:

  * Class A: `1.0.0.0 – 126.255.255.255`
  * Class B: `128.0.0.0 – 191.255.255.255`
  * Class C: `192.0.0.0 – 223.255.255.255`

#### 🔒 **Private IP Ranges (RFC 1918)**

| Range                         | CIDR  | Use                            |
| ----------------------------- | ----- | ------------------------------ |
| 10.0.0.0 – 10.255.255.255     | `/8`  | Large networks                 |
| 172.16.0.0 – 172.31.255.255   | `/12` | Medium networks                |
| 192.168.0.0 – 192.168.255.255 | `/16` | Small networks (home, offices) |

---

### 🔍 **Subnetting Overview**

Subnetting splits a large network into smaller logical segments to improve routing and security.

* **Subnet mask**: Defines the division between network and host bits.
* **CIDR notation**: e.g., `/24` = 255.255.255.0 = 256 IPs (254 usable).
* **Formula**: `2^(32 - subnet_bits) - 2 = usable IPs`
* **Example**:

  * `192.168.1.0/24` → Hosts from `192.168.1.1` to `192.168.1.254`
  * Network = `192.168.1.0`
  * Broadcast = `192.168.1.255`

---

### 🧠 **Use Cases**

* Allocate different subnets to departments or virtual networks.
* Reduce broadcast traffic.
* Isolate devices for security.

---

### 🔧 **Useful Commands**

#### Windows

```cmd
ipconfig /all
ping 8.8.8.8
tracert google.com
```

#### Linux/macOS

```bash
ip a
ping 8.8.8.8
traceroute google.com
```

