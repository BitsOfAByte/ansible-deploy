# Ansible Deploy
## About
A re-implementation of my dotfiles bootstrapper made to be as distribution agnostic as possible using Ansible instead of shell scripts with all configuration handled locally and syncing from this git repository. 

Please note this ReadMe is meant more for self-documentation.

### Whats Imported?
Most dotfiles configurations, common desktop environment configuration changes, backgrounds, packages, etc. You can explore the `roles/{device-type}` directories yourself for more information.

### Why is workstation always ran?
Currently I do not use these files for server deployments, but if I decide to change that workstation will be conditionally checked before being ran.

### What platforms work?
Any GNU/Linux based distribution from any of the major families (Such as Arch, Debian, Fedora) should work fine as long as they have a mutable filesystem and supported package managers. If you want the desktop layout, you will need to be using newer version of GNOME. 

## Installing & Running
⚠ Warning: It is not advised to run these on your system unless you are happy with overwriting a large majority of your configuration. I am not responsible for any issues it may cause with your system, nor will any support be offered.

If you still want to run them anyway, install `ansible` and `git` with your package manager and then run:
```
ansible-pull -U https://github.com/BitsOfAByte/ansible-deploy.git --ask-become-pass
```

Please note the script may freeze on certain tasks momentarily. Please allow some time for tasks to run, especially for the first time.

After running for the first time, restart your system fully.

## Adding more programs
When adding additional programs, they should be put inside of the correct roles, package managers or critical dependencies should be inside of the base role and GUI packages should be put inside of the workstation role. Use best judgement when deciding, and please ensure that the result from running the files repeatedly is idempotent.