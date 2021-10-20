FROM alpine:latest
RUN apk add --update --no-cache openssh 
RUN echo 'PasswordAuthentication yes' >> /etc/ssh/sshd_config
RUN adduser -h /home/GwlSSHPxyUser -s /bin/sh -D GwlSSHPxyUser
RUN echo -n 'GwlSSHPxyUser:BRWe7dzyPUpJXA4AD0Al' | chpasswd
ENTRYPOINT ["/entrypoint.sh"]
EXPOSE 22
COPY entrypoint.sh /
