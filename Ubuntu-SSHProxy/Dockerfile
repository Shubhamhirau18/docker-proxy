FROM ubuntu:latest
RUN apt update && apt install openssh-server -y
RUN useradd -md /home/GalaxyEuro -s /bin/bash GalaxyEuro
RUN echo 'GalaxyEuro:kUhuJYiqm9oOUezLmaPl' | chpasswd
RUN service ssh start
EXPOSE 22
CMD ["/usr/sbin/sshd","-D"]
