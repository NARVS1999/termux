# DevSecOps Engineer Roadmap: Fundamentals → Intermediate

> General knowledge for DevOps engineers, with DevSecOps-specific context.

## Security Fundamentals (Prerequisites)

- [ ] **Phase 1** — Security principles: CIA triad, authentication, authorization, accountability
- [ ] **Phase 2** — Threat modeling: STRIDE, attack surfaces, risk scoring, threat trees
- [ ] **Phase 3** — Cryptography basics: hashing, symmetric vs asymmetric, TLS, certificates
- [ ] **Phase 4** — Network & OS security: ports, firewalls, hardening baselines, patching

## Secure Development

- [ ] **Phase 5** — Secure coding: input validation, injection prevention, output encoding
- [ ] **Phase 6** — OWASP Top 10: XSS, CSRF, SSRF, insecure deserialization, mitigations
- [ ] **Phase 7** — SAST: static analysis tools, rulesets, CI integration, triaging findings
- [ ] **Phase 8** — Dependency scanning: SCA tools, CVE triage, upgrade automation, lockfiles
- [ ] **Phase 9** — Secrets in code: detection tools, pre-commit hooks, git history scrubbing

## CI/CD Security

- [ ] **Phase 10** — Pipeline security: injection attacks, approval gates, environment isolation
- [ ] **Phase 11** — Build integrity: reproducible builds, provenance, artifact verification
- [ ] **Phase 12** — Software supply chain: SLSA levels, SBOMs, package provenance
- [ ] **Phase 13** — Environment security: branch protection, privileged runners, sandboxing
- [ ] **Phase 14** — Deployment security: secure promotion, sign-off flows, audit trails

## Container & Orchestration Security

- [ ] **Phase 15** — Image security: base image hygiene, scanning, minimal images, multi-stage
- [ ] **Phase 16** — Docker security: non-root users, read-only filesystems, capabilities, seccomp
- [ ] **Phase 17** — Kubernetes RBAC: roles, bindings, service accounts, least privilege
- [ ] **Phase 18** — Network policies: namespace isolation, pod-to-pod restrictions, ingress rules
- [ ] **Phase 19** — Admission control: Pod Security Standards, policy engines, OPA/Gatekeeper

## Cloud Security

- [ ] **Phase 20** — IAM: least privilege, roles, policies, temporary credentials
- [ ] **Phase 21** — Shared responsibility model: cloud vs customer controls
- [ ] **Phase 22** — Data protection: encryption at rest/in transit, KMS, key rotation
- [ ] **Phase 23** — Cloud monitoring: CloudTrail/Activity Logs, anomaly detection, guardrails
- [ ] **Phase 24** — Cloud security tools: CSPM, CWPP, config compliance scanners

## Secrets & Identity Management

- [ ] **Phase 25** — Secrets management: Vault, cloud secret stores, dynamic secrets
- [ ] **Phase 26** — Secret rotation: lifecycle, automated rotation, break-glass access
- [ ] **Phase 27** — Identity providers: SSO, SAML, OIDC, service-to-service auth
- [ ] **Phase 28** — MFA & access: phishing-resistant MFA, conditional access, least privilege

## Security Testing

- [ ] **Phase 29** — DAST: dynamic scanning, authenticated scans, baseline configs
- [ ] **Phase 30** — Penetration testing: scoping, methodologies, reporting, remediation
- [ ] **Phase 31** — Infrastructure scanning: cloud misconfig checks, IaC scanning
- [ ] **Phase 32** — Vulnerability management: prioritization, CVSS, patching SLAs, CVE feeds
- [ ] **Phase 33** — Fuzzing & edge cases: fuzz targets, crash triage, regression coverage
- [ ] **Phase 34** — Security regression: re-running tests, drift detection, evidence capture

## Monitoring & Incident Response

- [ ] **Phase 35** — SIEM: log ingestion, correlation rules, dashboards, retention
- [ ] **Phase 36** — Log & audit: centralized logging, immutable audit trails, alerts
- [ ] **Phase 37** — Incident response: playbooks, detection, containment, eradication
- [ ] **Phase 38** — Forensics basics: evidence handling, timelines, memory analysis
- [ ] **Phase 39** — Post-incident: blameless reviews, lessons learned, control updates

## Compliance & Governance

- [ ] **Phase 40** — Frameworks: SOC 2, ISO 27001, NIST, PCI DSS basics
- [ ] **Phase 41** — Audit readiness: evidence collection, continuous compliance
- [ ] **Phase 42** — Policy as code: OPA, Sentinel, compliance-as-code pipelines
- [ ] **Phase 43** — Risk management: risk registers, acceptable risk, exception processes

## Automation & Culture

- [ ] **Phase 44** — Security automation: orchestrated scans, auto-remediation, guardrails
- [ ] **Phase 45** — Shift-left culture: developer security training, champions, friction reduction
- [ ] **Phase 46** — Security metrics: MTTR, coverage, critical findings, trend reporting
- [ ] **Phase 47** — Secure defaults: hardening baselines, golden paths, reference architectures

## Recommended Learning Path (priority order)

1. **Phase 1–4** — Security fundamentals
2. **Phase 5–9** — Secure development
3. **Phase 10–14** — CI/CD security
4. **Phase 15–19** — Container & K8s security
5. **Phase 20–24** — Cloud security
6. **Phase 35–39** — Monitoring & incident response
7. **Phase 40–43** — Compliance & governance

> Focus on building real projects — employers hire mid-level DevSecOps engineers for secure, clean, automated pipelines plus ownership of security end-to-end.
