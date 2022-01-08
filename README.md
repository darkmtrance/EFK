# EFK

>We’ll be using ElasticSearch (Storage), Fluentd (Logging Layer), and Kibana (Visualization) to store, aggregate & visualise logs.

## Requirements

- kubectl (check via kubectl version)
- a working kube-context with access to a Kubernetes cluster (check with kubectl get namespaces)

## Steps

- get file EFK

```
git clone https://github.com/darkmtrance/EFK.git
cd EFK
```

- install EFK

```
kubectl apply -f .
```