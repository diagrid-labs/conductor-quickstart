# Conductor Quickstart

## Overview
The Conductor Quickstart project streamlines the deployment of a Daprized application based on the [Hello Kubernetes](https://github.com/dapr/quickstarts/tree/master/tutorials/hello-kubernetes) tutorial from the Dapr project. This simplified project repository contains only the essential deployment and configuration files required to get started quickly.

## Application Components
- **Python App**: Generates messages.
- **Node App**: Persists the messages into a Redis state store.

## Getting Started
To deploy this application, ensure that you have Conductor connected to your Kubernetes environment. Follow the detailed steps in our [Conductor Quickstart Documentation](https://docs.diagrid.io/conductor/getting-started/quickstart) to set up the environment and deploy this application.

## Deployment
This repository is designed to make the deployment process as straightforward as possible.

Apply Kubernetes resources directly from the remote GitHub repository:

```bash
$ kubectl apply -f https://raw.githubusercontent.com/diagrid-labs/conductor-quickstart/main/deploy.yaml
```

For more detailed information and further steps, please refer to the Conductor Quickstart Documentation linked above.

