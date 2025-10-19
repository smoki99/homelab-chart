# Project Brief: homelab-chart

## Overview
This project is a Helm chart repository designed to manage and configure a homelab Kubernetes infrastructure running on k3s with 1 master node and 2 worker nodes. The charts will be used with ArgoCD for GitOps deployment.

## Core Requirements
- Independent Sealed Secrets chart from Bitnami for secret management
- Postfix server implementation using bokysan/docker-postfix image
- Proper Helm chart structure with dependencies and configurations

## Project Scope
This is a streamlined chart repository that provides independent management of core infrastructure components in the homelab environment through ArgoCD.

## Success Criteria
- Complete working Helm charts that can be deployed to k3s cluster
- Independent integration of Sealed Secrets and Postfix services  
- Ready-to-use configuration for ArgoCD deployment
