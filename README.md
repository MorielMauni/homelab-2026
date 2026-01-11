### Home-Lab 2026

Remaking my home-lab just for the Kubernetes training and make sure my documentes are up on everything.
Making on a VM on my Proxmox machine.

### Updates

**11/1/26 Updates:**
File tree for infrastructure:

```
infrastructure
└── controllers
    ├── base
    │   ├── kustomization.yaml
    │   └── renovate
    │       ├── configmap.yaml
    │       ├── cronjob.yaml
    │       ├── kustomization.yaml
    │       ├── namespace.yaml
    │       └── renovate-container-env.yaml
    └── staging
        ├── kustomization.yaml
        └── renovate
            └── kustomization.yaml

 
```

- Added in root directory `renovate.json`.
- Added in `/cluster/staging/infrastructure.yaml`.

**10/1/26 Updates:**

- Edited `monitoring/controllers/base/kube-prometheuse-stack/release.yaml` to have ingress.
- Added `monitoring/configs/staging/kube-prometheuse-stack/grafana-tlc-secret.yaml`.
- Added `monitoring/configs/staging/kube-prometheuse-stack/staging/kustomization.yaml`.
- Added `monitoring/configs/staging/kustomization.yaml`.
- Edited `/clusters/flux-system/monitoring.yaml`.

**8-9/1/26 Updates:**

Adding Prometheus monitoring with Helm:
files tree:

Fixed file tree with all the updates from 8/1/26 to 10/1/26

```
monitoring
├── configs
│   └── staging
│       ├── kube-prometheus-stack
│       │   ├── grafana-tls-secret.yaml
│       │   └── kustomization.yaml
│       └── kustomization.yaml
└── controllers
    ├── base
    │   └── kube-prometheus-stack
    │       ├── kustomization.yaml
    │       ├── namespace.yaml
    │       ├── release.yaml
    │       └── repository.yaml
    └── staging
        ├── kube-prometheus-stack
        │   └── kustomization.yaml
        └── kustomization.yaml
```

- Added `/clusters/staging/monitoring.yaml`

**7/1/26 Updates:**

- Installed:
  - `brew install sops`
  - `brew install age`
- Created `clusters/staging/.sops.yaml` to point the encryption.
- Edited `clusters/staging/apps.yaml` to know to decrypt SOPS
- Re-deployed linkding with SOPS:
  - Created a secret for CloudFlare `cloudflare-secret.yaml`.
  - Created a secret for linkding user `linkding-container-env-secret.yaml`.

linkding was Re-deployed with secrets now.

**6/1/26 Updates:**

Storage:

- Added `linkding/storage.yaml` as a PVC.
- Updated `linkding/deployment.yaml` to list the storage.

Security:

- Pod using 'www-data' user and not root.
- Removed `Privilege Escalation`.

CloudFlare:

- Created tunnels for CloudFlare through CloudFlared.
- Created `app/base/linkding/service,yaml`

First app was deployed! linkding is up on the web.
**5/1/26 Updates:**
Deployed first app: Linkding.

Created files:

- `clusters/staging/apps.yaml`
- `/apps/staging/linkding/`
- `apps/base/linkding/`
  - `linkding/deployment.yaml`
  - `linkding/kustomization.yaml`
  - `linkding/namespace.yaml`

**4/1/26 Updates:**

Starting point:

- Created a `.devcontinaer.json`.
- Installed `brew`.
- Installed `flux`.
  - Bootstrap flux to the cluster.

### Tech Slack

- K3S: core.
- FluxCD: GitOps options of choice.
- DevContainers: working environment.
- Linux
- GitOps: method of work.
- kubectx
- CloudFlare: tunnels.
- SOPS: encrypt secrets in Kubernetes.
- renovate: Automated dependency updates.
