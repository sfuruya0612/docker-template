# td-agent

## Architecture

localhost -(port: 8080)-> nginx -> (output nginx logs) -> td-agent -> (output td-agent logs)  

## Getting started

### Image build and launch backgroud

``` sh
make up
```

### Container down

``` sh
make down
```
