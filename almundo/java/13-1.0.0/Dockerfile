FROM openjdk:13
MAINTAINER Franco Morinigo <franco.morinigo@almundo.com>

# Install jq
RUN yum -y update && \
 		yum -y install wget

WORKDIR /bin
RUN wget "http://stedolan.github.io/jq/download/linux64/jq" && chmod 755 jq

WORKDIR /

# Copy java startup script
COPY startup.sh startup.sh
RUN chmod +x startup.sh

CMD ["./startup.sh"]

# Application port
EXPOSE 8080

# JMX or Debugging port
EXPOSE 9010
