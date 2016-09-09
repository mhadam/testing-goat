Provisioning a new site
=======================

## Required packages:

* nginx
* Python 3
* Git
* pip
* virtualenv

e.g.,, on Ubuntu:

	sudo apt-get install nginx git python3 python3-pip
	sudo pip3 install virtualenv

## Nginx Virtual Host config

* see nginx.template.conf
* replace SITENAME with, e.g., staging.my-domain.com

## Systemd Scripts

* see gunicorn.template.{service, socket, conf}
* replace SITENAME with, e.g., staging.my-domain.com
* replace VIRTUALENV_NAME with the name of the virtual env you're using

## Folder structure:
Assume we have a user account at /home/username

/home/username
└── sites
    └── SITENAME
         ├── database
         ├── source
         ├── static
         └── virtualenv
