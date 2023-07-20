FROM prom/node-exporter:v1.6.0

ENV NODE_ID=none

USER root

COPY conf /etc/node-exporter/

RUN chmod +x /etc/node-exporter/docker-entrypoint.sh

ENTRYPOINT  [ "/etc/node-exporter/docker-entrypoint.sh" ]

CMD [ "/bin/node_exporter" ]
