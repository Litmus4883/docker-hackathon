FROM nginx:1.26

WORKDIR /workspace

RUN apt-get update && \
    apt-get install -y locales curl

ENV TZ=UTC

# COPY ./web/*.conf /etc/nginx/conf.d/