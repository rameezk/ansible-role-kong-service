KONG_SERVICE
=========

An Ansible Role for Managing Kong Services

Requirements
------------

The Kong Admin URL needs to be enabled. This should ideally be exposed via a route on the Kong proxy URL. Kong does not recommend the Admin URL to be exposed directly.

Only JWT auth is supported for now. 

Example Playbook
----------------

The easiest way to use this role in your playbooks is by adding it as a submodule.
```bash
git submodule add https://github.com/rameezk/ansible-role-kong-service roles/kong_service
```

Usage:
```yaml

- hosts: servers
  vars:
    KONG_ADMIN_URL: "<<KONG_ADMIN_URL>>"
    KONG_JWT: "<<KONG_JWT>>"
  roles:
    - role: kong_service
      name: "testservice"
      url: "http://httpbin.org"
```

License
-------

MIT

