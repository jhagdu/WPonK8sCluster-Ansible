# Deploy Wordpress on Kubernetes Cluster  

<img src="https://netapp.io/wp-content/uploads/2017/04/Kubernetes-logo.png" height=100 width=170 alt="Kubernetes" /> <img src="https://gorillalogic.com/wp-content/uploads/2016/10/maxresdefault-1.jpg" height=100 width=170 alt="Ansible" /> <img src="https://www.metaltoad.com/sites/default/files/styles/large_personal_photo_870x500_/public/2020-05/aws-logo-blog-header.png?itok=t4o3meiH" height=100 width=170 alt="AWS" /> <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQb94q92qPTymjepAYkKO4Lekseh1vNgHcgBqz1f7_U22LVM6iA54F17Ss2q9gNqGYbrwA&usqp=CAU" height=100 width=170 alt="WordPress" /> <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSiNlfxDH2kp0esfF62rTRrnQ3spHTbE-HMpw&usqp=CAU" height=100 width=170 alt="MySQL" />

This repository contains the Ansible Playbook and Roles to deploy WordPress with MySQL as a backend database on the K8s Cluster  
  
### Ansible Roles -   

**Role Name** | **Role Description**
------------- | --------------------
**jhagdu.awsinfra4k8s** | To create a AWS Infrastructure for Kubernetes MultiNode Cluster
**jhagdu.k8smaster** | To configure Kubernetes Master Node using Kubeadm  
**jhagdu.k8sworker** | To configure Kubernetes Worker Node using Kubeadm
**wordpressonk8s** | To deploy wordpress with mysql over a kubernetes cluster
  
Here to setup the Kubernetes multinode cluster I've used my roles present at my Ansible Galaxy   
Link to repository of other roles included - (https://github.com/jhagdu/k8sMultinode-Ansible.git)

## Prerequisites   
- Ansible should be installed and Configured
- AWS CLI Should be Installed and Configured  
- Other requirements of Roles are included in Readme file of particular Role

## How to Start 
- Clone or Download the Repository  
- Change the value of variables according to requirement  
- Finally run wpOnK8sCluster.yml using 'ansible-playbook wpOnK8sCluster.yml' command  

## Note  
- Recommended to use RedHat AMI or OS for K8s Master and Workers  
- Ansible Config file should include previliage_escalation block to become root user in order to configure AWS Instances  

# Links

[Click here for Video and Post](https://www.linkedin.com/in/amanjhagrolia143)
  
***Feel free to Contact if any issue!!***

<a href="https://www.linkedin.com/in/amanjhagrolia143" target="_blank"> <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /> </a> 
<a href="https://galaxy.ansible.com/jhagdu" target="_blank"> <img src="https://galaxy.ansible.com/assets/galaxy-logo-02.svg" height=30 width=140 /> </a>