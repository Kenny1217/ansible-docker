FROM python:3.13-slim-trixie

ENV DEBIAN_FRONTEND=noninteractive

USER root

RUN useradd -m -s /bin/bash ansible

RUN apt-get update && apt-get install -y --no-install-recommends \
    git \ 
    openssh-client \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install --no-cache-dir ansible==13.0.0

USER ansible
