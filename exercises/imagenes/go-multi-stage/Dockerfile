FROM golang:1.7.3 as builder
WORKDIR /go-multi-stage
RUN go get github.com/sirupsen/logrus
COPY app.go .
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o app .

FROM alpine:latest
WORKDIR /root/
COPY --from=builder /go-multi-stage/app .
CMD ["./app"]
