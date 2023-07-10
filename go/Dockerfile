FROM golang:1-alpine3.18 AS builder

WORKDIR /usr/src/app
COPY ./src .
RUN go build .

FROM scratch
WORKDIR /usr/src/app
COPY --from=builder /usr/src/app/hello hello
CMD [ "./hello" ]


