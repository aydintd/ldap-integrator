## LDAP Client Integrator 

Note : Only Tested on Debian 8 (Jessie) and Pardus Kurumsal 5 Operating Systems.

It makes sure your ldap clients will be integrated with your LDAP server and make sure all LDAP users can login to their client machines with their LDAP username/password.
Also it gives cache support away to your LDAP users. (via lib-ccreds)

### Usage :

You need to modify your inventory file content and make sure you defined all your ldap clients' ip addresses in this inventory.
Also you need a user with sudo privileges to get all steam machines work like a charm. :)

You can apply the playbook via this command :

`$ ansible-playbook -i client.inventory site.yml --limit ldapclients --ask-sudo-pass --ask-pass`

It's going to ask your SSH and SUDO passwords and your clients will be able to connected and integrated to your LDAP server which you define in integrateldap/vars/main.yml file

If you apply the base role, you will be able to use "admin" user to manage all system operations.
This command will use this ldapclients.yml file so make sure you define all necessary informations in this file before applying the playbook.

### TO-DO

- It only runs on Debian and its derivatives so it makes me so sad. I'm going to work on this playbook for RHEL implementations for ldap integration.
