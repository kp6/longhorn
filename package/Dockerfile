FROM ubuntu:16.04
RUN apt-get update && apt-get install -y kmod curl

RUN curl -sSL -o share-mnt https://github.com/rancher/runc/releases/download/share-mnt-v0.0.3/share-mnt && \
    chmod u+x share-mnt && mv share-mnt /usr/bin

COPY longhorn longhorn-agent launch launch-driver docker-longhorn-driver copy-binary launch-replica-with-vm-backing-file /usr/bin/
CMD ["longhorn"]
