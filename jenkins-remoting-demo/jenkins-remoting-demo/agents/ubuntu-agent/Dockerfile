FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \         && apt-get install -y openssh-server openjdk-17-jdk git sudo \         && mkdir -p /var/run/sshd \         && useradd -m -s /bin/bash jenkins \         && echo 'jenkins:jenkins' | chpasswd \         && usermod -aG sudo jenkins \         && echo 'jenkins ALL=(ALL) NOPASSWD:ALL' > /etc/sudoers.d/jenkins \         && chmod 0440 /etc/sudoers.d/jenkins \         && echo "PasswordAuthentication yes" >> /etc/ssh/sshd_config \         && echo "PermitRootLogin no" >> /etc/ssh/sshd_config

EXPOSE 22
CMD ["/usr/sbin/sshd","-D","-e"]
