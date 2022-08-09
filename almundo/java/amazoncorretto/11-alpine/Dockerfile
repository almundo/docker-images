FROM amazoncorretto:11-alpine
MAINTAINER Ignacio Gabbarini <ignacio.gabbarini@bibamgroup.com>

RUN apk add --no-cache wget

WORKDIR /bin
RUN wget "http://stedolan.github.io/jq/download/linux64/jq" && chmod 755 jq

WORKDIR /

# Copy java startup script
COPY startup.sh startup.sh

CMD ["./startup.sh"]

# Application port
EXPOSE 8080

# JMX or Debugging port
EXPOSE 9010