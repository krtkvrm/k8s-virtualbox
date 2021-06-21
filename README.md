# k8s-virtualbox

Provision Kubernetes cluster on VirtualBox using Vagrant and Ansible. It uses Calico as network plugin.

## Requirements
- [Vagrant](https://www.vagrantup.com/downloads)
- [Ansible](https://docs.ansible.com/ansible/latest/index.html)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

## Instructions
- Create Cluster. It will create 2 node cluster. Modify `N` variable in Vagrantfile to change number of nodes
```
    $ vagrant up
```
- SSH into `k8s-master` and [export kubeconfig](https://stackoverflow.com/questions/61829214/how-to-export-kubeconfig-file-from-existing-cluster)
```
    $ vagrant ssh k8s-master
```

## Limitations
- Currently exploring options to expose service using Metallb & ingress
