Basic Demonstration Microservice Mesh with Istio
===
![Kiali Console](https://user-images.githubusercontent.com/618412/120837175-99217000-c590-11eb-917c-eb3fd6dde4c6.png)


# Quick Start
1. Provision a Kubernetes Cluster.
2. Install Istio with addons Prometheus, Grafana, Kiali, Jaeger.
```bash
$ cd app-1

# Create namespace
$ kubectl create namespace app-1

# Set automation sidecar injection for this namespace
$ kubectl label namespace app-1 istio-injection=enabled

# Create deployment, service, destination rules, gateway
$ kubectl apply -f .
```
3. Open Kiali Dashboard for visualizing service mesh
```bash
$ istioctl dashboard kiali
```