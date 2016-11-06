# Ansible

My own ansible deployment scripts.

## Playbooks:
  
- **`ttrss`: Install Tiny Tiny RSS**<br />
  This playbook allow the install and configuration of all Tiny Tiny RSS dependencies, but does not configure Tiny Tiny RSS itself.
  This is done at first launch, or by backup/restore scripts (which are not in this repository).

## Roles

- `debian-jessie`: define repositories, set system up to date, add some useful packages and remove useless ones
- `mysql`: Install and configure native MySQL 5.5
- `php`: Install and configure PHP CLI (+ extensions), native 5.6 or 7.0 from added repository
- `composer`: Install and configure composer
- `fpm`: Install and configure PHP FPM (version 5.6 or 7.0)
- `nginx`: Install and configure nginx according to PHP FPM settings
- `ttrss`: Install and prepare Tiny Tiny RSS to use with nginx, PHP-FPM and MySQL

# License

This repository is under the MIT license. See the complete license in the `LICENSE` file.
