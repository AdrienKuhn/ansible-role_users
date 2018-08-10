SSH
=========

This role will create admin and web users

Requirements
------------

None

Role Variables
--------------

```yaml
users_web:
  - {
      name: webuser,
    }

# These users will have a user account with sudo access on all servers 
# if defined in all.yml group_vars
users_admin:
  - {
    name: adminuser,
    pub_key: ssh-ed25519 dummy_key user@domain.tld # Authorized public key for adminuser
  }
```

Dependencies
------------

None

Tests
-----

```
$ cd tests
$ vagrant up --provision
```