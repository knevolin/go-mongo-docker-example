FROM golang:1.12.1

ENV GO111MODULE=on

RUN adduser --disabled-password --gecos '' api
USER api

RUN export GIT_SSL_NO_VERIFY=1
RUN git config --global http.sslverify false

WORKDIR /go/src/app
COPY . .

RUN go get github.com/pilu/fresh
RUN go get ./...

CMD [ "fresh" ]
