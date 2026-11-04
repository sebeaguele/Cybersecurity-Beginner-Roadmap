# ☁️ Cloud & Identity Path: Days 31–90

**Goal:** Go from "I know the basics" to **junior cloud security / IAM engineer ready**. By Day 90 you'll have secured a real cloud account, attacked and fixed vulnerable labs, written IaC guardrails and built a portfolio to show employers.

**Before you start:** finish the [30-Day Foundations Track](../README.md#-the-30-day-foundations-track).

🆓 = free · 💲 = paid (optional) · 🧪 = hands-on lab · 💸 = can cost money if you forget to clean up

> 💸 **Cost safety first.** Cloud labs can bill you. On Day 31, set up a **budget alert**. At the end of every lab day, **delete what you created**. Never commit access keys to GitHub.

---

## 🗺️ Overview

| Week | Days | Focus | Outcome |
|---|---|---|---|
| 5 | 31–37 | Secure cloud account setup | A locked-down account with MFA, budgets and audit logging |
| 6 | 38–44 | Identity fundamentals | You can explain SSO, OAuth, OIDC and SAML |
| 7 | 45–51 | Cloud IAM hands-on | You can write least-privilege policies and spot over-permission |
| 8 | 52–58 | Cloud logging & detection | You can detect attacks in cloud audit logs |
| 9 | 59–65 | Posture management | You can scan an account and fix the findings |
| 10 | 66–72 | Infrastructure as code security | You can catch misconfigurations before deployment |
| 11 | 73–79 | Zero Trust & identity attacks | You understand modern identity attacks and defences |
| 12 | 80–86 | Containers & Kubernetes | You can scan images and harden a cluster |
| 🏁 | 87–90 | Capstone | Portfolio, CV and interview prep |

---

## Week 5: Secure cloud account setup
**Outcome:** You have a cloud account set up the way a security team would want it.

| Day | Task | Resource |
|---|---|---|
| 31 | Create a free-tier account and **immediately** set a budget alert | 🆓 [AWS Free Tier](https://aws.amazon.com/free/) · [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) |
| 32 | Secure the root user with MFA, and stop using root | 🆓 [Root user best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/root-user-best-practices.html) |
| 33 | Create an admin identity through IAM Identity Center (SSO) | 🆓🧪 [IAM Identity Center](https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html) |
| 34 | Learn the shared responsibility model | 🆓 [Shared responsibility model](https://aws.amazon.com/compliance/shared-responsibility-model/) |
| 35 | Read the security pillar of a well-architected framework | 🆓 [AWS Well-Architected: Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html) |
| 36 | Find your audit log and look at your own activity | 🆓🧪 [CloudTrail event history](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/view-cloudtrail-events.html) |
| 37 | **Journal:** Write your "secure account baseline" checklist | Your GitHub |

> Prefer Azure? Use the 🆓 [Azure free account](https://azure.microsoft.com/en-us/pricing/free-services/) and [Microsoft Learn](https://learn.microsoft.com/en-us/training/). The concepts are the same.

## Week 6: Identity fundamentals
**Outcome:** You can explain how modern logins work.

| Day | Task | Resource |
|---|---|---|
| 38 | Learn authentication vs authorisation, MFA and SSO | 🆓 [Microsoft Learn: SC-900 learning path](https://learn.microsoft.com/en-us/credentials/certifications/security-compliance-and-identity-fundamentals/) |
| 39 | Learn OAuth 2.0 and OpenID Connect | 🆓 [oauth.net](https://oauth.net/2/) · [OpenID Connect explained](https://openid.net/developers/how-connect-works/) |
| 40 | Learn SAML and federation | 🆓 SC-900 learning path, identity modules |
| 41 | Decode a real token and read its claims | 🆓🧪 [jwt.io](https://jwt.io/) (use test tokens only) |
| 42 | Learn joiner/mover/leaver and access reviews | 🆓 [Here-IAM plan](https://github.com/sebeaguele/Here-IAM) |
| 43 | Set up SSO into a test app with an open-source identity provider | 🆓🧪 [Keycloak](https://www.keycloak.org/getting-started/getting-started-docker) |
| 44 | **Journal:** Draw a login flow: user → IdP → app | 🆓 [draw.io](https://www.drawio.com/) |

## Week 7: Cloud IAM hands-on
**Outcome:** You can write least-privilege policies and find over-permissioned identities.

| Day | Task | Resource |
|---|---|---|
| 45 | Learn how IAM policies are evaluated (allow, deny, conditions) | 🆓 [IAM policy evaluation logic](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html) |
| 46 | Write a least-privilege policy and test it | 🆓🧪 [IAM policy simulator](https://policysim.aws.amazon.com/) |
| 47 | Find unused access and external sharing | 🆓🧪 [IAM Access Analyzer](https://docs.aws.amazon.com/IAM/latest/UserGuide/what-is-access-analyzer.html) |
| 48–50 | Hack a deliberately misconfigured AWS environment (no account needed) | 🆓🧪 [flAWS](http://flaws.cloud/) · [flAWS 2](http://flaws2.cloud/) |
| 51 | **Journal:** Write up the flAWS levels and how you'd fix each one | Your GitHub |

## Week 8: Cloud logging & detection
**Outcome:** You can spot an attacker in cloud audit logs.

| Day | Task | Resource |
|---|---|---|
| 52 | Create a CloudTrail trail that logs to S3 | 🆓🧪 [Creating a trail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-create-a-trail-using-the-console-first-time.html) 💸 |
| 53 | Learn which events matter: console logins, IAM changes, key creation | 🆓 [MITRE ATT&CK Cloud Matrix](https://attack.mitre.org/matrices/enterprise/cloud/) |
| 54 | Turn on managed threat detection (use the free trial) | 🆓🧪 [Amazon GuardDuty](https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html) 💸 |
| 55–56 | Simulate cloud attacks and find them in your logs | 🆓🧪 [Stratus Red Team](https://github.com/DataDog/stratus-red-team) 💸 |
| 57 | Write a Sigma rule for a cloud attack you detected | 🆓 [SigmaHQ cloud rules](https://github.com/SigmaHQ/sigma/tree/master/rules/cloud) |
| 58 | **Journal:** Write up your attack → detection walkthrough | Your GitHub |

## Week 9: Posture management
**Outcome:** You can scan an account against a benchmark and fix the findings.

| Day | Task | Resource |
|---|---|---|
| 59 | Learn what CSPM is and what CIS Benchmarks cover | 🆓 [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks) |
| 60 | Scan your account | 🆓🧪 [Prowler](https://github.com/prowler-cloud/prowler) |
| 61–62 | Fix your top 5 findings and re-scan | 🧪 Your account |
| 63 | Learn the native posture tools | 🆓 [AWS Security Hub](https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html) · [Microsoft Defender for Cloud](https://learn.microsoft.com/en-us/azure/defender-for-cloud/defender-for-cloud-introduction) |
| 64 | Practise on a deliberately vulnerable cloud lab | 🆓🧪 [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) 💸 |
| 65 | **Journal:** Publish a before/after posture report | Your GitHub |

## Week 10: Infrastructure as code security
**Outcome:** You can catch misconfigurations before they reach the cloud.

| Day | Task | Resource |
|---|---|---|
| 66 | Learn Terraform basics | 🆓 [Terraform tutorials](https://developer.hashicorp.com/terraform/tutorials) |
| 67 | Scan vulnerable IaC | 🆓🧪 [TerraGoat](https://github.com/bridgecrewio/terragoat) + [Checkov](https://github.com/bridgecrewio/checkov) |
| 68 | Scan IaC and containers with a second tool and compare results | 🆓🧪 [Trivy](https://github.com/aquasecurity/trivy) |
| 69 | Find leaked secrets in a repo | 🆓🧪 [Gitleaks](https://github.com/gitleaks/gitleaks) |
| 70–71 | Add Checkov and Gitleaks to a GitHub Actions pipeline | 🆓🧪 [GitHub Actions docs](https://docs.github.com/en/actions) |
| 72 | **Journal:** Publish your "secure IaC pipeline" repo | Your GitHub |

## Week 11: Zero Trust & identity attacks
**Outcome:** You understand how identities get attacked and how to defend them.

| Day | Task | Resource |
|---|---|---|
| 73 | Learn Zero Trust principles | 🆓 [NIST SP 800-207](https://csrc.nist.gov/pubs/sp/800/207/final) · [CISA Zero Trust Maturity Model](https://www.cisa.gov/zero-trust-maturity-model) |
| 74 | Learn phishing-resistant MFA: FIDO2 and passkeys | 🆓 [FIDO Alliance: passkeys](https://fidoalliance.org/passkeys/) |
| 75 | Learn the common identity attacks: password spraying, MFA fatigue, token theft, consent phishing | 🆓 [MITRE ATT&CK: Valid Accounts](https://attack.mitre.org/techniques/T1078/) |
| 76 | Learn conditional access and risk-based sign-in policies | 🆓 [Microsoft Entra Conditional Access](https://learn.microsoft.com/en-us/entra/identity/conditional-access/overview) |
| 77–78 | Hunt for suspicious sign-ins in logs (impossible travel, spraying patterns) | 🆓🧪 [KC7 Cyber](https://kc7cyber.com/) |
| 79 | **Journal:** Write a "Zero Trust for a 50-person company" one-pager | Your GitHub |

## Week 12: Containers & Kubernetes
**Outcome:** You can scan images and check a cluster against a benchmark.

| Day | Task | Resource |
|---|---|---|
| 80 | Learn container security basics: images, least privilege, secrets | 🆓 [OWASP Docker Security Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html) |
| 81 | Run a local Kubernetes cluster | 🆓🧪 [kind](https://kind.sigs.k8s.io/) |
| 82 | Check your cluster against the CIS Kubernetes Benchmark | 🆓🧪 [kube-bench](https://github.com/aquasecurity/kube-bench) |
| 83–85 | Attack and defend a deliberately vulnerable cluster | 🆓🧪 [Kubernetes Goat](https://github.com/madhuakula/kubernetes-goat) |
| 86 | **Journal:** Write up 3 Kubernetes Goat scenarios and the fixes | Your GitHub |

---

## 🏁 Days 87–90: Capstone

1. **💸 Cleanup:** Delete every lab resource, check your bill and keep only your budget alert and audit trail
2. **Portfolio README:** Link your account baseline, flAWS write-up, attack → detection walkthrough, posture report, IaC pipeline and Zero Trust one-pager
3. **CV:** List outcomes, e.g. "Reduced Prowler findings by 80% in a test account" or "Built a CI pipeline that blocks insecure Terraform"
4. **Interview prep:** Practise answering "How would you secure a brand-new cloud account?" in 3 minutes
5. **Optional certifications** (check the vendor sites for current exam versions):
   - 💲 [SC-300](https://learn.microsoft.com/en-us/credentials/certifications/identity-and-access-administrator/): Microsoft identity and access
   - 💲 [AZ-500](https://learn.microsoft.com/en-us/credentials/certifications/azure-security-engineer/): Azure security engineer
   - 💲 [AWS Certified Security – Specialty](https://aws.amazon.com/certification/certified-security-specialty/)
   - 💲 [CCSK](https://cloudsecurityalliance.org/education/ccsk): vendor-neutral cloud security knowledge

✅ **After Day 90:** you can say "I secured a cloud account, broke and fixed vulnerable labs and automated guardrails", and prove it.

---

⬅️ [Back to the roadmap](../README.md) · 🔵 [Defensive path](DEFENSIVE.md)
