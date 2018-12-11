# Caddy Ansible Git

This Ansible role installs [Caddy](https://caddyserver.com/) from the Caddy
[git repo](https://github.com/mholt/caddy). This allows Caddy to be used
for commercial projects, as the binary Caddy download requires a license.

## Example Playbook

```
- hosts: all
  roles:
    - role: caddy-ansible-git
      caddy_config: |
        portal.simpleiot.org {
	  proxy / localhost:8080
	}
```

## Todo

- [x] test on Ubuntu
- [ ] add option to disable telemetry
- [ ] configure plugins
- [ ] test on Fedora
- [ ] create custom caddy user instead of using www-data
