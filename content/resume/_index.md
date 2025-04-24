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

Cloud Infrastructure Architect and DevOps leader with 25+ years of technology industry experience. Proven track reccord of building, scaling, and securing systems in both startup and enterprise environments. Skilled in architecting resilient, cost-efficient cloud infrastructure with a strong emphasis on developer experience, automation, and operational excellence.

Passionate about simplifying complexity and improving existing systems — from reducing cloud spend and modernizing CI/CD pipelines to establishing infrastructure standards and mentoring engineers. Technically versatile, with deep expertise in AWS and a wide range of tools and technologies that enable high-performing engineering organizations.

Primarily interested in architect-level individual contributor roles where I can shape infrastructure and platform strategy in high-impact, engineering-driven organizations — particularly in sectors such as technology, healthcare, and life sciences.

---

## Platforms, Tools & Languages

**Cloud/Platform:** AWS, Snowflake, Kubernetes  

**IaC/Automation:** Terraform/OpenTofu, Docker, Atlantis, Ansible, Packer  

**CI/CD:** GitHub Actions, AWS CodeBuild, Jenkins

**Security:** SSO/OIDC/SAML, Okta, SumoLogic, Mend, IAM, VPN  

**Misc:** Containers, git, Linux, Slackbots, "glue code"

---

## Selected Projects & Initiatives

**Planner**  
Designed, built and drove adoption of a CLI tool to validate Terraform changes via AWS ECS before PR submission. Enables remote, pre-PR Terraform plan execution for improved CI/CD safety.

**Event-Driven AMI Builder**  
Automated AMI pipeline triggered by AWS EventBridge and SQS. Replaced manual builds with an event-driven approach to ensure up-to-date, reproducible base images.

**CI/CD Platform Migration to GitHub Actions**  
Led migration from self-hosted Jenkins to GitHub Actions across multiple services. Implemented OIDC-based IAM role access for secure, scoped AWS access from workflows. Enabled hybrid runners using AWS CodeBuild to support in-VPC, cost-effective, and platform-flexible build agents.

**AWS SSO Rollout via IAM Identity Center + Okta Integration**  
Designed and implemented a secure, scalable migration from IAM users to AWS IAM Identity Center (AWS SSO) across a multi-account organization. Integrated with Okta for centralized user/group management, preserved existing access patterns, and enabled full decommissioning of non-automated IAM users and access keys. Managed entirely via Terraform for version control and auditable change history.

**Terraform Provisioning for AWS SageMaker AI Studio**  
Developed a reusable Terraform module to provision AWS SageMaker AI Unified Studio domains across multiple accounts. Automates configuration of SSO integration, Jupyter environments, CodeSpaces, MLflow, and other key SageMaker components. Enables consistent, auditable deployment of AI/ML workspaces via infrastructure-as-code.

**Devcontainer Environment Standardization for Local + CI**  
Designed a unified devcontainer workflow using VSCode’s Dev Containers feature to ensure parity between local development and CI environments. Included optional dotfile loading for personal shell setups in local environments, and integrated GitHub Actions to use the same container image in CI pipelines.

---

## Experience

### Principal Infrastructure Engineer  
**OM1, Inc.** — Boston, MA (Remote) · *Mar 2021 – Present*

Architect and maintain all cloud infrastructure for OM1’s HIPAA-compliant Real World Data platform, spanning multiple environments and services.

- Reduced AWS spend by over 50% through infrastructure right-sizing, environment cleanup, and tagging-based cost analysis  
- Led company-wide adoption of AWS IAM Identity Center (SSO), replacing IAM users across all accounts with Okta-integrated, Terraform-managed identity architecture  
- Migrated CI/CD workflows from Jenkins to GitHub Actions with OIDC integration and hybrid CodeBuild runners  
- Designed and deployed secure, VPC-connected SageMaker Studio domains using reusable Terraform modules  
- Built developer-facing automation and tooling for Terraform plan verification, AMI pipelines, and devcontainer standardization  
- Provide infrastructure mentorship and technical leadership across engineering, with an emphasis on automation, security, and observability

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

Early infrastructure engineer supporting OM1’s HIPAA-compliant AWS environment.

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

Contributed across support, IT, and DevOps; managed infrastructure, supported customers, and built internal tooling during Hadapt’s early growth phase.

---

## Certifications

- AWS Certified Cloud Practitioner (2019)

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