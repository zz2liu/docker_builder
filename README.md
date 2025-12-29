# docker_builder
Build dockers for real world evidence, clinical research.

## docker examples to get started
### linux shell
docker run -it --name ubuntu_mount --mount type=bind,source="$(pwd)",target=/app ubuntu bash
- image pull: ubuntu:latest
- container create: ubuntu_mount
- container start: ubuntu_mount
- container exec: -it ubuntu_mount bash

docker container: ps -a; start, stop, rm: better in UI.
docker exec -it <container_name_or_id> /bin/bash*	

### python notebook
docker run -dp 8888:8888 --name scipy_mount -v "$(pwd):/home/jovyan/work" jupyter/scipy-notebook
ref: https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#image-relationships

### rstudio
docker run -dp 8787:8787 --name rstudio_mount -e PASSWORD=rstudio -v "$(pwd)":/home/rstudio/projects rocker/tidyverse

combined: docker run --rm -ti -p 8888:8888 -p 8787:8787 rocker/binder:4
ref: https://rocker-project.org/


Next: 
docker compose for rstudio + scipy
docker postgres / ms sql server
