# ansible-deploy-azure
Playbooks to deploys ressources in Azure

## Initialise empty hosts file
echo "localhost" > hosts

## Deploy VMs and all related ressources in Azure
ansible-playbook -i hosts azure-deploy.yml
