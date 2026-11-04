# 🔵 Defensive Path: Days 31–90

**Goal:** Go from "I know the basics" to **SOC-analyst ready**. By Day 90 you'll have a home SOC lab, your own detection rules, an incident report and a portfolio to show employers.

**Before you start:** finish the [30-Day Foundations Track](../README.md#-the-30-day-foundations-track). You should have a Wazuh lab running.

🆓 = free · 💲 = paid (optional) · 🧪 = hands-on lab

---

## 🗺️ Overview

| Week | Days | Focus | Outcome |
|---|---|---|---|
| 5 | 31–37 | Endpoint visibility | Windows VM with Sysmon feeding your SIEM |
| 6 | 38–44 | Query languages | You can hunt with KQL and search logs fast |
| 7 | 45–51 | Detection engineering | You've written and tested 3 Sigma rules |
| 8 | 52–58 | Network detection | You can spot malicious traffic in a PCAP |
| 9 | 59–65 | Incident response | You can run an investigation end to end |
| 10 | 66–72 | Endpoint forensics | You can collect and analyse evidence |
| 11 | 73–79 | Threat hunting & intel | You've run a hypothesis-driven hunt |
| 12 | 80–86 | Phishing & malware triage | You can triage a suspicious email safely |
| 🏁 | 87–90 | Capstone | Portfolio, CV and interview prep |

---

## Week 5: Endpoint visibility
**Outcome:** You have a Windows VM sending detailed logs to your SIEM.

| Day | Task | Resource |
|---|---|---|
| 31 | Create a Windows VM in your lab | 🆓 [Windows evaluation images](https://www.microsoft.com/en-us/evalcenter/) |
| 32 | Install the Wazuh agent on Windows | 🆓🧪 [Wazuh agent install](https://documentation.wazuh.com/current/installation-guide/wazuh-agent/index.html) |
| 33 | Learn what Sysmon is and why defenders love it | 🆓 [Sysmon (Microsoft Sysinternals)](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon) |
| 34 | Install Sysmon with a community config | 🆓🧪 [sysmon-modular](https://github.com/olafhartong/sysmon-modular) |
| 35 | Forward Sysmon events to Wazuh | 🆓🧪 Wazuh docs, "Sysmon" section |
| 36 | Run some normal activity, then find the events in your SIEM | 🧪 Your lab |
| 37 | **Journal:** Draw your lab diagram (endpoint → agent → SIEM) | 🆓 [draw.io](https://www.drawio.com/) |

## Week 6: Query languages
**Outcome:** You can search large volumes of logs quickly with KQL.

| Day | Task | Resource |
|---|---|---|
| 38 | Learn KQL basics: `where`, `project` and `summarize` | 🆓 [KQL on Microsoft Learn](https://learn.microsoft.com/en-us/kusto/query/) |
| 39–41 | Play a free KQL investigation game | 🆓🧪 [KC7 Cyber](https://kc7cyber.com/) |
| 42 | Practise in a free, real KQL environment | 🆓🧪 [Azure Data Explorer free cluster](https://learn.microsoft.com/en-us/azure/data-explorer/start-for-free) |
| 43 | Build a "failed logins by user" query and an alert in Wazuh | 🧪 Your lab |
| 44 | **Journal:** Publish your 5 most useful queries | Your GitHub |

## Week 7: Detection engineering
**Outcome:** You've written, tested and documented 3 detection rules.

| Day | Task | Resource |
|---|---|---|
| 45 | Learn the Sigma rule format | 🆓 [SigmaHQ](https://github.com/SigmaHQ/sigma) |
| 46 | Convert Sigma rules to your SIEM's query language | 🆓🧪 [sigma-cli](https://github.com/SigmaHQ/sigma-cli) |
| 47 | Map detections to ATT&CK techniques | 🆓 [ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) |
| 48 | Simulate an attack on your Windows VM | 🆓🧪 [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team) |
| 49–50 | Write 3 Sigma rules that catch your simulations, then tune out the false positives | 🧪 Your lab |
| 51 | **Journal:** Create a `detections/` repo with your rules plus test notes | Your GitHub |

## Week 8: Network detection
**Outcome:** You can open a PCAP and find the bad traffic.

| Day | Task | Resource |
|---|---|---|
| 52 | Learn what Zeek logs tell you (conn, dns, http) | 🆓 [Zeek docs](https://docs.zeek.org/) |
| 53 | Learn how Suricata IDS rules work | 🆓 [Suricata docs](https://docs.suricata.io/) |
| 54–55 | Install Security Onion in your lab (allow 16 GB+ of RAM) | 🆓🧪 [Security Onion](https://docs.securityonion.net/) |
| 56–57 | Analyse real malware-traffic exercises | 🆓🧪 [malware-traffic-analysis.net](https://www.malware-traffic-analysis.net/training-exercises.html) |
| 58 | **Journal:** Write up one PCAP investigation | Your GitHub |

> ⚠️ Treat files from malware-traffic-analysis.net as **live malware**. Open them only in an isolated VM.

## Week 9: Incident response
**Outcome:** You can run an investigation from alert to report.

| Day | Task | Resource |
|---|---|---|
| 59 | Learn the IR lifecycle | 🆓 [NIST SP 800-61 Rev. 3](https://csrc.nist.gov/pubs/sp/800/61/r3/final) |
| 60 | Study real IR playbooks | 🆓 [CISA incident response playbooks](https://www.cisa.gov/resources-tools/resources/federal-government-cybersecurity-incident-and-vulnerability-response-playbooks) |
| 61–63 | Complete 3 blue-team investigations | 🆓🧪 [CyberDefenders](https://cyberdefenders.org/) / [Blue Team Labs Online](https://blueteamlabs.online/) |
| 64 | Write an incident report: timeline, impact, root cause, lessons learned | 🧪 Use one of your investigations |
| 65 | **Journal:** Publish your incident report template | Your GitHub |

## Week 10: Endpoint forensics
**Outcome:** You can collect evidence from an endpoint and build a timeline.

| Day | Task | Resource |
|---|---|---|
| 66 | Learn the forensic artefacts that matter: prefetch, shimcache, event logs, browser history | 🆓 [SANS DFIR posters](https://www.sans.org/posters/) |
| 67–68 | Install Velociraptor and collect artefacts from your Windows VM | 🆓🧪 [Velociraptor](https://docs.velociraptor.app/) |
| 69 | Parse artefacts with free forensic tools | 🆓🧪 [Eric Zimmerman's tools](https://ericzimmerman.github.io/) |
| 70 | Learn memory forensics basics | 🆓🧪 [Volatility 3](https://github.com/volatilityfoundation/volatility3) |
| 71 | Build a timeline of a simulated attack | 🧪 Your lab |
| 72 | **Journal:** Write up your forensic timeline | Your GitHub |

## Week 11: Threat hunting & intel
**Outcome:** You've run a hypothesis-driven hunt and documented it.

| Day | Task | Resource |
|---|---|---|
| 73 | Learn the threat-hunting loop: hypothesis → hunt → findings → detection | 🆓 [ThreatHunter-Playbook](https://github.com/OTRF/ThreatHunter-Playbook) |
| 74 | Read a real threat report and pull out the TTPs | 🆓 [The DFIR Report](https://thedfirreport.com/) |
| 75 | Map those TTPs to ATT&CK | 🆓 ATT&CK Navigator |
| 76–77 | Hunt for one of those TTPs in your lab data | 🧪 Your lab |
| 78 | Turn your hunt into a detection rule | 🧪 Sigma |
| 79 | **Journal:** Publish your hunt write-up | Your GitHub |

## Week 12: Phishing & malware triage
**Outcome:** You can triage a suspicious email and attachment safely.

| Day | Task | Resource |
|---|---|---|
| 80 | Read email headers: SPF, DKIM, DMARC and spoofing signs | 🆓 [MXToolbox header analyser](https://mxtoolbox.com/EmailHeaders.aspx) |
| 81 | Extract and defang IOCs | 🆓🧪 [CyberChef](https://gchq.github.io/CyberChef/) |
| 82 | Check IOCs against threat intel | 🆓 [VirusTotal](https://www.virustotal.com/) · [AbuseIPDB](https://www.abuseipdb.com/) |
| 83 | Detonate a sample in a public sandbox and read the report | 🆓🧪 [ANY.RUN](https://any.run/) (free plan) |
| 84–85 | Complete phishing-analysis challenges | 🆓🧪 Blue Team Labs Online / CyberDefenders |
| 86 | **Journal:** Write a phishing triage checklist | Your GitHub |

> ⚠️ Never upload sensitive or company emails to public sandboxes. Their results are public.

---

## 🏁 Days 87–90: Capstone

1. **Portfolio README:** Link your lab diagram, `detections/` repo, incident report, forensic timeline and hunt write-up
2. **CV:** List your home SOC lab as experience, with tools and outcomes (e.g. "Wrote 3 Sigma detections tested with Atomic Red Team")
3. **Interview prep:** Practise explaining one investigation end to end in 3 minutes
4. **Optional certifications:** 💲 [BTL1 by Centri](https://www.centri.org/certifications/blue-team-level-1/) (hands-on; Centri was formerly Security Blue Team) or 💲 [SC-200](https://learn.microsoft.com/en-us/credentials/certifications/security-operations-analyst/) (Microsoft SOC)

✅ **After Day 90:** you can say "I built a SOC, wrote detections and investigated incidents", and prove it.

---

⬅️ [Back to the roadmap](../README.md) · ☁️ [Cloud & Identity path](CLOUD-IDENTITY.md)
