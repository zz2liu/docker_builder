docker build . -t ubuntu_jupyter
docker run -v "$PWD/app:/app" -w /app -p 8888:8888 ubuntu_jupyter
# then follow the link
#bash -c "pip3 freeze > requirements.txt"