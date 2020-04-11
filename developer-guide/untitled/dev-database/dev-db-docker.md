# Dev - DB - Docker



Docker's dockerfile is located at `docker/dockerfile`

## `Build docker image`

```text
$> ./docker-build.sh
```

This will tak care of removing previous created image and create a new one with the tag of `tmjee/fuyuko-db`.

## Run a docker image

```text
$> ./docker-run.sh
```

This will take care of removing previous created container and create a new one named `tmjee-fuyuko-db`

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
$> docker logs tmjee-fuyuko-db
```

## Inspect docker container's properties

```text
$> docker inspect tmjee-fuyuko-fe
```

