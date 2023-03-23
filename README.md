# fastapi-ubuntu

* Currently built against jammy / python 3.10.
* Incorporating libjpeg-turbo and libwebp, to optimize for use of pillow-simd.
* Puppeteer support baked in.

Default configuration is for 2 workers per CPU, running on port 5001.

Premade docker image is available at:
https://hub.docker.com/repository/docker/servabofidem/fastapi-ubuntu

# Credit due to Sebastián Ramírez
Forked from: https://github.com/tiangolo/uvicorn-gunicorn-fastapi-docker
I just don't like Alpine, and I wanted a more useful base image without having to deal with a million different layers.
