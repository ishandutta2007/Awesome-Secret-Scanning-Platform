# Awesome-Secret-Scanning-Platform

## Top Secret Scanning Platform Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Detecting Hardcoded Credentials, API Keys, Tokens & Secrets in Code, Repositories, CI/CD & Beyond*  

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Secret Scanning**. These tools find leaked credentials (API keys, passwords, tokens, certificates) in source code, git history, containers, and other locations so teams can revoke them before attackers do.



**Examples** include GitGuardian, TruffleHog, Gitleaks, Doppler Secret Scanner, GitHub Secret Scanning, SpectralOps, Cycode, GitLab Secret Detection, Checkmarx Secrets, and Legit Security (the category leaders).



**Open-source emphasis**: Secret scanning is one of the strongest open-source security domains. **TruffleHog** and **Gitleaks** are industry standards used in virtually every modern DevSecOps pipeline. Additional tools such as detect-secrets, ggshield (CLI), and others provide complementary capabilities. This section is heavily expanded with every major active project.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[GitGuardian](https://www.gitguardian.com/)**  

  Leading enterprise secrets detection platform with broad coverage across code, CI/CD, collaboration tools, and public monitoring, plus remediation workflows and honeytokens.



- **[TruffleHog (Truffle Security commercial offerings)](https://trufflesecurity.com/)**  

  Commercial platform and support built around the popular open-source TruffleHog engine, adding enterprise features, scale, and workflow integrations.



- **[SpectralOps (Check Point)](https://spectralops.io/)**  

  Secrets and misconfiguration scanning platform often delivered as part of broader cloud and code security suites.



- **[Cycode](https://cycode.com/)**  

  Application security platform that includes secrets detection alongside broader pipeline and code security capabilities.



- **[GitHub Secret Scanning](https://docs.github.com/en/code-security/secret-scanning)**  

  Native secret scanning and push protection available through GitHub Advanced Security, with partner validity checks for many secret types.



- **[GitLab Secret Detection](https://docs.gitlab.com/ee/user/application_security/secret_detection/)**  

  Built-in secret detection capabilities in GitLab that scan repositories and pipelines for leaked credentials.



- **[Doppler Secret Scanner / secrets tooling](https://www.doppler.com/)**  

  Secrets management platform that also provides scanning and detection features to prevent secrets from landing in code.



- **[Checkmarx Secrets, Legit Security](https://checkmarx.com/)**  

  Secrets detection modules within broader ASPM / code-security platforms focused on enterprise governance and risk prioritization.



- **[Other commercial secret scanning platforms](https://www.gitguardian.com/)**  

  Additional vendors offering multi-repo scanning, historical analysis, and integration with ticketing or rotation workflows.



## Open-Source GitHub Projects



- **[TruffleHog](https://github.com/trufflesecurity/trufflehog)**  

  Leading open-source secret scanner that detects credentials via high-entropy analysis and regex, then **verifies** many findings with live API checks against providers. Supports git, filesystems, S3, Docker, and more.



- **[Gitleaks](https://github.com/gitleaks/gitleaks)**  

  Fast, lightweight, MIT-licensed secret scanner optimized for git repositories and pre-commit/CI use. Highly configurable rule sets and excellent performance for blocking leaks early.



- **[detect-secrets (Yelp)](https://github.com/Yelp/detect-secrets)**  

  Open-source tool built around a baseline file model—ideal for large legacy repositories where existing findings are accepted and only new secrets are flagged.



- **[ggshield (GitGuardian CLI)](https://github.com/GitGuardian/ggshield)**  

  Open-source CLI that can scan local repositories and integrate with GitGuardian’s detection engine; useful in hybrid open-source + platform setups.



- **[git-secrets and classic scanners](https://github.com/awslabs/git-secrets)**  

  Earlier-generation tools (including AWS git-secrets) that prevent commits containing specific patterns; still useful in constrained environments.



- **[Trivy secrets module](https://github.com/aquasecurity/trivy)**  

  Secrets detection capabilities included in the popular open-source Trivy vulnerability scanner, convenient for teams already using Trivy.



- **[Combined scanners & wrappers](https://github.com/padok-team/git-secret-scanner)**  

  Community tools that orchestrate TruffleHog + Gitleaks (or similar) to maximize coverage across organizations and groups.



- **[Other entropy & pattern scanners](https://github.com/search?q=secret+scanning+OR+credential+detection+OR+gitleaks+OR+trufflehog)**  

  Additional open-source projects focused on specific languages, file types, or historical repository analysis.



### Additional Strong Open-Source Options



- **Pre-commit framework hooks**: Official and community hooks that run Gitleaks, TruffleHog, or detect-secrets before code is committed.

- **SARIF output & GitHub Code Scanning integration**: Native support in major tools for surfacing findings in pull requests.

- **Custom detector development**: Extensible rule formats (TOML, YAML, or code) for organization-specific secret patterns.

- **Container & IaC scanning**: Tools that extend secret detection into images, Terraform, and Kubernetes manifests.

- **Baseline & allow-list management**: Practices and helpers for reducing noise in mature codebases.

- Education and CTF resources that teach developers how secrets leak and how to prevent them.



**Frameworks for building custom systems**:  

The recommended open-source baseline is **Gitleaks** (fast pre-commit + CI) + **TruffleHog** (deep history scans with live verification).  

Add **detect-secrets** when dealing with large legacy repositories that need a baseline approach.  

Commercial platforms (GitGuardian, GitHub Advanced Security, Spectral, Cycode, etc.) add organization-wide visibility, historical scanning at scale, collaboration-tool coverage, remediation workflows, and support that pure open-source tools do not fully provide.  

Most mature programs run open-source scanners in every developer workflow and layer a commercial platform for enterprise governance.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Finding a secret is only the first step. Secrets must be rotated/revoked, and the root cause (why the secret was committed) must be addressed. Scanning does not replace proper secrets management (vaults, short-lived credentials, OIDC, etc.).

- Open-source scanners can produce false positives and may miss novel or highly customized secret formats. Always combine automated scanning with secure development practices, least-privilege credentials, and incident response readiness.



---



**Made for security engineers, DevSecOps teams, platform engineers, and developers who want to stop credential leaks.**  

Let's keep secrets out of git history through fast open-source tools and robust platform workflows.
