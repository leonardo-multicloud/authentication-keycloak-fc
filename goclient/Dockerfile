## Build
FROM golang:1.20rc1-alpine3.17

WORKDIR /app

COPY go.mod .
COPY go.sum .

RUN go mod download
RUN go mod verify

COPY *.go .

# Build the Go app
RUN go build -o /go-default-app

EXPOSE 8081

CMD [ "/go-default-app" ]