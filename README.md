# Azure Kubernetes Service (AKS) Learning Series

Demo code for Hands on Series for `Azure kubernetes Series (AKS) learning series`. 

## Code organization

- `Docker-compose V1`

Contains the docker-compose file in its simplest form

- `Docker-compose V2`

Contains the docker-compose files split into a base compose file and separate files for build and run scenarios. This is a preferred approach as it allows to have clear separation in terms of images which are built as part of application code and images which are used from other pre-built images. This also allows us to separate configurations between different environments like Dev / Integration / Production etc.

- `Helm`
Contains the Helm charts which are useful for deploying Kubernetes applications. Refer to the [Helm readme](/helm/Readme.md) file for more details.

- `k8s`

Contains Kubernetes Manifest files. These are grouped into `Minikube` version with services exposed using `NodePort` type. `AKS` version exposes the `TechTalksWeb` and `TechTalksDB` using LoadBalancer. The data is also persisted to outside of the container using `Persistent Volume (PV)` and `Persistent Volume Claim (PVC)`. The volume is backed by `Azure Disk`. 

- `Powershell`

Contains the powershell scripts used for deploying application resources to Minikube or AKS cluster

- `Skaffold`

[Skaffold](https://github.com/GoogleContainerTools/skaffold) adds ability to do continuous deployment of Kubernetes application. This is similar to live unit testing feature. Refer to the two links below to know more about using Skaffold.

1 - Use [Skaffold with Minikube](https://www.handsonarchitect.com/2018/08/continuous-kubernetes-deployments-with.html)

2 - Use [Skaffold with Docker for Mac with Kubernetes](https://www.handsonarchitect.com/2018/08/continuous-kubernetes-deployments-with.html)

- `src`

Contains the source code.
    
    - `TechTalksAPI` contains code for Web API project

    - `TechTalksDB` contains database initialization script

    - `TechTalksWeb` contains code for ASP.Net Core MVC frontend

- `Minikube`

Contains instructions for setting up `Minikube` cluster and `Kubectl`

## Online resources

The Azure Kubernetes Service (AKS) Learning Series is recorded and videos are available on Engineers.sg website. 

- [AKS Part 1 - Getting started with Docker](https://engineers.sg/video/azure-container-service-aks-part-1-getting-started-with-docker-by-nilesh-gule--2732)
- [AKS Part 2 - Stitch multiple containers using Docker Compose](https://www.engineers.sg/video/azure-kubernetes-service-aks-2-stitch-multi-container-apps-with-docker-compose--2814)
- [AKS Part 3 - Container Orchestration using Kubernetes / Minikube](https://engineers.sg/video/orchestrating-containers-using-minikube--2849)
- [AKS Part 4 - Deploy Multi-container Apps to Azure Kubernetes Service (AKS)](https://www.engineers.sg/video/aks-learning-series-4-multi-container-apps-via-aks--2880)

## Slides at Slideshare

- [AKS Part 1 - Getting started with Docker](https://www.slideshare.net/nileshgule/azure-kubernetes-service-aks-part-1)
- [AKS Part 2 - Stitch multiple containers using Docker compose](https://www.slideshare.net/nileshgule/azure-kubernetes-service-aks-part-2-stitch-multi-container-apps-using-docker-compose)
- [AKS Part 3 - Container Orchestration using Kubernetes / Minikube](https://www.slideshare.net/nileshgule/azure-kubernetes-service-aks-part-3-110006705)
- [AKS Part 4 - Deploy Multi-container Apps to Azure Kubernetes Service (AKS)](https://www.slideshare.net/nileshgule/azure-kubernetes-service-aks-part-4-deploy-multicontainer-app-to-aks-cluster)

## Slides at Speakerdeck

- [AKS Part 1 - Getting started with Docker](https://speakerdeck.com/nileshgule/azure-kubernetes-service-learning-series-part-1-docker)
- [AKS Part 2 - Stitch multiple containers using Docker compose](https://speakerdeck.com/nileshgule/stitch-multi-container-apps-using-docker-compose)
- [AKS Part 3 - Container Orchestration using Kubernetes / Minikube](https://speakerdeck.com/nileshgule/container-orchestration-using-kubernetes)
- [AKS Part 4 - Deploy Multi-container Apps to Azure Kubernetes Service (AKS)](https://speakerdeck.com/nileshgule/aks-learning-series-deploy-multi-container-apps-to-azure-kubernetes-service-aks)