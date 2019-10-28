FROM golang:1.13-stretch

RUN apt-get update \
	&& apt-get install -y mysql-client
WORKDIR /app
COPY go /app/go
COPY public /app/public
COPY sql /app/sql

WORKDIR /app/go
ENV GO111MODULE=on

EXPOSE 8000
CMD ["go", "run", "main.go", "api.go"]
