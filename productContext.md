# Product Context: homelab-chart

## Why This Project Exists
The homelab-chart project addresses the need for a centralized, GitOps-based infrastructure management solution for personal Kubernetes homelab environments. It provides a structured approach to deploying and managing essential services in a k3s cluster.

## Problems This Solves
- Complex manual configuration of homelab infrastructure components
- Inconsistent secret management across services
- Lack of declarative infrastructure as code practices
- Difficulty maintaining multiple service configurations

## How It Should Work
The project provides Helm charts that can be managed through ArgoCD, allowing for:
1. Declarative infrastructure definition using Kubernetes manifests
2. Version-controlled configuration changes
3. Automated deployment and synchronization with the cluster state
4. Centralized management of core services like secrets and mail servers

## User Experience Goals
- Simple setup process with clear documentation
- Reliable deployments that maintain system stability
- Easy to extend for additional infrastructure components
- Consistent interface across all charts in the repository

## Core Services
1. **Sealed Secrets** - Secure secret management using Bitnami chart
2. **Postfix Mail Server** - Email service implementation with docker image
3. **Infrastructure Base** - Foundation for other services to be deployed

## Technical Approach
- Helm 3 charts following best practices
- ArgoCD integration for GitOps deployment
- Multi-node k3s cluster support (1 master, 2 workers)
- Remote chart dependencies management
