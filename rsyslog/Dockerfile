FROM debian:bookworm-slim
RUN apt-get update && \
    apt-get install -y rsyslog && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
RUN mkdir -p /var/log/network
EXPOSE 1514/udp 1514/tcp
CMD ["rsyslogd", "-n", "-f", "/etc/rsyslog.conf"]
