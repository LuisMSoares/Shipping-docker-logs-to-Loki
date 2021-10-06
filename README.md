# Description
A quick and simple example showing how to send the application container logs to an external instance of Loki.

In this example I was using a Loki instance running on kubernets and using port forwarding to connect to it. 

## Docker loki plugin
Our docker compose will not work without this plugin, so we need to install it. Just follow the instructions on link below.
https://grafana.com/docs/loki/latest/clients/docker-driver/

## Build and Run our test application
`docker-compose up -d --build`

## Loki query
To see our shipped logs on Loki just use this query
`{lokiapp="docker-test-logs"}`

## Stop test application
`docker-compose stop`
