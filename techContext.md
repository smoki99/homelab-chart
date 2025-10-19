# Tech Context: homelab-chart

## Technologies Used
- **Helm 3**: Package manager for Kubernetes applications
- **Kubernetes (k3s)**: Lightweight Kubernetes distribution for homelab use
- **ArgoCD**: GitOps continuous delivery tool for Kubernetes
- **Docker**: Containerization platform for application deployment
- **Git**: Version control system for infrastructure as code

## Development Setup
- Local development environment: Linux Mint 22.2
- Helm CLI installed and configured
- Kubectl CLI installed and configured
- ArgoCD CLI installed and configured
- Git repository initialized for version control

## Technical Constraints
- Must work with k3s cluster (1 master, 2 worker nodes)
- Follow Helm best practices for chart structure and packaging
- Maintain compatibility with ArgoCD deployment workflows
- Ensure proper resource definitions for all deployed services
- Support configuration through values.yaml files

## Dependencies
- **Sealed Secrets**: Official Bitnami Helm chart dependency
- **Postfix Server**: bokysan/docker-postfix Docker image
- **Kubernetes API server**: For manifest deployment

## Tool Usage Patterns
- Using `helm create` to initialize chart structure
- Leveraging remote chart repositories for dependencies
- Implementing values.yaml files for configuration management
- Following GitOps patterns with ArgoCD for deployment orchestration

## Configuration Management
- All service configurations will be managed through Helm values
- Environment-specific overrides supported via value files
- Default configurations provided but easily customizable
