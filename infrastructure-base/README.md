# infrastructure-base

This is a meta-application chart that manages the dependency relationships between core infrastructure services.

## Architecture Overview

The infrastructure-base chart acts as an orchestrator for:
- **sealed-secrets**: Secure secret management using Bitnami's sealed-secrets controller
- **postfix**: Mail server implementation  

## Deployment Flow

1. `infrastructure-base` - Meta-application that manages relationships between components
2. `sealed-secrets` - Independent ArgoCD application for Sealed Secrets deployment  
3. `postfix` - Independent ArgoCD application for Postfix mail server

This structure follows GitOps best practices where each service is independently deployable while maintaining proper dependency management through ArgoCD.

## Configuration

Configuration values are passed through to the respective child applications:
- `sealedSecrets.enabled`: Controls sealed-secrets deployment
- `postfix.enabled`: Controls postfix deployment

## Usage

To manage infrastructure components:
1. Deploy all three applications in ArgoCD
2. The meta-application ensures proper ordering and relationship management
3. Each service can be updated independently through its own application
