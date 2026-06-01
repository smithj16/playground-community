FROM golang:1.24.6

RUN mkdir /app
WORKDIR /app
COPY . .

RUN go mod download
RUN go build .

EXPOSE 8080

CMD ["./jwt-revoker", "-server", "krakend_ce:1234"]
