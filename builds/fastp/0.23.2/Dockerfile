# This template is based on the StaPH-B dockerfile template with some modifications: https://github.com/StaPH-B/docker-builds/blob/master/dockerfile-template/Dockerfile
# Base image 
    # Ubuntu 20.04, official docker image is called focal
FROM ubuntu:focal

# ARG variable 
ARG FASTP_VER="0.23.2"

# Metadata labels 
LABEL base.image="ubuntu:focal"
LABEL dockerfile.version="1"
LABEL software="fastp"
LABEL software.version=$SOFTWARENAME_VER
LABEL description="Quality filtering and processing of fastQ files"
LABEL website="https://github.com/OpenGene/fastp"
LABEL license="https://github.com/OpenGene/fastp/blob/master/LICENSE"
LABEL maintainer="Elizabeth McDaniel"
LABEL maintainer.email="elizabethmcd93@gmail.com"

# RUN executes code during the build
# Install dependencies
RUN apt-get update && apt-get install -y \
    autoconf \
    automake \
    build-essential \
    git \
    wget && \
    apt-get autoclean

# Download and install fastp
WORKDIR /opt
RUN wget http://opengene.org/fastp/fastp.0.23.2 && \
    mv fastp.0.23.2 fastp && \
    chmod a+x ./fastp && \
    ln -s /opt/fastp /usr/local/bin


# set final working directory
WORKDIR /data 
