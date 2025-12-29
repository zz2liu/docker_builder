FROM ubuntu:22.04 

RUN apt update && apt upgrade -y
RUN apt-get install -y vim man less htop ncdu
RUN apt install -y  postgresql-client
RUN apt-get install -y python3.10 python3-pip
RUN apt-get install -y python3-tk

# see https://stackoverflow.com/questions/46503947/how-to-get-pipenv-running-in-docker for why using the tags
#RUN pip3 install pipenv \
#    && export LC_ALL=C.UTF-8 && export LANG=C.UTF-8

# typer > click
# padasql > pandas > numpy
RUN pip3 install pandasql psycopg2-binary sqlalchemy
RUN pip3 install parameterized typer
RUN pip3 install ipython pytest matplotlib
# RUN pip3 install jupyter

# CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root"]
CMD ["bash"]