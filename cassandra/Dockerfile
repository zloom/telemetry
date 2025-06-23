from cassandra:4.0.15

RUN wget https://github.com/prometheus/jmx_exporter/releases/download/1.1.0/jmx_prometheus_javaagent-1.1.0.jar -O /opt/jmx_prometheus_javaagent.jar

COPY jmx-exporter-config.yaml /opt/jmx-exporter-config.yaml
COPY logback.xml /etc/cassandra/logback.xml

ENV JVM_EXTRA_OPTS=-javaagent:/opt/jmx_prometheus_javaagent.jar=7070:/opt/jmx-exporter-config.yaml

EXPOSE 7070