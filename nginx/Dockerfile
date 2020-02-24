# NGINX image with build artifact

FROM nginx:latest

COPY static.zip /tmp/static.zip

RUN apt-get update -qq \
  && apt-get install -qqy curl wget unzip nano \
  && apt-get clean \
  \
  && unzip /tmp/static.zip -d /usr/share/nginx/assets/

COPY default.conf /etc/nginx/conf.d/default.conf