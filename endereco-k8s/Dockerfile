FROM golang:1.15-alpine

WORKDIR /app

COPY go.mod ./
COPY go.sum ./
RUN go mod download

COPY . .

RUN go build -o /endereco

EXPOSE 8080

CMD [ "/endereco" ]