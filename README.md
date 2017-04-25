# Linux-Server

1. * IP Address: `52.23.204.218`
    * ssh port: `2200`
2. * URL of hosted web-application: `http://52.23.204.218/`
3.   * Software installed: 
        * apache2 (`sudo apt-get install apache2`)
        * mod_wsgi (`sudo apt-get install libapache2-mod-wsgi python-dev`)
        * postgresql (`sudo apt-get install postgresql postgresql-contrib`)
        * `pip`
        * `virtualenv` using pip
        * In virtualenv, installed `Flask`, `sqlalchemy`, `oauth2client`, `requests` using pip python-psycopg2
        
    * Configuration changes:
        * `/etc/ssh/sshd_config` 
            - Disabled remote root login (PermitRootLogin no)
            - Disabling password authentication (PasswordAuthentication no)
        * Given sudo access to grader (added a file in `/etc/sudoers.d`)
        * Used `ufw` to allow connections only for SSH (port 2200), HTTP (port 80), and NTP (port 123)
        * Created a Virtual Host by adding `FlaskApp.conf` in ` /etc/apache2/sites-available/`
        * `.wsgi` file added in /var/www/FlaskAPp directory

4. Third-party resources:
    * Used `oauth2` providers - Google and Facebook login. 
