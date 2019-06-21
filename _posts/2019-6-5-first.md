---
layout: post
title: Running Eclipse Che on Minikube
comments: true
---

Below are the requirements for deploying multi-user deployment of Eclipse Che on Kubernetes on Debian-based Linux distributions.

**A) Before launching Che on Minkube, we need to ensure that below requirements are fulfilled.**
1.	Kubectl  
  
    Linux  
      
        a. Download the latest release with the command:  
          curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl    
        b.	Make the kubectl binary executable.  
          chmod +x ./kubectl    
        c.	Move the binary in to your PATH.  
          sudo mv ./kubectl /usr/local/bin/kubectl  
        d.	Now, you check the version of kubectl installed kubectl version.  

2.	Hypervisor: KVM or VirtualBox   
  
    Linux – VirtualBox  
      
    Installed VirtualBox for Linux from https://www.virtualbox.org/wiki/Linux_Downloads

3.	Minikube 
   
    Linux  
      
    curl -Lo minikube https://storage.googleapis.com/minikube/releases/v1.1.0/minikube-linux-amd64 && chmod +x minikube && sudo cp minikube /usr/local/bin/ && rm minikube

4.	Helm  
  
    Linux  
      
    Downloaded Helm from the script  
      
    $ curl -LO https://git.io/get_helm.sh
    $ chmod 700 get_helm.sh
    $ ./get_helm.sh

5.	Chectl

        a.	Download the binary and then navigate to the location where you have downloaded the binary  
        a.	Make the checktl binary executable. chmod +x ./chectl-linux  
        b.	Move the binary in to your PATH sudo mv ./chectl-linux /usr/local/bin/chectl

**B) After fulfilling the requirements, we can start Kubernetes Cluster** 
    
Start Kubernetes cluster with at least 10 GB RAM and RBAC:  
  
minikube start --vm-driver=kvm2 --extra-config=apiserver.authorization-mode=RBAC --cpus 4 --memory 10240

**C) We can start Che server using chectl where you can pass the below command in the terminal**
**chectl server:start**


![_config.yml]({{ site.baseurl }}/images/blog-1-img.png)

