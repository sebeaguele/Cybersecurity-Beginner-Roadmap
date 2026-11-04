<h1 align="center">🛡️ Cybersecurity Beginner Roadmap</h1>
<p align="center"><b>Go from zero to job-ready in cybersecurity using free resources and open-source tools you can rely on.</b></p>

<p align="center">
  <img src="https://img.shields.io/badge/level-beginner-brightgreen?style=flat-square" alt="Beginner"/>
  <img src="https://img.shields.io/badge/cost-free--first-blue?style=flat-square" alt="Free-first"/>
  <img src="https://img.shields.io/badge/tools-open--source-orange?style=flat-square" alt="Open source"/>
  <img src="https://img.shields.io/badge/PRs-welcome-purple?style=flat-square" alt="PRs welcome"/>
</p>

---

## 👋 Who this is for

- You're **new to cybersecurity**, or switching from IT, development or a non-tech career
- You want a **clear weekly plan** rather than a list of 500 links
- You want to learn by **doing**, with tools that real security teams use

You don't need a degree or paid courses to start. You need about **1 to 2 hours a day** and a laptop.

## 🧭 How this roadmap works

```
 Foundations (Days 1–30)  ──►  Pick a path (Days 31–90)  ──►  Prove it (portfolio + cert)
                                 ├─ 🔵 Defensive (SOC, detection, incident response)
                                 └─ ☁️ Cloud & Identity
```

- Every week has **one outcome**. When you can do it, move on.
- 🆓 = free · 💲 = paid (optional) · 🧪 = hands-on lab
- Keep a **learning journal**, such as a GitHub repo or a blog. Hiring managers love seeing what you built.

---

## 🚀 The 30-Day Foundations Track

### Week 1: Build your lab and learn how computers talk
**Outcome:** You have a working home lab and can read network traffic.

