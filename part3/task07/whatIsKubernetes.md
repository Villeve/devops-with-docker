# What is Kubernetes?
According to Kubernetes [homepage](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/) *it is an open-source platform for managing containerized workloads and services, that faciliates both declarative configuration and automation*

## Why to Use
An [article](https://www.developintelligence.com/blog/2017/02/kubernetes-actually-use/) published by *DevelopIntelligence* states that using Kubernetes *lowers the cost of cloud computing expenses and simplified operations and architecture.* Basic idea of Kubernetes is to create a single interface for deploying containers to different cloud platforms by further abstracting machines, storage and networks away from their physical implementations. Besides the container management capabilities Kubernetes provides following features: *Service discovery and load balancing, Storage orchestration, Automated rollouts and rollbacks, Automatic bin packing, Self-healing and Secret & configuration management* [Kubernetes 2019](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/).

### Kubernetes V.S.
Cloud services often have their own cloud orchestration, for example *CloudOrchestration* on *Amazon EC2*. So why would you use Kubernetes instead of the "local" services? Because Kubernetes can be also used on other clouds (Azure or GCC for example), virtual machines or physical machines. That way you do not get tied to a single Cloud provider and their technologies.

## When to use
Kubernetes should be used to help the deployment and management of services which are part of a massive system. When hunreds or thousands of containers are spread between multiple hosts the management is no longer a trivial task. Also, the self-healing abilities and highly automated processes increase the operational safety, so Kubernetes is solid choice for critical systems. In smaller deployments Kubernetes might only add an unnecessary layer of complexity.

*Ville Vehniä 22.12.2019*