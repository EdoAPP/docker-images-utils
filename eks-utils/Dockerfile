FROM alpine:latest

LABEL maintainer="Eduardo Pacheco"

ENV PACKAGES "curl python py-pip"

RUN apk add --no-cache $PACKAGES && \
    pip install awscli && \
    curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl && \
    chmod +x ./kubectl && \
    mv ./kubectl /usr/local/bin/kubectl