FROM golang:1.26 AS builder

WORKDIR /app

COPY . .

RUN go mod download

RUN go build -o server .

FROM debian:bookworm-slim

WORKDIR /app

COPY --from=builder /app/server .

EXPOSE 8089

CMD ["./server"]