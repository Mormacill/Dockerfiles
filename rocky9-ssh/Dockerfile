FROM rockylinux:9

RUN dnf update -y
RUN dnf install epel-release -y
RUN crb enable
RUN dnf install openssh-server htop -y
RUN ssh-keygen -A

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
