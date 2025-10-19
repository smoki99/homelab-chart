# Active Context: homelab-chart

## Current Work Focus
The current focus is on establishing the foundational Helm chart structure for managing a homelab k3s infrastructure with ArgoCD integration. This includes implementing core services like Sealed Secrets and Postfix mail server.

## Recent Changes
- Created project brief documentation
- Defined product context and requirements
- Setting up base Helm chart structure

## Next Steps
1. Create the main Helm chart structure for infrastructure base application
2. Configure Sealed Secrets chart integration from Bitnami
3. Implement Postfix server deployment using bokysan/docker-postfix
4. Set up ArgoCD application manifests for proper deployment orchestration

## Active Decisions and Considerations
- Using remote chart dependencies for Sealed Secrets to leverage official Bitnami charts
- Including Postfix as an additional service in the base infrastructure
- Following Helm best practices for multi-service deployments
- Planning for future extensibility of the chart structure

## Important Patterns and Preferences
- GitOps workflow with ArgoCD as deployment mechanism
- Use of remote charts for well-maintained dependencies
- Consistent naming conventions and directory structures
- Proper separation of concerns between services

## Learnings and Project Insights
The project benefits from starting with a clear documentation foundation before implementing the technical components. This ensures all requirements are properly understood and documented.

## Implementation Strategy
This is a foundational chart that will serve as the base for managing all infrastructure in the homelab environment, following GitOps principles through ArgoCD.
