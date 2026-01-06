### Home-Lab 2026

Remaking my home-lab just for the Kubernetes training and make sure my documentes are up on everything.
Making on a VM on my Proxmox machine.

### Updates

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

- K3S
- FluxCD
- DevContainers
- Linux
- GitOps
- kubectx
- CloudFlare: tunnels
