
## 🔍 Task 1: Scan Your Local Network for Open Ports

### 🎯 Objective

Learn to discover open ports on devices in your local network to understand your network's exposure and gain basic reconnaissance skills.

### 🛠️ Tools Required

* **[Nmap](https://nmap.org/)** – Port scanning tool (Free)
* **[Wireshark](https://www.wireshark.org/)** – Packet analyzer (Optional)

---

### 🧭 Step-by-Step Guide

1. **Install Nmap**

   * Download from the [official site](https://nmap.org/download.html) or install via terminal:

     * Linux: `sudo apt install nmap`
     * macOS: `brew install nmap`
     * Windows: Use the executable installer.

2. **Find Your Local IP Range**

   * Use the `ip a` (Linux/macOS) or `ipconfig` (Windows) command to find your local IP.
   * Example: If your IP is `192.168.182.134`, your subnet is likely `192.168.182.134/24`.

3. **Perform a TCP SYN Scan**

   ```bash
   nmap -sS 192.168.182.134/24
   ```

   * This scans all devices on the network for open TCP ports.

4. **Note IP Addresses & Open Ports**

   * Record all active hosts and the ports open on each.

5. **(Optional) Analyze Packets with Wireshark**

   * Capture network traffic during the scan and inspect SYN/ACK responses for more detail.

6. **Research Common Services**

   * Use resources like [Exploit-DB](https://www.exploit-db.com/) or [Shodan](https://www.shodan.io/) to understand what services run on the open ports (e.g., 22 = SSH, 80 = HTTP).

7. **Identify Potential Security Risks**

   * Look for unnecessary open ports or outdated services that may pose vulnerabilities.

8. **Save Scan Results**

   * As text:

     ```bash
     nmap -sS 192.168.182.134/24 -oN scan_results.txt
     ```
   

### ✅ Outcome

* Hands-on experience with **Nmap scanning**
* Understanding of open ports and exposed services
* Awareness of potential **security risks in your network**

