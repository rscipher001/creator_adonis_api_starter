# How to deploy

This file contains instructions on how to deploy this project on a VPS

## Requirement

You will need access to a VPS with the following software installed:your_
- NodeJS
- NPM
- NPM package `pm2` globally installed using `npm i -g pm2`
- Nginx (`sudo apt install nginx` on Ubuntu/Debian based systems)

## How to host
Push code to your server using FTP(SFTP) or rsync and run `npm ci` in the project root.

Update `nginx.conf` file and put it into `/etc/nginx/sites-enabled` on your server and run `sudo nginx -s reload`

## How to enable HTTPS
You can use Let's Encrypt to generate a free SSL certificate for your domain. Refer to https://certbot.eff.org/ for more information. Here are instructions on how to do it on Ubuntu 20.04 server

```bash
sudo apt install python3-certbot-nginx
sudo certbot -d <yourdomain.com> # and follow steps
```
