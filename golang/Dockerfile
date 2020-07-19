FROM golang:1.14.6-alpine3.12 AS builder
COPY ./hello.go .
RUN go build -o /go/bin/hello

FROM scratch
COPY --from=builder /go/bin/hello /go/bin/hello
ENTRYPOINT ["/go/bin/hello"]