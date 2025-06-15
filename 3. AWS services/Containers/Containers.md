# Containers

[Containers](cont1.png)

# Microservices

[Containers](cont2.png)

# Kubernetes

- Kubernetes is an open-source container orchestration system for automating deployment scaling and management of containers 
- It was originally created by Google and now maintained by the cloud native Computing foundation (cncf) 

- kubernetes is commonly called K8 the 8 represents the remaining letters for "ubernete"

- The advantage of kubernetes over Docker is the ability to run containers distributed across multiple VMs 

- A unique component of kubernetes are pods 
- a pod is a group of one or more containers with shared storage network resources and other shared settings 

- kubernetes is ideally for microservice architectures where company has tens to hundreds of services they need to manage 

[Kubernetes](kub1.png)

# Docker

- Set of Platform as a service (PaaS) products that use OS level virtualization to deliver software in packages called containers 
- Docker was the earliest popularized open source container platform meaning there's lots of tutorials there's a lot of services that integrate with Docker or make it really easy to use 
- when people think of containers they generally think of Docker 
- there's of course a lot more options out there than Docker to run containers but this is what people think

- Suite of tools
	- Docker CLI: CLI commands to download, upload, build, run and debug containers 
	- Docker file a configuration file on how to provision a container 
	- Docker compose which is a tool and configuration file when working with multiple containers 
	- Docker swarm an orchestration tool for managing deployed multicontainer architectures 
	- Docker Hub a public online repository for containers published by the community for download


- Open container initiative - open container initiative (oci) which is an open government structure for creating open industry standards around container formats and runtimes. Docker established the OCI and it is now maintained by the Linux foundation

- Docker has been losing favor with developers due to their handling of introducing a paid open source model and alternative like Podman are growing.

# Podman

- Podman is a container engine that is OCI compliant and is a drop in replacement for Docker 
- Podman is Deamon-less where Docker uses a container Deamon 
- Podman allows you to create pods like K8  where Docker does not have pods 
- Podman only replaces one part of Docker podman is is to be used alongside buildah and uh skopio 

- Docker is an all-in-one kind of tool everything is done via single CLI and everything is there but you know they just wanted to make it more module
- Buildah is a tool used to build the oci images 
- scopio is a tool for moving container images between different types of container storages.

[Overview of Container](cont3.png)
