FROM kibana

MAINTAINER kobadlve

# Setup user, groups and configs
RUN sed -i 's/#server.basePath: ""/server.basePath: "\/kibana"/' /usr/share/kibana/config/kibana.yml && \
    sed -i 's/#kibana.defaultAppId: "discover"/kibana.defaultAppId: "dashboards"/' /usr/share/kibana/config/kibana.yml && \
    sed -i 's/#server.host: "localhost"/server.host: "0.0.0.0"/' /usr/share/kibana/config/kibana.yml && \
    sed -i 's/#elasticsearch.url: "http:\/\/localhost:9200"/elasticsearch.url: "http:\/\/elasticsearch:9200"/' /usr/share/kibana/config/kibana.yml && \
    /usr/share/kibana/bin/kibana 2>&1 | grep -m 1 "Optimization of bundles" && \
    addgroup -g 2000 kibana && \
    adduser -S -H -s /bin/bash -u 2000 -D -g 2000 kibana && \
    chown -R kibana:kibana /usr/share/kibana/

RUN mkdir -p /data_kibana/
VOLUME ["/data_kibana/"]

# Start kibana
USER kibana
CMD ["/usr/share/kibana/bin/kibana"]
