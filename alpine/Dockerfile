ARG image_tag=3.8.5-alpine3.12
FROM python:${image_tag}
WORKDIR /root
RUN apk --update-cache \
    add musl \
    linux-headers \
    gcc \
    g++ \
    make \
    gfortran \
    openblas-dev \
    python3 \
    python3-dev \
    zlib-dev
COPY ./requirements.txt .
RUN pip3 install --upgrade pip \
    && pip3 install -r /root/requirements.txt
