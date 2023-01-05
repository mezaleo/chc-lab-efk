FROM fluent/fluentd:latest
USER root
COPY conf/fluent.conf /fluentd/etc/fluent.conf
COPY conf/fluent.conf.1 /fluentd/etc/fluent.conf
RUN ["gem", "install", "faraday-net_http", "--no-document", "--version", "2.1.0"]
RUN ["gem", "install", "fluent-plugin-elasticsearch", "--no-document", "--version", "5.2.4"]
