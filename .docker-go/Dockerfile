FROM golang:onbuild as builder

LABEL maintainer="David Kestering<davidkestering@gmail.com>"

WORKDIR /go/src/app
COPY . .

RUN go build -o app .

FROM scratch
COPY --from=builder /go/src/app /
CMD ["/app"]
