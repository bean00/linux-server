# Linux Server Configuration

**NOTE**: The server was successfully created and deployed. Once verified by Udacity's code reviewer, I took down the server to save cost. I have carefully detailed all steps I took, so re-deploying should not be too difficult.

A project where I've created a server, configured a firewall, and deployed an application to the server (used Amazon Lightsail, Ubuntu, and Flask). Part of the Udacity Full Stack Web Developer Nanodegree.

I deployed the [Item Catalog](https://github.com/bean00/item-catalog) project (which can still be run locally).

## Software Installed
- Apache HTTP Server
- PostgreSQL
- Git
- Flask
- SQLAlchemy

## Configurations
- Updated all installed packages on Ubuntu
- Configured the firewalls (Lightsail and UFW)
    - SSH (port 2200)
    - HTTP (port 80)
    - NTP (port 123)
- Created a user called `grader`
    - Gave `grader` `sudo` access
    - Also created an SSH key pair for `grader`, and forced key-based authentication
- Configured the local timezone to UTC (was already set to UTC)
- Configured Apache to handle requests using the WSGI module
- Configured PostgreSQL, creating a limited user named `catalog`
    - Ensured that remote connections are not allowed
- Configured Git
- Set up and deployed the Item Catalog project

## Third-party Resources Used
- Change the SSH port from 22 to 2200
    - https://knowledge.udacity.com/questions/1009
    - https://postimg.cc/image/uvjqwhpzb/
    - https://www.liquidweb.com/kb/changing-the-ssh-port/
- Configure NTP
    - https://askubuntu.com/questions/709843/how-to-configure-ufw-to-allow-ntp-to-work
- Connect to my instance using SSH
    - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html
- Set up PostgreSQL
    - https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04
- Set up Git
    - https://www.liquidweb.com/kb/install-git-ubuntu-16-04-lts/
- Not allow remote connections to postgres database
    - https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
- Use PostgreSQL instead of SQLite
    - http://docs.sqlalchemy.org/en/latest/core/engines.html
    - http://www.patricksoftwareblog.com/database-using-postgresql-and-sqlalchemy/
- Deploy a Flask application on Ubuntu
    - https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
