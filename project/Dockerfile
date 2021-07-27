FROM ubuntu:18.04
RUN apt-get update \
&& apt-get install -y -qq\
    wget \
    sudo \
    apt-transport-https \
    ca-certificates \
    gnupg2
RUN sh -c "echo 'deb https://gitsecret.jfrog.io/artifactory/git-secret-deb git-secret main' >> /etc/apt/sources.list"
RUN wget -qO - 'https://gitsecret.jfrog.io/artifactory/api/gpg/key/public' | apt-key add -
RUN apt-get update && apt-get install -y git-secret=0.4.0
RUN git secret --version