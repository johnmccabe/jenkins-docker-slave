FROM ubuntu:16.04
MAINTAINER John McCabe <john@johnmccabe.net>

RUN apt update \
 && apt -y upgrade \
 && apt install -y git \
                   openssh-server \
                   ruby \
 && sed -i 's|session    required     pam_loginuid.so|session    optional     pam_loginuid.so|g' /etc/pam.d/sshd \
 && mkdir -p /var/run/sshd \
 && adduser --quiet jenkins \
 && echo "jenkins:jenkins" | chpasswd

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
