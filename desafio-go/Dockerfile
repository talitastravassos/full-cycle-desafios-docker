FROM golang:alpine3.16 AS builder

COPY . /app

WORKDIR /app

RUN go build hello.go

FROM scratch

WORKDIR /app

COPY --from=builder /app/hello .

CMD [ "./hello" ]