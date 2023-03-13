FROM ubuntu

RUN apt-get update && apt-get install nginx -y

COPY nginx.conf /etc/nginx/nginx.conf
COPY index.html /var/www/html/
RUN mkdir /var/www/html/css
COPY css/*  /var/www/html/css/
ADD media/ /var/www/html/

EXPOSE 80

CMD ["nginx","-g", "daemon off;"]