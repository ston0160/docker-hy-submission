# We need golang 1.16
FROM golang:1.16

EXPOSE 8080

WORKDIR /usr/src

# Copy all of the source code
COPY . .

# Run to generate a binary named "server"
RUN go build

# Run tests
RUN go test ./...

# And finally the command to run the application 
CMD ["./server"]
