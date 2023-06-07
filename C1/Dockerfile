FROM ubuntu:14.10
RUN sed -i 's/archive.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list && \
    sed -i 's/security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y openssh-server && \
    useradd --create-home --shell /bin/bash test && \
    echo 'test:test' | chpasswd

CMD service ssh start && bash
EXPOSE 22
RUN service ssh restart