| Day | Task | Resource |
|---|---|---|
| 1 | Install VirtualBox and create an Ubuntu VM | 🆓 [VirtualBox](https://www.virtualbox.org/) · [Ubuntu Desktop](https://ubuntu.com/download/desktop) |
| 2 | Learn the Linux basics: files, permissions and users | 🆓 [Linux Journey](https://labex.io/linuxjourney) |
| 3 | Practise the command line through a game | 🆓🧪 [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/) (levels 0–10) |
| 4 | Learn networking basics: IP, ports, DNS and TCP/UDP | 🆓 [Professor Messer Network+ videos](https://www.professormesser.com/) |
| 5 | Capture your own traffic and open a website while recording | 🆓🧪 [Wireshark](https://www.wireshark.org/) |
| 6 | Scan your own lab VM and see which ports are open | 🆓🧪 [Nmap](https://nmap.org/book/man.html) |
| 7 | **Journal:** Write up what you saw in Wireshark and Nmap | Your GitHub |

### Week 2: Core security concepts
**Outcome:** You can explain the CIA triad, common attacks and how they're defended.

| Day | Task | Resource |
|---|---|---|
| 8 | Learn the CIA triad, risk, threats and vulnerabilities | 🆓 [Professor Messer Security+ videos](https://www.professormesser.com/) |
| 9 | Learn about phishing, malware and social engineering | 🆓 Professor Messer Security+, threats section |
| 10 | Learn passwords, hashing and MFA, and why they matter | 🆓🧪 [CyberChef](https://gchq.github.io/CyberChef/), so you can hash and encode things yourself |
| 11 | Learn encryption basics: symmetric, asymmetric and TLS | 🆓 Professor Messer Security+, cryptography section |
| 12 | See how attackers operate | 🆓 [MITRE ATT&CK](https://attack.mitre.org/). Explore 5 techniques |
| 13 | Complete a beginner path | 🆓🧪 [TryHackMe: Pre Security](https://tryhackme.com/path/outline/presecurity) (free rooms) |
| 14 | **Journal:** Explain one ATT&CK technique in your own words | Your GitHub |

### Week 3: Logs, alerts and the blue-team mindset
**Outcome:** You can find suspicious activity in logs.

| Day | Task | Resource |
|---|---|---|
| 15 | Learn the Windows Event Logs that matter (4624, 4625, 4688) | 🆓 [Microsoft Docs: security auditing](https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-10/security/threat-protection/auditing/security-auditing-overview) |
| 16 | Read Linux logs with `journalctl` and `/var/log/auth.log` | 🆓🧪 Your Ubuntu VM |
| 17 | Learn what a SIEM is and install Wazuh in your lab | 🆓🧪 [Wazuh quickstart](https://documentation.wazuh.com/current/quickstart.html) |
| 18 | Trigger some failed logins and watch the alerts fire | 🆓🧪 Wazuh + your VM |
| 19 | Learn how detection rules are written | 🆓 [Sigma rules](https://github.com/SigmaHQ/sigma) |
| 20 | Investigate your first alert | 🆓🧪 [LetsDefend](https://letsdefend.io/) or [Blue Team Labs Online](https://blueteamlabs.online/) (free tiers) |
| 21 | **Journal:** Write up your Wazuh lab with screenshots | Your GitHub |

### Week 4: Web, cloud and AI security basics
**Outcome:** You understand the OWASP Top 10 and can spot basic cloud misconfigurations.

| Day | Task | Resource |
|---|---|---|
| 22 | Learn the OWASP Top 10 | 🆓 [OWASP Top 10](https://owasp.org/projects/top-ten) |
| 23 | Try SQL injection and XSS legally, in a lab | 🆓🧪 [PortSwigger Web Security Academy](https://portswigger.net/web-security) |
| 24 | Hack a deliberately vulnerable app | 🆓🧪 [OWASP Juice Shop](https://owasp.org/projects/juice-shop) |
| 25 | Learn the cloud shared responsibility model and IAM basics | 🆓 [AWS Skill Builder](https://skillbuilder.aws/) / [Microsoft Learn](https://learn.microsoft.com/en-us/training/) |
| 26 | Scan a cloud account for misconfigurations | 🆓🧪 [Prowler](https://github.com/prowler-cloud/prowler) (use a free-tier account) |
| 27 | Learn about AI security: prompt injection and the OWASP Top 10 for LLMs | 🆓 [OWASP GenAI Security Project](https://genai.owasp.org/) · 🧪 [Lakera Agent Breaker](https://play.lakera.ai/agent-breaker) |
| 28 | Scan a container image for vulnerabilities | 🆓🧪 [Trivy](https://github.com/aquasecurity/trivy) |
| 29–30 | **Capstone:** Publish a "30 Days of Cyber" summary repo and choose your path | Your GitHub + LinkedIn |

✅ **After Day 30:** you'll have a home lab, a working SIEM, hands-on writeups and a public portfolio.

---

## 🛤️ Days 31–90: Choose your path

### 🔵 Defensive path (SOC analyst, detection engineer, incident responder)
Focus: SIEM, detection rules, incident response and threat hunting.
- Practise on 🧪 [CyberDefenders](https://cyberdefenders.org/) and [Blue Team Labs Online](https://blueteamlabs.online/)
- Learn a query language: 🆓 [KQL on Microsoft Learn](https://learn.microsoft.com/en-us/kusto/query/)
- Run attacks against your lab and detect them: 🆓🧪 [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)
- Do endpoint forensics: 🆓🧪 [Velociraptor](https://github.com/Velocidex/velociraptor)
- 📅 *A detailed weekly plan is coming soon*

### ☁️ Cloud & Identity path (cloud security engineer, IAM engineer)
Focus: Cloud IAM, posture management, Zero Trust and infrastructure as code.
- Learn IAM deeply: 🆓 [Here-IAM 6-month plan](https://github.com/sebeaguele/Here-IAM)
- Scan infrastructure as code: 🆓🧪 [Checkov](https://github.com/bridgecrewio/checkov)
- Practise deliberately vulnerable cloud labs: 🆓🧪 [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat)
- 📅 *A detailed weekly plan is coming soon*

---

## 🎓 Beginner-friendly certifications (optional)

Certifications help you get past HR filters, but **projects get you hired**. Do these after you've built something.

| Cert | Good for | Notes |
|---|---|---|
| ISC2 Certified in Cybersecurity (CC) | Absolute beginners | ISC2 has offered free training and exam vouchers, so check their site for current offers |
| Google Cybersecurity Certificate | Career switchers | Self-paced, beginner-friendly |
| CompTIA Security+ | First security job | Widely requested in job ads 💲 |
| Blue Team Level 1 (BTL1) | SOC / defensive | Very hands-on 💲 |
| Microsoft SC-200 | SOC on Microsoft stack | KQL, Sentinel, Defender 💲 |

---

## 🧰 Open-source tools you can rely on

See **[TOOLS.md](TOOLS.md)** for a curated list of trusted, actively maintained, open-source security tools. Each one has its purpose, difficulty level and first steps.

## 🤝 Contributing

Found a broken link or a great free resource? See **[CONTRIBUTING.md](CONTRIBUTING.md)**. Links are checked automatically every week.

## ⚖️ Responsible use

Only test systems you **own** or have **written permission** to test. Every lab in this roadmap is legal and designed for practice.

---

<p align="center">Created by <a href="https://github.com/sebeaguele">Seb (cyberseb)</a> · <a href="https://twitter.com/cyberseb_">@cyberseb_</a> · ⭐ Star this repo if it helps you</p>
