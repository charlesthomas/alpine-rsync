# alpine-rsync

I wanted an alpine image with rsync pre-installed, and I found a few, but they all did other stuff I didn't want

This is literally just:

```Dockerfile
FROM alpine:latest

RUN apk add --no-cache openssh rsync
```

With a github action to publish it so you can:

```bash
docker run --rm -it ghcr.io/charlesthomas/alpine-rsync:latest rsync --help
```
