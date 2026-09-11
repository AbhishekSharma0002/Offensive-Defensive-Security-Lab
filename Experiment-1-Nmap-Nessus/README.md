# Experiment 01 – Scanning for Vulnerabilities in a Network using Nmap and Nessus

## Objective

To identify active hosts, open ports, and running services in a network using Nmap and to detect known vulnerabilities using Nessus.

## Requirements

- Kali Linux
- Metasploitable 2
- VirtualBox
- Nmap
- Nessus

## Theory

Nmap is a network scanning tool used to discover active hosts, open ports, running services, and operating system information on a network.

Nessus is a vulnerability assessment tool used to identify known vulnerabilities, security weaknesses, and potential risks present in a system or network.

Together, Nmap and Nessus help in understanding the security status of a network in a controlled environment.

## Procedure

### 1. Check IP Address and Connectivity

First, check the IP address of the Kali Linux system and verify connectivity with the target machine.

```bash
ifconfig
```

To test connectivity with the target:

```bash
ping <target-ip>
```

---

### 2. Discover Active Hosts

Use Nmap to identify active hosts available in the network.

```bash
nmap -sn 192.168.56.0/24
```

The `-sn` option performs host discovery without performing a port scan.

---

### 3. Scan Open Ports

Perform a TCP SYN scan to identify open ports on the target system.

```bash
nmap -sS <target-ip>
```

The `-sS` option performs a TCP SYN scan and helps identify open TCP ports.

---

### 4. Detect Services and Operating System

Use Nmap to identify the services running on the target and determine the operating system.

```bash
nmap -sV -O <target-ip>
```

Here:

- `-sV` is used for service and version detection.
- `-O` is used for operating system detection.

---

### 5. Save Scan Results

The scan results can be saved into a text file for future analysis and documentation.

```bash
nmap -sV -O <target-ip> -oN nmap-scan-results.txt
```

The `-oN` option saves the output in normal text format.

---

### 6. Install Nessus

Install Nessus in Kali Linux using the downloaded Nessus package.

```bash
sudo dpkg -i <nessus-package.deb>
```

After installation, start the Nessus service:

```bash
sudo systemctl start nessusd
```

---

### 7. Start Nessus Service

Make sure that the Nessus service is running.

```bash
sudo systemctl start nessusd
```

The Nessus web interface can then be accessed through the browser.

---

### 8. Open Nessus

Open a web browser in Kali Linux and enter:

```text
https://localhost:8834
```

Log in to the Nessus interface using the configured credentials.

---

### 9. Create a New Scan

In the Nessus interface:

1. Click **New Scan**.
2. Select **Basic Network Scan**.
3. Enter a suitable scan name.
4. Enter the target IP address.
5. Save the scan.
6. Launch the scan.

Nessus will begin checking the target for possible vulnerabilities.

---

### 10. Run the Scan

After launching the scan:

1. Wait for Nessus to complete the scanning process.
2. Nessus checks the target system and its available services.
3. The scan identifies possible security weaknesses.
4. Open the completed scan to view the detailed results.

---

### 11. Review the Results

After the scan is completed, review the vulnerabilities reported by Nessus.

The vulnerabilities are generally categorized as:

- **Critical**
- **High**
- **Medium**
- **Low**
- **Informational**

These categories help determine the severity and priority of the identified security issues.

## Result

The target network was successfully scanned using Nmap and Nessus. Nmap identified active hosts, open ports, running services, and operating system information. Nessus was then used to identify and categorize the vulnerabilities present on the target system.

## Discussion

Nmap provides useful information about the network by discovering active hosts, open ports, services, and operating systems. This information helps in understanding the exposed attack surface of a system.

Nessus performs a more detailed vulnerability assessment by checking the target for known security weaknesses. The results are classified according to their severity, making it easier to identify which vulnerabilities should be addressed first.

Using both tools together provides a better understanding of the security condition of a network in a controlled laboratory environment.

## Conclusion

The experiment successfully demonstrated network scanning and vulnerability assessment using Nmap and Nessus. Nmap was used to discover hosts, ports, services, and operating system details, while Nessus was used to identify and classify vulnerabilities according to their severity.

This experiment helped in understanding the importance of network reconnaissance, vulnerability identification, and security assessment in a controlled environment.
