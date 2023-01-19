# Container image that runs your code
FROM golang:1.15.8-buster
RUN apt update
RUN apt install git
RUN git clone https://github.com/WilsonValer/holbertonschool-validation.git
RUN mv holbertonschool-validation/* .
RUN apt install xz-utils
RUN apt install make -y
RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash -
RUN apt install nodejs
RUN npm install -g markdownlint-cli
RUN apt install zip -y
RUN apt install sudo -y
# Copies your code file from your action repository to the filesystem path `/` of the container
RUN wget https://github.com/gohugoio/hugo/releases/download/v0.84.0/hugo_extended_0.84.0_Linux-64bit.deb
RUN dpkg -i hugo_extended_0.84.0_Linux-64bit.deb
# Code file to execute when the docker container starts up (`entrypoint.sh`)
