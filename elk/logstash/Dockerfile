FROM logstash

MAINTAINER kobadlve

RUN mkdir -p /data_logstash/
VOLUME ["/data_logstash/"]

# Start logstash
CMD /usr/share/logstash/bin/logstash -f /etc/logstash/conf.d/logstash.conf
