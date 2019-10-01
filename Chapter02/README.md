# Deploying Ansible

Created two groups *web* & *db*. 
You can inherit both the inventory from the above groups.

```
ansible web --list-hosts
ansible db --list-hosts
anbsible all --list-hosts
```

You can also define inventory with wildchar, RE. 

e.g

```
192.168.56.[1:100]
server[1:10].example.com
