# dbt-docs-server-helm-chart

DBT (Data Build Tool) - https://www.getdbt.com/

## Introduction

This chart will bootstrap an DBT docs server deployment on a Kubernetes cluster using the Helm package manager.
A pod contains 3 containers:

- git-sync: to periodically download changes from the remote Git repo,
- doc-sync: to regenerate the dbt catalog once the changes are detected.
- doc-server: to serve the doc to the UI. This forms a normal web application together with K8S service and Ingress resource.
## Requirements
- Kubernetes 1.14+ cluster
- Helm 2.11+ or Helm 3.0+

## Features
 - Self-managed DBT document server
 - Auto detect changes from Git and re-generate documents

## Quickstart

Use `values-example.yaml` for quick start, update the values arcordingly.

Usage:
```
NS=dbt
helm -n $NS upgrade --install . -f values-sample.yaml
```