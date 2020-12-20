FROM tensorflow/tensorflow:2.3.0-gpu

RUN add-apt-repository ppa:paulo-miguel-dias/mesa
RUN apt-get update

RUN apt-get install python3.7 -y

RUN update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 1
RUN update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 2

RUN update-alternatives  --set python3 /usr/bin/python3.7


# Dependency for opencv (corresponding apt repo added above)
RUN apt-get install libgl1-mesa-glx -y

# ===========
# Update pip and install all pip dependencies
# ===========

# Required dependency to upgrade pip below
RUN python3 -m pip install six

RUN python3 -m pip install --upgrade pip
COPY ./docker/requirements.txt /opt/project/requirements.txt
RUN pip install -r /opt/project/requirements.txt
