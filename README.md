# Ansible Role: Portainer for Docker

This role install Portainer using Docker container and also configure Traefik.

## Requirements

- Docker
- Traefik ( Optional )

## Example Playbook

    - hosts: your_hosts

      vars:
        pip_install_packages:
          - name: docker

      roles:
        - role: geerlingguy.docker
          become: true

        - role: geerlingguy.pip
          become: true

        - role: shuntps.portainer_docker
          become: false