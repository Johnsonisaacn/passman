# dev image
FROM ubuntu:22.04 AS dev

ARG DEBIAN_FRONTEND=noninteractive

# install apt packages
RUN apt-get update && apt-get -y install \
    bash \
    build-essential \
    cmake \
    curl \
    gdb \
    git-all \
    python3 \
    vim \
    xclip

# enable colored prompt
RUN /bin/bash -c  "sed -i 's/^#force_color_prompt=yes/force_color_prompt=yes/' ${HOME}/.bashrc"

# create an alias for build script
RUN /bin/bash -c "echo alias $'build=/workspaces/passman/build.sh\n' >> /root/.bash_aliases"

ENV PROJECT_SOURCE_DIR /workspaces/passman
