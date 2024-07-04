![[Pasted image 20240630135950.png]]
Standard login-info
```
user: admin
password: prom-operator
```
https://grafana.com/docs/grafana/latest/setup-grafana/
## What is Grafana?

## What is the *simplest way of setting it up?*
The simplest way to setup Grafana (from my research) is probably to use MicroK8s with the service *observability*.  A guide for this can be found at [Debian 12 config guide](https://www.server-world.info/en/note?os=Debian_12&p=microk8s&f=8). 
Short:
1. Enable observability
```
microk8s enable observability
```
2. Check services
```
microk8s kubectl get services -n observability
```
3. Check pods
```
microk8s kubectl get pods -n observability
```
4. Set port-forwarding to enable external access
```
#Prometheus UI
microk8s kubectl port-forward -n observability service/prometheus-operated --address 0.0.0.0 9090:9090

#Grafana UI
microk8s kubectl port-forward -n observability service/kube-prom-stack-grafana --address 0.0.0.0 3000:80
```

### Running Grafana as a service
You can use multiple methods of running grafana as a service on Linux:
- systemd
- init.d
- binary
- docker
## What is the *best* way of setting it up with Kubernetes+Ansible+Prometheus


## What are some good practices when developing with Grafana?
### User management
### 

## What display options do we have

## The network layer 

## Monitoring [[Kubernetes]] clusters

### Performance metrics

1. Node Resource util metrics
2. Object capacity and health
3. Storage health
4. Kubelet metrics
### Kubernetes logs
1. Common logs
2. Traces
3. Kubernetes Events 


