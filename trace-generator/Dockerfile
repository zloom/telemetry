from alpine:3.21.3 AS cert

run apk add --update --no-cache ca-certificates

from jaegertracing/example-hotrod:1.63.0

copy --from=cert /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/ca-certificates.crt