# Deploying Tiny Tiny RSS with Ansible

## Prerequisites

This playbook and its roles are to be used only on a server with Debian 10 "Buster".

One must ensure the following packages are installed on the remote machine, or Ansible will not work:
- apt-utils
- python
- python-apt 
- python-requests

## Deploy

First copy the configuration example:
```bash
$ cp inventories/ttrss.dist inventories/<provider name>/ttrss
```

Complete the configuration with needed values, then deploy the Ansible playbook:
```bash
$ ansible-playbook -i inventories/provider/ttrss tiny-tiny-rss.yml
```

## License

This repository is under the MIT license. See the complete license in the `LICENSE` file.
