FROM tensorflow/tensorflow:latest-gpu-jupyter 

RUN apt-get update ##[edited]
RUN apt-get install ffmpeg libsm6 libxext6  -y

RUN pip install sklearn
RUN pip install keras==2.4.3 numpy==1.19.3 pillow==7.0.0 scipy==1.4.1 h5py==2.10.0 matplotlib==3.3.2 opencv-python keras-resnet==0.2.0
RUN pip install imageai --upgrade
RUN pip install tqdm

COPY jupyter_notebook_config.py /root/.jupyter/
COPY run_jupyter.sh /
RUN chmod +x /run_jupyter.sh

WORKDIR "/notebooks" 
CMD ["/run_jupyter.sh"]



