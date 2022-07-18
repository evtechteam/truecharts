# Introduction

Create fully functional virtual Kubernetes clusters - Each vcluster runs inside a namespace of the underlying k8s cluster. It's cheaper than creating separate full-blown clusters and it offers better multi-tenancy and isolation than regular namespaces.

## Source Code

* <https://github.com/loft-sh/vcluster>

## Requirements

Kubernetes: `>=1.16.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| https://github.com/loft-sh/vcluster | vcluster | 0.11.0 |

## vcluster Kube Config

Run the following from TrueNAS Shell to export kube config
```
k3s kubectl get secret vc-vcluster -n ix-vcluster --template={{.data.config}} | base64 -d
```

Change the URL in the kubeconfig to `https://truenas-ip:6443`
