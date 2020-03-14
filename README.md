# udacity-microservice
[![wnjuguna](https://circleci.com/gh/wnjuguna/udacity-microservices.svg?style=svg)](https://circleci.com/gh/wnjuguna/udacity-microservices)


## Summary:

This project builds and deploys a web-based House-price prediction microservice on Kubernetes.

## Dependencies:
 - python3
 - minikube
 - docker
 - virtualbox

## How to build:

 Create the virtual environment:
```bash
make setup
```
 Upgrades pip and installs python libraries:
```bash
make install
```
lint python and Docker files:
```bash
make lint
```
shortcut for make install and make lint:
```bash
make all
```

## How to deploy on docker:
 Execute the script run_docker.sh. This will:
 - Build an image tagged sklearn:v1
 - Launch a docker container that exposes the microservice on port 8000

## How to publish the new images:
 Execute the `upload_docker.sh` This will:
 - Authenticate and publish the image to hub.docker.com

## How to deploy on kubernetes:
 Execute `run_kubernetes.sh` This will:
 create deployment named sklearn
 create a service exposing the microservice externally

## How to make a prediction:
 Execute the script `make_prediction.sh` This will:
  - Send a JSON formatted request to the microservice. 
