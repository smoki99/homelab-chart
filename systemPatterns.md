# System Patterns: homelab-chart

## System Architecture
The homelab-chart follows a GitOps architecture using Helm charts and ArgoCD for infrastructure management. The system is designed around the concept of declarative configuration where cluster state matches the desired state defined in the repository.

## Key Technical Decisions
1. **Helm 3 Charts**: Using Helm 3 for chart management without Tiller, leveraging modern Kubernetes deployment patterns
2. **Remote Chart Dependencies**: Leveraging official Bitnami charts for Sealed Secrets to ensure reliability and maintainability
3. **Multi-Service Approach**: Bundling core infrastructure services in a single base application chart
4. **ArgoCD Integration**: Using ArgoCD for continuous synchronization of desired state with cluster

## Design Patterns in Use
1. **Composite Chart Pattern**: Combining multiple service deployments (Sealed Secrets + Postfix) within a single Helm chart
2. **Dependency Management Pattern**: Using remote chart dependencies for well-maintained components
3. **Configuration Abstraction Pattern**: Separating deployment configuration from base manifests
4. **GitOps Workflow Pattern**: Maintaining infrastructure as code with version control

## Component Relationships
- **Infrastructure Base Chart** serves as the root chart containing:
  - Sealed Secrets (Bitnami remote chart)
  - Postfix Server (custom deployment)
- All components are deployed to the same namespace or appropriately separated namespaces
- Configuration is passed through values.yaml files for easy customization

## Critical Implementation Paths
1. **Chart Structure Setup**: Proper Helm directory layout and metadata
2. **Remote Dependency Integration**: Correctly configuring Bitnami chart dependencies
3. **Service Deployment**: Implementing Postfix server as a Kubernetes deployment
4. **ArgoCD Manifest Creation**: Generating proper application definitions for GitOps

## Deployment Flow
1. ArgoCD monitors the repository for changes
2. Helm charts are rendered with appropriate values
3. Kubernetes manifests are applied to the cluster
4. Cluster state synchronizes with desired state
