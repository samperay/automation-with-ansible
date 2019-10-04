Ansible may need access to sensitive data such as passwords or API keys in order to configure managed hosts.

# Ansible-vault 

** Creating an Ecnrypted File **

```
ansible-vault create password.yml
```

Instead, providing with password on command line, you can provie it from file.

```
ansible-vault create --vault-password-file=.pass password.yml
```

** Viewing/Editing Ecnrypted File **

```
ansible-vault view password.yml
ansinle-vault edit password.yml
```

** Encrypt existing file **

```
ansible-vault encrypt passworless.yml
```

** Decrypt existing file **
```
ansible-vault decrypt password.yml --output=decrypted-secret.yml
```

** change password of encryted file **

```
ansible-vault rekey password.yml
```
