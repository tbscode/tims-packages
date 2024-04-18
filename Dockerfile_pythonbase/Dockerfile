FROM python:3.11-alpine as backend

WORKDIR /back
COPY ./back/requirements.txt /tmp/requirements.txt

RUN pip install "Cython<3.0" pyyaml --no-build-isolation
RUN apk add --no-cache git
RUN apk add --no-cache gcc g++ musl-dev libffi-dev openssl-dev
RUN pip install --no-cache-dir -r /tmp/requirements.txt
RUN apk add --no-cache git
RUN pip cache purge

