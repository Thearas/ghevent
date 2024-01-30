FROM naskio/n8n-python:1.15.2

USER root

RUN apk update && apk add bash wget curl jq tar coreutils && \
    curl -fsSL https://github.com/cli/cli/releases/download/v2.34.0/gh_2.34.0_linux_amd64.tar.gz -o gh.tar.gz  && \
    tar xzf gh.tar.gz && cp gh_2.34.0_linux_amd64/bin/gh /usr/local/bin && rm -rf gh.tar.gz gh_2.34.0_linux_amd64 && \
    cd /usr/local/lib/node_modules/n8n && npm install n8n-nodes-python

