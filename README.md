# Maintenance page

## Description

This repository contains a simple maintenance page and the configuration of the nginx web server.

## Instructions

1. Setup webserver with nginx.
2. Go to ```cd /var/www```.
3. Clone repo with: ```git clone https://github.com/PHKA-ZIM/maintenance.git```.
4. Go to ```cd /etc/nginx``` and remove ```rm nginx.conf``` and symlink nginx.conf with ```ln -s /var/www/maintenance/nginx/nginx.conf```.
5. Go to ```cd /etc/nginx/sites-available``` and symlink maintenance with ```ln -s /var/www/maintenance/nginx/sites-available/maintenance```.
6. Go to ```cd /etc/nginx/sites-enabled``` and disable default site with ```rm default``` if enabled.
7. Go to ```cd /etc/nginx/sites-enabled``` and enable site with ```ln -s /etc/nginx/sites-available/maintenance```.
8. Restart nginx web server with ```service nginx restart```.

