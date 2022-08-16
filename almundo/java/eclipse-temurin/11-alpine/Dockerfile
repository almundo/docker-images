FROM eclipse-temurin:11-alpine
MAINTAINER Ignacio Gabbarini <ignacio.gabbarini@bibamgroup.com>

RUN apk add --no-cache jq

WORKDIR /

# Copy java startup script
COPY startup.sh startup.sh

CMD ["sh", "startup.sh"]

# Application port
EXPOSE 8080

# JMX or Debugging port
EXPOSE 9010