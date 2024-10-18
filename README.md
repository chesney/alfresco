# Alfresco Installation

This is an argocd project to install Alfresco using ArgoCD ApplicationSet and Application Templates for the subcomponents.

## Directory Structure

.
├── apps
│   ├── alfresco
│   │   └── values.yaml         # Helm values for Alfresco
│   ├── postgresql
│   │   └── values.yaml         # Helm values for PostgreSQL
│   └── configmap
│       └── alfresco-configmap.yaml  # ConfigMap for Alfresco settings
└── argocd
    └── applicationset.yaml     # ArgoCD ApplicationSet manifest


# Information
The `alfresco-app.yaml` file is an argocd `Application` that will deploy the argocd alfresco `ApplicationSet`. This is the only workaround to deploy an `ApplicationSet` using argocd and not the `kubectl apply` command.