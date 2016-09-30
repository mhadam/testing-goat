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

* the correct location is: /etc/nginx/sites-available/SITENAME
* ln -s {above SITENAME file} /etc/nginx/sites-enabled/SITENAME
* see nginx.template.conf
* replace SITENAME with, e.g., staging.my-domain.com
* sudo service nginx reload

## Systemd Scripts

* their correct locations are: /etc/systemd/system/gunicorn.{service, conf}
* additional file location: /usr/lib/tmpfiles.d/gunicorn.conf
* see gunicorn.template.{service, socket, conf}
* replace SITENAME with, e.g., staging.my-domain.com
* replace VIRTUALENV_NAME with the name of the virtual env you're using
* sudo service 

## Folder structure:
Assume we have a user account at /home/username

/home/username
└── sites
    └── SITENAME
         ├── database
         ├── source
         ├── static
         └── virtualenv
