# Elastic AIOPS Demo

This demo shows how to implement AIOPS using the Elastic Stack, it is built on top of the [opentelemetry-demo](https://github.com/open-telemetry/opentelemetry-demo).


<kbd><img src="screenshots/2022-11-28-13-34-10.png" width="640"></kbd>

## Prerequisites

- An Elastic Deployment (we recommend using [Elastic Cloud](https://cloud.elastic.co))
- A Kubernetes Cluster
- [Helm](https://helm.sh/) 


## Install the Chart

Add OpenTelemetry Helm repository:

```shell
helm repo add aiops-demo https://open-telemetry.github.io/opentelemetry-helm-charts
```

To install the chart with the release name `aiops-demo`, run the following command:

```shell
helm install aiops-demo open-telemetry/opentelemetry-demo
```

Update the `values.yml` file with the corresponding APM endpoint and credentials: 
```yml
...
exporters:
  otlp/http:
    endpoint: "https://YOUR-APM-ENDPOINT-HERE:443"  
    headers:
      Authorization: "Bearer YOUR-APM-SECRET-TOKEN-HERE"  
...
```

then run:

```shell
helm upgrade aiops-demo open-telemetry/opentelemetry-demo -f values.yml     
```
