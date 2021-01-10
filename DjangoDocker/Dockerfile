FROM python:3.8

ENV PYTHONUNBUFFERED 1

RUN mkdir /DjangoDocker

WORKDIR /DjangoDocker

ADD . /DjangoDocker/

RUN pip install -r requirements.txt
EXPOSE 8000
CMD exec gunicorn DjangoDocker.wsgi:application --bind 0.0.0.0:8000 --workers 3