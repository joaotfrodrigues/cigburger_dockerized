FROM nginx:1.26.1

# Set working directory for the web files
WORKDIR /var/www/html

# Install git and clone repositories
RUN apt update && apt install -y git

# Clone the backoffice repository
RUN git clone https://github.com/joaotfrodrigues/cigburger_backoffice.git

# Clone the request repository
RUN git clone https://github.com/joaotfrodrigues/cigburger_request.git

# Clone the kitchen repository
RUN git clone https://github.com/joaotfrodrigues/cigburger_kitchen.git

# Ensure the application can write to this directory
RUN chown -R www-data:www-data /var/www/html

# NGINX CONFIG FILES
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./nginx/cigburger_backoffice.conf /etc/nginx/conf.d/cigburger_backoffice.conf
COPY ./nginx/cigburger_request.conf /etc/nginx/conf.d/cigburger_request.conf
COPY ./nginx/cigburger_kitchen.conf /etc/nginx/conf.d/cigburger_kitchen.conf

# APP CONFIG FILES

# .env
COPY ./files/backoffice.env /var/www/html/cigburger_backoffice/.env
COPY ./files/request.env /var/www/html/cigburger_request/.env
COPY ./files/kitchen.env /var/www/html/cigburger_kitchen/.env

# config.json
COPY ./files/config.json /var/www/html/cigburger_request/config.json
COPY ./files/config.json /var/www/html/cigburger_kitchen/config.json

# constants.php
COPY ./files/backoffice_constants.php /var/www/html/cigburger_backoffice/app/Config/Constants.php
COPY ./files/request_constants.php /var/www/html/cigburger_request/app/Config/Constants.php
COPY ./files/kitchen_constants.php /var/www/html/cigburger_kitchen/app/Config/Constants.php
