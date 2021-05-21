# NginX
Basic usage of nginx. How to set it up and add configuration.

## Installing nginx
```
$ sudo apt update
$ sudo apt install nginx
```
After installing nginx, add necessary domain and subdomain configurations under `/etc/nginx/` directory. </br>
Add separate `.conf` files for each domain / subdomain as shown in the files in `conf.d` directory. </br>

## Installing Certificates
```
$ apt-get install certbot python3-certbot-nginx
$ certbot --nginx
```
After running the last command you will be prompted to choose the domains for which the certificates need to be installed and configured. Select those and the certificate public and private key files will be generated and certificate related configuration will automatically be added to `.conf` files.  

## Starting NginX
Always before starting / reloading nginx, test if the changed configurations are correct by running this command:
```
$ nginx -t
```
To start nginx, we can simply run:
```
$ nginx
```
To Stop/Reload nginx:
```
$ nginx -s [stop|reload]
```
