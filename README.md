# test-app Helm chart

A minimal nginx application chart intended for Harness GitOps testing.

## Install

```sh
helm upgrade --install test-app ./test-app --namespace gitops-test --create-namespace
```

The chart creates a Deployment and ClusterIP Service. The image, replica count,
service type, service port, and resource requests/limits can be overridden with
Helm values.

For example, to scale the test workload:

```sh
helm upgrade --install test-app ./test-app \
  --namespace gitops-test \
  --set replicaCount=2
```
