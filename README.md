## tims packages

simple repo containing some of my public packages.

Currently:

- `Dockerfile.alpine_langchain`: `ghcr.io/tbscode/tims-packages_alpine_langchain:latest` A minimal alpine python image with my langchain frok pre-installed.
- `Dockerfile.alpine_bash_yq`: `ghcr.io/tbscode/tims-packages_alpine-bash-yq-make:latest` A minimal alpine make yq bash image

## Build / Update images

automaticly done using the workflows or:

```
echo $(gha_token) | docker login ghcr.io -u $(github_user) --password-stdin
```

### langchain

```
docker build -f Dockerfile.alpine_langchain -t ghcr.io/tbscode/tims-packages_alpine_langchain:latest .
docker push ghcr.io/tbscode/tims-packages_alpine_langchain:latest
```

### alpine bash make yq

```
docker build -f Dockerfile.alpine_bash_yq -t ghcr.io/tbscode/tims-packages_alpine-bash-yq-make:latest .
docker push ghcr.io/tbscode/tims-packages_alpine-bash-yq-make:latest
```