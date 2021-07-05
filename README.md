# Data tools Helm charts


## Quickstart

```
helm repo add data-tools-on-k8s https://misurin.github.io/data-tools-on-k8s/
```

## Development

To manually package and deploy helm chart to GitHub repo:

```
CHART_NAME=<name of the helmchart dir>
helm package ./$CHART_NAME -d packages
helm repo index .
```

//TODO: Automate this part with Github Action.