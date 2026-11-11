# Awesome-Cloud-Native-Serverless-Backup-Architecture

## Top Cloud-Native Serverless Backup Architecture Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Event-Driven Backup Orchestration, Serverless Compute & Cloud-Native Data Protection*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud-Native Serverless Backup Architecture**. These tools leverage serverless compute (Lambda, Cloud Functions, Workers) and managed services to orchestrate backup and recovery workflows without provisioning or managing dedicated backup infrastructure—covering event-triggered snapshots, policy-driven retention, and cross-region replication.

**Examples** include Druva Serverless Architecture, AWS Backup with Lambda, Azure Backup with Functions, Google Cloud Backup and DR, Cloudflare Workers for backup APIs, Vercel Serverless Functions, Serverless Framework, Fastly Compute, Supabase Edge Functions, and Wasmer Edge (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted backup orchestration, Kubernetes-native data protection, and serverless backup automation—ideal for SREs, platform engineers, and organizations seeking transparent, vendor-neutral resilience without per-TB appliance licensing.

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Druva](https://www.druva.com/)** | Fully cloud-native SaaS data protection platform built on AWS, requiring no hardware or software deployment. Uses serverless architecture for backup, DR, and archival across endpoints, servers, VMs, and SaaS apps. Includes immutable backups, ransomware anomaly detection, and AES-256 encryption . | Quote-only (per TB/month after global deduplication; minimum 12 credits initial contract) | No permanent free tier; trial via sales |
| **[AWS Backup](https://aws.amazon.com/backup/)** | Fully managed, policy-based backup service for AWS services including EC2, EBS, RDS, DynamoDB, EFS, and Redshift Serverless. Automates backup scheduling, retention, and cross-region copy. Integrates with Lambda for custom backup actions and notifications . | Pay-per-use: backup storage ~$0.05/GB-month (warm), ~$0.01/GB-month (cold); restore and cross-region transfer billed separately | **AWS Free Tier**: limited backup storage and restore allowances for new accounts |
| **[Azure Backup](https://azure.microsoft.com/en-us/products/backup/)** | Native Azure service with policy-driven backup for VMs, SQL Server, SAP HANA, PostgreSQL, Azure Files, Blobs, and AKS. Uses Recovery Services Vault or Backup Vault as secure boundaries. Can trigger Azure Functions for custom post-backup workflows . | Pay-per-protected instance + storage consumed (LRS/GRS/RA-GRS rates) | **Azure Free Account**: $200 credit for 30 days; limited free backup storage for first 30 days |
| **[Google Cloud Backup and DR](https://cloud.google.com/backup-disaster-recovery)** | Backup and disaster recovery service for Google Cloud workloads, protecting virtual copies in native format. Manages backup lifecycle, retention, and recovery for VMs, databases, and file systems. New customers receive $300 in free credits . | Pay-per-use (backup storage + compute for backup/recovery operations) | **$300 free credits** for new Google Cloud customers (90 days) |
| **[Cloudflare Workers](https://workers.cloudflare.com/)** | Serverless compute platform for building backup APIs, webhooks, and event handlers at the edge. Can trigger backup workflows, validate webhook signatures, and route notifications without managing servers. | Free: 100,000 requests/day; Paid: $5/month (10M requests, then $0.30/million) | **Free**: 100,000 requests/day, 10ms CPU time per request, 3 scripts |
| **[Vercel Serverless Functions](https://vercel.com/)** | Serverless functions for deploying backup-related APIs and webhook handlers with Git integration. Pairs with Vercel Cron Jobs for scheduled backup triggers. | Hobby: Free (non-commercial); Pro: $20/month | **Hobby (free)**: 100 GB-hours/month function execution, 1M invocations, 100 GB bandwidth; non-commercial use only |
| **[Serverless Framework](https://www.serverless.com/)** | Open-source CLI and framework for deploying serverless functions (AWS Lambda, Azure Functions, Google Cloud Functions) with infrastructure-as-code. Can orchestrate backup workflows across cloud providers. | Free (open-source CLI); Serverless Dashboard paid tiers for team features | **Free**: full CLI functionality, unlimited deployments |
| **[Fastly Compute](https://www.fastly.com/products/edge-compute)** | Edge compute platform for running backup-related logic at the network edge. Suitable for request validation, notification routing, and lightweight orchestration. | Pay-as-you-go: $0.50/million requests + $0.01/GB egress | **Free trial**: $50 credit for new accounts |
| **[Supabase Edge Functions](https://supabase.com/edge-functions)** | Serverless Deno-based functions within the Supabase ecosystem. Can trigger database backups, send webhook notifications, and integrate with Supabase Storage for backup artifact management. | Included with Supabase plans; Free tier: 500K function invocations/month | **Free**: 500K Edge Function invocations/month, 1 GB storage, 2 GB bandwidth |
| **[Wasmer Edge](https://wasmer.io/)** | WebAssembly-based serverless platform. Can run backup orchestration logic in a lightweight, portable runtime across edge locations. | Free tier available; Pro plans for production workloads | **Free**: limited compute and request allowances for development |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Velero](https://github.com/vmware-tanzu/velero)** | [![Stars](https://img.shields.io/github/stars/vmware-tanzu/velero?style=social&color=white)](https://github.com/vmware-tanzu/velero/stargazers) | Kubernetes backup and restore tool for cluster resources and persistent volumes. Supports AWS, Azure, GCP, and on-premises storage; includes schedules, pre/post hooks, and Restic integration for volume backups . |
| **[Kanister](https://github.com/kanisterio/kanister)** | [![Stars](https://img.shields.io/github/stars/kanisterio/kanister?style=social&color=white)](https://github.com/kanisterio/kanister/stargazers) | Open-source data protection workflow management for Kubernetes. Uses blueprints to define backup/restore tasks for databases and applications; supports any object storage via provider APIs. Built-in RBAC and observability integration . |
| **[Restic](https://github.com/restic/restic)** | [![Stars](https://img.shields.io/github/stars/restic/restic?style=social&color=white)](https://github.com/restic/restic/stargazers) | Fast, secure, deduplicated backup tool with encryption. Supports S3, GCS, Azure Blob, and local storage. Can be triggered by serverless functions for event-driven backups. |
| **[snapr](https://github.com/maximseshuk/snapr)** | [![Stars](https://img.shields.io/github/stars/maximseshuk/snapr?style=social&color=white)](https://github.com/maximseshuk/snapr/stargazers) | Go-based backup orchestrator with Web UI and REST API. Supports Postgres, MySQL, MongoDB, Redis, and SQLite dumps; compression, encryption, retention per storage, and webhook/Telegram/email notifications. Single binary, Docker-ready . |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[BorgBackup](https://github.com/borgbackup/borg)** | [![Stars](https://img.shields.io/github/stars/borgbackup/borg?style=social&color=white)](https://github.com/borgbackup/borg/stargazers) | Deduplicating, authenticated backup tool with encryption. Can be invoked from Lambda/Functions for scheduled backups to S3-compatible storage. |
| **[Kopia](https://github.com/kopia/kopia)** | [![Stars](https://img.shields.io/github/stars/kopia/kopia?style=social&color=white)](https://github.com/kopia/kopia/stargazers) | Backup/restore tool with deduplication, encryption, and S3/Azure/GCS support. Includes server mode and web UI; suitable as a backup target for serverless-triggered jobs. |
| **[cloud-dr-orchestrator](https://github.com/Kobeep/cloud-dr-orchestrator)** | [![Stars](https://img.shields.io/github/stars/Kobeep/cloud-dr-orchestrator?style=social&color=white)](https://github.com/Kobeep/cloud-dr-orchestrator/stargazers) | Multi-cloud DR orchestrator with automated scheduling, encryption, and restore workflows. Can be paired with serverless triggers for cross-cloud failover. |

**Frameworks for building custom systems**: Combine **Velero** for Kubernetes workload protection, **Kanister** for application-consistent database backups, **Restic** or **Kopia** for encrypted object storage backups, and **snapr** for a lightweight REST-driven orchestrator—all triggerable via AWS Lambda, Azure Functions, or Cloudflare Workers for a fully serverless backup architecture.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Serverless backup architectures must account for execution time limits (e.g., Lambda 15-minute max), cold start latency, and idempotency to avoid duplicate or incomplete backups.
- Self-hosted open-source solutions require proper IAM scoping, encryption key management, and restore testing; serverless triggers should be secured with least-privilege roles and signed webhooks.

---

**Made for SREs, platform engineers, cloud architects, and developers building event-driven data protection.**  
Let's make serverless backup architecture more open, observable, and resilient.
