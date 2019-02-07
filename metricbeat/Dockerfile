FROM docker.elastic.co/beats/metricbeat:6.5.1

COPY metricbeat.yml /usr/share/metricbeat/metricbeat.yml
COPY wait-for-it.sh /usr/share/metricbeat/wait-for-it.sh

USER root
RUN chown root:metricbeat /usr/share/metricbeat/metricbeat.yml
RUN chown root:metricbeat /usr/share/metricbeat/wait-for-it.sh
RUN chmod a+rx /usr/share/metricbeat/wait-for-it.sh
USER metricbeat