FROM alpine:latest
RUN apk add --update --no-cache openssh 
RUN echo 'PasswordAuthentication yes' >> /etc/ssh/sshd_config
RUN sed -i 's/AllowTcpForwarding no/AllowTcpForwarding yes/g' /etc/ssh/sshd_config 
RUN adduser -h /home/GwlSSHPxyUser -s /bin/sh -D GwlSSHPxyUser
RUN echo -n 'GwlSSHPxyUser:ASKalD0Al' | chpasswd
ENTRYPOINT ["/entrypoint.sh"]
EXPOSE 22
COPY entrypoint.sh /
