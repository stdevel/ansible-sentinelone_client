# sentinelone_client

Installs and registers the SentinelOne Endpoint agent.

## Requirements

No requirements.

## Role Variables

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `sentinelone_filename` | *(empty)* | Package file to install |
| `sentinelone_token` | *(empty)* | Group/Site token |

## Dependencies

No dependencies.

## Example Playbook

```yml
- hosts: clients
  roles:
    - role: sentinelone
      sentinelone_filename: SentinelAgent_linux_v21_10_3_3.rpm
      sentinelone_token: trustno1
```

Repository installation:

```yml
- hosts: clients
  roles:
    - role: sentinelone
      sentinelone_filename: https://simone.giertz.dev/SentinelAgent_linux_v13_37.deb
      sentinelone_token: trustno1
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
