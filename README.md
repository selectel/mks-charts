# About this repository

This repository is used to install [applications](https://docs.selectel.ru/managed-kubernetes/clusters/applications/) in Managed Kubernetes. You can install or update helm charts directly through this repository. For example:
```bash
helm install myrelease oci://ghcr.io/selectel/ingress-nginx:4.12.1
```

# CI/CD

Building of helm charts is done through GitHub Actions. 
[release.yaml](https://github.com/selectel/mks-charts/blob/main/.github/workflows/release.yml) detects changes and collects the chart in [packages](https://github.com/orgs/selectel/packages?repo_name=mks-charts).

To create a new helm chart: push the new chart to main branch in . /charts folder and create an app-name/chart-version tag.
