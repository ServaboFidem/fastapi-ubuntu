# fastapi-ubuntu
This release will soon be updated to support different python versions, and ubuntu releases.

* Currently built against jammy / python 3.10.
* Incorporating libjpeg-turbo and libwebp, to optimize for use of [pillow-simd](https://github.com/uploadcare/pillow-simd).
* Puppeteer support baked in.

Default configuration is for 2 workers per CPU, running on port 5001.

Premade docker image is available at:
[https://hub.docker.com/repository/docker/servabofidem/fastapi-ubuntu](https://hub.docker.com/repository/docker/servabofidem/fastapi-ubuntu)

# Credit due to Sebastián Ramírez
Image based on: [https://github.com/tiangolo/uvicorn-gunicorn-fastapi-docker](https://github.com/tiangolo/uvicorn-gunicorn-fastapi-docker)

I just don't like Alpine, and I wanted a more useful base image without having to deal with a million different layers.
