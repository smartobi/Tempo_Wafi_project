FROM golang:1.16
WORKDIR /app

COPY go.mod ./
COPY go.sum ./
RUN go mod download
RUN go mod tidy
COPY ./worker/main.go ./
COPY . .

RUN go build -o ./worker/main
CMD ["./worker/main" ]



