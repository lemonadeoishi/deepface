FROM tensorflow/tensorflow:latest-gpu-jupyter
 
# -----------------------------------
# update image os
RUN apt-get update
RUN apt-get install ffmpeg libsm6 libxext6 -y
 
RUN apt-get update && apt-get upgrade -y
RUN apt-get update && apt-get install -y cmake g++
RUN python3 -m pip install --upgrade pip setuptools
RUN pip install --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host=files.pythonhosted.org tensorflow
RUN pip install --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host=files.pythonhosted.org cmake==3.24.1.1
RUN pip install --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host=files.pythonhosted.org dlib
RUN pip install --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host=files.pythonhosted.org lightgbm==2.3.1
# COPY requirements.txt .
# RUN pip3 install -r requirements.txt
#RUN apt-get -y update && apt-get -y upgrade && apt-get autoremove -y
RUN apt update && apt install -y zstd
RUN pip install --ignore-installed blinker
RUN apt install tmux -y

ENV TF_ENABLE_ONEDNN_OPTS=0