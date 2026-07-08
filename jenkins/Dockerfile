FROM jenkins/jenkins:lts

USER root

RUN apt-get update && \
    apt-get install -y git wget

RUN wget https://go.dev/dl/go1.26.4.linux-amd64.tar.gz

RUN rm -rf /usr/local/go

RUN tar -C /usr/local -xzf go1.26.4.linux-amd64.tar.gz

ENV PATH=$PATH:/usr/local/go/bin

USER jenkins