FROM ubuntu:focal

RUN apt-get update && apt-get install -y --no-install-recommends \
    python3-dev \
    python3-pip \
    pkg-config \
    libfreetype6-dev \
    libpng-dev \
    libqhull-dev \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

COPY invisible-trainer /invisible/src/invisible-trainer
WORKDIR /invisible

RUN python3 -m pip install --upgrade pip && \
    python3 -m pip install -r src/invisible-trainer/requirements.txt