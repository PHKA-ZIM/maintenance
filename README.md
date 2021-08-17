# Maintenance page

## Description

This repository contains a simple maintenance page and the configuration of the nginx web server.

## Instructions

1. Setup webserver with nginx.
2. Clone repo with: ```git clone https://github.com/PHKA-ZIM/maintenance.git```.
3. Go to ```cd /var/www``` and symlink site folder with: ```ln -s path-to-cloned-repo/public maintenance```.
4. Go to ```cd /etc/nginx``` and remove ```rm nginx.conf``` and symlink nginx.conf with ```ln -s path-to-cloned-repo/nginx/nginx.conf```.
5. Go to ```cd /etc/nginx/sites-available``` and symlink maintenance with ```ln -s path-to-cloned-repo/nginx/sites-available/maintenance```.
6. Go to ```cd /etc/nginx/sites-enabled``` and enable site with ```ln -s /etc/nginx/sites-available/maintenance```.
7. Restart nginx web server with ```service nginx restart```.

