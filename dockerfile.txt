FROM jupyter/scipy-notebook:python-3.11
ENV PIP_NO_CACHE_DIR=1 PIP_DISABLE_PIP_VERSION_CHECK=1
COPY requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir -r /tmp/requirements.txt
ENV JUPYTER_ENABLE_LAB=yes
WORKDIR /home/jovyan/work
