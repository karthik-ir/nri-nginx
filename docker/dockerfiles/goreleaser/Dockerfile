# Based on https://github.com/goreleaser/goreleaser/blob/master/Dockerfile
FROM golang:1.14-alpine

ENV GITHUB_TOKEN 0f823963adb6b7e9f36e1f0cbb9361be06a09c83

RUN apk add --no-cache bash \
                       bzr \
                       curl \
                       docker-cli \
                       git \
                       rpm

RUN curl -sfL https://install.goreleaser.com/github.com/goreleaser/goreleaser.sh | sh

COPY .goreleaser.yml /
COPY . /repo

WORKDIR /repo/src
