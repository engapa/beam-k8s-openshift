# beam-k8s-openshift

Apache Beam is

A single docker container and how to deploy on docker-compose,
kubernetes and openshift.

## Docker

In [docker directory](docker) we have three Dockerfiles:

- Dockerfile.python: A dockerfile with python SDK
- Dockerfile.jdk: A dockerfile with Java SDK ([based on it](https://github.com/carlossg/docker-maven/blob/2357d3394f19730172ac9c7f4afe7cf052f36b4d/jdk-7/Dockerfile))
- Dockerfile: A dockerfile with both java and python SDK.

Building the docker image:

```sh
$ docker build --no-cache -t engapa/beam[:SDK] -f docker/Dockerfile[.SDK] docker
```
> NOTE: Choose one SDK of: python,jdk or '' (none means both SDKs)

## Kubernetes

Work in progress ...

## Openshift

Work in progress ...

## TODO
[ ] Runners: Apex, Flink, Spark.
