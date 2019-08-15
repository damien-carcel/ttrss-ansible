# Ansible

My own ansible deployment scripts.

## Prerequisites

Those playbooks and roles are to be used only with Debian 10 (Buster).

## Playbooks:
  
- **`docker.yml`: Install and configure Docker**<br />
  This playbook allow the install and configuration of Docker in `swarm` mode.

## Roles

- `debian`: Define repositories, set system up to date, add some useful packages and remove useless ones
- `docker`: Install and configure Docker in `swarm` mode

# License

This repository is under the MIT license. See the complete license in the `LICENSE` file.
