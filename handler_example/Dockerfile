FROM python:3.7-alpine
RUN apk update && apk add git
RUN apk add --no-cache python3-dev libffi-dev gcc musl-dev make
VOLUME /logs
ADD it.py /
ADD wsgi.ini /
COPY requirements.txt /tmp/
RUN pip3 install -r /tmp/requirements.txt
COPY . /tmp/
CMD ["uwsgi", "--ini", "wsgi.ini"]