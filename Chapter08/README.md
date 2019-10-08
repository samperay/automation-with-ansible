# Simplifying Playbooks with Roles

As you develop more playbooks, you will probably discover that you have many opportunities to reuse code from playbooks that you have already written.

You can package, in a standardized directory structure, all the tasks, variables, files, templates, and other resources needed to provision infrastructure or deploy applications. You can copy that role from project to project simply by copying that role's directory. You can then simply call that role from a play to execute it.

Roles skelton is being created as 
```
ansible-galaxy init <role>
```

Order of high precedence for variables:
- Roles
- vars
- defaults
- vars defined in playscope

# ansible-galaxy

Public library of Ansible content written by a variety of Ansible administrators and users.

**ansible-cli**
```
ansible-galaxy search 'redis' --platforms EL
ansible-galaxy info ansible-sudo
ansible-galaxy install ansible-sudo -p roles/
ansible-galaxy list
ansible-galaxy remove ansible-sudo
```
You can install from the specific version using the requirements file

*roles/requirements.yml*
```
# Install latest from ansible-galaxy
- src: geerlingguy.redis

# Install roles using from any GIT based repository using SSH
- src: git@github.com:weareinteractive/ansible-sudo.git
  scm: git
  version: master
  name: ansible-sudo
```
Then, 
```
ansible-galaxy install -r roles/requirements.yml -p roles
```


