FROM docker.elastic.co/apm/apm-server:6.5.1
EXPOSE 8200:8200

VOLUME [ "/var/log/empamini" ]

COPY apm-server.yml /usr/share/apm-server/apm-server.yml
COPY wait-for-it.sh /usr/share/apm-server/wait-for-it.sh

USER root
RUN chown root:apm-server /usr/share/apm-server/apm-server.yml
RUN chown root:apm-server /usr/share/apm-server/wait-for-it.sh
RUN chmod a+rx /usr/share/apm-server/wait-for-it.sh

USER apm-server 