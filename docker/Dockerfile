FROM  alpine:3.8
MAINTAINER Wenpeng Xiao <xiaowp@flamingoeda.com>

# Install packages.
RUN apk update && \
  apk add --no-cache hostapd dnsmasq

# Clean up when done.
RUN rm -rf /tmp/* /var/cache/apk/* /var/tmp/*

# Initialize script when container start.
COPY start_ap.sh /usr/bin/start_ap
RUN chmod a+x /usr/bin/start_ap
