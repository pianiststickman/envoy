FROM golang:alpine@sha256:1e2917143ce7e7bf8d1add2ac5c5fa3d358b2b5ddaae2bd6f54169ce68530ef0 AS builder

RUN apk --no-cache add make
COPY . /app
RUN make -C /app/grpc-service

FROM alpine@sha256:124c7d2707904eea7431fffe91522a01e5a861a624ee31d03372cc1d138a3126

COPY --from=builder /app/grpc-service/server /app/server
CMD ["/app/server", "-users", "/etc/users.json"]
