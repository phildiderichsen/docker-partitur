FROM ubuntu:bionic

# Install dependencies
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive \
    apt-get install --no-install-recommends -y \
    python3 \
    python3-pip \
    sqlite3 \
    git \
    vim \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Fetch partitur code and install dependencies
RUN echo "Break that cacheeeeee ... :-)"
WORKDIR /opt
RUN echo $GIT_EXEC_PATH
RUN git clone https://bitbucket.org/philip_diderichsen/lanchart_partitur.git
WORKDIR lanchart_partitur
RUN pip3 install -r requirements.txt
RUN cp config/config_docker.py config/config.py


# Start the main process
COPY start.sh ./
RUN chmod +x ./start.sh
CMD ./start.sh

