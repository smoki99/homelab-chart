# Infrastructure Base Helm Chart

This is a foundational Helm chart for managing homelab k3s infrastructure with ArgoCD.

## Overview

This chart provides the base infrastructure components for your homelab environment, including:
- Sealed Secrets from Bitnami (for secure secret management)
- Postfix mail server implementation

## Prerequisites

- Kubernetes 1.19+
- Helm 3+

## Installing the Chart

```bash
helm install infrastructure-base ./infrastructure-base
```

## Configuration

The following table lists the configurable parameters for this chart and their default values.

| Parameter | Description | Default |
|-----------|-------------|---------|
| `sealedSecrets.enabled` | Enable Sealed Secrets chart integration | `true` |
| `postfix.enabled` | Enable Postfix server deployment | `true` |
| `postfix.image` | Postfix Docker image name | `bokysan/docker-postfix` |
| `postfix.imageTag` | Postfix Docker image tag | `latest` |
| `postfix.config.domain` | Mail domain configuration | `example.com` |
| `postfix.config.hostname` | Mail hostname configuration | `mail.example.com` |

## ArgoCD Integration

This chart is designed to work with ArgoCD. The application manifest can be found in `argocd-application.yaml`.

## Dependencies

- Sealed Secrets (Bitnami Helm Chart)

## Notes

1. Make sure you have the Bitnami repository added:
   ```bash
   helm repo add bitnami https://charts.bitnami.com/bitnami
   ```

2. For production use, consider customizing values for resource limits and security contexts.
