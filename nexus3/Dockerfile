FROM alpine

RUN apk --no-cache add openjdk8-jre
RUN apk --no-cache add curl tar

ENV NEXUS_USER nexus
ENV NEXUS_HOME /opt/nexus
ENV NEXUS_VERSION 3.3.1-01

RUN mkdir -p /opt/sonatype-work/nexus3 && adduser -D -h $NEXUS_HOME $NEXUS_USER && curl -s https://sonatype-download.global.ssl.fastly.net/nexus/3/nexus-${NEXUS_VERSION}-unix.tar.gz | tar -xz -C $NEXUS_HOME --strip-components=1 nexus-${NEXUS_VERSION} && chown -R ${NEXUS_USER}: $NEXUS_HOME /opt/sonatype-work
USER $NEXUS_USER
WORKDIR $NEXUS_HOME

EXPOSE 8081
CMD ${NEXUS_HOME}/bin/nexus run
