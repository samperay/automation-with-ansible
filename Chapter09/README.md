# Troubleshooting Playbooks

By default, Red Hat Ansible Engine is not configured to log its output to any log file. you can redirect logs to the file in *ansible.cfg*
using vairable *log_path*

Syntax check for ansible playbook  
```
ansible-playbook play.yml --syntax-check
```

use  **--step** to step through a playbook one task at a time, this will interactively ask for your confirmation to proceed each task defined.
```
ansible-playbook play.yml --step
```

Further, you can troubleshoot using the **debug** by increasing the **verbose** level. 
```
- name: Display the "output" variable
debug:
var: output
verbosity: 2
```

# Check mode as Testing tool
```
ansible-playbook --check playbook.yml
```

Some modules can provide additional information about the status of a managed host.
*stat*: The stat module gathers facts for a file much like the **stat** command. You can use it to register a variable and then test to determine if the file exists or to get other information about the file.

*assert*: The assert module is an alternative to the fail module. The assert module supports a that option that takes a list of conditionals. If any of those conditionals are false, the task fails

# Troubleshooting Connections

Many common problems when using Ansible to manage hosts are associated with connections to the host and with configuration problems around the remote user and privilege escalation.

Ensure from your *ansible.cfg* with privileges have been set correctly, else you need to re-check..

```
[privlege escalation]
become = true 
become_method = sudo 
become_ask_pass = false
become_user = root 
```

use, ad-hoc commads to test and then write into playbooks..
```
ansible demohost -m ping
ansible demohost -m ping --become
ansible demohost -m command -a 'df'
ansible demohost -m command -a 'free -m'
```

