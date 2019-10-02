# automation-with-ansible
This repository would be helpful for system administrators who intend to use Ansible for automation, configuration, and management. You will create and run playbooks to configure systems and manage inventories.
All this course has been written using an DevOps environment with Vagrant.

# Objectives

- Automate system administration tasks on managed hosts with Ansible.
- Learn how to write Ansible playbooks to standardize task execution

# Prerequsites
Red Hat Certified System Administrator (RHCSA in Red Hat Enterprise Linux) certification or equivalent experience.

# Ansible Version
I have been using Ansible version *2.5* in this project. 

```
$ansible --version
  ansible 2.5.1
  config file = /home/user/.ansible.cfg
  configured module search path = [u'/home/user/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python2.7/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 2.7.15+ (default, Jul  9 2019, 16:51:35) [GCC 7.4.0]

```

All the chapters have an *example* section which has been written with few playbooks related. 
These are the basic instructions which are included for execution of playbooks.

*Check Playbook syntax*
```
ansible-playbook --syntax-check <playbook.yml>
```

*Executing Playbook dry run*
```
ansible-playbook -C <playbook.yml>
```

*Executing playbook*
```
ansible-playbook <playbook.yml>
```