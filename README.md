# Ansible Role: Linux_docker

An Ansible Role that installs `Docker` on Linux.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    docker_version: 18.06.1~ce~3-0~debian       # the version of docker to install
    
The version of `docker` to install.

    docker_dir: /var/lib/docker             # the directory containing all Docker's files
    
The path of the `Docker`'s files.
If the value is not `/var/lib/docker`, a symlink will be created to point to the new directory path.
We do not want to modify the behaviour of `Docker`.
    
    docker_force_dir: False                 # True|False
    
Setting this variable to `True` will destroy everything in the `Docker`'s directory:
- if there is an existing installation of `Docker`
- if the directory does not remain the same
    
    
    docker_daemon_enabled: True                 # True|False
    
Set this variable to disable Docker at boot.

## Dependencies

- t18s.fr_*_pkg_config
- t18s.fr_pkg

## Example Playbook

    - hosts: webservers
      roles:
        - role: t18s.fr_Linux_docker
          docker_dir: /data/docker

## Todo

Only works for Debian.

## License

```
Copyright (c) 2018 Tristan Weil <titou@lab.t18s.fr>

Permission to use, copy, modify, and distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```
