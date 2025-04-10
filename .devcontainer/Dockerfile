# syntax=docker/dockerfile:1.6.0
# escape=\

FROM ubuntu:jammy AS android_vendor_lineage_bootanimation-container

USER root

ARG WORKSPACE_DIR=/project/workspace

WORKDIR $WORKSPACE_DIR

RUN apt-get update && \
    apt-get install -y ffmpeg imagemagick bc dos2unix aria2

ARG BOOT2GIF_URL="https://gist.githubusercontent.com/jaredrummler/cf4a8fd53a0cff5f8802d55f4f5d14aa/raw/7663a290bc2f53b7db809a0398c5bafa7192eb64/boot2gif.sh"

RUN mkdir -p /root/.bin

WORKDIR /root/.bin

RUN aria2c --file-allocation=none $BOOT2GIF_URL -o boot2gif

WORKDIR $WORKSPACE_DIR

RUN chmod 755 /root/.bin/boot2gif

ENV PATH=/root/.bin:$WORKSPACE_DIR/.bin:$WORKSPACE_DIR/bin:$PATH

RUN boot2gif --help
