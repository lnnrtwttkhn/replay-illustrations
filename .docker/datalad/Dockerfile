FROM python:3-slim

ARG DOCKER_TAG

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get -y update
RUN apt-get -y install --no-install-recommends locales curl gnupg
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen
RUN locale-gen

# add neurodebian sources for git-annex-standalone
RUN curl http://neuro.debian.net/lists/buster.de-m.full > /etc/apt/sources.list.d/neurodebian.sources.list
RUN apt-key adv --recv-keys --keyserver keyserver.ubuntu.com 0xA5D32F012649A5A9
RUN apt-get -y update

# rclone is a useful add-on
RUN curl -O https://downloads.rclone.org/v1.59.2/rclone-v1.59.2-linux-arm64.deb && dpkg -i rclone*deb && rm -f rclone*deb

# install packages
RUN apt-get -y install --no-install-recommends git git-annex-remote-rclone git-annex make

RUN pip3 install "datalad${DOCKER_TAG+==$DOCKER_TAG}"

# clean up
RUN apt-get clean

RUN git config --global user.name "Docker Datalad"
RUN git config --global user.email "docker-datalad@example.com"

ENTRYPOINT ["datalad"]