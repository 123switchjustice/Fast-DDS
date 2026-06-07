FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

ARG USERNAME=freedom
ARG USER_UID=1000
ARG USER_GID=1000

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    build-essential \
    cmake \
    ninja-build \
    git \
    gdb \
    wget \
    curl \
    python3 \
    python3-pip \
    pkg-config \
    libasio-dev \
    libtinyxml2-dev \
    libssl-dev \
    libp11-dev \
    softhsm2 \
    libgtest-dev \
    libgmock-dev \
    clang \
    clangd \
    clang-format \
    vim \
    sudo \
    openssh-client \
    bash-completion \
    && rm -rf /var/lib/apt/lists/*

RUN groupadd --gid ${USER_GID} ${USERNAME} \
    && useradd --uid ${USER_UID} --gid ${USER_GID} -m -s /bin/bash ${USERNAME} \
    && echo "${USERNAME} ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/${USERNAME} \
    && chmod 0440 /etc/sudoers.d/${USERNAME}

RUN chown -R ${USERNAME}:${USERNAME} /home/${USERNAME}

WORKDIR /workspace

USER ${USERNAME}

CMD ["bash"]