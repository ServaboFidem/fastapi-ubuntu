FROM ubuntu:jammy
LABEL maintainer="Gordon Mott <gordon.mott@gmail.com>"
COPY requirements.txt /tmp/requirements.txt
RUN apt update -y
RUN apt upgrade -y
RUN apt install -y python3 python3-pip
# add accelerated imaging libraries
RUN apt install -y libjpeg-turbo* libwebp* cmake

# add playwright support
RUN pip install playwright
RUN playwright install-deps
RUN playwright install

RUN pip install --no-cache-dir -r /tmp/requirements.txt

COPY ./start.sh /start.sh
RUN chmod +x /start.sh

COPY ./gunicorn_conf.py /gunicorn_conf.py

COPY ./start-reload.sh /start-reload.sh
RUN chmod +x /start-reload.sh

COPY ./app /app
WORKDIR /app/

ENV PYTHONPATH=/app

EXPOSE 5001

# Run the start script, it will check for an /app/prestart.sh script (e.g. for migrations)
# And then will start Gunicorn with Uvicorn
CMD ["/start.sh"]