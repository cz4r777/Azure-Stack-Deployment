# Azure-Projuction-Environment
Azure Prototype Topology Diagram

============================================
1. topology-diagram.md
(Pure Markdown — GitHub‑ready)
============================================
markdown
# Azure Production Topology Diagram

This document provides a clean, resume‑ready 2D ASCII topology diagram representing the minimal Azure prototype environment used for demonstrating identity, endpoint management, and cloud infrastructure capability.

Code
## Modern Cloud Endpoint Architecture (Public‑Safe)

                          Azure Region
                        (US West 3)

                             │
                             ▼
                   Secure Cloud Access Layer
                             │
                             ▼
                 Public IP Address (Static)
                 - Standard inbound access controls
                             │
                             ▼
                 Azure Load Balancer
                 - Basic inbound mapping for management access
                             │
                             ▼
                 Virtual Machine (General Purpose)
                 - Modern Windows OS
                 - Cloud identity joined
                 - Centrally managed
                 - Security baseline applied
                 - Endpoint protection enabled
                             │
                             ▼
                 Network Interface (NIC)
                 - Private addressing
                 - Network security applied
                             │
                             ▼
                 Virtual Network (VNet)
                 - Private address space
                 - Segmented subnet design
                 - Network security applied
                             │
                             ▼
                 Cloud Identity Platform
                 - Authentication
                 - Device identity
                 - Access control
                 - Conditional Access
                             │
                             ▼
                 Microsoft 365 Platform
                 - Cloud productivity services
                 - File storage and collaboration
                 - Device and application management
                 - Security and compliance capabilities
                             │
                             ▼
                 Unified Endpoint Management
                 - Windows device enrollment
                 - Mobile device enrollment
                 - Configuration and compliance
                 - Application deployment
                 - Security integration
                             │
                             ▼
                 Endpoint Security Platform
                 - Threat detection and response
                 - Device risk scoring
                 - Security posture insights
                             │
                             ▼
                 Mobile Device Platform (Android Enterprise)
                 - Work Profile separation
                 - Managed application deployment
                 - Corporate data protection
                 - Privacy‑preserving BYOD model

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
