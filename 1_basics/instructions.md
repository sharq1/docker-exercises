# Prerequisites

Run this command early to have the following images downloaded for futher use:

```bash
docker pull nginx:alpine && docker pull alpine && docker pull redis:alpine && docker pull rediscommander/redis-commander && docker pull python:3.9.7-alpine
```


# docker command basics exercise

1. Start a simple `nginx:alpine` container (optionally ensure that it gets removed upon stopping)
2. Confirm that it works via a browser
3. Stop the container
4. Remove the stopped container (or confirm that it's gone)