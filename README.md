# kube-mongo

A Kubernetes-ready MongoDB deployment for development and production environments.

## Features

- Easy deployment of MongoDB on Kubernetes
- Configurable replica sets
- Persistent storage support
- Health checks and readiness probes

## Prerequisites

- [Kubernetes](https://kubernetes.io/) cluster (v1.18+)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Minikube](https://minikube.sigs.k8s.io/docs/) (for local clusters)
- [Docker](https://www.docker.com/) (for building and running containers)

## Quick Start

### 1. Clone the repository

```sh
git clone https://github.com/yourusername/kube-mongo.git
cd kube-mongo
```

### 2. Deploy with kubectl

```sh
kubectl apply -f k8s/
```

## Configuration

Edit the files in the `k8s/` directory to customize:

- Replica count
- Storage class and size
- MongoDB version
- Resource requests/limits

## Accessing MongoDB

To connect from your local machine:

```sh
kubectl port-forward svc/mongo 27017:27017
```

Then connect using your preferred MongoDB client.

## Cleanup

```sh
kubectl delete -f k8s/
```

## License

MIT License. See [LICENSE](LICENSE) for details.