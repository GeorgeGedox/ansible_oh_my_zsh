Oh-My-Zsh Ansible Role
=========

A role to install and configure Oh-My-Zsh along with the required dependencies.
This is my first role and was used for learning how Ansible works.

Requirements
------------

All users defined for this role must have have `sudo` access.

Role Variables
--------------

Default vars:
- `oh_my_zsh_theme` - **String** - Default theme used in the template file
- `oh_my_zsh_template` - **String** - Default template path for .zshrc
- `oh_my_zsh_plugins` - **List** - Default plugins used in the template file

Required vars:
- `oh_my_zsh.username` - **String** - The user for which to install Oh-My-Zsh

Dependencies
------------

None

Example Playbook
----------------

```yml
- hosts: vbox
  roles:
    - role: georgegedox.oh_my_zsh
      oh_my_zsh:
        username: george
        theme: bira
        plugins:
          - git
          - vagrant
          - ansible
```

License
-------

MIT