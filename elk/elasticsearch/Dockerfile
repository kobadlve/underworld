FROM elasticsearch

MAINTAINER kobadlve

# Setup user, groups and configs
RUN addgroup -g 2000 elasticsearch && \
    adduser -S -H -s /bin/bash -u 2000 -D -g 2000 elasticsearch && \
    chown -R elasticsearch:elasticsearch /usr/share/elasticsearch/ 

RUN mkdir -p /data_elasticsearch/
VOLUME ["/data_elasticsearch/"]

# Start ELK
USER elasticsearch
CMD ["/usr/share/elasticsearch/bin/elasticsearch"]
