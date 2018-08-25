# DNS
- add domain in digital ocean
- change nameservers of domain. [Link](https://www.digitalocean.com/community/tutorials/how-to-point-to-digitalocean-nameservers-from-common-domain-registrars)
- IPv4: add A record

# Apache
- [Virtual Hosts](https://httpd.apache.org/docs/2.4/vhosts/name-based.html) in /etc/apache2/sites-available/000-default.conf

## PHP 7
- `apt-cache search php7.0-*`: Show all modules available for installation 
- `apt-get install php7.0-{mod1,mod2}`: Install all listed modules

## MySQL
- Start as root: `mysql -u root -p`
- Adding new `user` with `password` and `database`, grant all priviliges:
```SQL
CREATE USER 'user'@'localhost' IDENTIFIED BY 'password';
CREATE DATABASE database;
GRANT ALL PRIVILEGES ON database.* TO 'user'@'localhost';  
FLUSH PRIVILEGES;
``` 

# SSH
- add none-root super-user and deactivate access via pasword: [DigitalOcean Initial Server Setup](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-16-04)

# SSL 
- Before: Add [Virtual Host](#apache)
- [Lets Crypt in Digital ocean](https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-16-04)
- maybe need to change /etc/apache2/sites-enabled/000-default-le-ssl.conf (set ports to 443)
- After changes: `service apache restart`

# Important Accounts to remember
- Server root
- MySQL root

# Workflow (MAYBE):
1. Create Server, configure [SSH](#ssh)
2. Add folder in `var/www/html` for project with dummy html/phpinfo... or  project content
3. Add [Virtual Host](#apache) to direct domain to this folder (for http at first)
4. Add subdomain / domain for project in [DNS](#dns)
5. Make [SSl certificates](#ssl), check if it is right configured
6. Test HTTPS
6. Create [MySQL](#mysql) user and DB
7. Configure [PHP](#php-7)
8. Configure / Setup App