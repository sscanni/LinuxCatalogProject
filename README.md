# Linux Server Configuration Project

## IP Address and SSH port for the server

```
IP Address: 35.183.33.123
Port: 2200
```
## URL to the hosted web application

[http://35.183.33.123.xip.io/](http://35.183.33.123.xip.io/)

## Summary of software installed and configuration changes made

Installed the following packages:

- apache2 -web server
- libapache2-mod-wsgi -Python WSGI adapter module for Apache
- postgresql - database
- git - version control
- virtualenv - virtual environment for installing packages
- Flask - flask python framework
- python-pip - to install python packages
- tree - to view dir structure as a tree
- SQLAlchemy - for processing databases in python
- flask-sqlalchemy - for processing databases with flask
- python-psycopg2 - postgresql with python
- psycopg2 - postgresql with python
- oauth2client - oauth
- funtools - needed for login_required function



Configurations changes:

- Updated the currently installed packages
-  Change the SSH port from 22 to 2200 and configured the Lightsail firewall to allow it.
- Configured the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123)
- Created a new account name "grader".
- Gave the "grader" user sudo permission.
- Created an SSH key pair for the "grader" user using the ssh-keygen pair tool.
- created postgresql grader user
- Created a new database user named "catalog" that has limited permissions to your catalog application database.
- set up git repository
- Created directory structure under the /var/www directory.
- Created a /etc/apache2/sites-available/catalog.conf file and made appropriate changes for the catalog application.
- Created a catalog.wsgi file in the /var/www/catalog directory and made appropriate changes.
- cloned and setup the item Catalog application from my git repository.
- Added http://35.183.33.123.xip.io to the google oauth app list on the google website.

Catalog directory structure and files:
```
|--------catalog
|----------------catalog
|-----------------------images
|-----------------------static
|-----------------------templates
|-----------------------venv
|-----------------------__init__.py
|-----------------------models.py
|-----------------------client_secrets.json
|-----------------------fb_client_secrets.json
|----------------catalog.wsgi
```

## Any third-party resources used to complete Project

Using xip.io to obtain a DNS name for the instance's ip address. This was required for the oauth authentication.

## Credits and Acknowledgments
Created by: Steven Scanniello
Email: sscanni@comcast.net
