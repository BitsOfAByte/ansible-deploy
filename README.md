# Ansible Deploy
## About
A re-implementation of my dotfiles bootstrapper made to be as distro agnostic as possible using Ansible instead of shell scripts with all configuration handled locally and syncing from this git repository.

### Whats Imported?
Most dotfiles configurations, common desktop environment configuration changes, backgrounds, packages, etc. You can explore the `roles/{device-type}` directories yourself for more information.

### Why is workstation always ran?
Right now I do not use this for server deployments, but if I decide to change that workstation will be conditionally checked before being ran so this configuration can also be deployed on servers for a unified experience.

## Installing & Running
⚠ Warning: It is not advised to run these on your system unless you are happy with overwriting a large majority of your configuration. I am not responsible for any issues it may cause with your system, nor will any support be offered.

If you still want to run them anyway, install `ansible` and `git` with your package manager and then run:
```
ansible-pull -U https://github.com/BitsOfAByte/ansible-deploy.git --ask-become-pass
```

Please note the script may freeze on certain tasks momentarily. Please allow some time for tasks to run, especially for the first time.
