FROM nginx:1.16.1
RUN apt-get update && apt-get install -y nginx-extras

RUN usermod -a -G root www-data

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]