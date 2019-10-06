# Configuring parallelism

**fork** -  maximum number of simultaneous connections that Ansible makes
Above, the of the settings are to be configured in *ansible.cfg*

If not requited to be in config file, you can use *-f* option while running *ansible-playbook*

**serial** - run the hosts through the play in batches.