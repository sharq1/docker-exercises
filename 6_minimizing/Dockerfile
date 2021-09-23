# set base image (host OS)
FROM python:3.9.7-alpine

ENV FLASK_APP=server.py
ENV FLASK_RUN_HOST=0.0.0.0

# set the working directory in the container
WORKDIR /code

# copy the content of the local src directory to the working directory
COPY src/ .

# copy the dependencies file to the working directory
COPY requirements.txt .

# Install build dependencies
RUN apk add --no-cache gcc musl-dev linux-headers && pip install --user -r requirements.txt

# document that server listens on port 5000
EXPOSE 5000

# command to run on container start
ENTRYPOINT ["flask", "run"]

# potentially useful info: `pip install` caches the downloaded packages - but we don't need these caches in final image - you can find cache using `pip cache dir`
# potentially useful info: `pip install` with `--user` flag as above saves the dependencies to `/root/.local`
