# Implementing Ansible

*Playbooks*

A play is an ordered set of tasks which should be run against hosts selected from your inventory.
A playbook is a text file that contains a list of one or more plays to run in order

using *adhoc* command for creation of users
```
ansible servera -m user -a 'user=user1 uid=4000 state=present' 
```

The same above you can refer using ansible playbooks.. you can find code in *example* section of this chapter. 
You can have a task with one or more plays in the playbook. 

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

