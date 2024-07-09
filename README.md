Docker Compose File
The docker-compose.yml file consists of the following services:

MySQL Database (my_mysql_db):

Uses the mysql:5.7 image.
Configured with environment variables for the database.
PHP Laravel API (my_laravel_api):

Uses the php:8.0-apache image.
Copies application source code and installs dependencies.
Nginx Proxy (my_nginx_proxy):

Uses the nginx:latest image.
Configured to listen on port 443 with SSL.
Acts as a reverse proxy for the Laravel API.

Building and Starting Containers:

sh
Copy code
docker-compose up --build
Stopping Containers:

sh
Copy code
docker-compose down
Viewing Container Logs:

sh
Copy code
docker-compose logs
Restarting Docker Service:

sh
Copy code
sudo systemctl restart docker
Self-Signed SSL Certificate
Generate SSL Certificate:

sh
Copy code
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-selfsigned.key -out nginx-selfsigned.crt
Generate Diffie-Hellman Group:

sh
Copy code
openssl dhparam -out dhparam.pem 2048
Copy Certificates to Nginx Container:
Add the following lines to docker-compose.yml:
