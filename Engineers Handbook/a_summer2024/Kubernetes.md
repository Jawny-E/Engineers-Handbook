**Table of Contents**

- [[#Questions|Questions]]
- [[#Dictionary|Dictionary]]
- [[#What Kubernetes *does*|What Kubernetes *does*]]
- [[#What Kubernetes *cannot* do|What Kubernetes *cannot* do]]
- [[#Kubernetes - beyond the overview|Kubernetes - beyond the overview]]
	- [[#Questions#Architecture|Architecture]]
	- [[#Questions#Deployments|Deployments]]
	- [[#Questions#Volumes|Volumes]]
	- [[#Questions#Secrets|Secrets]]
	- [[#Questions#Kubectl|Kubectl]]
	- [[#Questions#ConfigMap|ConfigMap]]
- [[#Micro Kubernetes - Canonical|Micro Kubernetes - Canonical]]
- [[#History of Kubernetes|History of Kubernetes]]

### Questions
- ~~What is PaaS?~~
- Whats the difference between stateless, stateful and data-processing workloads?
- How is Continuous Integration/Deployment implemented?
- ==How is Kubernetes installed/set up on each individual Node?==
	- How is the system managed, is there a "controller node"?
	- What operating systems are "the smartest" to use?
	- How does one add additional nodes to the cluster?
	- How are applications distributed between clusters?
- ==How does the MicroK8 differ from the full K8?==
- How does the network layer function in this setup?
	- Connected to WWW or entirely local?
	- Wireless or Ether?
	- Dynamic or Static IP-addresses?
	- Are the nodes connected to a DNS system?
- What rules should we follow regarding authorization?
- ==How does it integrate with Prometheus and by extension Grafana?==
- What data am I interested in monitoring, for that matter what data can I get?
- How is Kubernetes integrated with the jigs/dev kits?
- How can I create a test-system that is transferable to the Nordic Semiconductor system?
- What is .yaml used for in Kubernetes?

## Dictionary

| Term             | Short                                |
| ---------------- | ------------------------------------ |
| Virtual Machine  |                                      |
| Application      |                                      |
| Containers       | A way to bundle and run Applications |
| Pods             |                                      |
| Cluster          |                                      |
| Kube             |                                      |
| Highly available |                                      |
| Namespaces       |                                      |

# Kubernetes Introduction
>Is a portable, extensible, open source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation. 

>[!tip] Kubernetes is commonly refered to as K8s

## What Kubernetes *does*
Kubernetes provides you with a framework to run distributed systems resiliently. Some tasks it handles are:
- Service discovery and load balancing
- Storage orchestration
- Automated rollouts and rollbacks
- Automated bin packing
- Self-healing
- Secret and configuration management
- Batch execution
- Horizontal scaling
- IPv4/IPv6 dual-stack
- Designed for extensibility
## What Kubernetes *cannot* do
Kubernetes operates at the container level, so some PaaS(Platform as a Service) features are not included. 
- Does not limit the types of applications supported
- Does not deploy Source Code and Does not build your application
- Does not provide application level services
- Does not dictate logging, monitoring or alerting solutions
- Does not provide nor mandate a configuration language/system
- Does not provide any comprehensive machine configuration, maintenance or self-healing systems

## Key Components
### Control PLane
- API Server
- Scheduler
- Controller-Manager
- etcd
### Worker Node
- Kubelet
- Kube-Proxy
- Docker
- Pods
![[Kubernetes.webp]]
## Kubernetes - beyond the overview

#### Architecture
##### Cluster Architecture

##### Kubernetes Components

##### Control Plane

##### Node Components

##### Addons

##### Commands for Kubectl


#### Deployments

#### Volumes

#### Secrets

#### Kubectl

#### ConfigMap

## Micro Kubernetes - Canonical
Lightweight Kubernetes implementation.  

## History of Kubernetes
- Traditional Deployment
- Virtualized Deployment
- Container Deployment
