FROM debian:bullseye

#instalando o nginx
RUN apt update 
    apt ugrade
    apt install nginx -y
    apt install openssl

#gerando o certificado autoassinado

CMD sudo openssl req -x509 -nodes -days 365 \
    -newkey rsa:2048 \
    -keyout /etc/ssl/private/nginx-selfsigned.key \
    -out /etc/ssl/certs/nginx-selfsigned.crt