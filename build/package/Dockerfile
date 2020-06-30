FROM golang:1.13.12-buster AS builder
COPY main.go .
RUN go build -o /app main.go

FROM gcr.io/distroless/static
CMD ["./app"]
COPY --from=builder /app .
