# This template is based on the StaPH-B dockerfile template with some modifications: https://github.com/StaPH-B/docker-builds/blob/master/dockerfile-template/Dockerfile
# Base image 
    # Ubuntu 20.04, official docker image is called focal
FROM ubuntu:focal

# ARG variable 
ARG SOFTWARENAME_VER="1.0.0"

# Metadata labels 
LABEL base.image="ubuntu:focal"
LABEL dockerfile.version="1"
LABEL software="SoftwareName"
LABEL software.version=$SOFTWARENAME_VER
LABEL description="This software does X, Y, Z"
LABEL website="the github repo"
LABEL license="where licenses are listed"
LABEL maintainer="Firstname LastName"
LABEL maintainer.email="myemail@email.com"

# RUN executes code during the build
# Install dependencies
RUN apt-get update && apt-get install -y \
    dependency_a \
    dependency_b \
    dependency_c \

# Installation and setup 
# Use /data as the working directory (might have to change this later)
# Example is ncbi-blast+ 2.9.0
RUN wget ftp://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/2.9.0/ncbi-blast-2.9.0+-x64-linux.tar.gz && \
 tar -xzf ncbi-blast-2.9.0+-x64-linux.tar.gz && \
 rm ncbi-blast-2.9.0+-x64-linux.tar.gz && \
 mkdir /data

# ENV instructions set environment variables that persist from the build into the resulting image
# Use for e.g. $PATH and locale settings for compatibility with Singularity
ENV PATH="/ncbi-blast-2.9.0+/bin:$PATH" \
 LC_ALL=C

# WORKDIR sets working directory
WORKDIR /data
