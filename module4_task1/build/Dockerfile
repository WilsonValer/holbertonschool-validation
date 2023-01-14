# Container image that runs your code
FROM golang:1.15.8-buster

# Copies your code file from your action repository to the filesystem path `/` of the container
COPY setup.sh /setup.sh
RUN wget https://github.com/gohugoio/hugo/releases/download/v0.84.0/hugo_extended_0.84.0_Linux-64bit.deb
RUN dpkg -i hugo_extended_0.84.0_Linux-64bit.deb
# Code file to execute when the docker container starts up (`entrypoint.sh`)
ENTRYPOINT ["/setup.sh"]
