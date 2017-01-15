FROM nvidia/cuda:8.0-cudnn5-devel
LABEL maintainer "Yuta Namiki <namikister@gmail.com>"

RUN apt-get update
RUN apt-get install -y --no-install-recommends \
            python-pip \
            python-dev \
            build-essential \
            git \
            libhdf5-dev \
            zlib1g-dev
RUN rm -rf /var/lib/apt/lists/*

RUN pip install numpy==1.11

RUN pip install h5py

ENV CUDA_PATH /usr/local/cuda

RUN pip install chainer==1.19

ENV LD_LIBRARY_PATH /usr/lib/x86_64-linux-gnu:$LD_LIBRARY_PATH

# ENTRYPOINT ["/bin/bash"]
