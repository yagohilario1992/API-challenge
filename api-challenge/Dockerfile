FROM python:3.9.0a3-alpine3.10

RUN echo -e "http://nl.alpinelinux.org/alpine/v3.10/main\nhttp://nl.alpinelinux.org/alpine/v3.10/community" > /etc/apk/repositories

RUN apk update && \
	apk add git \
	build-base \
	tzdata \
	postgresql-dev

RUN cp /usr/share/zoneinfo/America/Sao_Paulo /etc/localtime &&\
	echo "America/Sao_Paulo" > /etc/timezone

RUN mkdir -p /dock-challenge

WORKDIR /api-challenge

COPY ./requirements.txt /api-challenge/

RUN pip install -r requirements.txt

ADD . /api-challenge/
