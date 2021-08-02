# docker build -t simple-worker:no-dependency-do -f 5-no-dependency/do/Dockerfile .
FROM mcr.microsoft.com/dotnet/sdk:5.0-alpine
RUN apk update && \
    apk add curl

RUN curl -o jq -L https://github.com/stedolan/jq/releases/download/jq-1.6/jq-linux64 && \
    chmod +x jq && \
    mv jq /usr/bin/jq

RUN curl -o yq -L https://github.com/mikefarah/yq/releases/download/3.4.1/yq_linux_amd64 && \
    chmod +x yq && \
    mv yq /usr/bin/yq