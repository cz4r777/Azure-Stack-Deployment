# Azure-Prototype-Environment
Azure Prototype Topology Diagram

============================================
1. topology-diagram.md
(Pure Markdown — GitHub‑ready)
============================================
markdown
# Azure Prototype Topology Diagram

This document provides a clean, resume‑ready 2D ASCII topology diagram representing the minimal Azure prototype environment used for demonstrating identity, endpoint management, and cloud infrastructure capability.

Code
                          Azure Region
                    (Australia Southeast)

                             │
                             ▼
                   Public Internet (RDP/SSH)
                             │
                             ▼
                 Public IP Address (Static, Basic)
                             │
                             ▼
                 Azure Load Balancer (Basic SKU)
                 • Inbound NAT Rule:
                   - Port 50001 → 3389 (RDP)
                 • No Firewall
                 • No NAT Gateway
                             │
                             ▼
                 Virtual Machine (B1s)
                 • Windows or Ubuntu
                 • Entra ID Join / Hybrid Join
                 • Intune-managed
                             │
                             ▼
                 Network Interface (NIC)
                 • Private IP only
                 • NSG with minimal inbound rules
                             │
                             ▼
                 Virtual Network (VNet)
                 • 10.0.0.0/16
                 • mgmt-subnet (10.0.0.0/24)
                             │
                             ▼
                 Microsoft Entra ID (Tenant)
                 • Identity backbone
                 • Authentication
                             │
                             ▼
                 Microsoft Intune
                 • Device compliance
                 • Configuration profiles
                 • App deployment
                             │
                             ▼
                 Microsoft 365 Services
                 • Exchange Online
                 • SharePoint / OneDrive
                 • Teams
markdown
This topology reflects a minimal-cost, production-pattern Azure environment suitable for demonstrating modern cloud identity, endpoint management, and infrastructure skills.
============================================
8. public-redacted.md
(Strong visual formatting)
============================================
markdown
# PUBLIC VERSION — REDACTED

## Azure Prototype Environment

A Production-pattern Azure environment demonstrating:

- Identity (Entra ID)
- Endpoint Management (Intune)
- Security (Defender)
- Infrastructure (VM, VNet, Load Balancer)
- IaC (Bicep, PowerShell, Terraform)

## Architecture Diagram (Simplified)

Public IP → Load Balancer → NAT → VM → Intune → Defender → M365

## Purpose

Demonstrates capability to design, deploy, and manage a modern cloud environment aligned with current industry expectations.

## Redacted Elements

- Internal domain names
- Admin accounts
- Subscription details
- Billing configuration
- Internal scripts
============================================
6. iac-tooling-overview.md
(Pure Markdown — GitHub‑ready)
============================================
markdown
# Infrastructure as Code Tooling Overview

This document describes where Bicep, PowerShell, and Terraform are used in the Azure prototype environment.

## Bicep
Used for:
- VNet and subnet creation
- NIC creation
- Public IP
- Load Balancer + NAT rules
- VM deployment
- NSG rules

## PowerShell
Used for:
- Entra ID automation
- Intune device onboarding
- VM configuration scripts
- Local hardening tasks

## Terraform
Used for:
- Cross-cloud portability
- Demonstrating multi-cloud IaC capability
- Mirroring Bicep modules for comparison
============================================
