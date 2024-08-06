Caddy
=========

Installs Caddy on Debian.

Based on:  
https://caddyserver.com/docs/install#debian-ubuntu-raspbian


Requirements
------------

Debian OS.

Role Variables
--------------

No variables

Dependencies
------------

No dependencies.

Example Playbook
----------------

Install Caddy

```
- name: Install Caddy
  hosts: all
  gather_facts: false
  roles:
  - ansible-role-caddy
```

Copy Caddyfile with useful snippets

```
- name: Install Caddy
  hosts: all
  gather_facts: false
  tasks:
  - name: Update Caddyfile
    import_role:
      name: ansible-role-caddy
      tasks_from: caddyfile.yml
```

License
-------

MIT

Author Information
------------------

Pawel Idzikowski
Wincognito