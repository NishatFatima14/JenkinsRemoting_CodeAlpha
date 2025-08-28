FROM jenkins/jenkins:lts-jdk17

USER root
RUN apt-get update \
    && apt-get install -y git sudo \
    && rm -rf /var/lib/apt/lists/*

# Pre-install essential plugins
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli --plugin-file /usr/share/jenkins/ref/plugins.txt

# Let Jenkins run as the jenkins user
USER jenkins
