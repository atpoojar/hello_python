FROM python:3.7
RUN curl -fsSLO https://get.docker/builds/Linux/x86_64/docker-17.04.0-ce.tgz \
  && tar xzvf docker-17.04.0-ce.tgz \
  && mv docker/docker /usr/local/bin \
  && rm -r docker docker-17.04.0-ce.tgz

RUN mkdir /app
WORKDIR /app
ADD . /app/
RUN pip install -r app/requirements.txt

EXPOSE 5000
CMD ["python", "/app/main.py"]
