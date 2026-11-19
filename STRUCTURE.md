# How the repositories are organised

One repository per process. Inside each repository the layout is always:

```
<process-repository>/
  <sub-process>/            what part of the process you are in
    <technology>/           what you operate (Entra ID, Exchange, Azure SQL, Windows ...)
      <script, query or rule>   one file solves one problem
      README.md                 table: problem it solves, what it does, requirements, effect
```

Rules:

1. **Folders follow the pain, not the tool.** A script that reports who can read a shared mailbox lives under security-operations, in identity and access, in the Exchange folder. A script that tidies address lists lives under cloud-operations.
2. **Every script states its objective** in the header: problem solved, what it does, requirements and effect (read-only, changes state or destructive).
3. **Anything that changes state** defaults to dry-run or needs an explicit switch.
4. **Placeholders** such as `ENTRE_AQUI_COM_SEU_*` and `<TENANT_ID>` mark every value you must replace.
5. **Reference or field.** Scripts are either written from scratch as reference code or adapted from real operations work; the folder README says which.

| Repository | Sub-processes |
|---|---|
| security-operations | incident-response, identity-and-access, vulnerability-management, service-catalog-and-sla |
| detection-engineering | use-cases-by-technology, use-case-management |
| data-protection | classification-and-labeling, dlp, privacy-lgpd-gdpr, retention-and-log-architecture, insider-risk-and-ediscovery, encryption-and-key-management, breach-response, third-party-privacy, data-inventory-and-masking |
| devsecops | infrastructure-as-code, pipelines-and-gates, secure-development-lifecycle, containers-and-kubernetes, threat-modelling, training and domain folders |
| governance | corporate-governance-and-policies, risk-management, compliance-and-frameworks, internal-audit, isms-core, third-party-risk, training-and-awareness, reports-and-metrics |
| threat-intelligence | program-and-requirements, brand-abuse, data-breach-and-leaks, credential-leaks, phishing-and-fraud-intel, vulnerability-intelligence, threat-actors-and-campaigns, ioc-management, threat-hunting, reporting |
| offensive-security | engagement-management, reconnaissance, scanning-and-vulnerability-analysis, web-and-api-testing, network-and-active-directory, cloud-testing, mobile-testing, red-and-purple-team, reporting-and-retest |
| artificial-intelligence | ai-governance-and-policy, ai-risk-assessment, llm-guardrails-and-security, agentic-ai, vendor-and-model-due-diligence, evaluation-and-golden-sets, ai-incident-response, ai-red-team, data-handling-for-ai, iso-42001-and-frameworks |
| cloud-operations | azure, microsoft-365, endpoints, shared helpers |
