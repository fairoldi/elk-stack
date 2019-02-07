FROM docker.elastic.co/beats/filebeat:6.5.1

# Volume used to read logs from the backend app
VOLUME [ "/var/log/empamini" ]

COPY filebeat.yml /usr/share/filebeat/filebeat.yml
COPY wait-for-it.sh /usr/share/filebeat/wait-for-it.sh

USER root
RUN chown root:filebeat /usr/share/filebeat/filebeat.yml
RUN chown root:filebeat /usr/share/filebeat/wait-for-it.sh
RUN chmod a+rx /usr/share/filebeat/wait-for-it.sh

USER filebeat

