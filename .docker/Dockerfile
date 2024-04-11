# Anaconda Environment build
# docker build --platform linux/amd64 -t initial_py311_grad_cam_py_torch-v1 .
# docker tag 521e95886276 initial_py311_grad_cam_py_torch-v1:latest
# docker push initial_py311_grad_cam_py_torch-v1:latest

FROM continuumio/miniconda3:latest

# Set the working directory in the container to /app
WORKDIR /app

# Make RUN commands use `bash --login`:
SHELL ["/bin/bash", "--login", "-c"]

RUN apt-get update
RUN apt-get install -y --no-install-recommends libdbus-glib-1-dev libgirepository1.0-dev libgtk-3-dev wget && apt-get -y clean && apt-get -y autoremove && apt-get -y autoclean

RUN apt-get -y upgrade

COPY initial_py311_grad_cam_py_torch-v1.yml .

RUN conda init bash

RUN CONDA_VERBOSITY=1 conda env create -f initial_py311_grad_cam_py_torch-v1.yml --name custom-environment && conda clean --all -y && find /opt/conda/pkgs/ -delete

RUN echo "conda activate custom-environment" > ~/.bashrc
RUN echo "Make sure pytorch is installed:"
RUN python -c "import torch"

# Cleanup
RUN echo "conda clean --all" > ~/.bashrc
RUN find ~/.cache/pip -delete
# RUN find /root/.cache/pip/ -delete
# RUN find /opt/conda/pkgs/ -delete
# RUN find /var/cache/ -delete

ENV PATH /opt/conda/envs/env/bin:$PATH
CMD ["/bin/bash"]
