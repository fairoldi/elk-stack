FROM sebp/elk

ENV ES_HOME /opt/elasticsearch
WORKDIR ${ES_HOME}

# these plugins are needed by the filebeat apache2 module
RUN yes | CONF_DIR=/etc/elasticsearch gosu elasticsearch bin/elasticsearch-plugin \
    install -b ingest-geoip
RUN yes | CONF_DIR=/etc/elasticsearch gosu elasticsearch bin/elasticsearch-plugin \
    install -b ingest-user-agent 