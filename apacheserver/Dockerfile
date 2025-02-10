FROM debian:12

RUN apt update && apt install -y net-tools procps most iproute2  iputils-ping whois

RUN apt install -y rsyslog apache2

RUN apt clean && rm -rf /var/lib/apt/list/*

RUN a2enmod auth_digest.load

RUN a2enmod authz_groupfile.load

RUN a2enmod ssl

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]