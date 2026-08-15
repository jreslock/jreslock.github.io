---
title: "Resume"
description: "An evergreen representation of my work history and professional experience"
type: resume
---

# Jason Reslock

**Mansfield, MA**  
[github.com/jreslock](https://github.com/jreslock) · [linkedin.com/in/jreslock](https://linkedin.com/in/jreslock) · [jreslock.github.io](https://jreslock.github.io)

---

## Summary

Principal Architect with 25+ years in technology, currently responsible for the cloud platform behind OM1's HIPAA-compliant Real World Data products — 30+ AWS environments, 200+ reusable OpenTofu modules, and the developer platform the engineering organization builds on.

I design and build the systems other engineers build on: a multi-account AWS landing zone, a Kubernetes control plane for Snowflake, self-service cloud development environments, and the agent tooling that keeps a two-person infrastructure team ahead of a growing engineering org. My work tends to start as architecture and end as shipped software — I write the design doc, socialize it for critique, then build it in Python, Go, or OpenTofu and own it through adoption, incident response, and eventual decommissioning.

What I care about is leverage: standards that hold, abstractions that lower the cost of the next team's work, and evidence-driven decisions about what to keep and what to kill. Most of it isn't visible to any single team, which is rather the point.

Interested in architect-level individual contributor roles where I can shape infrastructure and platform strategy in engineering-driven organizations — particularly technology, healthcare, and life sciences.

---

## Platforms, Tools & Languages

**Cloud & Platform:** AWS (Control Tower, Organizations, Account Factory for Terraform, Transit Gateway, Route 53 Resolver, Client VPN, EKS, ECS/Fargate, Lambda, RAM, EventBridge, SSM), Kubernetes, Snowflake, Databricks

**Infrastructure as Code:** OpenTofu/Terraform, Atlantis, Packer, Helm, Ansible, Docker, private module registry

**CI/CD & Developer Platform:** GitHub Actions, AWS CodeBuild, OIDC federation, Dev Containers, devcontainer features, Taskfile, semantic release automation

**Languages:** Python (Typer, FastAPI, Pydantic, pytest, boto3), Go, Shell, HCL · tooling: uv, ruff, pre-commit

**AI & Agent Engineering:** Amazon Bedrock, Model Context Protocol server development, Strands, LiteLLM, Claude Code plugins/skills and private marketplace distribution, agent evaluation harnesses (replay gates, judge/critic), token and cost instrumentation

**Identity & Security:** Okta, Auth0, AWS IAM Identity Center, SSO/OIDC/SAML, JWT/JWKS, Snowflake Workload Identity Federation, GuardDuty, Inspector, Security Hub, WAF, CIS Benchmark hardening, Mend

**Observability & FinOps:** CloudWatch (cross-account observability, OAM), CloudTrail, Athena, CUR 2.0, Kinesis Firehose, Prometheus/blackbox probes, SumoLogic, AWS Budgets and Cost Anomaly Detection

**Data Platform:** Snowflake (WIF, reader accounts, shares, storage integrations), Airflow/MWAA, Airbyte, dbt, Aurora Postgres, Redis

**Healthcare:** HIPAA-compliant architecture, PHI access logging and scrubbing, Orthanc/DICOM, SMART on FHIR, FDA-validated software release processes

---

## Selected Projects & Initiatives

**The Developer Platform Flywheel**  
Three tools that compound: **OBT** standardizes build, test, release, and deploy across every repository; **DevEnv** gives every engineer an on-demand cloud workspace with tooling pre-installed; **App Factory** turns roughly ten lines of YAML into a running application with auth, database, DNS, CDN, IAM, and Helm deployment already wired. Each makes the others more valuable. Together they took the path from idea to running application from weeks to hours.

Adoption through H1 2026: OBT on **75 repositories** org-wide with 4× commit velocity growth; App Factory from **11 to 40 active applications in eight months**, with distinct contributors rising from 12 to 18 per quarter — more people shipping independently, not the same people shipping more.

**AWS Multi-Account Landing Zone & Network Architecture**  
Designed and delivered OM1's landing zone on AWS Control Tower and Account Factory for Terraform, growing the estate from 11 to ~25 accounts while replacing a multi-week manual provisioning process with an automated one. Re-architected the network as a Transit Gateway hub-and-spoke with a centralized Route 53 Resolver hub, RAM-shared resolver rules, DNS canaries, and cross-account Reachability Analyzer probes. Consolidated seven per-account Client VPN endpoints into a single Okta SAML endpoint with access tiers driven by dynamic group rules.

**Snowflake Kubernetes Control Plane**  
A Kopf-based operator that manages Snowflake through declarative custom resources — databases, roles, grants, storage integrations, service users — replacing ticket-driven provisioning and hand-run destructive SQL. Built on an IRSA and IAM-boundary foundation with a three-party separation-of-duties model, so compromising any single party doesn't yield the chain. Its distinguishing feature is a set of five safety interlocks: refuse to recreate a schema over a recoverable dropped twin, require approval annotations before any drop, refuse unrecoverable drops, make `CASCADE` unreachable, and circuit-break bulk deletes.

**Jagent — Autonomous Infrastructure Triage Agent**  
A Slack-native, Bedrock-backed agent that answers grounded questions and performs first-pass PR reviews for the infrastructure team, built explicitly to absorb load from a two-person team. Governance-first: grounded in live systems through purpose-built MCP servers, shipped shadow-before-live, gated by a replay harness and a judge/critic scorer, and structurally unable to merge — it is never a code owner. Reviews lead with blast radius and verify a PR's claims rather than trusting them. Prompts live in code so every behavior change goes through review and the gate; prompts are production behavior, not configuration.

**MCP Servers & Internal Plugin Marketplace**  
Built and shipped Model Context Protocol servers giving natural-language access to AWS Cost Explorer (including CUR 2.0 via Athena) and CloudWatch Logs across the organization, the latter with source-account attribution logic that prevents agents from misreading centrally-aggregated logs. Runs OM1's internal Claude Code plugin marketplace so a capability built once by anyone propagates to everyone.

**Observability & Cost Governance**  
Centralized GuardDuty, Inspector, and Security Hub into a dedicated security tooling account as delegated administrator across the organization. Implemented CloudWatch Cross-Account Observability, organization-level CloudTrail, and an S3 + Athena archive for CloudWatch Logs with automated retention management. Established org-wide AWS Budgets and Cost Anomaly Detection with Slack routing.

**CI/CD Modernization & Legacy Decommissioning**  
Migrated the infrastructure monorepo and ~30 other repositories from Jenkins to GitHub Actions, reducing a major org-wide dependency to four remaining repositories. Rolled OIDC federation across the organization to eliminate static credentials. Built Atlantis drift detection with GitHub PR-files-API-driven project auto-detection. Retired services deliberately and with evidence — usage metrics, per-tenant inventories, and stakeholder sign-off before teardown.

---

## Experience

### Principal Architect  
**OM1, Inc.** — Boston, MA (Remote) · *Mar 2021 – Present*  
*Promoted August 2025 to OM1's most senior engineering position.*

Architect and maintain the cloud platform behind OM1's HIPAA-compliant Real World Data products, spanning ~25 AWS accounts, 30+ environments, and the developer tooling the engineering organization depends on.

- Designed and delivered the AWS multi-account landing zone (Control Tower, Account Factory for Terraform, Transit Gateway hub-and-spoke, centralized DNS), scaling the estate from 11 to ~25 accounts
- Built the developer platform — cloud dev environments, standardized build tooling, and a YAML-to-running-application factory — taking idea-to-deployed-app from weeks to hours and growing App Factory from 11 to 40 applications in eight months
- Reduced per-account infrastructure cost **~29%** while the account footprint grew 2.3×; drove **~$70K/year** in verified recurring reductions, including eliminating $2,200/month of redundant cross-region registry replication and cutting CloudTrail spend **99.7%** after detecting a 282% month-over-month anomaly
- Maintained **99.4% Savings Plans utilization** — under $300 of unused commitment across six months — while committed spend grew 54%
- Built the organization's AI engineering substrate: Bedrock access and governance, MCP servers, an internal plugin marketplace, and an autonomous triage agent with a replay-gated evaluation harness
- Centralized security tooling and audit logging org-wide; led incident response including same-day recovery of 261 destroyed production resources with a blameless root cause and durable process fix
- Authored **1,170 pull requests** and reviewed **1,992** for other engineers across ~90 repositories over the last year; org-wide merged PR throughput rose **77% year over year** across the same period
- Rebuilt how the infrastructure team plans and reports work, and run weekly office hours, standups, and pairing sessions as the team's enablement forums

---

### Lead Member of Technical Staff – Philanthropy Cloud  
**Salesforce** — Remote, US · *Aug 2019 – Mar 2021*

Joined Salesforce post-acquisition of Salesforce.org as an individual contributor. Led infrastructure modernization for the Philanthropy Cloud product suite.

- Re-architected CI infrastructure to support containerized builds, PR gating, artifact versioning, and publishing  
- Migrated all AWS and Heroku infrastructure to Terraform for codified, repeatable deployments  
- Co-designed Lambda + API Gateway–based architecture compliant with org-wide security standards  
- Delivered a new product launch under tight deadlines during COVID while building new DNS and TLS infrastructure  
- Represented the operations team in architecture planning and roadmap discussions  
- Managed and mentored three engineers and one intern

---

### Senior DevOps Engineer  
**OM1, Inc.** — Boston, MA · *Oct 2017 – Aug 2019*

Early infrastructure engineer supporting OM1's HIPAA-compliant AWS environment.

- Consolidated AWS footprint from 11 to 5 accounts to simplify architecture and reduce costs  
- Built a scalable VPN solution using OpenVPN, Terraform, AWS Managed AD, and MFA  
- Implemented company-wide SSO via Okta; deployed SumoLogic and Terraform-managed logging  
- Migrated from TravisCI to Jenkins for improved control of build/release processes  
- Reduced AWS costs by ~40% in the first few months through optimization and tagging

---

### Lead DevOps Engineer  
**Teradata (via Hadapt acquisition)** — Boston, MA · *Jul 2014 – Oct 2017*

Led infrastructure and DevOps initiatives across internal product teams and open-source data platforms.

- Built CI/CD pipelines and automated testing frameworks for PrestoDB and internal systems  
- Migrated engineering infrastructure from AWS to internal VMware environments  
- Recruited and grew an infrastructure team from 1 to 5 engineers  
- Promoted DevOps adoption through internal enablement, demos, and platform tooling

---

### Technical Operations / IT / Customer Support  
**Hadapt** — Cambridge, MA · *Feb 2013 – Jul 2014*

Contributed across support, IT, and DevOps; managed infrastructure, supported customers, and built internal tooling during Hadapt's early growth phase.

---

## Open Source

Merged contributions to [HashiCorp packer-plugin-amazon](https://github.com/hashicorp/packer-plugin-amazon/pull/568) (IMDS credential detection in the AMI datasource — restored a blocked CVE-patching pipeline), [loft-sh/devpod-provider-aws](https://github.com/loft-sh/devpod-provider-aws/pull/48), and [runatlantis/atlantis](https://github.com/runatlantis/atlantis/pull/5735).

---

## Education

**Framingham State University**  
Coursework toward B.A. · *1996 – 1997*

**Clark University Computer Career Institute**  
MCSE+I Certification Program, A+ Certification Training · *1997*

---

## Community & Interests

- Active in the Boston DevOps community; regular attendee and past volunteer at DevOps Days Boston  
- Previously hosted local meetups and engineering talks  
- Passionate about music and board sports (snow/skate/wake)
