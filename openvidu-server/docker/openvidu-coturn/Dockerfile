FROM ubuntu:16.04

RUN apt-get update \
    && apt-get install -y coturn curl

COPY ./configuration-files.sh /tmp/
COPY ./entrypoint.sh /usr/local/bin

RUN chmod +x /tmp/configuration-files.sh \
    && chmod +x /usr/local/bin/entrypoint.sh

CMD /usr/local/bin/entrypoint.sh