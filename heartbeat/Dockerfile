FROM docker.elastic.co/beats/heartbeat:6.5.1

COPY heartbeat.yml /usr/share/heartbeat/heartbeat.yml
COPY wait-for-it.sh /usr/share/heartbeat/wait-for-it.sh

USER root
RUN chown root:heartbeat /usr/share/heartbeat/heartbeat.yml
RUN chown root:heartbeat /usr/share/heartbeat/wait-for-it.sh
RUN chmod a+rx /usr/share/heartbeat/wait-for-it.sh
USER heartbeat