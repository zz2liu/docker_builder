FROM rocker/tidyverse 

RUN apt update && apt upgrade -y
RUN apt install -y vim man less htop ncdu
RUN apt install -y  postgresql-client

# R dev
RUN apt install -y --no-install-recommends libxt6
RUN Rscript -e "install.packages(c('RPostgres', 'markdown', 'reticulate'))"

# python dev
RUN apt install -y python3 python3-pip python3-tk
RUN pip3 install pandasql psycopg2-binary sqlalchemy
RUN pip3 install ipython pytest typer matplotlib seaborn
RUN pip3 install jupyterlab