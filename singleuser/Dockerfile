# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.

# Pin to version of notebook image that includes start-singleuser.sh script
ARG DOCKER_NOTEBOOK_IMAGE
FROM $DOCKER_NOTEBOOK_IMAGE
ARG JUPYTERHUB_VERSION

ENV JUPYTER_ENABLE_LAB=YES

# Install packages in default Python 3 environment
RUN python3 -m pip install --no-cache \
  jupyterhub==$JUPYTERHUB_VERSION \
  jupyterlab

USER jovyan
WORKDIR /home/jovyan/work
