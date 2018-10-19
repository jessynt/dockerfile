FROM python:3.6

RUN apt-get update && apt-get install -y rsync
#Installing ansible
RUN pip install 'ansible==2.7.0'
RUN apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
