# PENETRATION-TESTING_REPORTS CyberSecurity_Networkwalks_WK02
CyberSecurity project covering footprinting, reconnaissance, and local network scanning using Kali Linux tools and Zenmap.
# 🔐 Penetration Testing Report
### Footprinting & Network Scanning Phases

**Week 02 | Cybersecurity Internship | NetworkWalks**

---

## 📌 Project Overview

This project documents the practical activities completed during Week 2 of my Cybersecurity and Ethical Hacking internship at NetworkWalks.

The project covers two main modules:

- **W2-PM1:** Footprinting and Reconnaissance using Multiple Kali Linux Tools.
- **W2-PM5:** Network Scanning and Host Discovery using Zenmap.

The purpose of these activities was to understand how publicly available information can be collected from a domain and how active devices can be identified within a local network.

All activities were performed within the authorized scope or on my own local network.

## 🎯 Objectives

The main objectives of this project are to:

- Understand the fundamentals of footprinting and reconnaissance.
- Collect publicly available domain registration information using WHOIS.
- Identify website technologies using WhatWeb.
- Perform DNS lookup using Nslookup.
- Inspect HTTP response headers using Curl.
- Identify Web Application Firewall technology using Wafw00f.
- Enumerate DNS records using DNSRecon.
- Identify local IP addresses and network subnets.
- Discover active hosts using Zenmap.
- Identify IP and MAC addresses of discovered devices.
- Generate a network topology.
- Document findings, potential risks, and recommendations.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Reconnaissance and footprinting environment |
| WHOIS | Domain registration information |
| WhatWeb | Website technology fingerprinting |
| Nslookup | DNS resolution |
| Curl | HTTP response header inspection |
| Wafw00f | Web Application Firewall detection |
| DNSRecon | DNS record enumeration |
| Zenmap | Network scanning and host discovery |
| Nmap | Network discovery engine |
| Windows CMD | Local IP and MAC identification |

## 📚 Modules Completed

### Module 1: W2-PM1 – Multiple Kali Tools

This module focused on footprinting and reconnaissance using six Kali Linux tools.

Activities included:

1. WHOIS domain information gathering.
2. Website technology identification using WhatWeb.
3. DNS resolution using Nslookup.
4. HTTP header inspection using Curl.
5. WAF detection using Wafw00f.
6. DNS enumeration using DNSRecon.

### Module 2: W2-PM5 – Zenmap Scanning

This module focused on local network discovery using Zenmap.

Activities included:

1. Identifying the local IP address using Windows CMD.
2. Identifying the local subnet.
3. Performing Ping Scan using Zenmap.
4. Discovering live hosts.
5. Identifying IP and MAC addresses.
6. Generating network topology.
7. Saving the topology in PDF format.

## ⚙️ Environment & Configuration

| Component | Configuration |
|---|---|
| Attacking OS | Kali Linux |
| Scanning OS | Windows |
| Footprinting Target | networkwalks.com |
| Scanning Tool | Zenmap / Nmap |
| Scan Type | Ping Scan |
| Example Network | 10.0.0.0/24 |
| Report | W2-PM-FINAL |
| Program | NetworkWalks |
| Batch | B084 |

## 🪜 Practical Activities & Procedures

### 1. Footprinting & Reconnaissance

The first activity involved gathering publicly available information about the `networkwalks.com` domain using multiple Kali Linux tools.

#### 1.1 WHOIS

**Purpose:** Obtain domain registration information, registrar details, registration dates, and name servers.

**Command:**

```bash
whois networkwalks.com
```

**Observation:**

The command returned publicly available domain registration information, including registrar and name server details.

#### 1.2 WhatWeb

**Purpose:** Identify technologies and services used by a website.

**Command:**

```bash
whatweb networkwalks.com
```

**Observation:**

The results identified WordPress 7.0.4 and WP Download Manager 3.3.58, along with additional website technology information.

#### 1.3 Nslookup

**Purpose:** Resolve a domain name into its corresponding IP address using DNS.

**Command:**

```bash
nslookup networkwalks.com
```

**Observation:**

The recorded result resolved the domain to:

`192.232.216.135`

#### 1.4 Curl

**Purpose:** Inspect HTTP response headers returned by a web server.

**Command:**

```bash
curl -I https://networkwalks.com
```

**Observation:**

The command returned HTTP response headers and exposed technical information, including the `/wp-json/` endpoint.

#### 1.5 Wafw00f

**Purpose:** Identify whether a Web Application Firewall protects a website.

**Command:**

```bash
wafw00f https://networkwalks.com
```

**Observation:**

The result identified ModSecurity (SpiderLabs) as the Web Application Firewall.

#### 1.6 DNSRecon

**Purpose:** Enumerate DNS records and collect information about the domain's DNS infrastructure.

**Command:**

```bash
dnsrecon -d networkwalks.com
```

**Observation:**

The activity involved collecting DNS-related information, including name servers, mail servers, SPF/TXT records, and service records.

## 🌐 2. Network Scanning with Zenmap

The second activity focused on discovering active devices within my own local network.

#### 2.1 Identify Local IP Configuration

First, Windows CMD was used to identify the local IP address and network configuration.

**Command:**

```cmd
ipconfig
```

This helped identify the local network subnet required for scanning.

#### 2.2 Perform Network Discovery

Zenmap was used to perform a Ping Scan against the example local subnet.

**Target:**

```text
10.0.0.0/24
```

**Profile:** Ping Scan

**Equivalent Nmap Command:**

```bash
nmap -sn 10.0.0.0/24
```

#### 2.3 Identify Live Hosts

The recorded example scan identified four live hosts:

