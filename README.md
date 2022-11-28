# Elastic AIOPS Demo

This demo shows the 

is built on top of the [opentelemetry-demo](https://github.com/open-telemetry/opentelemetry-demo)

## Prerequisites

- An Elastic Deployment (we recommend using [Elastic Cloud](https://cloud.elastic.co))
- A Kubernetes Cluster
- [Helm](https://helm.sh/) 


## Install the Chart

Add OpenTelemetry Helm repository:

```shell
helm repo add aiops demo https://open-telemetry.github.io/opentelemetry-helm-charts
```

To install the chart with the release name my-otel-demo, run the following command:

```shell
helm install my-otel-demo open-telemetry/opentelemetry-demo
```


