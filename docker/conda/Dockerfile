FROM continuumio/miniconda3

RUN apt update #&& apt upgrade -y
RUN apt install -y vim man less htop ncdu

RUN conda install pandasql psycopg2 sqlalchemy
RUN conda install parameterized typer
RUN conda install ipython pytest matplotlib
RUN conda install jupyterlab 
CMD ["jupyter", "lab", "--allow-root", "--ip=*"]
