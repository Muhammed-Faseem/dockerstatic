# dockerstatic

# A Static Site using Docker and Nginx

This repo contains code for building a simple static website served using an Nginx container inside Docker. The code for the site is contained in `index.html`, and the Nginx config is in `default.conf`. The Dockerfile contains commands to build a Docker Image.

To build a Docker image from the Dockerfile, run the following command from inside this directory

```sh
$ docker build -t staticsite .
```

To run the image in a Docker container, use the following command
```sh
$ docker run -itd  --p 80:80 staticsite 
```

This will start serving the static site on port 8080. If you visit `http://localhost:8080` in your browser, you should be able to see our static site!
