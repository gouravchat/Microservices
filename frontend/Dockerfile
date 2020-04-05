FROM python:3-alpine

MAINTAINER Gourav Chatterjee 

COPY ./frontend_serv/requirements.txt /app/requirements.txt

WORKDIR /app

RUN apk add --update \
  && pip install --upgrade pip  \
  && pip install -r requirements.txt \
  && rm -rf /var/cache/apk/*

COPY ./frontend_serv /app

WORKDIR /app

CMD python3 app.py -h 0.0.0.0
