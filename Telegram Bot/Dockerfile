FROM python:3.7-alpine3.8
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN mkdir /code

ENV TZ 'Asia/Tehran'
RUN apk add --update alpine-sdk \
                     libxml2-dev \
                     libxslt-dev \
                     python-dev \
                     libffi-dev \
                     zlib-dev

RUN apk update && apk add tzdata libpq postgresql-dev build-base
RUN apk add jpeg-dev zlib-dev freetype-dev lcms2-dev openjpeg-dev tiff-dev tk-dev tcl-dev && \
    cp /usr/share/zoneinfo/Asia/Tehran /etc/localtime && \
    echo $TZ > /etc/timezone

COPY ./requirements.txt ./requirements.txt
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

COPY ./ ./
CMD ["python", "main.py"]
