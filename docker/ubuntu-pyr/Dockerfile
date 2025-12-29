FROM zongzhiliu/ubuntu_python:1.0
RUN apt install -y  r-base-dev
Rscript -e "install.packages(c('tidyverse'))"

# CMD ["jupyter", "lab", "--allow-root",  "--ip=0.0.0.0"]
