FROM debian:12

RUN apt update && apt install -y net-tools procps iproute2 \
    most iputils-ping dnsutils firefox-esr curl wget

RUN apt clean && rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["firefox-esr"]