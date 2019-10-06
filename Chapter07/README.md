# Selecting Hosts with host patters


# Configuring parallelism

**fork** -  maximum number of simultaneous connections that Ansible makes
Above, the of the settings are to be configured in *ansible.cfg*

If not requited to be in config file, you can use *-f* option while running *ansible-playbook*

**serial** - run the hosts through the play in batches.

# Including & Importing Files

When a playbook gets long or complex, you can divide it up into smaller files to make it easier to manage. You can combine multiple playbooks into a main playbook in a modular way, or insert lists of tasks from a file into a play. This can make it easier to reuse plays or sequences of tasks in
different projects.