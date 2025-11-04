# sentinelone_client

Installs and registers the SentinelOne Endpoint agent.

This role is **deprecated** and was replaced with [`sva.sentinelone.sentinelone_client_legacy`](https://galaxy.ansible.com/ui/repo/published/sva/sentinelone/content/role/sentinelone_client_legacy/) and - even better - [`sva.sentinelone.install_agent`](https://galaxy.ansible.com/ui/repo/published/sva/sentinelone/content/role/install_agent/).

## Requirements

No requirements.

## Role Variables

| Variable                             | Default   | Description                      |
| ------------------------------------ | --------- | -------------------------------- |
| `sentinelone_client_filename`        | *(empty)* | Package file to install          |
| `sentinelone_client_token`           | *(empty)* | Group/Site token                 |
| `sentinelone_client_gpgkey`          | *(empty)* | GPG signing key to import        |
| `sentinelone_client_force_new_token` | `false`   | Set to true to force a new token |

## Dependencies

No dependencies.

## Example Playbook

```yml
- hosts: clients
  roles:
    - role: stdevel.sentinelone_client
      sentinelone_client_filename: SentinelAgent_linux_v21_10_3_3.rpm
      sentinelone_client_token: trustno1
```

Repository installation:

```yml
- hosts: clients
  roles:
    - role: stdevel.sentinelone_client
      sentinelone_client_filename: https://simone.giertz.dev/SentinelAgent_linux_v13_37.deb
      sentinelone_client_token: trustno1
```

## Development / testing

Use [Ansible Molecule](https://molecule.readthedocs.io/en/latest/index.html) for running tests:

```shell
$ molecule create
$ molecule converge
$ molecule verify
```

## License

BSD

## Author Information

Christian Stankowic
