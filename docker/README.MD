# Docker Folder

The `docker` folder contains the Dockerfile and tools necessary to create the base image. This image will be used in a variety of CI/CD applications that the company utilizes.

## Dockerfiles

### Dockerfile.ci

This Dockerfile is used to create a CI (Continuous Integration) image with the necessary tools for building and deploying applications. It uses the `alpine:latest` base image and installs various dependencies such as `curl`, `git`, `docker`, `tree`, and `unzip`. It also sets up environment variables and downloads tools like `envsubst`, `skaffold`, `helm`, and `kubectl`. The working directory is set to `/root`.

You can find this Dockerfile at [docker/Dockerfile.ci](docker/Dockerfile.ci).

### Dockerfile.py-uvbase

This Dockerfile is used to create a base image for Python applications. It uses the `python:3.11-slim-bookworm` base image and installs system packages like `supervisor` and `git`. It also copies the `uv` tool from a remote repository. This base image can be used as a foundation for building Python applications.

You can find this Dockerfile at [docker/Dockerfile.py-uvbase](docker/Dockerfile.py-uvbase).