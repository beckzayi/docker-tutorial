## Full Node.js Deployment - NGINX, SSL With Lets Encrypt

Video: https://www.youtube.com/watch?v=oykl1Ih9pMg


Commands & Steps: https://gist.github.com/bradtraversy/cd90d1ed3c462fe3bddd11bf8953a896


1. Build a simple Node.js express app locally, and upload to Github

2. Create a droplet in Digital Ocean

3. Set up Node.js
```sudo apt install nodejs```

3. Set up SSH

4. Use SSH to log into your Digital Ocean droplet
```ssh root@<ip_address>```

5. mkdir ```~/apps/```, git clone the project

6. Install pm2, and use pm2 to start your express app

7. On server, ```ufw enable, ufw allow ssh, ufw allow http, ufw allow https```

8. Install Nginx ```sudo apt install nginx```

9. ```sudo nano /etc/nginx/sites-available/default``` server_name & location

9. Create A Record on Digital Ocean with the domain name

10. Add name servers (Digital Ocean) to namecheap (domain name service)

11. Add a free SSL from Lets Encryp
