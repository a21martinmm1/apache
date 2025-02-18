FROM debian:12

RUN apt update && apt install -y net-tools procps most iproute2  iputils-ping whois

RUN apt install -y rsyslog nginx curl

RUN apt clean && rm -rf /var/lib/apt/list/*

EXPOSE 80

RUN /etc/init.d/nginx restart

CMD ["tail", "-f", "/var/log/nginx/access.log"]