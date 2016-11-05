# Ansible

My own ansible deployment scripts.

## Playbooks:
  
- ttrss: Install Tiny Tiny RSS.
  
  This playbook allow the install and configuration of all TTRSS dependencies + cron configuration, but does not configure TTRSS itself.
  This is done by TTRSS itself for a first launch, or by backup/restore scripts (which are not in this repository).

## Roles

- debian-jessie: define repositories, set system up to date, add some useful packages and remove useless ones
- mysql: Install and configure native MySQL 5.5
- php: Install and configure PHP CLI (+ extensions), native 5.6 or 7.0 from added repository
- composer: Install and configure composer
- fpm: Install and configure PHP FPM (version 5.6 or 7.0)

# License

This repository is under the MIT license. See the complete license in the `LICENSE` file.
