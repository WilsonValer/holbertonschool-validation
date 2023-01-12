# Container image that runs your code
FROM golang:1.15.8-buster

# Copies your code file from your action repository to the filesystem path `/` of the container
COPY setup.sh /setup.sh

# Code file to execute when the docker container starts up (`entrypoint.sh`)
ENTRYPOINT ["/setup.sh"]
