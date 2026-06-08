FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y nginx

COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

RUN echo "server {\n\
    listen 9000;\n\
    root /var/www/html/softy-pinko-front-end;\n\
    index index.html;\n\
    location / {\n\
        try_files \$uri \$uri/ =404;\n\
    }\n\
}" > /etc/nginx/sites-available/default

CMD ["nginx", "-g", "daemon off;"]
