# homelab-chart

## Overview
This repository contains Helm charts for managing a home lab Kubernetes environment with GitOps practices using ArgoCD.

## Architecture
The project uses a modular approach with independent service deployments rather than a single meta-application structure. Each core service (Postfix, Sealed Secrets) is managed as its own ArgoCD application.

## Key Components

### Services
- **Postfix**: Mail server implementation
- **Sealed Secrets**: Kubernetes secrets management solution

### Infrastructure Management
The infrastructure-base chart has been deprecated in favor of independent service deployments that provide better modularity and maintainability.

## Documentation

### Memory Bank
For detailed troubleshooting guides, patterns, and best practices:
- `memory-bank/infrastructure-resolution-notes.md` - Issue resolution documentation
- `memory-bank/argocd-meta-application-patterns.md` - Meta-application implementation patterns

## Deployment Approach
Services are deployed independently through their own ArgoCD applications following GitOps principles with automated sync policies.

## Status
All services are properly configured and functioning. The restructuring from a meta-application approach to independent deployments has been completed successfully.
