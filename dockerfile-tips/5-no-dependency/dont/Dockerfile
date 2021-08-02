# docker build -t simple-worker:no-dependency-dont -f 5-no-dependency/dont/Dockerfile .
FROM mcr.microsoft.com/dotnet/sdk:5.0-alpine
RUN apk update && \
    apk add curl && \
    curl -o jq -L https://github.com/stedolan/jq/releases/download/jq-1.6/jq-linux64 && \
    chmod +x jq && \
    mv jq /usr/bin/jq && \
    curl -o yq -L https://github.com/mikefarah/yq/releases/download/3.4.1/yq_linux_amd64 && \
    chmod +x yq && \
    mv yq /usr/bin/yq

# this example show how to minimize the number of layers
# but it is not always good because it bundle different purpose to same layer 

# it will rebuild the whole layer if your just want to change the version of yq