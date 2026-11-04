# 🧰 Open-Source Security Tools You Can Rely On

Every tool here is **open source**, **actively maintained** and **used by real security teams**.

**Difficulty:** 🟢 Beginner · 🟡 Intermediate · 🔴 Advanced

> ⚠️ Only run these against systems you own or have written permission to test.

## 🌐 Networking & Recon

| Tool | What it does | Level | Start here |
|---|---|---|---|
| [Wireshark](https://github.com/wireshark/wireshark) | Captures and inspects network traffic | 🟢 | [User guide](https://www.wireshark.org/docs/wsug_html_chunked/) |
| [Nmap](https://github.com/nmap/nmap) | Discovers hosts and open ports | 🟢 | [Reference guide](https://nmap.org/book/man.html) |
| [Zeek](https://github.com/zeek/zeek) | Turns network traffic into searchable logs | 🟡 | [Zeek docs](https://docs.zeek.org/) |
| [Suricata](https://github.com/OISF/suricata) | Detects threats in network traffic (IDS/IPS) | 🟡 | [Suricata docs](https://docs.suricata.io/) |

## 🔵 Detection & Monitoring (SIEM / XDR)

| Tool | What it does | Level | Start here |
|---|---|---|---|
| [Wazuh](https://github.com/wazuh/wazuh) | An all-in-one SIEM and XDR, and the best first SIEM for a home lab | 🟢 | [Quickstart](https://documentation.wazuh.com/current/quickstart.html) |
| [Security Onion](https://github.com/Security-Onion-Solutions/securityonion) | A full threat-hunting and monitoring platform | 🟡 | [Docs](https://docs.securityonion.net/) |
| [Sigma](https://github.com/SigmaHQ/sigma) | A shared detection-rule format that works with any SIEM | 🟡 | [Rule guide](https://github.com/SigmaHQ/sigma-specification) |
| [osquery](https://github.com/osquery/osquery) | Lets you query your endpoints using SQL | 🟡 | [osquery docs](https://osquery.readthedocs.io/en/latest/) |

## 🚨 Incident Response & Forensics

| Tool | What it does | Level | Start here |
|---|---|---|---|
| [CyberChef](https://github.com/gchq/CyberChef) | Decodes, encodes and analyses data in the browser | 🟢 | [Web app](https://gchq.github.io/CyberChef/) |
| [Velociraptor](https://github.com/Velocidex/velociraptor) | Collects forensic evidence from endpoints and hunts across them | 🟡 | [Docs](https://docs.velociraptor.app/) |
| [Volatility 3](https://github.com/volatilityfoundation/volatility3) | Analyses memory dumps | 🔴 | [Docs](https://volatility3.readthedocs.io/en/stable/) |
| [YARA](https://github.com/VirusTotal/yara) | Pattern-matches to find malware | 🟡 | [Writing rules](https://yara.readthedocs.io/en/stable/writingrules.html) |

## 🕸️ Web Application Security

| Tool | What it does | Level | Start here |
|---|---|---|---|
| [OWASP ZAP](https://github.com/zaproxy/zaproxy) | Scans web apps for vulnerabilities | 🟢 | [Getting started](https://www.zaproxy.org/getting-started/) |
| [OWASP Juice Shop](https://github.com/juice-shop/juice-shop) | A deliberately vulnerable app for practice | 🟢 | [Pwning OWASP Juice Shop](https://pwning.owasp-juice.shop/) |
| [Nuclei](https://github.com/projectdiscovery/nuclei) | A fast vulnerability scanner driven by templates | 🟡 | [Docs](https://docs.projectdiscovery.io/opensource/nuclei/overview) |

## ☁️ Cloud & Container Security

| Tool | What it does | Level | Start here |
|---|---|---|---|
| [Prowler](https://github.com/prowler-cloud/prowler) | Checks AWS, Azure and GCP security posture | 🟢 | [Docs](https://docs.prowler.com/introduction) |
| [Trivy](https://github.com/aquasecurity/trivy) | Scans containers, code and infrastructure as code for vulnerabilities | 🟢 | [Docs](https://trivy.dev/) |
| [Checkov](https://github.com/bridgecrewio/checkov) | Finds misconfigurations in Terraform and other IaC | 🟡 | [Docs](https://www.checkov.io/) |
| [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) | A deliberately vulnerable AWS lab | 🟡 | [README](https://github.com/RhinoSecurityLabs/cloudgoat#readme) |

## 🧪 Attack Simulation (for defenders)

| Tool | What it does | Level | Start here |
|---|---|---|---|
| [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team) | Small, safe tests mapped to MITRE ATT&CK techniques | 🟡 | [Getting started](https://github.com/redcanaryco/atomic-red-team/wiki) |
| [Caldera](https://github.com/apache/caldera) | An automated adversary emulation platform, originally built by MITRE | 🔴 | [Docs](https://caldera.readthedocs.io/en/latest/) |

---

**How tools get on this list:** open-source licence ✅ · updated in the last 12 months ✅ · clear README and docs ✅ · used in industry ✅

Want to suggest a tool? See [CONTRIBUTING.md](CONTRIBUTING.md).
