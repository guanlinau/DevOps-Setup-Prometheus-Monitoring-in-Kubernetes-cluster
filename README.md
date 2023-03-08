### Setup Prometheus Monitoring in Kubernetes cluster

### Technologies used:

Kubernetes, Helm, Prometheus

### Project Description:

1- Deploy Prometheus in local Kubernetes cluster using a Helm chart

2- Browser the Grafana UI

3- Browser the Prometheus UI

### Instructions:

###### Step 1: Run cluster by minikube

```
minikube start
```

###### Step 2: Add prometheus repo

```
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
```

```
helm repo update
```

###### Step 4: Install prometheus operator helm chart

```
helm install prometheus prometheus-community/kube-prometheus-stack
```

or

```
helm install prometheus prometheus-community/kube-prometheus-stack --version "9.4.1"
```

###### Step 6: Browser Grafana UI via port 3000 by port-forward

```
kubectl port-forward deployment/prometheus-grafana 3000
```

###### Step 7: Browser Prometheus UI via port 9090 by port-forward

```
kubectl port-forward prometheus-prometheus-prometheus-oper-prometheus-0 9090
```
