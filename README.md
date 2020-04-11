# Deploying Tiny Tiny RSS with Ansible

## Prerequisites

Those playbooks and roles are to be used only with Debian 9 (Stretch).

One must ensure the following packages are installed on the remote machine, or Ansible will not work:
- apt-utils
- python
- python-apt 
- python-requests

## Deploy

From your machine:
```bash
$ ansible-playbook -i inventories/provider/ttrss tiny-tiny-rss.yml -t debian
```

Then on the server:
```bash
$ sudo certbot certonly --manual -d example.com -d *.example.com --agree-tos --no-bootstrap --manual-public-ip-logging-ok --preferred-challenges dns-01 --server https://acme-v02.api.letsencrypt.org/directory --email you@email.com
```

Finally from your machine again:
```bash
$ ansible-playbook -i inventories/provider/ttrss tiny-tiny-rss.yml
```

## License

This repository is under the MIT license. See the complete license in the `LICENSE` file.
