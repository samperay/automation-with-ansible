# Introductio Ansible

- Ansible is Simple, powerful, agentless. 

For more info, please find below link
https://www.linkedin.com/pulse/ansible-agentless-architecture-sunil-amperayani/

# Usecases

- Configuration Management
- Application Deployment
- Application Deployment
- Continuous Delivery
- Security and Compliance
- Orchestrations

# Setup Ansible Controller node

*Centos/RedHat*

```
sudo yum install -y ansible
```

*Ubuntu*
```
sudo apt-get update
sudo apt-get install ansible -y
```

Once after installing, you have an invetory file in this repo and you are required to query to check, 
if that lists you all the hosts from Ansible

```
ansible all -m ping
ansible web -m ping
ansible db -m ping
```