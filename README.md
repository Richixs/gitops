# GitOps Repository

Personal Kubernetes infrastructure managed using GitOps principles with ArgoCD.

## 📋 About

This repository serves as the single source of truth for all Kubernetes deployments in my personal infrastructure. Using the GitOps methodology, every change to the cluster state is made through Git commits, enabling version control, audit trails, and automated deployments.

## 🛠️ Technologies

- **ArgoCD**: Continuous deployment tool for Kubernetes
- **Kustomize**: Template-free customization of Kubernetes manifests
- **Kubernetes**: Container orchestration platform

## 🏗️ Structure

```
.
├── apps/                       # Application manifests
│   └── <app-name>/            # Your applications here
│       ├── base/              # Base Kustomize configuration
│       └── overlays/          # Kustomization and Ingress configs
│           └── <env>/         # kustomization.yaml and ingress.yaml
├── argocd/                    # ArgoCD configuration
│   ├── root.yaml              # Root ArgoCD Application (App of Apps)
│   └── applications/          # ArgoCD Application definitions
│       └── <app-name>/        # Application-specific ArgoCD configs
└── namespaces/                # Namespace definitions
    └── <app-name>/            # Application namespace configs
```
