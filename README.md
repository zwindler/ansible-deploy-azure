# ansible-deploy-azure
Playbooks to deploys resources in Azure

## Prerequisites
```
apt install python-pip #or yum install python-pip
pip install --user ansible[azure]
pip install --user netaddr
```

## Initialise empty hosts file
```
echo "localhost" > hosts
```

## Deploy VMs and all related resources in Azure

```
ansible-playbook -i hosts azure-deploy.yml
Choose region to deploy VMs [westeurope]:
Choose a prefix for all the resources [test]:
Choose a number of virtual machines to create [1]:
Choose a size for azure virtual machines [Standard_B2s]:
Choose a type for azure virtual disks [Standard_LRS]:
Choose an admin username [zwindler]:
Where can I find the admin public key ? [~/.ssh/id_rsa.pub]:
your local IP address (skip if you don't want to add 22 port to NSG) [skip]:
Give a network CIDR for virtual network (large) [172.16.0.0/18]:
Give a subnet of that network [172.16.1.0/24]:
```