| No. | IP Address |
|---|---|
| 1 | 10.0.0.1 |
| 2 | 10.0.0.4 |
| 3 | 10.0.0.5 |
| 4 | 10.0.0.19 |

The scan also returned MAC address information for the discovered hosts.

**Note:** These are the example results documented in the practical report. Actual local network results should be used when performing the exercise.

#### 2.4 Generate Network Topology

After completing the scan:

1. Open the Topology tab in Zenmap.
2. Enable the topology legend.
3. Review the discovered network hosts.
4. Save the network topology in PDF format.

This provided a visual representation of the discovered local network.

## 📸 Practical Screenshots & Evidence

The following screenshots provide evidence of the practical activities.

### W2-PM1: Footprinting & Reconnaissance

**1. WHOIS Domain Information**

![WHOIS Evidence](screenshots/01-whois.png)

**2. WhatWeb Technology Fingerprinting**

![WhatWeb Evidence](screenshots/02-whatweb.png)

**3. Nslookup DNS Resolution**

![Nslookup Evidence](screenshots/03-nslookup.png)

**4. Curl HTTP Response Headers**

![Curl Evidence](screenshots/04-curl.png)

**5. Wafw00f Detection**

![Wafw00f Evidence](screenshots/05-wafw00f.png)

### W2-PM5: Network Scanning

**6. Zenmap Network Discovery**

![Zenmap Evidence](screenshots/06-zenmap.png)

**7. Network Topology**

Add your exported Zenmap topology PDF or its screenshot here when available.

## ⚠️ 3. Risk Analysis & Impact

Based on the information collected during the exercises, the following potential risks were identified.

| No. | Finding | Potential Impact | Risk Level |
|---|---|---|---|
| 1 | Web technology information exposed | Helps identify software requiring security review | Medium |
| 2 | Server IP address identifiable | Provides information about web infrastructure | Low |
| 3 | HTTP technical information exposed | Assists technology fingerprinting | Low |
| 4 | WAF technology identifiable | Reveals information about security architecture | Low |
| 5 | DNS infrastructure information exposed | Helps build an infrastructure profile | Medium |
| 6 | Multiple live hosts visible | Unknown devices may require investigation | Medium |

**Important:** These are observations from footprinting and scanning, not confirmed vulnerabilities. No exploitation or vulnerability validation was performed during these two modules.

## 💡 4. Security Recommendations

Based on the observations, the following recommendations were identified:

1. **Review Publicly Exposed Technology Information:** Regularly review publicly visible website technologies and plugins.
2. **Keep Software Updated:** Maintain updated CMS platforms, plugins, and web technologies.
3. **Review HTTP Headers:** Check response headers for unnecessary technical information.
4. **Review DNS Records:** Periodically verify publicly exposed DNS information.
5. **Configure and Monitor WAF:** Keep ModSecurity enabled and properly configured.
6. **Perform Regular Network Discovery:** Identify active devices within internal networks.
7. **Investigate Unknown Devices:** Verify unexpected devices discovered during scanning.
8. **Maintain Network Documentation:** Keep network topology and device information updated.
9. **Perform Authorized Security Testing:** Ensure all testing activities remain within the approved scope.

## 📚 5. Key Learnings

Through these practical activities, I gained experience in:

- Domain footprinting and information gathering.
- Website technology fingerprinting.
- DNS resolution and enumeration.
- HTTP response header analysis.
- Web Application Firewall identification.
- Network scanning and host discovery.
- IP and MAC address identification.
- Network topology generation.
- Risk identification and security reporting.
- Ethical and authorized penetration testing practices.

## 📝 6. Conclusion

During Week 2 of my Cybersecurity and Ethical Hacking internship at NetworkWalks, I completed practical activities covering footprinting, reconnaissance, and network scanning.

Using multiple Kali Linux tools, I collected publicly available information about a domain and examined its web technologies, DNS information, HTTP headers, and WAF.

I also used Zenmap to discover active hosts within my local network, identify IP and MAC addresses, and generate a network topology.

These exercises helped me understand how information gathering and network discovery contribute to the initial stages of penetration testing.

I also learned the importance of documenting technical findings, analyzing potential risks, and performing security assessments only within an authorized scope.

## 🔐 7. Security & Ethical Disclaimer

All activities documented in this repository were performed within an authorized educational scope or on systems and networks owned by me.

The information is provided for educational and research purposes only.

Unauthorized scanning, access, or exploitation of systems is strictly prohibited.

## 🔗 8. Tools & Resources

- [Kali Linux](https://www.kali.org/get-kali/)
- [Nmap](https://nmap.org/)
- [Zenmap](https://nmap.org/zenmap/)
- [WHOIS](https://www.icann.org/resources/pages/whois-2018-01-17-en)
- [WhatWeb](https://github.com/urbanadventurer/WhatWeb)
- [Wafw00f](https://github.com/EnableSecurity/wafw00f)
- [DNSRecon](https://github.com/darkoperator/dnsrecon)

## 👤 Author

**Muhammad Farhan Iftikhar**

**CEH Certified | Cybersecurity Professional**

- Certification: Certified Ethical Hacker (CEH), EC-Council
- Batch: B084 – NetworkWalks
- Focus Areas: Cybersecurity, Penetration Testing, Network Security

**LinkedIn:** [M. Farhan Iftikhar](https://www.linkedin.com/in/m-farhan-iftikhar-7a7832322/)

## 📌 Project Information

- **Program:** Cybersecurity Program at NetworkWalks
- **Week:** 02
- **Modules:** W2-PM1 and W2-PM5
- **Project:** Footprinting & Network Scanning
- **Repository:** GitHub
