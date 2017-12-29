FROM ubuntu:16.04

RUN apt-get update && apt-get install -y \
    make \
    git \
    wget \
    python \
    python-setuptools \
    python-pip \
    python-dev \
    gcc \
    libffi-dev \
    libssl-dev

WORKDIR /tmp

#RUN wget https://dist.apache.org/repos/dist/dev/incubator/ariatosca/0.2.0-candidate/
RUN wget https://dist.apache.org/repos/dist/dev/incubator/ariatosca/0.2.0-candidate/apache-ariatosca-0.2.0-incubating.tar.gz

RUN tar xvzf apache-ariatosca-0.2.0-incubating.tar.gz

WORKDIR /tmp/apache-ariatosca-0.2.0-incubating

RUN pip install -r requirements.txt

RUN python setup.py install
