# Caddy Ansible Git

This Ansible role builds and installs [Caddy](https://caddyserver.com/) from
the Caddy Go module. This allows Caddy to be used
for commercial projects.

## Example Playbook

```
- hosts: all
  roles:
    - role: caddy-git
      caddy_config: |
        portal.simpleiot.org {
        proxy / localhost:8080
      }
```

## Todo

- [x] test on Ubuntu
- [x] version number in compiled binary
- [ ] add option to disable telemetry
- [ ] configure plugins
- [ ] test on Fedora
- [ ] create custom caddy user instead of using www-data
- [ ] add Vagrant tests
