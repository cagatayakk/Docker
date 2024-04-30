##
## Build the application from source
##

FROM golang:1.19 AS build-stage

WORKDIR /app

COPY go.mod go.sum ./
RUN go mod download

COPY *.go ./

RUN CGO_ENABLED=0 GOOS=linux go build -o /docker-gs-ping
RUN useradd nonroot

##
## Deploy the application binary into a lean image
##

FROM scratch AS build-release-stage

WORKDIR /

COPY --from=build-stage /docker-gs-ping /docker-gs-ping
COPY --from=build-stage /etc/passwd /etc/passwd

EXPOSE 8080

ENTRYPOINT ["/docker-gs-ping"]