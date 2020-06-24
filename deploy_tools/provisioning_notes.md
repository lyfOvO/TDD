Provisioning a new site
=======================

## Required packages:

* nginx
* Python 3.6
* virtualenv + pip
* Git

eg, on Ubuntu:

    sugo add-apt-repository ppa:fkrull/deadsnakes
    sudo apt-get install nginx git python 36 python3.6-env

## Nginx Virtual Host config

* see nginx.template.conf
* replace SITENAME with, e.g., staging.my-domain.com

## Systemd service

* see gunicorn-systemd.template.service
* replace SITENAME iwth, e.g., staging.my-domain.com

## Folder structure
Assume we have a user account at /home/username

/home/username
|__sites
    |__SITENAME
        |--datebase
        |--source
        |--static
        |--virtualenv