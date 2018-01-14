FROM logstash

MAINTAINER kobadlve

ADD conf/ /root/conf

# Config
RUN cd /root/conf && \
    mkdir -p /etc/logstash/conf.d && \
    cp logstash.conf /etc/logstash/conf.d

RUN rm -rf /root/*
# Start logstash
CMD /usr/share/logstash/bin/logstash -f /etc/logstash/conf.d/logstash.conf
