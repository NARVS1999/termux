# DevOps Engineer Roadmap: Fundamentals → Intermediate

> General knowledge for DevOps engineers, with DevOps-specific context.

## Prerequisites

- [ ] **Phase 1** — OS & networking basics: TCP/IP, DNS, ports, subnets, firewalls
- [ ] **Phase 2** — Linux command line: shell navigation, file operations, pipes, redirection
- [ ] **Phase 3** — Scripting fundamentals: Bash basics, variables, loops, conditionals
- [ ] **Phase 4** — Git & version control: init, branches, merging, remotes, tags

## Linux & Operating Systems

- [ ] **Phase 5** — Filesystem: permissions, ownership, symlinks, mounts, filesystem types
- [ ] **Phase 6** — Processes & services: ps, kill, background jobs, systemd units
- [ ] **Phase 7** — Package management: apt, yum/dnf, repositories, container packaging
- [ ] **Phase 8** — Networking config: IP, routing, iptables, ssh keys, hardening
- [ ] **Phase 9** — Logs & troubleshooting: journalctl, dmesg, strace, resource monitoring

## Scripting & Automation

- [ ] **Phase 10** — Bash scripting: functions, arguments, exit codes, error handling
- [ ] **Phase 11** — Python for automation: modules, argparse, requests, yaml/json handling
- [ ] **Phase 12** — Scheduling: cron, at, automation patterns, idempotency
- [ ] **Phase 13** — Text processing: grep, sed, awk, jq, sorting pipelines

## Version Control & Collaboration

- [ ] **Phase 14** — Advanced git: rebase, cherry-pick, hooks, tags, submodules
- [ ] **Phase 15** — Branching strategies: GitFlow, trunk-based, pull request workflows
- [ ] **Phase 16** — Collaboration: code review, semantic commits, changelogs

## CI/CD

- [ ] **Phase 17** — CI concepts: triggers, stages, jobs, caching, artifacts
- [ ] **Phase 18** — GitHub Actions: workflows, actions, secrets, matrix builds
- [ ] **Phase 19** — Jenkins: pipelines, plugins, agents, shared libraries
- [ ] **Phase 20** — Pipeline design: build, test, security scan, artifact stages
- [ ] **Phase 21** — Artifact management: registries, versioning, immutable artifacts
- [ ] **Phase 22** — CD strategies: blue-green, canary, rolling, feature flags, rollback

## Containers & Orchestration

- [ ] **Phase 23** — Docker basics: images, containers, Dockerfile, layers, caching
- [ ] **Phase 24** — Docker ecosystem: registries, multi-stage builds, distroless, security
- [ ] **Phase 25** — Docker Compose: services, networks, volumes, local dev environments
- [ ] **Phase 26** — Kubernetes basics: pods, deployments, services, namespaces
- [ ] **Phase 27** — Kubernetes workloads: StatefulSets, DaemonSets, Jobs, config & secrets
- [ ] **Phase 28** — Helm: charts, templating, releases, chart repositories

## Infrastructure as Code

- [ ] **Phase 29** — Terraform basics: resources, providers, plan/apply, state
- [ ] **Phase 30** — Terraform advanced: modules, workspaces, remote state, locking
- [ ] **Phase 31** — Ansible: playbooks, inventory, roles, idempotency
- [ ] **Phase 32** — Packer: golden images, builders, provisioners
- [ ] **Phase 33** — IaC patterns: drift detection, environments, policy as code

## Cloud Providers

- [ ] **Phase 34** — AWS core: EC2, S3, IAM, VPC, RDS, Lambda
- [ ] **Phase 35** — AWS advanced: EKS, ECS, CloudFormation, cost management
- [ ] **Phase 36** — GCP basics: Compute Engine, GKE, Cloud Storage, IAM
- [ ] **Phase 37** — Azure basics: VMs, AKS, Azure DevOps, resource groups
- [ ] **Phase 38** — Multi-cloud patterns: abstraction layers, vendor neutrality, cost optimization

## Monitoring & Observability

- [ ] **Phase 39** — Metrics: Prometheus, exporters, metric types, queries
- [ ] **Phase 40** — Logging: ELK stack, Loki, structured logging, retention
- [ ] **Phase 41** — Tracing: OpenTelemetry, distributed traces, span sampling
- [ ] **Phase 42** — Alerting: alert rules, routing, on-call, SLOs
- [ ] **Phase 43** — Dashboards: Grafana, visualization, SRE practices

## Security & Compliance

- [ ] **Phase 44** — Secrets management: Vault, cloud secret stores, rotation
- [ ] **Phase 45** — Network security: security groups, VPCs, VPN, zero trust
- [ ] **Phase 46** — Container security: image scanning, runtime security, SBOM
- [ ] **Phase 47** — Compliance: audit logs, SOC 2 basics, GDPR, policy as code

## Recommended Learning Path (priority order)

1. **Phase 1–4** — Prerequisites
2. **Phase 5–9** — Linux fundamentals
3. **Phase 17–22** — CI/CD
4. **Phase 23–25** — Docker
5. **Phase 26–28** — Kubernetes
6. **Phase 29–33** — Infrastructure as code
7. **Phase 39–43** — Monitoring & observability

> Focus on building real projects — employers hire mid-level DevOps engineers for clean, performant, well-tested infrastructure plus ownership of systems end-to-end.
