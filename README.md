# Ansible Deploy
A re-implementation of my dotfile bootstrapper made to be as distro agnostic as possible using Ansible instead of shell scripts.

All configuration is handled completely locally, and works to import as many settings across systems as possible to ensure all environments are similar.

In future this will be expanded out to not automatically assume it's being used on a workstation and will power all servers I use.

⚠ Warning: It is not advised to run these on your system unless you are happy with overwriting a large majority of your configuration. I am not responsible for any issues it may cause with your system, nor will any support be offered.

If you still want to run them anyway, use the following command:
```
ansible-pull -U https://github.com/BitsOfAByte/ansible-deploy.git --ask-become-pass
```