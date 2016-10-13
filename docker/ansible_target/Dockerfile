FROM philm/ansible_target:latest

USER root

COPY docker_rsa.pub /root/.ssh/authorized_keys

RUN bash -c "chmod 600 $HOME/.ssh/authorized_keys"
