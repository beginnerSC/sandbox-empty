FROM python:3.7-slim
# install the notebook package
RUN pip install --no-cache --upgrade pip && \
    pip install --no-cache notebook && \
    pip install --no-cache jupyterlab && \
    pip install --no-cache nbconvert && \
    apt-get clean && apt-get update && apt-get install -y \
    pandoc \
    texlive-xetex \ 
    texlive-fonts-recommended \
    texlive-generic-recommended

# create user with a home directory
ARG NB_USER
ARG NB_UID
ENV USER ${NB_USER}
ENV HOME /home/${NB_USER}

RUN adduser --disabled-password \
    --gecos "Default user" \
    --uid ${NB_UID} \
    ${NB_USER}
WORKDIR ${HOME}
USER ${USER}