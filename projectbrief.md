# Project Brief: homelab-chart

## Overview
This project is a Helm chart repository designed to manage and configure a homelab Kubernetes infrastructure running on k3s with 1 master node and 2 worker nodes. The charts will be used with ArgoCD for GitOps deployment.

## Core Requirements
- Infrastructure base application for homelab k3s cluster
- Sealed Secrets chart from Bitnami for secret management
- Postfix server implementation using bokysan/docker-postfix image
- Proper Helm chart structure with dependencies and configurations

## Project Scope
This is the foundational chart repository that will serve as the basis for managing all infrastructure components in the homelab environment through ArgoCD.

## Success Criteria
- Complete working Helm charts that can be deployed to k3s cluster
- Proper integration of Sealed Secrets and Postfix services
- Ready-to-use configuration for ArgoCD deployment
