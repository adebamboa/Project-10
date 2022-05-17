## CONFIGURE NGINX AS A LOAD BALANCER

` sudo apt update && sudo apt install nginx -y`

`sudo systemctl enable nginx && sudo systemctl start nginx`

`sudo systemctl status nginx`

[NGINX.PNG](./images/NGINX%20RUNNING.jpg)

`sudo vi /etc/nginx/sites-available/load_balancer.conf`

`sudo rm -f /etc/nginx/sites-enabled/default`

`sudo nginx -t`

[NGINX2.PNG](./images/NGINX%20SUCCEFULLY%20CONFIGURED.jpg)

`cd /etc/nginx/sites-enabled/`

`sudo ln -s ../sites-available/load_balancer.conf .`

[NGINX3.PNG](./images/LOAD%20BALANCER%20POINTED%20TO%20THE%20AVAILABLE%20SITES.jpg)

`sudo systemctl reload nginx`

[NGINX4.PNG](./images/REGISTERED%20DOMAIN.jpg)

[NGINX5.PNG](./images/My%20doamin%20loading%20the%20page..jpg)

`sudo apt install certbot -y`

`sudo apt install python3-certbot-nginx -y`

`sudo certbot --nginx -d bam-bo.co.uk -d www.bam-bo.co.uk`

[NGINX7.PNG](./images/SECURED%20WEB%20PAGE.jpg)


[NGINX8.PNG](./images/Certificate%20Issues%20information..jpg)


[NGINX9.PNG](./images/certificate%20installed..jpg)

`crontab -e`


[NGINX10.PNG](./images/crontab%20-e.jpg)






