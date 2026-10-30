# Experiment 7: OSINT Reconnaissance Using Google Dorking and Shodan

## 1. Objective

To perform Open-Source Intelligence (OSINT) reconnaissance using Google search operators and Shodan to find publicly available information and identify exposed services.

## 2. Procedure

### Step 1: Perform Domain-Based Reconnaissance Using Google

Open Google and search using `site:gov.in` to find publicly indexed pages from government websites.

**Search Query:**
```text
site:gov.in
```

**Screenshot:**

![Step 1 - Google Domain Search](https://github.com/2024A7R025/Offensive-Defensive-Security-Lab/raw/main/Experiment-7-OSINT-Recon/images/Ss1.png.jpeg)

### Step 2: Search for Publicly Accessible Directories

Enter `intitle:"index of"` in Google to find pages that may display directory listings.

**Search Query:**
```text
intitle:"index of"
```

**Screenshot:**

![Step 2 - Directory Search](https://github.com/2024A7R025/Offensive-Defensive-Security-Lab/raw/main/Experiment-7-OSINT-Recon/images/Ss2.png.jpeg)

### Step 3: Find Cybersecurity-Related PDF Documents

Use Google search operators to find PDF documents related to cybersecurity.

**Search Query:**
```text
inurl:cybersecurity filetype:pdf
```

**Screenshot:**

![Step 3 - PDF Search](https://github.com/2024A7R025/Offensive-Defensive-Security-Lab/raw/main/Experiment-7-OSINT-Recon/images/Ss3.png.jpeg)

### Step 4: Search for Login-Related Pages

Enter `inurl:login` in Google to find web pages containing login in their URLs.

**Search Query:**
```text
inurl:login
```

**Screenshot:**

![Step 4 - Login Page Search](https://github.com/2024A7R025/Offensive-Defensive-Security-Lab/raw/main/Experiment-7-OSINT-Recon/images/Ss4.png.jpeg)

### Step 5: Examine Google's Cache Operator

Search for `cache:google.com` and observe the result. Google's public Cache feature has been discontinued.

**Search Query:**
```text
cache:google.com
```

**Screenshot:**

![Step 5 - Google Cache](https://github.com/2024A7R025/Offensive-Defensive-Security-Lab/raw/main/Experiment-7-OSINT-Recon/images/Ss5.png.jpeg)

### Step 6: Identify Internet-Facing Services Using Shodan

Open Shodan and search for `apache` to find publicly visible hosts reporting Apache web-server services.

**Search Query:**
```text
apache
```

Observe IP addresses, server banners, and service information.

**Screenshot:**

![Step 6 - Shodan Apache Search](https://github.com/2024A7R025/Offensive-Defensive-Security-Lab/raw/main/Experiment-7-OSINT-Recon/images/Ss6.png.jpeg)

### Step 7: Search for Services on a Specific Port in India

Enter the query in Shodan to filter publicly visible hosts associated with port 23 in India.

**Search Query:**
```text
port:23 country:"IN"
```

Port 23 is commonly used by Telnet.

**Screenshot:**

![Step 7 - Shodan Port Search](https://github.com/2024A7R025/Offensive-Defensive-Security-Lab/raw/main/Experiment-7-OSINT-Recon/images/Ss7.png.jpeg)

### Step 8: Perform Hostname-Based Reconnaissance

Enter the hostname filter in Shodan to search for hosts matching the government domain.

**Search Query:**
```text
hostname:gov.in
```

Observe the available host and service information.

**Screenshot:**

![Step 8 - Shodan Hostname Search](https://github.com/2024A7R025/Offensive-Defensive-Security-Lab/raw/main/Experiment-7-OSINT-Recon/images/Ss8.png.jpeg)

## 3. Result

The experiment demonstrated OSINT reconnaissance using Google Dorking and Shodan. Google was used to find publicly indexed information, while Shodan helped identify internet-facing services and filter hosts by port, country, and hostname. This experiment highlighted the importance of identifying and securing publicly exposed information and services.
