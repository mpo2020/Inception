FROM alpine:3.20

#instalando o nginx
RUN apk update && apk upgrade && apk add --no-cache nginx

#gerando o certificado autoassinado

CMD  openssl req -x509 -nodes -days 365 \
    -newkey rsa:2048 \
    -keyout /etc/ssl/private/cert.key \
    -out /etc/ssl/certs/cert.crt\
    -subj="/C=BR/ST=RJ/L=Rio-de-Janeiro/O=1337 School/OU=mpolisse/CN=mpolisse.42.fr"

CMD  ["nginx", "-g", "daemon off;"]

