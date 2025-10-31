FROM fluent/fluentd:edge-debian
USER root
RUN gem install fluent-plugin-elasticsearch --no-document --version 5.4.3
# Optionally install other plugins if needed
# RUN gem install fluent-plugin-docker --no-document

# Copy Fluentd configuration file
COPY fluent.conf /fluentd/etc/fluent.conf

# Ensure correct permissions
RUN chown fluent:fluent /fluentd/etc/fluent.conf
USER fluent