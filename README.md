# Cyber Templates

Practical, vendor-neutral templates for the nine processes we run in cybersecurity and cloud delivery. Each process is its own repository with practical, vendor-neutral procedures as code: scripts, queries, detection rules and infrastructure as code. Assessments, policy and playbook documents and the strategy for using them are shared with clients as part of an engagement and are not published here.

| # | Process | Repository |
|---|---------|--------|
| 1 | Security Operations Center | [security-operations](https://github.com/insight4business/security-operations/tree/main) |
| 2 | Detection Engineering | [detection-engineering](https://github.com/insight4business/detection-engineering/tree/main) |
| 3 | Data Protection | [data-protection](https://github.com/insight4business/data-protection/tree/main) |
| 4 | DevSecOps | [devsecops](https://github.com/insight4business/devsecops/tree/main) |
| 5 | Governance, Risk and Compliance | [governance](https://github.com/insight4business/governance/tree/main) |
| 6 | Threat Intelligence | [threat-intelligence](https://github.com/insight4business/threat-intelligence/tree/main) |
| 7 | Offensive Security | [offensive-security](https://github.com/insight4business/offensive-security/tree/main) |
| 8 | Artificial Intelligence | [artificial-intelligence](https://github.com/insight4business/artificial-intelligence/tree/main) |
| 9 | Cloud Operations | [cloud-operations](https://github.com/insight4business/cloud-operations/tree/main) |

See [STRUCTURE.md](./STRUCTURE.md) for how every repository is laid out.

## Principles
- **Generic by design.** No client data, names, hosts, IPs, accounts or URLs. Examples are fictional.
- **Ready to run.** PowerShell, KQL, SPL, Bash, Terraform and YAML.
- **Mapped to frameworks.** NIST CSF and 800-61, MITRE ATT&CK, ISO/IEC 27001 control numbers (our own wording), LGPD and GDPR.

## Quality gate
Every change passes `tools/sanitize.py` (patterns for IPs, e-mails, URLs, cloud account IDs, keys and an optional private deny-list). See [SANITIZATION.md](./SANITIZATION.md).

## License
Apache License 2.0. See [LICENSE](./LICENSE).
