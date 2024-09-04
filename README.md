# Mail Server with Postfix and Dovecot
Running Postfix and Dovecot together using Docker Compose involves setting up both services in a docker-compose.yml file and configuring each service appropriately.


## Generate SSL Certificate
```console
mkdir -p ./ssl
openssl req -newkey rsa:2048 -nodes -keyout ./ssl/mailserver.key -x509 -days 365 -out ./ssl/mailserver.crt
```


## Run the Mail Server
After updating the configuration files, run the following command to start the mail server:
```console
docker-compose up -d
```