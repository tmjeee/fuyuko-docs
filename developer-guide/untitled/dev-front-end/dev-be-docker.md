# Dev - FE - Docker

Docker's dockerfile is located at `docker/dockerfile`

## `Build docker image`

```text
$> ./docker-build.sh
```

This will tak care of removing previous created image and create a new one with the tag of `tmjee/fuyuko-fe`.

## Run a docker image

```text
$> ./docker-run.sh
```

This will take care of removing previous created container and create a new one named `tmjee-fuyuko-fe`

## See docker image created

```text
$> docker image ls | grep -i tmjee
```

This will list all fuyuko application related docker images

## See docker container created

```text
$> docker container ls | grep -i tmjee
```

This will list all fuyuko application related docker containers

## See docker container's logs

```text
$> docker logs tmjee-fuyuko-fe
```

