# TinkerPop3

Run TinkerPop3 Gremlin console/server in a Docker container.

## Gremlin console

Adapt the version number. Here is an example for TinkerPop 3.2.5:

### Build

    docker build -f ./Dockerfile-gremlin-console -t gremlin-console:3.2.5 --build-arg tinkerpopVersion=3.2.5 [--build-arg https_proxy=$https_proxy] .
    
### Run

    docker run -it --rm gremlin-console:3.2.5

## Gremlin server

Adapt the version number. Here is an example for TinkerPop 3.2.5:

### Build

    docker build -f Dockerfile-gremlin-server -t gremlin-server:3.2.5 --build-arg tinkerpopVersion=3.2.5 [--build-arg https_proxy=$https_proxy] .

### Run

    docker run -d -p 8182:8182 --name gremlin-server gremlin-server:3.2.5
