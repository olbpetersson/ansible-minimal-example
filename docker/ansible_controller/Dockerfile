FROM ansible/centos7-ansible:stable

USER root

## COPY private key to controller
COPY docker_rsa /root/.ssh/id_rsa
COPY ssh_config /root/.ssh/config
RUN chmod 600 /root/.ssh/config /root/.ssh/id_rsa
WORKDIR /home

ENTRYPOINT ["bash"]
