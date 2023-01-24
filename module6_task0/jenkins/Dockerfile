FROM jenkins/jenkins:lts-jdk11
# USER root
COPY --chown=jenkins:jenkins plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt
# COPY and install the plugins
# COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
# RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
# RUN apt-get install openjdk-11-jdk-headless
# RUN apt-get update && apt-get install -y lsb-release
# RUN curl -fsSLo /usr/share/keyrings/docker-archive-keyring.asc \
#  https://download.docker.com/linux/debian/gpg
# RUN echo "deb [arch=$(dpkg --print-architecture) \
#  signed-by=/usr/share/keyrings/docker-archive-keyring.asc] \
#  https://download.docker.com/linux/debian \
#  $(lsb_release -cs) stable" > /etc/apt/sources.list.d/docker.list
# RUN apt-get update && apt-get install -y docker-ce-cli
# USER jenkins
# RUN jenkins-plugin-cli --plugins "blueocean docker-workflow"
