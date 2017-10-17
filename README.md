# crawlers


# Requirement

Install Docker

https://docs.docker.com/engine/installation/

# How to use

After clone this repository, you need to build docker image using Dockerfile.

```
docker build -t=crawler-dev .
```

Running instance of image.

```
docker run -it -v="$PWD/demo:/opt/notebooks" -p 8888:8888 crawler-dev /bin/bash -c "/opt/conda/bin/conda install jupyter -y --quiet  && /opt/conda/bin/jupyter notebook --allow-root --notebook-dir=/opt/notebooks --ip='*' --port=8888 --no-browser"
```

If it runs successfully, you will see something like this on your terminal

```
Copy/paste this URL into your browser when you connect for the first time,
to login with a token:
  http://localhost:8888/?token=xxxxxxxxxxxx
```

Just follow it.
