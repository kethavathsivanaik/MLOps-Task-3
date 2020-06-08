FROM debian:latest

RUN apt-get update -qq \
 && apt-get install --no-install-recommends -y \
    build-essential \
    g++ \
    git \
    apache2 \
    openssh-client \
    python3 \
    python3-dev \
    python3-pip \
    python3-setuptools \
    python3-virtualenv \
    python3-wheel \
    pkg-config \
    libopenblas-base \
    python3-numpy \
    python3-scipy \
    python3-h5py \
    python3-yaml \
    python3-pydot \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN pip3 install  numpy

RUN pip3 install \
    pandas \
    scikit-learn \
    statsmodels \
    matplotlib \
    Pillow \
    papermill \
    jupyter \
    tensorflow \
    tensorflow-probability \
    keras \
    jupyter notebook 

RUN mkdir -p /root/workspace

WORKDIR /root/workspace
CMD ["/bin/bash"]
CMD ["python3","/root/workspace/model.py"]






