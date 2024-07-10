# Challenge

### Docker Compose file
The docker-compose.yml file consists of the following services:

- **MY_SQL DATABAASE**: 1-Uses the mysql:5.7 image.
2-Configured with environment variables for the database.

- **PHPLARAVEL API**: Uses the php:8.0-apache image.
Copies application source code and installs dependencies.
- **NUXUT client**: Uses node18 image.
Copies application source code and installs dependencies.
- **NGINX PROXY**: Uses the nginx:latest image.
Configured to listen on port 443 with SSL.
Acts as a reverse proxy for the Laravel API.



  ```Building and Starting Containers:
   docker-compose up --build
  ```

sudo systemctl restart dockerr-compose down
  ```
   ```Viewing  Containers logs:
   docker-compose logs
  ```
     ```Restarting Docker Service:
  sudo systemctl restart docker
  ```
       ```Restarting Docker Service:
  sudo systemctl restart docker
  ```



  
  
  - **SELFSIGNED SSLCERTIFICATE**
    

     ```Generate SSL Certificate:
 openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-selfsigned.key -out nginx-selfsigned.crt
  ```

