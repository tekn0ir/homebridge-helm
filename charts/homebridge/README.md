# Homebridge Helm Chart

This chart deploys Homebridge to a Kubernetes cluster.

> The implementation of the Helm chart is right now the bare minimum to get it to work.

## Usage
Use the HelmChart to deploy the Homebridge to a Device.

```yaml
---
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: homebridge
  namespace: default
spec:
  repo: https://tekn0ir.github.io/homebridge-helm
  chart: homebridge
  targetNamespace: default
  valuesContent: |-
    # Example for minimal configuration
    
```

## Adding the repository

```bash
helm repo add tekn0ir-homebridge https://tekn0ir.github.io/homebridge-helm/
```

## Installing the chart

```bash
helm install homebridge tekn0ir-homebridge/homebridge -f values.yaml
```