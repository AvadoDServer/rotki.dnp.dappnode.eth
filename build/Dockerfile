FROM ubuntu

RUN apt-get update && apt-get install -y wget unzip
RUN wget https://github.com/rotkehlchenio/rotkehlchen/releases/download/v1.0.4/rotki-linux-x64-v1.0.4.zip
RUN unzip rotki-linux-x64-v1.0.4.zip -d /opt
RUN rm rotki-linux-x64-v1.0.4.zip

ENTRYPOINT /opt/rotki-linux-x64-v1.0.4/rotki-v1.0.4
