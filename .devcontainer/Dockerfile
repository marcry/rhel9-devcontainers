FROM registry.access.redhat.com/ubi9/ubi:latest

LABEL dev.containers.features="common"

USER root

RUN dnf install -y \
        systemd sudo git autoconf automake libtool \
    && dnf clean all \
    && rm -rf /var/cache/yum

ENTRYPOINT ["/sbin/init"]