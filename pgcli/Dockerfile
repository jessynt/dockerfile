FROM python:3.7.0-slim

RUN apt-get -y update && apt-get -y install libpq-dev build-essential && rm -rf /var/lib/apt/lists/*
RUN pip install pgcli psycopg2-binary

ENTRYPOINT ["pgcli"]