FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
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
    && rm -rf /var/lib/apt/lists/*

WORKDIR /workspace/Fast-DDS

CMD ["bash"]