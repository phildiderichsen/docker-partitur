FROM ubuntu:bionic

# Install dependencies
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive \
    apt-get install --no-install-recommends -y \
    python3 \
    python3-pip \
    sqlite3 \
    mysql-client \
    git \
    vim \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Start the main process
COPY start.sh /opt/start.sh
RUN chmod +x /opt/start.sh
CMD /opt/start.sh

