FROM golang:1.12.1

RUN adduser --disabled-password --gecos '' api
USER api

ENV GO111MODULE=on
RUN git config --global http.sslverify false

WORKDIR /go/src/app
COPY . .

RUN go get ./...
RUN go get github.com/pilu/fresh

CMD [ "fresh" ]
