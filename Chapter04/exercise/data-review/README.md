- A developer has asked you to write an Ansible Playbook to automate the setup of a web server environment on servera.lab.example.com, which controls user access to its website using basic authentication.

- Create ansible.cfg and inventory file for this project.

- The files subdirectory contains an httpd.conf configuration file, which configures the Apache web service for basic authentication. The subdirectory also contains a .htaccess file which can be used to control access to the web server's document root directory

- In the project directory, create a playbook named playbook.yml, which installs and configures the firewall and web service on serverb.lab.example.com. The playbook should also create an index.html file that identifies the host name and IP address of the managed host using
Ansible facts. This content file should only be visible to web users who successfully authenticate. To maintain the security of the password used for basic authentication, define the user password as a variable in a file encrypted by Ansible Vault

- After the playbook is created, execute the playbook and then verify the results by retrieving the content file using basic authentication over HTTPS