FROM elasticsearch:6.4.0

MAINTAINER kobadlve

ADD conf/ /root/conf/

# Config
RUN cd /root/conf/ && \
    cp elasticsearch.yml  /usr/share/elasticsearch/config/

RUN rm -rf /root/*

# Start ELK
USER elasticsearch
CMD ["/usr/share/elasticsearch/bin/elasticsearch"]
