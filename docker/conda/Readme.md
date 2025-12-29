docker pull continuumio/miniconda3
docker run -i -t continuumio/miniconda3 /bin/bash
docker pull continuumio/miniconda3
docker run -i -t continuumio/miniconda3 /bin/bash
docker run -i -t -p 8888:8888 -v $PWD:/app -w /app continuumio/miniconda3 /bin/bash -c "\
    conda install jupyter -y --quiet && \
    jupyter notebook \
    --ip='*' --port=8888 \
    --no-browser --allow-root"