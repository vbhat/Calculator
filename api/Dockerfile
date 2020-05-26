# Start from base image
FROM golang:alpine

RUN mkdir -p /backend

# Set the current working directory inside the container
WORKDIR /backend

# Copy go mod and sum files
# COPY go.mod go.sum ./


# Download all dependencies
# RUN go mod download

# Copy source from current directory to working directory
# COPY . .
ADD server.go /backend

# Build the application
RUN go build ./server.go

# Expose necessary port
EXPOSE 8090

# Run the created binary executable after wait for mysql container to be up
# RUN ./server
CMD ["./server"]