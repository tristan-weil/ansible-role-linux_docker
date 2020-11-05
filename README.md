# Ansible Role: linux_docker

An Ansible Role that installs `Docker`.

[![Actions Status](https://github.com/tristan-weil/ansible-role-linux_docker/workflows/molecule/badge.svg?branch=master)](https://github.com/tristan-weil/ansible-role-linux_docker/actions)

## Role Variables


Available variables are listed below, along with default values (see `defaults/main.yml`):

Mandatory variables:

| Variable      | Description |
| :------------ | :---------- |

Optional variables:

| Variable      | Default | Description |
| :------------ | :------ | :---------- |
| docker_version | latest | the version to install |
| docker_users_to_group | [] | a list of users to add to the `docker` group |

## Example Playbook

    - hosts: 'webservers'
      roles:
        - role: 'ansible-role-linux_docker'

## Todo

None.

## Dependencies

See [requirements_galaxy.yml](https://github.com/tristan-weil/ansible-role-linux_docker/blob/master/requirements_galaxy.yml)

## Supported platforms

See [meta/main.yml](https://github.com/tristan-weil/ansible-role-linux_docker/blob/master/meta/main.yml)

## License

See [LICENSE.md](LICENSE.md)
