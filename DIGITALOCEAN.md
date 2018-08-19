# DNS
- add domain in digital ocean
- set nameservers of domain. [Link](https://www.digitalocean.com/community/tutorials/how-to-point-to-digitalocean-nameservers-from-common-domain-registrars)
- IPv4: add A record

# Apache
- /etc/apache2/sites-available/000-default.conf -> [Virtual Hosts](https://httpd.apache.org/docs/2.4/vhosts/name-based.html)

# SSH
- add none-root super-user and deactivate access via pasword: [DigitalOcean Docu](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-16-04)

# SSL 
- Lets Crypt in Digital ocean. [Link](https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-16-04)
- maybe need to change /etc/apache2/sites-enabled/000-default-le-ssl.conf (set ports to 443)
- `service apache restart`
