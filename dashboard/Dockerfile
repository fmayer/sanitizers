FROM docker.io/library/golang:bookworm

WORKDIR /app
COPY go.mod go.sum .
RUN go mod download
COPY *.go .
RUN go build -v -o sanitizers

CMD ["/app/sanitizers", "--serve"]
