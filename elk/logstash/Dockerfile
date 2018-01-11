FROM logstash

MAINTAINER kobadlve

# Logstash configuration
ADD conf/ /root/conf

RUN cd /root/conf && \
    mkdir -p /etc/logstash/conf.d && \
    cp logstash.conf /etc/logstash/conf.d/

# Start logstash
CMD /usr/share/logstash/bin/logstash -f /etc/logstash/conf.d/logstash.conf
