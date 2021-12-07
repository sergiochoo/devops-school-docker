FROM python:3.8-alpine

ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

WORKDIR /app
COPY . .
RUN apk add --no-cache --update libxslt libxslt-dev postgresql-dev gcc libxml2-dev musl-dev curl && \
    pip install -r requirements.txt