FROM  docker.io/centos
RUN yum install -y wget git unzip 
RUN wget https://dl.gogs.io/0.11.53/gogs_0.11.53_linux_386.zip
RUN unzip gogs_0.11.53_linux_386.zip
ENTRYPOINT ["/gogs/gogs","web"]
