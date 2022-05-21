FROM ubuntu:20.04
ENV DEBIAN_FRONTEND=noninteractive
ENV DEBCONF_NOWARNINGS=yes

RUN apt-get update && apt-get upgrade -y && apt-get install -y git wget python3 python3-pip && apt-get install -y libgl1-mesa-dev libglib2.0-0
# RUN apt-get install libopencv-dev -y
# RUN apt install libglib2.0-0 -y    # これ6は、6と79を押す必要が出てくる

# cpu version
RUN pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cpu

# install detectron2
RUN git clone https://github.com/facebookresearch/detectron2.git
RUN cd detectron2 && pip3 install -e .
# RUN pip install -e /detectron2

RUN git clone https://github.com/facebookresearch/Detic.git --recurse-submodules
RUN cd Detic && pip3 install -r requirements.txt