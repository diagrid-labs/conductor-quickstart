# Conductor Quickstart

## Overview
This is an accompanying repository for the [Conductor Quickstart](https://docs.diagrid.io/conductor/getting-started/quickstart)  documentation. It contains only the essential deployment and configuration files needed to quickly deploy the [Hello Kubernetes](https://github.com/dapr/quickstarts/tree/master/tutorials/hello-kubernetes) application into Kubernetes and explore its capabilities with Diagrid Conductor.


## Getting Started
To deploy this application, ensure that you have Conductor connected to your Kubernetes environment. Follow the detailed steps in  [Conductor Quickstart Documentation](https://docs.diagrid.io/conductor/getting-started/quickstart) to set up your environment.

## Deployment
This application comprises a Python App that generates messages and a Node App that stores these messages in a Redis state store. Follow these steps to deploy a Redis instance and the application into Kubernetes.

Install Redis using Helm:

```bash
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
helm install redis bitnami/redis --set cluster.enabled=false --set replica.replicaCount=0 --set fullnameOverride=dapr-dev-redis
```

Apply the Kubernetes resources directly from the GitHub repository to deploy the applications:

```bash
kubectl apply -f https://raw.githubusercontent.com/diagrid-labs/conductor-quickstart/main/deploy.yaml
```

## More info
For more detailed information and further steps, please refer to the [Conductor Quickstart Documentation](https://docs.diagrid.io/conductor/getting-started/quickstart) or visit the [Conductor page](https://www.diagrid.io/conductor) on the Diagrid website to learn about how Conductor can help you operate Dapr applications on Kubernetes.

