FROM golang:1.18

LABEL "name"="Go Builder"
LABEL "maintainer"="Greg Lyon <gregslyon@gmail.com>"
LABEL "from"="sosedoff/actions/golang-build/"
LABEL "version"="0.3.0"

LABEL "com.github.actions.name"="Go Builder"
LABEL "com.github.actions.description"="Cross-complile Go programs"
LABEL "com.github.actions.icon"="package"
LABEL "com.github.actions.color"="#E0EBF5"

RUN \
  apt-get update && \
  apt-get install -y ca-certificates openssl zip && \
  update-ca-certificates && \
  rm -rf /var/lib/apt

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
