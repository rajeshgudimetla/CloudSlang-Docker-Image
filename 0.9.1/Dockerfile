FROM java:openjdk-7-jre

MAINTAINER Meir Wahnon

RUN groupadd -r cslang && useradd -r -g cslang cslang

RUN mkdir -p /usr/cslang \
  && cd /usr/cslang \
  && wget "https://github.com/CloudSlang/cloud-slang/releases/download/cloudslang-0.9.1/cslang-cli-with-content.tar.gzip" \
  && tar xvf cslang-cli-with-content.tar.gzip \
  && rm cslang-cli-with-content.tar.gzip

WORKDIR /usr/cslang/cslang/bin/

ENTRYPOINT ["sh","cslang"]
