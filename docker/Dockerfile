FROM nvcr.io/nvidia/pytorch:20.12-py3

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -q -y --no-install-recommends \
    python3-pip \
    libgl1 \
    && rm -rf /var/lib/apt/lists/*

RUN python3 -m pip install --upgrade pip && \
    python3 -m pip install scalene

COPY invisible-trainer /invisible/src/invisible-trainer

WORKDIR /invisible

CMD ["bash"]