FROM ubuntu:20.10
RUN sed -i 's/archive.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list && \
    sed -i 's/security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y tcpdump && \
    apt-get install -y openssh-server && \
    useradd --create-home --shell /bin/bash test && \
    echo 'test:test' | chpasswd

EXPOSE 22
CMD service ssh start && bash
RUN service ssh restart

