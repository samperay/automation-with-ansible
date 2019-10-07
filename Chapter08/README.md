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
