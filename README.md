# Ansible

My own ansible deployment scripts.

## Prerequisites

Those playbooks and roles are to be used only with Debian 9 (Stretch).

One must ensure the following packages are installed on the remote machine, or Ansible will not work:
- apt-utils
- python
- python-apt 
- python-requests

## Playbooks:
  
- **`ttrss`: Install Tiny Tiny RSS**<br />
  This playbook allow the install and configuration of all Tiny Tiny RSS dependencies, but does not configure Tiny Tiny RSS itself.
  This is done at first launch, or by backup/restore scripts (which are not in this repository).
- **`static-website`: Install a static HTML + JavaScript application**<br />
  This playbook install a simple, static web site requiring only nginx to run.
  The web site is installed into the remote user home folder, into a designated subfolder.

## Roles

- `debian`: Define repositories, set system up to date, add some useful packages and remove useless ones
- `mysql`: Install and configure native MySQL 5.7
- `php`: Install and configure PHP 7.1 from Ondřej Surý repository
- `composer`: Install and configure Composer package manager
- `fpm`: Install and configure PHP FPM (version 7.1)
- `nginx`: Install and configure nginx
- `npm`: Install and configure NodeJS and NPM package manager
- `yarn`: Install Yarn package manager
- `ttrss`: Install and prepare Tiny Tiny RSS (to use with nginx, PHP-FPM and MySQL)
- `static-website`: Install and configure an HTML5 website from its git repository (to use with nginx)

# License

This repository is under the MIT license. See the complete license in the `LICENSE` file.
