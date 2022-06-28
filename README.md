# Arcadia Science Docker Builds 
This repository is the central hub for Docker builds implemented by Arcadia Science. This includes the Dockerfiles and other files necessary for building Docker images for various toolkits at Arcadia Science. The purpose of this repository is to provide a centralized location of all Docker images used across Arcadia Science with clear documentation. 

## Docker User Guide and Contributing
For a quick intro to using Docker you can get started with the [Docker Docs](https://docs.docker.com/). The State Public Health Bioinformatics Consortium (STaPH-B) has also put together a nice [user guide on Docker](https://staphb.org/docker-builds/). We encourage users to implement our Docker images outside of Arcadia Toolkits and also contribute new Dockerfiles for software that is not already provided. If you have an issue with an existing software Docker image, please open an issue. If you would like to contribute a Dockerfile for software that is not already provided follow these steps: 

1. Fork the repository to your github account
2. Clone the repository to your local machine
3. Build and make modifications to the Dockerfile for the given software
4. Add and commit the changes, and push the updates to your repository
5. Create a pull request and an Arcadia Scientist will review the updates to ensure there are no conflicts 
6. We will then push the image to our hosting site

## Glossary of Docker Images 

| Software | Usage | Versions | Link |
| :--------: | --------- | | --------- | -------- |
| [fastp](https://hub.docker.com/r/elizabethmcd/fastp) | 0.23.2 | Preprocessing & QC of fastQ files | https://github.com/OpenGene/fastp |