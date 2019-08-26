FROM phusion/baseimage:master

WORKDIR /root

RUN /bin/bash -c "apt-get update -y && apt-get install -y —no-install-recommends  \
  apt-transport-https \
  ca-certificates \
  curl \
  git \
  gnupg-agent \
  software-properties-common \
  && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add - > /dev/null \
  && add-apt-repository 'deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable' && apt update \
  && apt-get install docker-ce-cli && curl -s -o ballerina.deb https://product-dist.ballerina.io/dev/1.0.0-alpha/ballerina-linux-installer-x64-1.0.0-alpha.deb && apt install ./ballerina.deb \
  && rm -rf /var/lib/apt/lists/* "


// docker build -t iexalt/ballerina-build:1.0.0 -t iexalt/ballerina-build:latest .
