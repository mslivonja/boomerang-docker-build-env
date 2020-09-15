# Boomerang Docker Build env.

This repository contains the Dockerfiles which are used to build Docker images for the Travis CI jobs for the [Boomerang Decompiler](https://github.com/BoomerangDecompiler/boomerang).

To create complete docker image containing boomerang-cli use following command(prerequisite: run build-docker-images.sh):

    cd dockerfiles/boomerang-cli
    sudo docker build -t ceeac/boomerang-cli:latest .

To run boomerang-cli container use following command:

    cd <bin directory>
    docker run -it --rm -v$(pwd):/workspace ceeac/boomerang-cli:latest
