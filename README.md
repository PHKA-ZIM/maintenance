# Maintenance page

## Description

This repository contains a simple maintenance page and the configuration of the nginx web server.

## Instructions

1. Setup webserver with nginx.
2. Go to ```cd /var/www```.
3. Clone repo with: ```git clone https://github.com/PHKA-ZIM/maintenance.git```.
4. Copy ssl public cert to ```/var/www/maintenance/certs/cert.pem```.
5. Copy ssl private cert to ```/var/www/maintenance/certs/cert.key```.
6. Go to ```cd /etc/nginx``` and remove ```rm nginx.conf``` and symlink nginx.conf with ```ln -s /var/www/maintenance/nginx/nginx.conf```.
7. Go to ```cd /etc/nginx/sites-available``` and symlink maintenance with ```ln -s /var/www/maintenance/nginx/sites-available/maintenance```.
8. Go to ```cd /etc/nginx/sites-enabled``` and disable default site with ```rm default``` if enabled.
9. Go to ```cd /etc/nginx/sites-enabled``` and enable site with ```ln -s /etc/nginx/sites-available/maintenance```.
10. Restart nginx web server with ```service nginx restart```.
