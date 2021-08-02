# # execute this command same the same directory of this Dockerfile
# docker build -t download-gcs -f Dockerfile .
FROM gcr.io/google.com/cloudsdktool/cloud-sdk:alpine

WORKDIR /app
COPY gcs-key.json gcs-key.json
RUN echo "active account with gcs-key.json" && \
    echo "set default project"
RUN echo "gsutil download something" 
RUN rm gcs-key.json
