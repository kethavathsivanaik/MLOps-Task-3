FROM centos
MAINTAINER Kethavath Siva Naik <sivanaikk0903@gmail.com>
ENV PATH="/root/miniconda3/bin:${PATH}"
ARG PATH="/root/miniconda3/bin:${PATH}"
RUN yum install -y wget
RUN wget \
    https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh \
    && mkdir /root/.conda \
    && bash Miniconda3-latest-Linux-x86_64.sh -b \
    && rm -f Miniconda3-latest-Linux-x86_64.sh
RUN conda --version
RUN conda install anaconda-client -n base
COPY /home/student/Desktop/Mask-R-CNN/Anaconda Setup/  /root/Anaconda Setup/
RUN conda env create -f /root/Anaconda Setup/mask_rcnn.yml
RUN yum install python3-pip -y
RUN pip3 install -f /root/Anaconda Setup/requirements.txt
# Running Python Application
CMD ["bin/bash"]

