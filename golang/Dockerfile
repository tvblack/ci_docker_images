FROM golang:1.12

MAINTAINER tvblack <github@tvblack.com>

RUN set -xe \
    && apt-get update \
    && apt-get install -y mysql-client

RUN set -xe \
    && go get github.com/axw/gocov/gocov \
    && go get github.com/kardianos/govendor \
     golang.org/x/tools/cmd/cover \
     bitbucket.org/liamstask/goose/cmd/goose \
     github.com/alecthomas/gometalinter \
    && gometalinter -i

