# 🏗️ Security Engineering Path: Advanced

**Goal:** Go from "I can use security tools" to **"I can design, build and defend a system"**. You'll take one small app and secure it end to end: code, identity, cloud, pipeline and detections.

**Before you start:** finish the [Defensive](DEFENSIVE.md) or [Cloud & Identity](CLOUD-IDENTITY.md) path, or have equivalent experience. You should be comfortable with Linux, Git, Docker and one scripting language.

🆓 = free · 💲 = paid (optional) · 🧪 = hands-on lab · 💸 = can cost money if you forget to clean up

---

## 🧭 How to use this path

1. **Pick your app.** Build or fork a small web app with a **login, two user roles, a database, an API and a file upload**. You'll secure this same app in every stage.
2. **Start each stage with the skip test.** If you can answer all the questions out loud without searching, go straight to the stage project.
3. **For each topic:** learn, do the task, then check "Done when". If you can't show it, you're not done.
4. **Keep your evidence** in a repo called `security-engineering-portfolio`, with one folder per stage.
5. **Track progress** by pasting the [checklist](#-progress-tracker) into a GitHub issue in your repo, where you can tick the boxes.

| Stage | Focus | Topics | You'll produce |
|---|---|---|---|
| 1 | [Core security and systems](#-stage-1-core-security-and-systems) | 1–7 | A threat model |
| 2 | [Web, API and AI security](#-stage-2-web-api-and-ai-security) | 8–15 | A find-and-fix report |
| 3 | [Identity, access and secrets](#-stage-3-identity-access-and-secrets) | 16–23 | An access design |
| 4 | [Cloud and infrastructure](#%EF%B8%8F-stage-4-cloud-and-infrastructure) | 24–31 | A hardened deployment |
| 5 | [Detection, response and secure delivery](#-stage-5-detection-response-and-secure-delivery) | 32–40 | A guarded pipeline and an incident report |

⏱️ Go at your own pace. At 1–2 hours a day, allow roughly 2–3 weeks per stage.

> ⚠️ Only test systems you own or have written permission to test. 💸 Set a cloud budget alert before Stage 4 and delete lab resources when you finish.

---

## 🧱 Stage 1: Core security and systems

**Skip test:** What happens, step by step, when you open an HTTPS site? Why is hashing not encryption? Where is a trust boundary in your app?

| # | Topic | 🧪 Do this | ✅ Done when | Learn |
|---|---|---|---|---|
| 1 | Networking: TCP, UDP, HTTP, TLS, DNS | Capture one visit to your app over HTTPS | You can label the DNS lookup, TCP handshake and TLS handshake | [Wireshark user guide](https://www.wireshark.org/docs/wsug_html_chunked/) |
| 2 | OS internals and permissions | Create a low-privilege user to run your app | The app runs without root and can only write where it must | [Linux Journey](https://labex.io/linuxjourney) |
| 3 | Processes, threads and privilege boundaries | Inspect your app's processes, user IDs and capabilities | You can explain what an attacker gains if that process is taken over | [capabilities man page](https://man7.org/linux/man-pages/man7/capabilities.7.html) |
| 4 | Cryptography: hashing, encryption, signatures | Hash, encrypt and sign a file with OpenSSL | You can say which one gives integrity, secrecy or proof of origin | [Cryptographic Storage](https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html) |
| 5 | Threat modelling and trust boundaries | Draw a data-flow diagram of your app | Every arrow crossing a boundary has at least one listed threat | [OWASP Threat Dragon](https://owasp.org/www-project-threat-dragon/) |
| 6 | Secure design principles | Review your design for least privilege and defence in depth | You've listed 3 weak points and a fix for each | [Secure Product Design](https://cheatsheetseries.owasp.org/cheatsheets/Secure_Product_Design_Cheat_Sheet.html) |
| 7 | Security models: CIA triad, STRIDE, kill chain | Apply STRIDE to your diagram and map one attack to ATT&CK | Each threat has a category, a priority and a mitigation | [MITRE ATT&CK](https://attack.mitre.org/) |

**🏁 Stage project:** `01-threat-model/` with your diagram, a STRIDE table and your top 5 risks.

---

## 🌐 Stage 2: Web, API and AI security

**Skip test:** How do XSS and CSRF differ? How would you stop user A reading user B's record? Why is a JWT not secret by default?

> For each topic: **attack it in a lab, then check and fix it in your own app.**

| # | Topic | 🧪 Do this | ✅ Done when | Learn |
|---|---|---|---|---|
| 8 | XSS, SQL injection, CSRF, SSRF | Solve one lab for each | You've explained the root cause and fix for all four | [Web Security Academy](https://portswigger.net/web-security) 🆓🧪 |
| 9 | Input validation and output encoding | Add server-side validation and context-aware encoding | Your earlier injection payloads fail in your app | [Input Validation](https://cheatsheetseries.owasp.org/cheatsheets/Input_Validation_Cheat_Sheet.html) |
| 10 | Sessions and cookies | Set `Secure`, `HttpOnly` and `SameSite`; expire sessions | Logging out makes the old session unusable | [Session Management](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) |
| 11 | API authentication: keys, OAuth 2.0, JWT | Protect an endpoint with short-lived tokens | Expired, altered and wrong-audience tokens are rejected | [OAuth 2.0](https://oauth.net/2/) · [JWT labs](https://portswigger.net/web-security/jwt) |
| 12 | Broken access control and object-level authorisation | Try to read and change another user's data | Automated tests prove cross-user requests are denied | [API Security Top 10](https://owasp.org/www-project-api-security/) |
| 13 | Rate limiting and abuse prevention | Limit your login and most expensive endpoints | A burst of requests is throttled and logged | [Denial of Service](https://cheatsheetseries.owasp.org/cheatsheets/Denial_of_Service_Cheat_Sheet.html) |
| 14 | File uploads and deserialisation | Restrict type, size, name and storage location | A script disguised as an image cannot run | [File Upload](https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html) · [Deserialization](https://cheatsheetseries.owasp.org/cheatsheets/Deserialization_Cheat_Sheet.html) |
| 15 | AI and LLM application security | Attempt prompt injection in a lab | You can explain why model output and tool access need limits | [OWASP GenAI Security](https://genai.owasp.org/) |

**🏁 Stage project:** `02-appsec/` with 5 findings: steps to reproduce (in your own lab), impact, fix and a test that proves the fix.

---

## 🔑 Stage 3: Identity, access and secrets

**Skip test:** Why are passkeys phishing-resistant? When would you pick ABAC over RBAC? How should one service prove its identity to another?

| # | Topic | 🧪 Do this | ✅ Done when | Learn |
|---|---|---|---|---|
| 16 | Authentication factors and strong MFA | Add passkeys or TOTP to your app | You can rank SMS, TOTP, push and passkeys, and say why | [NIST SP 800-63B](https://pages.nist.gov/800-63-4/sp800-63b.html) · [Passkeys](https://fidoalliance.org/passkeys/) |
| 17 | Password storage and credential stuffing | Use a slow, salted password hash and block breached passwords | No password is stored or logged in readable form | [Password Storage](https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html) |
| 18 | Single sign-on flows | Connect your app to Keycloak using OpenID Connect | You can draw the authorisation code flow with PKCE | [Keycloak](https://www.keycloak.org/getting-started/getting-started-docker) |
| 19 | RBAC and ABAC | Write a permission matrix and enforce it in one place | Anything not explicitly allowed is denied | [Authorization](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html) |
| 20 | Service accounts and workload identity | Replace a long-lived CI cloud key with OIDC federation 💸 | Your pipeline deploys with no stored cloud key | [GitHub OIDC](https://docs.github.com/en/actions/concepts/security/openid-connect) |
| 21 | Least privilege and just-in-time access | Design a request, approve and expire flow for admin access | No one has standing admin rights in your design | [IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) |
| 22 | Secrets management and rotation | Move secrets into a vault, then rotate one | A secret scan is clean and rotation causes no outage | [Secrets Management](https://cheatsheetseries.owasp.org/cheatsheets/Secrets_Management_Cheat_Sheet.html) · [Gitleaks](https://github.com/gitleaks/gitleaks) |
| 23 | Delegation, impersonation and session hijacking | Add audit logs for "act as user" and token revocation | You can trace who really did an action and cut off a stolen session | [ATT&CK: Steal Web Session Cookie](https://attack.mitre.org/techniques/T1539/) |

**🏁 Stage project:** `03-identity/` with your login flow diagram, permission matrix and secret rotation runbook.

---

## ☁️ Stage 4: Cloud and infrastructure

**Skip test:** What should never be reachable from the internet? How does a storage bucket become public? What stops a compromised container reaching everything else?

| # | Topic | 🧪 Do this | ✅ Done when | Learn |
|---|---|---|---|---|
| 24 | Network segmentation and private connectivity | Put your database in a private subnet 💸 | The database has no route from the internet | [VPC security](https://docs.aws.amazon.com/vpc/latest/userguide/security.html) |
| 25 | Security groups, firewalls and WAF | Allow only required ports; add basic WAF rules 💸 | A port scan shows only what you intended | [AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html) |
| 26 | Storage security | Block public access, encrypt and log your file storage | Anonymous requests fail | [S3 security best practices](https://docs.aws.amazon.com/AmazonS3/latest/userguide/security-best-practices.html) |
| 27 | Containers and Kubernetes: namespaces, RBAC | Run your app as non-root in a local cluster | A pod's service account can only do what the app needs | [kind](https://kind.sigs.k8s.io/) · [Kubernetes RBAC](https://kubernetes.io/docs/reference/access-authn-authz/rbac/) |
| 28 | Infrastructure as code and policy as code | Define the deployment in Terraform and add a blocking rule | A public bucket fails the check before deployment | [Checkov](https://github.com/bridgecrewio/checkov) · [Open Policy Agent](https://www.openpolicyagent.org/docs) |
| 29 | Vulnerability management and prioritisation | Scan your images and rank findings by exploitability and exposure | Each finding has an owner, deadline and reason | [Trivy](https://github.com/aquasecurity/trivy) · [CISA KEV](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) · [EPSS](https://www.first.org/epss/) |
| 30 | Endpoint hardening and EDR concepts | Collect endpoint telemetry from a lab VM | You can find a new process and its parent in your logs | [Wazuh](https://documentation.wazuh.com/current/quickstart.html) · [osquery](https://osquery.readthedocs.io/en/latest/) |
| 31 | Secure configuration baselines | Check a host and cloud account against a benchmark | You've fixed the top findings and documented exceptions | [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks) · [Prowler](https://github.com/prowler-cloud/prowler) |

**🏁 Stage project:** `04-cloud/` with your Terraform, architecture diagram and before/after scan results. Then **delete the resources**.

---

## 🚨 Stage 5: Detection, response and secure delivery

**Skip test:** Which logs would show a stolen account? What makes a detection rule noisy? What do SAST, DAST and dependency scanning each miss?

| # | Topic | 🧪 Do this | ✅ Done when | Learn |
|---|---|---|---|---|
| 32 | Key log sources | Send app, authentication and host logs to one place | Failed logins, role changes and admin actions are searchable | [Logging](https://cheatsheetseries.owasp.org/cheatsheets/Logging_Cheat_Sheet.html) |
| 33 | Detection engineering | Write 3 rules for attacks you tried in Stage 2 | Each fires on the attack and stays quiet on normal use | [SigmaHQ](https://github.com/SigmaHQ/sigma) |
| 34 | Incident response lifecycle | Write a playbook for a leaked API key | It covers detection through lessons learned | [NIST SP 800-61 Rev. 3](https://csrc.nist.gov/pubs/sp/800/61/r3/final) |
| 35 | Triage, severity and escalation | Define severity levels, owners and response times | A teammate can classify 5 sample alerts the way you would | [CISA playbooks](https://www.cisa.gov/resources-tools/resources/federal-government-cybersecurity-incident-and-vulnerability-response-playbooks) |
| 36 | Forensics, timelines and evidence | Preserve logs, hash them and build a timeline | Someone else can verify the evidence is unchanged | [NIST SP 800-86](https://csrc.nist.gov/pubs/sp/800/86/final) |
| 37 | Secure coding and security code review | Review a pull request against a checklist | Your comments name the risk and suggest a fix | [Code Review Guide](https://owasp.org/www-project-code-review-guide/) |
| 38 | Security testing in CI: SAST, DAST, dependencies | Add all three to your pipeline | A known-vulnerable change is blocked | [Semgrep](https://github.com/semgrep/semgrep) · [ZAP](https://www.zaproxy.org/getting-started/) · [Trivy](https://trivy.dev/) |
| 39 | Software supply chain security | Pin dependencies, create an SBOM and sign your image | You can verify what's inside a release and who built it | [SLSA](https://slsa.dev/) · [Syft](https://github.com/anchore/syft) · [Cosign](https://github.com/sigstore/cosign) |
| 40 | Scripting and automation | Automate one repetitive task, such as alert enrichment | It runs safely twice, handles errors and has a README | [Python tutorial](https://docs.python.org/3/tutorial/) |

**🏁 Stage project:** `05-detect-and-deliver/` with your pipeline, detection rules, and an incident report from a drill you run on your own app.

---

## 🎓 Final challenge: prove it

Give your portfolio a README that answers these in plain language:

1. What are the app's top 5 risks, and how did you reduce them?
2. How does a user, and a service, get access? How is it taken away?
3. How would you know the app was under attack?
4. What happens in the first hour after a key leaks?
5. What risk is still open, and why did you accept it?

✅ **You're done** when you can walk someone through your answers in 15 minutes and show the evidence for each.

---

## 📋 Progress tracker

Paste this into a GitHub issue in your portfolio repo:

```markdown
### Stage 1: Core security and systems
- [ ] 1 Networking
- [ ] 2 OS permissions
- [ ] 3 Privilege boundaries
- [ ] 4 Cryptography
- [ ] 5 Threat modelling
- [ ] 6 Secure design
- [ ] 7 Security models
- [ ] 🏁 Threat model

### Stage 2: Web, API and AI security
- [ ] 8 Web attacks
- [ ] 9 Validation and encoding
- [ ] 10 Sessions
- [ ] 11 API authentication
- [ ] 12 Access control
- [ ] 13 Rate limiting
- [ ] 14 Uploads and deserialisation
- [ ] 15 AI and LLM security
- [ ] 🏁 Find-and-fix report

### Stage 3: Identity, access and secrets
- [ ] 16 MFA
- [ ] 17 Passwords
- [ ] 18 SSO
- [ ] 19 RBAC and ABAC
- [ ] 20 Workload identity
- [ ] 21 Just-in-time access
- [ ] 22 Secrets
- [ ] 23 Delegation and hijacking
- [ ] 🏁 Access design

### Stage 4: Cloud and infrastructure
- [ ] 24 Segmentation
- [ ] 25 Firewalls and WAF
- [ ] 26 Storage
- [ ] 27 Containers and Kubernetes
- [ ] 28 IaC and policy as code
- [ ] 29 Vulnerability management
- [ ] 30 Endpoint hardening
- [ ] 31 Baselines
- [ ] 🏁 Hardened deployment

### Stage 5: Detection, response and secure delivery
- [ ] 32 Log sources
- [ ] 33 Detection rules
- [ ] 34 Incident response
- [ ] 35 Triage
- [ ] 36 Forensics
- [ ] 37 Code review
- [ ] 38 CI security testing
- [ ] 39 Supply chain
- [ ] 40 Automation
- [ ] 🏁 Pipeline and incident report
```

---

⬅️ [Back to the roadmap](../README.md) · 🔵 [Defensive path](DEFENSIVE.md) · ☁️ [Cloud & Identity path](CLOUD-IDENTITY.md)
