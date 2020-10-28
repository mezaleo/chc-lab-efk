#Indico la imagen base
FROM nginx

EXPOSE 80

ADD index.html /usr/share/nginx/html/

ADD nginx/nginx.conf /etc/nginx/
ADD nginx/default.conf /etc/nginx/conf.d/
ADD nginx/expires.conf /etc/nginx/conf.d/