FROM fluent/fluentd:latest
USER root
COPY conf/fluent.conf /fluentd/etc/fluent.conf
RUN ["gem", "install", "fluent-plugin-elasticsearch", "--no-document", "--version", "3.5.2"]