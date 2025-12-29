# to build
docker build . -t zongzhiliu/ubuntu_python:1.0
docker compose build
# to run
docker run -it -p 8888:8888 -v "$PWD/app:/app" -w /app ubuntu_python:1.0 
docker compose run python
docker compose run python python3 test_plot.py

#bash -c "pip3 freeze > requirements.txt"
#source jupyter-notebook.sh
    #then follow the last link