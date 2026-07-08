FROM jenkins/jenkins:lts

USER root

RUN apt-get update && \
    apt-get install -y git wget ca-certificates curl && \
    install -m 0755 -d /etc/apt/keyrings && \
    curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc && \
    chmod a+r /etc/apt/keyrings/docker.asc && \
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian bookworm stable" > /etc/apt/sources.list.d/docker.list && \
    apt-get update && \
    apt-get install -y docker-ce-cli docker-compose-plugin

RUN wget https://go.dev/dl/go1.26.4.linux-amd64.tar.gz

RUN rm -rf /usr/local/go

RUN tar -C /usr/local -xzf go1.26.4.linux-amd64.tar.gz

ENV PATH=$PATH:/usr/local/go/bin

USER jenkins