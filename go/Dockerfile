FROM golang:1.8

WORKDIR /var/www/html/app_local

# pre-copy/cache go.mod for pre-downloading dependencies and only redownloading them in subsequent builds if they change
#COPY go.mod go.sum ./
#RUN go mod download && go mod verify

#COPY . .
#RUN go build -v -o /usr/local/bin/app ./...

CMD tail -f /dev/null
